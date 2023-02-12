# Lab Report 3
## `grep -rl` Command:
- The command `grep -rl` is used to search the files that contains the specific word in those files. It is useful because if I am trying to find a file that contains "Hi" value, I will use the `grep -rl` command to search for that file. 

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
### Example 2:
- The input of the command:
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:234$ grep -rl "Lucayans"
```
- The output: 
```
written_2/travel_guides/berlitz2/Bahamas-History.txt
```

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
