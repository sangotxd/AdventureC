# Adventure in C++ with parser
This project is not meant to be used as a guide to make a parser and it is not meant to release as a game at the momment. 
It's original goal is for educational porpuses.

# How to play

### IMPORTANT NOTES:
This Parser is **grammar sensitive.**
The Parser isn't case sensitve **BOTH LOWERCASE AND UPPERCASE ARE ALLOWED**

### SYNTACK:
```
Input: $Verb + $Name/Item/Adverb/Adjective
```

EXAMPLE: $Verb = "punch" $Name/Item/Adverb/Adjective/Direction = "boss"
```
Input: punch boss
```
### MULTIPLE Name/Item/Adverb/Adjective COMMAND:
```
Input: ask receptionist for money
```

### USING THE INVENTORY AND OBJECTS
GRAB:
```
Input: grab + Item
```

DROP:
```
Input: drop + Item
```
KNOWING WHAT YOU HAVE:
```
Input: inventory
Output: On inventory: Item1, Item2.
```

### THINGS THAT WON'T AFFECT THE OUTCOME
Phrases like "talk to the secretary" will be read as "talk secretary". This is done so it can generate the appropiate id and do the right action on actions.cpp

# WALKTHROUGH
Main Storyline:
- You appear on your bosses office and you have to procced to the next and only room by saying ``` go east``` or ``` go out ```.
- You are now on the secretary office and the game asks you to grab the "bosses mug" and go to a room that's called "Storage 2" to pick the Coffee grains in order to make coffee
- Once youre on the "Free time office" and try to enter the game won't allow it and will ask you to go grab the "Storage Key" at the secretary office by talking to the secretary and ```ask secretary for storage key```
- Now go back to storage to enter "Storage 2" and find no "Coffee grains".
- The game will ask you to go and talk to the receptionist in order to get "5$" (On Reception(Location) say ```ask receptionist for money```) and go to the market and buy "Coffe Grains.
- Now with the "Bosses mug" and "Coffee grains" in your inventory you have to go to the "Free time office" and ``` combine bosses mug with coffee grains``` works in reversal.
- Now the game will ask you what do you want to combine that with and in order to progress you have to say ``` coffee grains``` 
- And it's almost over! Now you have to go to your bosses office and you will beat the game.

# OTHER ENDINGS:
- You can punch your boss at the begining of the game.
- Talking to your colleagues.
- Sleeping at the couch on the Free time office.


# MAP AND ANVIGATION:
```
+-------------+------------------+----------------+------------------+-----------+
|             |                  |                |                  |           |
| Boss Office   Secretary Office   Meeting office | Storage            Storage 2 |
|             |                  |                |                  |           |
+-------------+-------  ---------+----------------+-------  ---------+-----------+
|             |                  |                |                  |           |
| Market        Reception          Open Office      Free time office   Balcony   |
|             |                  |                |                  |           |
+-------------+------------------+----------------+------------------+-----------+
```
```
Input: go + north,south,west,east
```
Locations + Num of actions: Boss Office(Talk, Punch), Secretary Office(Grab,Talk,Ask), Meeting office(Browse), Storage(), Storage2(), Market(Buy),Free time office(Sleep, Play), Reception(Ask), Open Office(Talk), Balcony(Throw, Grab).
# DICTIONARY:

### VERBS:
 - Grab 
 - Use 
 - Play 
 - Throw
 - Get 
 - Talk
 - Drink
 - Buy (Special) You can do: ```buy item1``` or ```buy item1 and item2```
 - Combine (Special) You can do: ```combine item1 with item2```
 - Browse 
 - Ask (Special) You can do: ```ask name1 for/about name2```
 - Sleep 
 - Go 
 - Punch 
 - Drop 
 
### NAMES, ITEMS AND OTHERS :
 - Out (Adverb)
 - North (Direction)
 - East (Direction)
 - West (Direction)
 - South (Direction)

 - Boss (NPC)
 - Receptionist (NPC)
 - Colleagues (NPC)
 - Secretary (NPC)
 
 - Couch(Scene)
 - Videogames(Scene)
 - Notebook (Scene)
 
 - Coffee grains (Object)
 - Soda can (Object)
 - Storage key (Object) (Used)
 - Ps1 controller (Object)
 - Secretary mug  (Object) (Used)
 - 5$ (Object) (Used)
 - Bosses mug (Object) (Used)
 - Coffee (Object) (Used)
 

# TODO:
1. Every room has 2 functions

