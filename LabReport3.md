# Lab Report 3
## `grep -rl` Command:
- The command `grep -rl` is used to search the files that contains the specific word in those files. If I am trying to find a file that contains "Hi", I will use the `grep -rl` command to search for that file.
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:233$ grep -rl "Bahamas"
.git/index
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```
```
[cs15lwi23aty@ieng6-203]:skill-demo1-data:234$ grep -rl "Lucayans"
written_2/travel_guides/berlitz2/Bahamas-History.txt
```
