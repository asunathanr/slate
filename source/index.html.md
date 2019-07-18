---
title: Picrafty API

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>


---
# Getting Started


## Menu bar
###Create your own Script

**File Name**: Enter the name of your script. 

**Naming Exceptions**: Cannot contain the following characters: 

* ? (Question Mark) 

* : (Colon)

* " (Double Quote)

* / (Forward Slash)

* \ (Back Slash)

* | (Veritcal Bar)

* \* (Asterisk)
 
* < (Less Than)

* \> (Greater Than)


##Create Script

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

This documentation is a spin-off of documentation for Raspberry Juice found at: **https://www.stuffaboutcode.com/p/minecraft-api-reference.html**  


# Minecraft

## Get Block
Retrieve block type located at Position variable

<img src="images/GetBlock.png" alt="Get block" width="250" height="100"/>


## Get Blocks
Get all block IDs ranging from one position to another

<img src="images/GetBlocks.png" alt="Get multiple blocks" width="250" height="100"/>


## Get Block Type and ID
Get the block Type and corresponding ID

<img src="images/GetBlockWithData.png" alt="Get block with data" width="250" height="100"/>


## Set Block
Sets a block at a Position variable to a particular type

<img src="images/SetBlock.png" alt="Set block" width="250" height="150"/>


## Set Blocks
Set many blocks at a time, filling the gap between 2 sets of Position variables

<img src="images/SetBlocks.png" alt="Set multiple blocks" width="250" height="200"/>


## Get Height
Find the y(vertical) of an x, z coordinate which represents the highest (non-air) block.

<img src="images/GetHeight.png" alt="Get height" width="250" height="100"/>


## Get Player Entity IDs
Get the entity IDs of the players connected to the game.

<img src="images/GetPlayerIds.png" alt="Get IDs of players in game" width="250" height="85"/>


## Get Player ID
Get the entity ID of a player

<img src="images/GetPlayerID.png" alt="Get a player's ID" width="250" height="85"/>


## Post to Chat
Writes the message to the chat window

<img src="images/PostToChat.png" alt="Post message to chat" width="250" height="100"/>
 



# Player

## Get Player's Position

Outputs player's current position.

<img src="images/GetPlayerPos.png" alt="Get player position" width="250" height="125"/>


## Set Player's Position
Change player's current location to a new position

### Input
 Position variable
 
<img src="images/SetPlayerPos.png" alt="Set player position" width="250" height="100"/>


## Get Tile Position
Output: Position of tile coordinates.

<img src="images/GetPosUnderPlayer.png" alt="Get tile position" width="250" height="100"/>


## Set Tile Position
Input: Position variable

<img src="images/SetPlayersPosOnTopOf.png" alt="Set player's position to tile" width="250" height="100"/>


## Get Player's Rotation
Output: Rotation angle as float

<img src="images/GetPlayersAngleOfRotation.png" alt="Get player's angle of rotation" width="250" height="100"/>


## Get Player's Pitch
Output: Pitch angle as float

<img src="images/GetPlayersPitch.png" alt="Get player's angle of pitch" width="250" height="100"/>


## Get Player's Direction
Output: Player direction as Position variable

<img src="images/GetPlayersDirection.png" alt="Get player's direction" width="250" height="100"/>




# Position

<img src="images/PositionModify.png" alt="Modify position" width="400" height="100"/>




# Entity

## Get Entity's Position
Input: Entity ID (can get using mc.getPlayerIds())

<img src="images/GetEntitysPos.png" alt="Get entity's position" width="350" height="100"/>


## Set Entity's Position
Input: Entity ID (can get using mc.getPlayerIds())

* Position variable

<img src="images/SetEntityPos.png" alt="Set entity's position" width="350" height="100"/>


## Get Position of Tile Underneath Entity
Input: Entity ID

Output: Position variable of the tile that an entity is on

<img src="images/GetPosDirectlyUnderEntity.png" alt="Get position of tile under entity" width="350" height="100"/>


## Set New Position Underneath Entity
Input: 
* Entity ID

* Position variable

<img src="images/SetNewPositionUnderEntity.png" alt="Set entity's new position" width="450" height="100"/>


## Get Entity's Rotation
Input: Entity ID

Output: Entity rotation angle

<img src="images/GetEntitysRotation.png" alt="Get entity's rotation" width="350" height="100"/>


## Get Entity's Pitch
Input: Entity ID

Output: Entity Pitch Angle

<img src="images/GetEntitysPitch.png" alt="Get entity's pitch" width="350" height="100"/>


## Get Entity's Direction
Input: Entity ID

Output: Position variable of entity direction

<img src="images/GetEntitysDirection.png" alt="Get entity's position" width="350" height="100"/>




# Block

## Modify Block
Input: Takes block variable

Output: New block type

<img src="images/ModifyBlock.png" alt="Modifies block" width="400" height="100"/>
