# Creation of new Pets for PetsReloaded

**Hi everyone!**
In this document you can see how to create a custom pet.
In order to do that you need to see how this file is made. 
For first, **create a file.yml** and *call it how you want your pet to be called for the plugin*, for example **MonkeyPet.yml** and put it in the folder called "pets" on the plugin folder.

```
#The first part is the "information" section; in which you can define every aestetic part of the pet.
information:
  #The Pet name used by the placeholder %pet% on messages.
  petName: "&aMonkey"
  #The list of items used as symbols on GUIs
  symbols:
    The item used as the symbol of the unlocked pet on the GUIs
    unlocked_symbol:
      material: "PLAYER_HEAD"
      #In order to set a skull, you can see another guide in this repository
      skull: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMjFlOTkzMzdkZGMyYzhkMTRjZjlmNTI3ZTk3MjI4NTEzMzU1OGM5NTM3NjVkZTRkZDVkN2E5MTlhOTg4ODIifX1"
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
called "entity" and if is it visible, you can also define other part of the pet such as armorstands; if your pet is made by only armorstands you can delete the "entity" 
and "visibile" entries. 
structure:
  entity: PIG
  visible: true
  stands:
    #Just a reference name to this armorstand, please do not use the same name for more that a reference, because the plugin will not count the other ones.
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
      #every part of the "0:0:0" refers to X:Y:Z of the EulerAngle
      #Use website such as: https://haselkern.com/Minecraft-ArmorStand/ or https://mrgarretto.com/armorstand/ for a better way to create pets
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
``` 

**For a better understanding of the pets creation, you should see every configuration of the default pets.*

