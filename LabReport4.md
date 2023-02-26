# Lab Report 4
## The Tasks from the Competition
### 1. Login to the ieng6 account:
<img width="520" alt="Screen Shot 2023-02-25 at 2 31 33 PM" src="https://user-images.githubusercontent.com/122575008/221382535-c72efac5-807e-4241-8bc4-124de013306c.png">

- Keys pressed: ```ssh<space>cs15lwi23aty@ieng6.ucsd.edu<enter>```
- I used the ```ssh cs15lwi23aty@ieng6.ucsd.edu``` command to login to my class server by typing ```ssh``` command and my account to login.

### 2. Clone your fork of the repository from your Github account:
<img width="310" alt="Screen Shot 2023-02-25 at 3 48 11 PM" src="https://user-images.githubusercontent.com/122575008/221384793-7685a485-a01a-406c-9fbd-b0db5cbe19f3.png">

<img width="415" alt="Screen Shot 2023-02-25 at 3 22 42 PM" src="https://user-images.githubusercontent.com/122575008/221384073-980ebacf-a925-4ab7-8a5e-f61d98915474.png">

<img width="725" alt="Screen Shot 2023-02-25 at 3 21 06 PM" src="https://user-images.githubusercontent.com/122575008/221384027-1f3aa209-3471-4499-bde3-f561dbcf3b5b.png">

- Keys pressed: ```git<space>clone<space>git@github.com:holin034/lab7.git<enter>```
- I first forked the repository to my own Github account. Then I copied the SSH url of the repository and used the ```git clone``` command to clone the fork of the repository to my Github account.

### 3. Run the tests, demonstrating that they fail:
<img width="978" alt="Screen Shot 2023-02-25 at 3 49 33 PM" src="https://user-images.githubusercontent.com/122575008/221384819-69e1f3de-f2eb-45c0-a0f3-e4ab16f7f509.png">

- Keys pressed: 
1. ```cd<space>lab7<enter>```
2. ```javac<space>-cp<space>.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar<space>*.java<enter>``` 
3. ```java<space>-cp<space>.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar<space>org.junit.runner.JUnitCore<space>ListExamplesTests<enter>```
- First, I used the ```cd``` command to change to ```lab7``` directory so that I can compile the files in it. Then, I used the ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command to compile all the codes in the files in lab7. Lastly, I used the command ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java``` to run the code in the ```ListExamplesTest.java``` file.

### 4. Edit the code file to fix the failing test:
<img width="50%" alt="Screen Shot 2023-02-25 at 3 54 24 PM" src="https://user-images.githubusercontent.com/122575008/221384948-5e915f5f-7c37-4385-a52f-d3bb50f93403.png">

- Before the error is fixed:

<img width="50%" alt="Screen Shot 2023-02-25 at 3 51 18 PM" src="https://user-images.githubusercontent.com/122575008/221384870-93a31ab8-6dcc-4fc5-9ad3-b2ca5f9635cf.png">

- After the error is fixed:

<img width="50%" alt="Screen Shot 2023-02-25 at 3 51 34 PM" src="https://user-images.githubusercontent.com/122575008/221384878-b0ba2fc6-ab7e-4caf-988b-605205d26711.png">

<img width="50%" alt="Screen Shot 2023-02-25 at 3 53 45 PM" src="https://user-images.githubusercontent.com/122575008/221384932-f925d6b6-47d8-418d-bff6-a2a33f4d58d2.png">

- Keys pressed:
1. ```nano<space>ListExamples.java<enter>```
2. ```<Scroll down>``` to the seventh line from the last
3. ```<right><right><right><right><right><right><right><right><right><right><right><right><delete>```
4. ```2```
5. ```Ctrl-X```
6. ```Y<enter>```
- First, I used the ```nano ListExamples.java``` command to display the code in the file. Then, I scrolled down to the seventh line from the last because the mistake is on that line. After that, I pressed the right arrow key 12 times and deleted the ```index1``` on that line and changed it to the ```index2```. Lastly, I pressed ```Ctrl-X``` to ```save and exit``` and pressed ```Y``` to confirm to save the changes.

### 5. Run the tests, demonstrating that they now succeed:
<img width="984" alt="Screen Shot 2023-02-25 at 3 54 48 PM" src="https://user-images.githubusercontent.com/122575008/221384958-b233529a-7c6e-42f3-a7a9-e8b3c04c8309.png">

- Keys pressed:
1. ```<up><up><up><enter>```
2. ```<up><up><up><enter>```
- The ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` command was 3 up in the search history, so I used up arrow to access it. Similarly, the ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` command was 4 up in the history, so I accessed and ran it in the same way.

### 6. Commit and push the resulting change to your Github account:
<img width="728" alt="Screen Shot 2023-02-25 at 3 55 48 PM" src="https://user-images.githubusercontent.com/122575008/221384978-3e8e0ae9-508a-4982-8595-ee98ad8f0208.png">

<img width="912" alt="Screen Shot 2023-02-25 at 3 56 18 PM" src="https://user-images.githubusercontent.com/122575008/221384988-d7a1729b-3d34-4512-aed4-fd00b71d5321.png">

- Keys Pressed:
1. ```git<space>commit<space>ListExamples.java<space>-m<space>"Updated"```
2. ```git<space>push```
- I used the ```git commit <file name> -m <note>``` command to commit the resulting change to my Github account. Then, I used the ```git push``` command to push the changes that I have made in ```ListExamples.java``` file to my Github account. As you can see, on my Github account page, the ```ListExamples.java``` file shows ```Updated``` and the errors are fixed.

