
Hi! In this document you can see how to create a custom pet.
In order to do that you need to see how this file is made. 
For first, create a file.yml and call it how you want your pet to be called for the plugin; for example MonkeyPet.yml

**The first section is the "information" section; in which you can define every aestetic part of the pet.**

information:
  #The Pet name displayed on messages.
  petName: "&aMonkey"
  #The Pet name displayed above the spawned pet.
  displayName: "&aMonkey of %player%"
  #The list of items used as symbols on GUIs
  symbols:
    The item used as the symbol of the unlocked pet on the GUIs
    unlocked_symbol:
      material: "PLAYER_HEAD"
      skull: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMjFlOTkzMzdkZGMyYzhkMTRjZjlmNTI3ZTk3MjI4NTEzMzU1OGM5NTM3NjVkZTRkZDVkN2E5MTlhOTg4ODIifX19"
      name: "&aMonkey"
      lore:
        - ""
        - "&7The slowest in the race,"
        - "&7But gets first place!"
        - ""
        - "&aUnlocked"
    The item used as the symbol of the locked pet on the GUIs    
    locked_symbol:
      material: "GRAY_DYE"
      name: "&cMonkey"
      lore:
        - ""
        - "&7The slowest in the race,"
        - "&7But gets first place!"
        - ""
        - "&cLocked"
  #The permission required to unlock this pet      
  permission: "pets.monkey"
#The section where you can create all the items need in order to create the pet, you can use each name in the section below to put them on the armorstands.  
items:
  head:
    material: "PLAYER_HEAD"
    skull: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMjFlOTkzMzdkZGMyYzhkMTRjZjlmNTI3ZTk3MjI4NTEzMzU1OGM5NTM3NjVkZTRkZDVkN2E5MTlhOTg4ODIifX19"
  lead:
    material: "LEAD"
  chest:
    material: "LEATHER_CHESTPLATE"
    
#the structure part is the most important part, because on here you have to define if your pet is made by only a basic entity, 
called "entity" and if it's visible and also you can define other part such as armorstands; if your pet is made by of only armorstands you can delete the "entity" 
and "visibile" entries. 
structure:
  entity: PIG
  visible: true
  stands:
    #Just a reference name to this armorstand, please do not use the same name for more that a reference.
    base:
      #On here you have to define what items does the armorstand have to have in: helmet, chestplate, legs, foot
      helmet: head
      chestplate: chest
      small: false
      #Here you can set the offset of each armorstand in relation of the spawnpoint
      location:
        xOffset: 0.0
        zOffset: 0.0
        yOffset: -0.7
      #On here you have to define every position for every part of the stand; you can remove the part that you don't need  
      positions:
        headPos: "0:0:0"
        bodyPos: "55:0:0"
        leftArmPos: "0:0:0"
        rightArmPos: "0:0:0"
        leftLegsPos: "0:0:0"
        rightLegsPos: "0:0:0"
    arms:
      chestplate: chest
      small: false
      location:
        xOffset: 0.0
        zOffset: 0.0
        yOffset: -1.1
      positions:
        headPos: "0:0:0"
        bodyPos: "90:0:0"
        leftArmPos: "0:0:0"
        rightArmPos: "0:0:0"
        leftLegsPos: "0:0:0"
        rightLegsPos: "0:0:0"
    body:
      chestplate: chest
      small: false
      location:
        xOffset: -0.5625
        zOffset: 0.0
        yOffset: -1.1
      positions:
        headPos: "0:0:0"
        bodyPos: "-115:0:0"
        leftArmPos: "0:0:0"
        rightArmPos: "0:0:0"
        leftLegsPos: "0:0:0"
        rightLegsPos: "0:0:0"
    tail:
      handItem: lead
      small: false
      location:
        xOffset: -0.65
        zOffset: 0.87
        yOffset: -0.9
      positions:
        headPos: "0:0:0"
        bodyPos: "0:0:0"
        leftArmPos: "0:0:0"
        rightArmPos: "270:90:0"
        leftLegsPos: "0:0:0"
        rightLegsPos: "0:0:0"
