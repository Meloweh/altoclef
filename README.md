# Meloweh's altoclef fork
This fork adds some additional features to altoclef.  
You can find the new features in my branch "Meloweh".

# New commands
## - build (WIP)
### Description:
It's the builder process from baritone but the bot will source missing materials by itself.

### Usage: 
1.) Ensure that the directory ".minecraft/schematics/" exists  
2.) Place a schematic file in "schematics" that is supported by baritone (As an example "myschem.schem")  
3.) Type "@build myschem.schem" in the chat  

### TODO/ISSUES:
- Anti mine protection zone facing needs to be fixed to be relative to the player facing  
- Anti mine protection zones are not seperated by world  
- Anti mine protection zones are not seperated by dimension  

## - autofill (WIP)
### Description:
Allows you to choose a chest and let the bot source and fill it with stuff you have specified.

### Usage:
1.) Look at a chest so that it is selected by the cursor block selection  
2.) Type "@autofill dirt" for an example  

### TODO:
If the inventory is full then non throwaway materials should be stored in a chest either somewhere around or in a 
base.

## - roundtrip
### Description:
Allows you to do tasks and return where you started.
It also allows you to create and save macros out of altoclef commands. That means you can queue a chain of tasks.

### Usage:
- "@roundtrip" queues a new milestone  

  #### Example:  
  @roundtrip get coal 3  
  
  Now a milestone has been added to the queued chain  

- "@roundtrip start" executes the queued chain  

  #### Example:  
  @roundtrip get coal 3  
  @roundtrip get oak_log 2  
  @roundtrip build myschem.schem  
  @roundtrip start  

  Now the bot will first collect 3 coal, then 2 oak_log and then it tries to build the schematic myschem.schem.  

- "@roundtrip stop" stops execution of the queued chain  
- "@roundtrip clear" clears the queued chain  
- "@roundtrip reset" stops and clears the queued chain  
- "@roundtrip list" prints the queue  
- "@roundtrip push" pushes a new command to the macro queue  

  #### Example:  
  @roundtrip push get coal 3  

  Now task "get coal 3" has been added to the macro queue

- "@roundtrip flushas" will save the current macro queue and flushes memory  

  #### Example:  
  @roundtrip push get coal 3  
  @roundtrip push get oak_log 2  
  @roundtrip push build myschem.schem  
  @roundtrip flushas myCoolMacro  

  Now you can let the bot do the exact same thing like in the first @roundtrip example by just typing:  
  @roundtrip myCoolMacro  

- "@roundtrip flush" removes all pushed macros from memory  
- "@roundtrip remove" removes a saved macro from the hard drive  

  #### Example:  
  @roundtrip remove myCoolMacro  
  
  Now a macro that was named myCoolMacro will be removed from the hard drive  



