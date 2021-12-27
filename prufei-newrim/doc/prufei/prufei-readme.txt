Mod Name:
    PRUFEI - Protection for Recipes Using Favorite and Equipped Items

Version:
    0.7.2

Important note for end users:
    Requires Elementary Smelting v0.9.3 or greater (or another compatible mod).
    This version WILL NOT WORK WITH ELEMENTARY SMELTING v0.9.2 OR EARLIER!
    If you are using version 0.7.1 you do NOT need to upgrade.
    This version simply does not depend on the Unofficial Skyrim patches.

Author:
    Matthew R. Karlsen (mattrk)

Nexus Mods files page:
    https://www.nexusmods.com/skyrim/users/3546091?tab=user+files

Mod Description:
    This mod stops you accidentally breaking-down favorite and equipped items when
    using recipes in compatible mods. This mod would have been impossible without
    major assistance from 'mrpwn' and 'IsharaMeradin' (who are not responsible for
    any bugs that may remain). ipmlj has also provided assistance improving the text
    used in the mod's messages. 

    For the mod to actually protect favorite items requires the break-down recipes to
    be set up in a particular way, such as in the "Elementary Smelting" mod, or
    in other mods that make use of PRUFEI. By itself this mod will have no effect,
    it merely enables the *possibility* of breakdown recipes that protect items.
    
Installation:
    Install SKSE from https://skse.silverlock.org/ using Vortex or another mod manager
    Install PRUFEI using Vortex or another mod manager

Changes:
    v0.5.1 -- Initial public release.
    v0.6.1 -- The script has been made more robust via the introduction of a 
              maintenance function.
    v0.6.2 -- Small change to ensure the mod updates smoothly from v0.5.1.
    v0.7.1 -- Crafting access is blocked whilst your favorites list is updated.
    v0.7.2 -- Remove dependency on the Unofficial Skyrim Patch.

Credits:
    Created by Matthew R. Karlsen
    This mod would have been impossible without major assistance from 'mrpwn' and 
    'IsharaMeradin'. They have provided valuable assistance both in creation of
    the initial public release and in creation of the more robust v0.6.2 release.
    For the v0.6.2 release 'mrpwn' provided a suggestion to improve compatibility
    with game controllers and also pointed me in the correct direction with 
    respect to the implementation of a maintenance function. ipmlj has also 
    provided assistance improving the text used in the mod's messages.
    These mod authors are not responsible for any bugs that may remain.
        
Thanks:
    Bethesda, for creating the game and making it moddable.
    You, for downloading and trying this mod.
    
For Mod Authors:
    To use PRUFEI you must set it's ESP as a master file (ESM) when editing your mod
    ESP (using Wrye Bash or similar) and then set the ESM back to an ESP after
    editing.

    The following conditional rules are required in each recipe (for example):
      PL    GetItemCount    Armor:'ArmorDwarvenBoots'    >     1.00    OR
      PL    GetItemCount    Armor:'ArmorDwarvenBoots'    >     0.00    AND
      PL    GetItemCount    Armor:'ArmorDwarvenBoots'    >     1.00    OR
      R     GetItemCount    Armor:'ArmorDwarvenBoots'    ==    0.00    AND
      PL    GetItemCount    Armor:'ArmorDwarvenBoots'    >     1.00    OR
      PL    GetEquipped     Armor:'ArmorDwarvenBoots'    ==    0.00    AND

    In the above example the breakdown recipe is using 'ArmorDwarvenBoots' as the
    input item. You can replace ArmorDwarvenBoots with any item you want to use.
    For the 'R' recipe, you want to select the Cell as 'PRUFEICell' and the Ref
    as 'PRUFEIChest 030012D2'.

License:

The .esp file contains data that belongs to the game's creators and is supplied under their particular license.
The changes specific to this mod, made by the mod authors, are released under the license in the LICENSE file.
