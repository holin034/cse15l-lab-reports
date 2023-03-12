# Lab Report 5
## My Favorite Lab Activity: The ```grep``` Commands
### How I do the tasks:
- First, I started looking for the ```grep``` commands by using the ```man grep``` command in the terminal which gives out lots of examples of grep command.
- Then, I also use **ChatGPT** to look up how the command is used. 
- Additionally, I used the lecture note to find out some other ```grep``` command ideas as well.

<img width="1079" alt="Screen Shot 2023-03-11 at 10 50 55 PM" src="https://user-images.githubusercontent.com/122575008/224529157-7c514de6-c90a-4f18-9ae7-e26402d82e9f.png">

### More ```grep``` commands:

#### 1. ```grep "[pattern]" [Filename].txt```
- Search for a pattern in a file: The most basic usage of ```grep``` is to search for a specific pattern or text string in a file. 
- For example, to search for the word ```car``` in a file called ```transportations.txt```, you can use the following command:
```
grep "car" transportations.txt
````

#### 2. ```grep "[pattern]" *.txt```
- Search for a pattern in multiple files: You can also search for a pattern in multiple files at once by specifying the filenames as arguments to ```grep```. 
- For example, to search for the word ```elephant``` in all text files in the current directory, you can use the following command:
```
grep "elephant" *.txt
```

#### 3. ```grep "^[character]" [Filename].txt```
- Use regular expressions to search for patterns: ```grep``` supports regular expressions, which allows you to search for more complex patterns. 
- For example, to search for all words that start with the letter ```a``` in a file called ```Bahama-History.txt```, you can use the following command:
```
grep "^a" Bahama-History.txt
```

#### 4. ```grep -i "[pattern]" [Filename].txt```
- Search for a pattern in a case-insensitive manner: By default, ```grep``` is case-sensitive, meaning that it will only match patterns that are exactly the same case as the one you specified. However, you can use the ```-i``` option to perform a case-insensitive search. 
- For example, to search for the word ```car``` regardless of its case in a file called ```transportations.txt```, you can use the following command:
```
grep -i "car" transportations.txt
```

#### 5. ```grep -f [Filename].txt [Filename].txt```
- Use a file as the pattern source: You can use the ```-f``` option to specify a file that contains patterns to search for. 
- For example, to search for all lines in a file called ```movies.txt``` that match any of the patterns in a file called ```transportations.txt```, you can use the following command:
```
grep -f transportations.txt movies.txt
```

#### 6. ```grep -e [pattern] -e [pattern] [Filename].txt```
- The ```-e``` option in grep is used to specify multiple search patterns or regular expressions in a single command. This option allows you to search for lines that match any of the specified patterns. 
- For example, you have a file called ```food.txt``` that contains a list of food, one per line. You want to search for lines that contain either the word ```pizza``` or the word ```burger```. You can use the ```-e``` option to search for both patterns in a single command, like this:
```
grep -e pizza -e burger food.txt
```

#### 7. ```grep -a "[pattern]" binaryfile```
- The ```-a``` option in ```grep``` is used to force the command to treat a file as a text file, even if it appears to be a binary file.
- Suppose you have a file called ```binaryfile``` that appears to be a binary file, but actually contains some text that you want to search for. You can use the ```-a``` option to search for the text like this:
```
grep -a "email" binaryfile
```

#### 8. ```grep -o "[pattern]" [Filename].txt```
- The ```-o``` option in grep is used to display only the matched parts of a line, rather than the entire line that contains the match.
- For example, you want to search for the word ```car``` in this file, but you only want to see the matched word itself, without any context. You can use the ```-o``` option to display only the matched part of each line, like so:
```
grep -o "car" transportations.txt
```





