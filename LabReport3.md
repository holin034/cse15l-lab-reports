# Lab Report 3
## `grep -rl` Command:
- The command `grep -rl` is used to search the files that contain the specific pattern/text in those files. It is useful because if the user is trying to find a file that contains a specific word, they can use the `grep -rl` command to search for that file.

### Example 1:
- The input of command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:233$ grep -rl "Bahamas"
```
- The ouput:
```
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```
- All the above files contain the word `Bahamas`.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 
### Example 2:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:234$ grep -rl "Lucayans"
```
- The output: 
```
written_2/travel_guides/berlitz2/Bahamas-History.txt
```
- All the above files contain the word `Lucayans`.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 

## `grep -n` Command:
- The command `grep -n` is used to search for the word in a specific file. It is useful when the user is trying to look for a specific word in that file. The words will be color coded in the output.

### Example 3:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:246$ cd written_2/travel_guides/berlitz2                    
[cs15lwi23aty@ieng6-203]:berlitz2:247$ grep -n "Lucayans" Bahamas-History.txt
```
- The output:
```
6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from 
South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. 
Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 
October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. 
Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed 
for only two weeks before sailing towards Cuba.
7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago 
en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as 
“Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of 
South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in 
Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
- In the terminal, the word `Lucayans` is highlighted in red (although it is not shown here).
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well.
### Example 4:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:254$ cd written_2/travel_guides/berlitz2
[cs15lwi23aty@ieng6-203]:berlitz2:256$ grep -n "Bahamas" Canada-WhereToGo.txt
```
- The output:
```
343:Without detracting from the significance of Columbus’s landing on the Bahamas, Newfoundland can lay a just claim to being the true beginning of 
Europe’s adventure in North America. Anyone seeking to understand Canada’s role in shaping North America should spare a few days for this bracing province 
of hardy fisherfolk — first Canadian land to be “found” and last to join the Confederation (incorporating Labrador), in 1949. The land and seascapes are 
impressively rugged and the spirited people a sheer delight. Life in isolated fishing communities has given the Newfies a keen sense of local identity. 
Citizens of the capital of St. John’s are “townees,” those on the outskirts “bay-men,” and the towns beyond are known as “outports.” “Canadian” is still 
reserved for a mainlander.
```
- In the terminal, the word `Bahamas` is highlighted in red (although it is not shown here).
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 

## `grep -v` command
- The command `grep -v` only prints out the lines that do not contain the specific pattern/text. It is useful when the users intend to display the contents in the file but do not want a specific text to be shown, therefore, they can use the `grep -v` command hide those lines that contain the words. 

### Example 5:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:261$ cd written_2/travel_guides/berlitz1
[cs15lwi23aty@ieng6-203]:berlitz1:262$ grep -v "Hong Kong" IntroHongKong.txt
```
- The output:
```
        Its People
        Exciting, mysterious, glamorous — these words have described
        crowded — it has one of the world’s greatest population densities. But
        it is also efficient, with one of the best transportation systems
        anywhere, and for such a crowded place, quiet — you don’t hear voices
        raised in anger, motorists sitting on their horns, or loud boomboxes.
        Shopping never ends — there’s always another inviting spot just down
        helpful, English spoken everywhere, and food that lives up to its
        reputation.
        reverted to Chinese sovereignty as a Special Administrative Region of
        enclave with its laws and rights intact, and China has promised that
        on the West, and the city is unrivaled in its commercial know-how and
        managerial expertise. Around the time of the transition there was much
        speculation about how things would change. But in fact, once news of
        returned to their usual topics of conversation: the economy and the
        price of housing.
        The impression of the visitor today will be that very little
        has changed. Establishments are no longer called “Royal,” Queen
        Elizabeth has vanished from the coinage, and the Union Jack has been
        bauhinia flower. But in fact, there have been changes, many of them due
        to economic progress, new construction, and other factors that
        influence cities all over the world.
        Others are more subtle. British social customs are still
        evident in the kind of polite service you get in hotels and in the long
        lines of people waiting for buses at rush hour. The British population
        has decreased; today there are as many American and Australian ex-pats
        as there are British.
        With a population of nearly eight million and a total area
        of just over 1,095 square km (423 square miles), housing is one of Hong
        Kong’s perennial nightmares. To alleviate the problem, the government
        has become the city’s major landlord with the construction of massive
        apartment blocks that, though they have every modern facility, average
        only 9 square m (100 square ft) in size. Whole cities have been created
        in the New Territories, although the unimaginative architecture of
        these towns has been criticized.
        there are immigrants from all over China. The Chinese people have been
        described as hardworking and pragmatic, attitudes that have contributed
        with nothing in their pockets, set up a small sidewalk stall, worked
        diligently until they had their own store, and then expanded it into a
        modest chain.
        Old customs are still followed: Fate and luck are taken very
        seriously, and astrologers and fortune-tellers do a steady business.
        Before a skyscraper can be built, a feng shui (see page 68)
        investigation must take place to ensure that the site and the building
        will promote health, harmony, and prosperity. You’ll also notice that
        gambling is a passion, whether it be cards, mah-jong, the lottery, or
        off-track betting system, and on weekends the ferries to Macau are
        crowded with people on their way to the casinos.
        enthralling water traffic — a mix of freighters, ferries, tugs, junks,
        and yachts. Views of the city and the harbor are panoramic. From
        hotels, they are especially exciting at night when the lights are
        on.
        The business and financial center and the signature soaring
        by ferry and the MTR rail line, is the Kowloon peninsula with its
        hotels, nightlife, and almost non-stop shopping. Beyond, in the New
        Territories, are a mixture of high-rise suburban towns, ancient sites
        and walled villages, country parks, and farms with ducks and fish
        Cheung Chau, provide getaways. You can also take a ferry to Macau to
        find an entirely different kind of city, a unique blend of Chinese and
        Iberian culture.
        It’s anyone’s guess what may happen in the future, but for
        this beautiful city with its contrasts and variety is an exhilarating
        experience.
```
- You can notice that the above passage has no lines that contain `Hong Kong` in it.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 

