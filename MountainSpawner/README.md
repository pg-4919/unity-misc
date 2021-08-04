## Installation ##
Sounds fancy, but just copy the code into MountainSpawner.cs and attach it to a Unity Empty. The inspector will have a Mountain Prefab option, and a Player Obj option. These are fairly self explanatory.

## Inspector Settings ##
Setting|Description
-|-
Z-Axis Offset|How far behind the player the mountains spawn; goes in the positive-Z direction.
Spawning Distance|How close the player has to be in order to spawn a new mountain.
Where To Start Generation|Where the mountains begin to spawn; negative-X direction.
Pre Generated Mountains|How many mountains to spawn before the Update loop, useful if Where To Start Generation is more than the Spawning Distance away.
Mountain Limit|How many concurrent mountains can exist at a time.

## A note on the prefabWidth ##
This is a way to dynamically spawn mountains based on their width, which ensures that mountains are always right next to each other. However, for this to work, the prefab origin must be directly in the center of the model. If this isn't true, some gaps might occur. Who cares, though?

## Modifying ##
The mountains only spawn in the positive-X direction. If you want it to go in another direction, you have to modify the code yourself. Change:
* Line 11
* Line 13
* Line 23
* The entire Update loop
* Lines 38-39
