BreadEternal.

tl;dr

1. Add Comment component with text "BreadEternalMaster" to your main bread.
2. Add Comment component with text "BreadEternalMinion" to empty (and properly connected) breads to give main bread redundancy without performance impact.
3. Done.

Video guide:
https://raw.githubusercontent.com/CornHollioFTD/BreadEternal/main/BreadEternal%20Setup.mov


Explanation:

BreadEternal is a mod that allows your bread to keep working after destruction/disconnect of its original breadboard block, without needing to add multiple full copies of the bread.

Its purpose is to improve loading time and gamespeed by having only one instance of full bread present and running on the vehicle. And to simplify bread maintenance/baking by removing the need to synchronize changes between multiple breads.

The mod works by keeping track of breadboard blocks, and when bread marked as Master is destroyed or disconnected from mainframe, BreadEternal will move Master's content into alive and connected bread marked as Minion.
Master will be moved as is - keeping its Outputs, timers, etc.

If no valid Minions are left for the Master to move into - Master-bread will stop working, as expected from destroyed breadboard.

Marking of breadboards is done by adding to the bread a Comment component with text containing "BreadEternalMaster" or "BreadEternalMinion". 
Only marked breadboards will be affected by the mod.

BreadEternal give no unfair advantages in combat - there is no indestructible blocks, Master-bread will be affected by combat damage to mainframes and it can be destroyed.
BreadEternal is fully compatible with vanilla, as it does not add any new components or blocks. It can be removed at any time.
BPs created for use with the mod will work in vanilla (just without redundancy for Master-bread), and BPs without marked breads will work as usual with the mod active.



Random notes:

Do not add multiple markers to the same bread.

Do not mark multiple breads as Master - only first one loaded will be Master, the rest will be considered Minions, and it's entirely pointless.

There is a third marker - "BreadEternalOptOut". Once discovered, the mod will completely ignore vehicle with such marker. There is absolutely no reason to use this marker - it will save you a nanosecond at best. But the option is there, in case you really really want it.

After been moved, Master-bread will use the exact same mainframe connection that Minion had - same Primary target, etc.

While in build mode, the mod will ignore disconnected or removed Master, so you don't have to hunt it down.

After original Master breadboard block is repaired or reconnected - Master will be moved back into it.

When vehicle is saved - Master will always be saved at its current location. Use "Repair All" after combat for best result.

Minion-breads are "real" breads - you can have stuff in them and it will work (that is until Master will get moved into it).



There is no Steam support.

To install the mod:
1. Download BreadEternal.zip.
https://raw.githubusercontent.com/CornHollioFTD/BreadEternal/main/BreadEternal.zip
2. Unzip it into FtD's mod folder.
3. It should look something like this:
c:\Users\[YourUserName]\Documents\From The Depths\Mods\BreadEternal\BreadEternal.dll