### Example 6:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:268$ cd written_2/travel_guides/berlitz2
[cs15lwi23aty@ieng6-203]:berlitz2:269$ grep -v "e" Beijing-WhatToDo.txt 
```
- The output:
```




What To Do
Shopping
Shopping Malls and Plazas



```
- All the lines that contain the letter `e` are hidden, only lines without `e` are shown.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 

## `grep -c` Command:
- The command counts all the occurrences of the pattern/text in the file. It is useful when the user tries to find out how many times the pattern occur in the text, and they can use the `grep -c` command to count the number.

### Example 7:
- The input of the command:
```
[cs15lwi23aty@ieng6-201]:skill-demo1-data:271$ cd written_2/travel_guides/berlitz2
[cs15lwi23aty@ieng6-201]:berlitz2:273$ grep -c "Beijing" Beijing-WhereToGo.txt 
```
- The output:
```
66
```
- `Beijing` appears 66 times in the passage `Beijing-WhereToGo.txt`.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 
### Example 8:
- The input of the command:
```
[cs15lwi23aty@ieng6-201]:berlitz2:275$ cd ..
[cs15lwi23aty@ieng6-201]:travel_guides:276$ cd berlitz1
[cs15lwi23aty@ieng6-201]:berlitz1:277$ grep -c "Hong Kong" IntroHongKong.txt 
```
- The output:
```
20
```
- `Hong Kong` appears 20 times in the passage `IntroHongKong.txt`.
- Sources: I found this command by using the `man grep` command in the terminal which gives out lots of examples of grep command. I also use **ChatGPT** to look up how the command is used. Additionally, I used the lecture note to find out some ideas as well. 
