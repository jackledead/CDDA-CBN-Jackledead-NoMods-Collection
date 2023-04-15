# CDDA-NoMods-Anthology
Jackledead's Fork of Kenan's **separate** No_Mods anthology for **LATEST** versions of Cataclysm - Dark Days Ahead and Bright Nights releases

**1) IF YOU ARE EXPERIENCING ANY BUGS OR ERRORS - EITHER THE FIXES WILL BE RELEASED SOON-ISH OR THE MOD IS WIP** ;

**2) IF YOU USE CDDA LAUNCHER BY REMYROY - UPDATE THE GAME FIRST VIA LAUNCHER and ONLY AFTER that put the mods IN**

# Installation Guide (MUST-READ)

**1) Download the No_Mods anthology** ;

**2) Copy all of the mods from the anthology folder as shown in the picture** https://imgur.com/a/cpok2UT ;

**3) Paste them all into the `cdda/data/mods` directory as shown in the picture** https://imgur.com/a/mK1cEER ;

**4) Overwrite and replace all the files if you get a prompt** ;

**5) Enjoy the mods**

**NEXT STEPS IF YOU USE THE LAUNCHER** 

**6) Update the game via the launcher** ;

**7) Repeat 2) , 3) , 4) and 5)** ;

**8) Enjoy the mods**

# NO! Mod Starter Kit by GoatGod
Have something you want to remove from the game? Perhaps the katana feels particularly overpowered, or the acid zombies just don't sit right with you. And, of course, you can't just settle for one of the already created mods. They don't have the right combination of features, remove too much, remove too little, and just generally are a nuisance to maintain. So, you want to create your own. 

It is, in fact, very simple. First, create a folder with your mod name, perhaps 'NO_pesky_insects', or 'NO_irritating_animals'. Put this folder inside your "\CDDA\data\mods\" folder. Second, create a '.json' file inside of the new folder. Name this file 'modinfo', and open it. 

Inside the file, if you want to remove some combination of monsters and items, paste this code (without the triple backticks):
```JSON
[
  {
    "type": "MOD_INFO",
    "id": "no_personal_edition",
    "name": "Put the display name of your NO! mod here. Keep it short and sweet.",
    "description": "Write a short description of your NO! mod here.",
    "category": "monster_exclude",
    "dependencies": [ "dda" ],
  },
  {
    "type": "MONSTER_BLACKLIST",
    "monsters": [
        "pesky_insect"
    ]
  },
  {
    "type": "ITEM_BLACKLIST",
    "whitelist": false,
    "items": [
        "irritating_item"
    ]
  }
]
```
If you don't want to remove any monsters (this category includes animals), paste this code (again without the backticks):
```JSON
[
  {
    "type": "MOD_INFO",
    "id": "no_personal_edition",
    "name": "Put the display name of your NO! mod here. Keep it short and sweet.",
    "description": "Write a short description of your NO! mod here.",
    "category": "monster_exclude",
    "dependencies": [ "dda" ],
  },
  {
    "type": "ITEM_BLACKLIST",
    "whitelist": false,
    "items": [
        "irritating_item"
    ]
  }
]
``` 
And, if you don't want to remove any items paste this code (again without the backticks):
```JSON
[
  {
    "type": "MOD_INFO",
    "id": "no_personal_edition",
    "name": "Put the display name of your NO! mod here. Keep it short and sweet.",
    "description": "Write a short description of your NO! mod here.",
    "category": "monster_exclude",
    "dependencies": [ "dda" ],
  },
  {
    "type": "MONSTER_BLACKLIST",
    "monsters": [
        "pesky_insect"
    ]
  }
]
```
Now for the tricky part: filling out the blacklists. To do this, you will have to search the '.json' files for the specific id of the item/monster you want to remove. The '.json' files are stored in "CDDA\data\json". If you want to remove an item, look through "\data\json\items". If you want to remove a monster, look through "\data\json\monsters". An example is included below. 

Let's say we wanted to remove the aforementioned katana and acid zombies from the game. Since a katana is an item, we'll start by looking through "\data\json\items". A search for katana reveals it under 'swords_and_blades.json' with the id of katana, along with katana_fake and katana_inferior. Fortunately, NO Acid Zombies is a pre-existing mod in this modpack, so we just copy the list of blacklisted monsters from there. Our final code will end up looking like this: 
```JSON
[
  {
    "type": "MOD_INFO",
    "id": "no_personal_edition",
    "name": "Put the display name of your NO! mod here. Keep it short and sweet.",
    "description": "Write a short description of your NO! mod here.",
    "category": "monster_exclude",
    "dependencies": [ "dda" ],
  },
  {
    "type": "MONSTER_BLACKLIST",
    "monsters": [
      "mon_zombie_spitter",
      "mon_zombie_corrosive",
      "mon_zombie_acidic",
      "mon_zombie_soldier_acid_1",
      "mon_zombie_soldier_acid_2",
      "mon_zombie_wretched"
    ]
  },
  {
    "type": "ITEM_BLACKLIST",
    "whitelist": false,
    "items": [
        "katana",
        "katana_fake",
        "katana_inferior"
    ]
  }
]
```
# Link to Supporters' and Contributors ASTOUNDINGLY NOICE WORKS

**1) https://discourse.cataclysmdda.org/t/secronom-zombies-mod-thread/16211**

**2) Legendary UDP tileset by SDG - https://github.com/SomeDeadGuy/UndeadPeopleTileset**

**3) https://github.com/chaosvolt/cdda-arcana-mod**

**4) https://github.com/TheGoatGod/Goats-Mod-Compilation**

**5) https://github.com/captainsawbones/Sly_Mutation_Mod_Medley**

**6) https://github.com/foulman/Fantasy**

**7) https://github.com/El-Jekozo/More_NPC**

**8) https://github.com/Noctifer-de-Mortem/nocts_cata_mod**

**9) https://github.com/foulman/Psioniclysm**

**10 )https://github.com/Maleclypse**

**11) https://discourse.cataclysmdda.org/t/fallout-new-england/17509**

**12) https://github.com/dissociativity/PKs_Rebalancing**

# Links to Kenan's other works

HUGE and AWESOME **BL9** mod

**1) https://github.com/Kenan2000/BL9**

Personal maintained CDDA modpack for **LATEST** experimental versions

**2) https://github.com/Kenan2000/CDDA-Kenan-Modpack**

Updated and even more awesome Otopack soundpack maintained by kenan

**3) https://github.com/Kenan2000/Otopack-Mods-Updates**

Bright Nights modpack

**4) https://github.com/Kenan2000/Bright-Nights-Kenan-Mod-Pack**

## Link to kenan's CDDA modding server 

**https://discord.com/invite/xj9E3Sp**
