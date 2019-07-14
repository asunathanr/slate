---
title: Picrafty API

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>


---
# Getting Started


## Menu bar
###Create your own Script

**File Name**: Enter the name of your script. 

**Naming Exceptions**:

Cannot contain the following characters: 

* ? (Question Mark) 

* : (Colon)

* " (Double Quote)

* / (Forward Slash)

* \ (Back Slash)

* | (Veritcal Bar)

* \* (Asterisk)
 
* < (Less Than)

* \> (Greater Than)

**Create Script**:


### Save and Load Blocks

Save Workspace to file and load Workspace from file

**Save Blocks**: Saves current Workspace to a file.

**Load Blocks**: Loads Workspace from a file.

### Create and Restore Snapshot

Snapshot is all of the blocks in the current Workspace.

**Create Snapshot**: Saves current state of workspace.

**Restore Snapshot**: Restores the previous snapshot and corresponding code. 

## View your Code

To display code created by current block Workspace, click Code tab.

Click Workspace to return to block view.

# Introduction

This is the documentation for the Picrafty API. Each block and its
corresponding python code is documented here.  

This API is based around three classes given in the Raspberry Juice mod used to control the minecraft game world inside Python scripts  
1. Minecraft --- Main class for connecting to and interacting with the game.  
2. Player --- Getting and changing a player's position and settings.  
3. Entity --- Getting and changing an entity's position and settings.  

This documentation is a spin-off of documentation for Raspberry Juice found at: **Add source here**.  


# Minecraft


## Get Block
Retrieve block type located at position x, y, z

<img src="images/GetBlock.png" alt="Get Block" width="250" height="100"/>

> Retrives block type at position 0,0,0


## Get Blocks
Get all block ids ranging from one position to another.

<img src="images/GetBlocks.png" alt="Get Blocks" width="250" height="100"/>

> Prints all block ids in a cuboid.


## Get Block Type and ID
Get the block Type and corresponding ID.

<img src="images/GetBlockWithData.png" alt="Get Block with Data" width="250" height="100"/>

> retrieves a block object for the block at 0,0,0 

## Set Block
Sets a block at an x,y,z coordinate to a particular type.

<img src="images/SetBlock.png" alt="Set Block" width="250" height="100"/>

> sets a block at an x,y,z coordinate to a particular type.

> sets a block to a particular type and subtype.

## Set Blocks
Set many blocks at a time, filling the gap between 2 sets of x,y,z coordinates.

<img src="images/SetBlocks.png" alt="Set several Blocks" width="250" height="100"/>

> Sets many blocks at a time, filling the gap between 2 sets of x,y,z coordinates.

## Get Height
Find the Y(vertical) of an x,z coordinate which represents the highest (non-air) block.

<img src="images/GetHeight.png" alt="Get Height" width="250" height="100"/>


> Find the y (vertical) of an x,z coordinate which represents the highest (non-air) block.

## Get Player Entity IDs
Get the entity IDs of the players connected to the game.

<img src="images/GetPlayerIds.png" alt="Get IDs of players in game" width="250" height="100"/>


> get the entity ids of the players connected to the game.

## Get Player ID
Get the entity ID of a player

<img src="images/GetPlayerID.png" alt="Get a Player ID" width="250" height="100"/>


> Get the entity id of a player named "martinohanlon".

## Post to Chat
Writes the message to the chat window

<img src="images/PostToChat.png" alt="Post message to chat" width="250" height="100"/>
 
> Writes the message "Hello Minecraft World" to the chat window.


# Player

## Get Player's Position

Outputs a Vec3 object with player's current position.

<img src="images/GetPlayerPos.png" alt="Get Player Position" width="250" height="100"/>


> Retrieves current position of the player.

## Set Player's Position
Change where you are now to a new position
### Input
 x,y,z coordinates (can be grouped in a Vec3 object)
 
<img src="images/SetPlayerPos.png" alt="Set Player Position" width="250" height="100"/>

> Sets player's position to be at (10, 10, 10)


## Get Tile Position
Output: Vec3 object of tile coordinates.

<img src="images/GetPosUnderPlayer.png" alt="Get Tile Position" width="250" height="100"/>

> Get player position as floats


## Set Tile Position
Input: x,y,z (can be grouped into a single Vec3 object)

<img src="images/SetPlayersPosOnTopOf.png" alt="Set player's position to tile" width="250" height="100"/>


> Move player to tile.


## Get Player's Rotation
Output: Rotation angle as float

<img src="images/GetPlayersAngleOfRotation.png" alt="Get Tile Position" width="250" height="100"/>


> Get and print player rotation.


## Get Player's Pitch
Output: Pitch angle as float

<img src="images/GetPlayersPitch.png" alt="Get Tile Position" width="250" height="100"/>


> Get and print player pitch.

## Get Player's Direction
Output: Player direction as Vec3 object.

<img src="images/GetPlayersDirection.png" alt="Get Player's Direction" width="250" height="100"/>

> Get and print player direction

# Position

**COME BACK TO!!!!!** 

<img src="images/Position.png" alt="Modify Position" width="350" height="100"/>



# Entity


## Get Entity's Position
Input: Entity ID (can get using mc.getPlayerIds())

<img src="images/GetEntitysPos.png" alt="Get Entity's Position" width="250" height="100"/>


> Get player's position


## Set Entity's Position
Input:
* Entity ID (can get using mc.getPlayerIds())

* x,y,z coordinates (can be grouped in Vec3 object)

<img src="images/SetEntityPos.png" alt="Set Entity's Position" width="250" height="100"/>

> 

## Get Position of Tile Underneath Entity
Input: Entity ID
Output: Vec3 position of the tile that an entity is on.

<img src="images/GetPosDirectlyUnderEntity.png" alt="Get Position of Tile Under Entity" width="250" height="100"/>


> Print Position of tile entity is on.

## Set New Position Underneath Entity
Input: 
* Entity ID
* x,y,z coordinates (can be grouped in a Vec3 object)

<img src="images/SetNewPositionUnderEntity.png" alt="Set Entity's New Position" width="250" height="100"/>


> Change entity position


## Get Entity's Rotation
Input: Entity ID
Output: Entity rotation angle

<img src="images/GetEntitysRotation.png" alt="Get Entity's Rotation" width="250" height="100"/>


> Get entity rotation.

## Get Entity's Pitch
Input: Entity ID
Output: Entity Pitch Angle

<img src="images/GetEntitysPitch.png" alt="Get Entity's Pitch" width="250" height="100"/>


> Get entity pitch

## Get Entity's Direction
Input: Entity ID
Output: Vec3 object of entity direction.

<img src="images/GetEntitysDirection.png" alt="Get Entity's Position" width="250" height="100"/>


> Get entity direction


# Block


