# Lab Report 2
## I. Creating a Web Server
- Code of my StringServer: 

```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {
    ArrayList<String> list = new ArrayList<>();

    public String handleRequest(URI url) {
        String printOut = "";
        if (url.getPath().equals("/")) {
            for (int i = 0; i < list.size(); i++) {
                printOut += list.get(i) + "\n";
            }
            return printOut;
        } 
        else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    list.add(parameters[1]);
                    for (int i = 0; i < list.size(); i++) {
                        printOut += list.get(i) + "\n";
                    }
                    return printOut;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
- Here are two examples of the outputs of my code

    <img width="513" alt="Screen Shot 2023-01-28 at 6 15 59 PM" src="https://user-images.githubusercontent.com/122575008/215300719-38409550-a061-4729-a7a9-43d11ce16a95.png">
    
    <img width="513" alt="Screen Shot 2023-01-28 at 6 36 09 PM" src="https://user-images.githubusercontent.com/122575008/215301310-f1685e4d-60a8-45d7-82da-3718d05e4d20.png">
    
- In the above example, the `main` method in `StringServer` class is first called, and it brings to `Handle` class with `handleRequest` method. To insert a string value into the webpage, users must type in the requests `/add-message?s=<your string>` after the url. In the 'handleRequest' method, the code splits the `=` sign into two parameters in the query. As stated, the parameter before the `=`, which is `s` will be checked. The parameter after the `=` sign will be the string elements that are supposed to be displayed. If parts of the parameter is incorrect, the server will show `404 Not Found!`. Each time when all the parameters are checked correctly, a string element will be added to the arraylist and displayed on the server. In this example, the string values changed. After the users input different strings after `=` in query, different strings are displayed and the value is changed.

    <img width="401" alt="Screen Shot 2023-01-28 at 10 45 44 PM" src="https://user-images.githubusercontent.com/122575008/215309889-d2c133f0-10d0-47e4-b400-6ea75ee8fed9.png">

- In the above example, I continue to add more string elements that will display in my server, however, I have done something wrong. In this case, the `main` method in `StringServer` class is first called, and it calls the `Handle` class that has `handleRequest` method in it. The requests will be the same as usual, as users must type `/add-message?s=<string>` to display a string element. In `handleRequest` method, the code splits `=` into two parameters: the first one is before the `=` sign and the second one is after. When code is checking, the first parameter must be an `s` character, and the second parameter will be string values that will be shown. However, in this circumstance, I missed an `s` before the `=` sign in the query which is the incorrect format, therefore, the result will be `404 Not Found!`. In this case, the value won't change because the incorrect query will always result as `404 Not Found!` value.

## II. Fixing a Bug
- I chose to fix the bug in the method `reverseInPlace` in `ArrayExample` class.
- This is a failure inducing input for the buggy program:
```
int[] input2 = {1, 2, 3, 4, 5};
ArrayExamples.reverseInPlace(input2);
assertArrayEquals(new int[]{5, 4, 3, 2, 1}, input2);
```
- This is an input that doesn't induce a failure:
```
int[] input3 = {0, 0, 0, 0};
ArrayExamples.reverseInPlace(input3);
assertArrayEquals(new int[]{0, 0, 0, 0}, input3);
```
- The symptom: 

    <img width="1087" alt="Screen Shot 2023-01-28 at 11 52 11 PM" src="https://user-images.githubusercontent.com/122575008/215312966-8d29fc3c-b829-464f-8d9c-51b54b5826d0.png">

- The codes before and after the change:
- Before the debug:
```
for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
}
```
- After the debug:
```
for (int i = 0; i < arr.length/2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - 1 - i];
    arr[arr.length - i - 1] = temp;
}
```
- Overall, before the debugging, the code is incorrect because it is taking the changed element in an array and copying again which causes a repeat, instead of making it reversed. Therefore, after addressing the issue, I divide the array length by two, and the first half elements in the array will be assigned to the last half elements, and the last half elements will be assigned back to the first half element, which assembles the entire array to become reversed. This eventually fixes the issue by making the array not repeating again.

## III. Conclusion
- In week 2 lab, I learned how to access and run the server by understanding how to look at path and query. I also learned using the split() function to split the query in order to create parameters by approaching different parts of the query. Additionally, I can run the server through accessing a specific port and display the information on a webpage. Lastly, I can change the query structures to input different functions or requests that can modify the information on the webpage.
- In week 3 lab, I learned how to use a tester class to test the programs to check if the outputs are corresponding to what we expect. I also understand how to find the bugs in the program through tester methods and fix them accordingly. 
