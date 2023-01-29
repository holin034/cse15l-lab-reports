# Lab Report 2
## Creating a Web Server
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
- Here are two examples of output of my code
<img width="513" alt="Screen Shot 2023-01-28 at 6 15 59 PM" src="https://user-images.githubusercontent.com/122575008/215300719-38409550-a061-4729-a7a9-43d11ce16a95.png">
<img width="513" alt="Screen Shot 2023-01-28 at 6 36 09 PM" src="https://user-images.githubusercontent.com/122575008/215301310-f1685e4d-60a8-45d7-82da-3718d05e4d20.png">
