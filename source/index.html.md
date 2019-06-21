---
title: Picrafty API

language_tabs: # must be one of https://git.io/vQNgJ
  - Blockly
  - python

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>


---

# Introduction

This is the documentation for the Picrafty API. Each block and its
corresponding python code is documented here.  

This API is based around three classes given in the Raspberry Juice mod used to control the minecraft game world inside Python scripts  
1. Minecraft --- Main class for connecting to and interacting with the game.  
2. Player --- Getting and changing a player's position and settings.  
3. Entity --- Getting and changing an entity's position and settings.  

This documentation is a spin-off of documentation for Raspberry Juice found at: Add source here.  


# Minecraft


## Create Minecraft Connection

Create a connection to your particular minecraft.

```python
mc = Minecraft().create()
```
> Creates a default server.

```python
mc = Minecraft().create("192.162.1.1", 4711)
```
> Specify IP Address and Port.


## Get Block
Retrieve block type located at position x, y, z

```python
blockType = mc.getBlock(0, 0, 0)
```
> Retrives block type at position 0,0,0


## Get Blocks
Get all block ids ranging from one position to another.

```python
blocks = mc.getBlocks(-1, -1, -1, 1, 1, 1)
for block in blocks:
   print(block)
```
> Prints all block ids in a cuboid.


## Get Block with Data
```python
blockObj = mc.getBlockWithData(0,0,0)
```
> retrieves a block object for the block at 0,0,0 

## Set Block
```python
mc.setBlock(0, 0, 0, block.DIRT.id)
```
> sets a block at an x,y,z coordinate to a particular type.

```python
mc.setBlock(0,0,0,block.WOOD.id, 1)
```
> sets a block to a particular type and subtype.

## Set Blocks
```python
mc.setBlocks(-1, -1, -1, 1, 1, 1, block.STONE.id)
```
> Sets many blocks at a time, filling the gap between 2 sets of x,y,z coordinates.

## Get Height
```python
y = mc.getHeight(0,0)
```
> Find the y (vertical) of an x,z coordinate which represents the highest (non-air) block.

## Get Player Entity IDs
```python
entityIds = mc.getPlayerEntityIds()
```
> get the entity ids of the players connected to the game.

## Get Player ID
```python
entityId = mc.getPlayerId("martinohanlon")
```
> Get the entity id of a player named "martinohanlon".

## Save Checkpoint
```python
mc.saveCheckpoint()
```
> Save a checkpoint that can be useful for restoring the world

## Post to Chat
```python
mc.postToChat("Hello Minecraft World")
```
> Writes the message "Hello Minecraft World" to the chat window.

## Change a Setting
```python
mc.setting("world_immutable", True)
```
> Change world immutable to True.

```python
mc.setting("nametags_visible", False)
> Change nametags_visible setting to False.


# Minecraft.player


## Get Player's Position

```Blockly

```
```python
  mc.player.getPos()

```
> Retrieves current position of the player.

## Set Player's Position
Change where you are now to a new position
```python
mc.player.setPos(10, 10, 10)
```
> Sets player's position to be at (10, 10, 10)


## Get Tile Position
```python
playerPos = mc.player.getPos()
```
> Get player position as floats


## Set Tile Position
```python
mc.player.setTilePos(1,1,1)
```
> Move player to tile.


## Change a Player Related Setting
```python
mc.player.setting("autojump", False)
print("Autojump off, 5 seconds to test.")
time.sleep(5)
mc.player.setting("autojump", True)
print("Autojump back on")
```
> Turn autojump off and on.


## Get Player's Rotation
```python
playerRot = mc.player.getRotation()
print(playerRot)
```
> Get and print player rotation.


## Get Player's Pitch
```python
playerPitch = mc.player.getPitch()
```
> Get and print player pitch.

## Get Player's Direction
```python
playerDirection = mc.player.getDirection()
print(playerDirection)
```
> Get and print player direction


# Entity



## Get Entity's Position
```python
entityPos = mc.entity.getPos(entityIds[0])
print("entity pos", entityPos)
```
> Get player's position


## Set Entity's Position
```python
entityPos = mc.entity.getPos(entityIds[0])
print("entity pos", entityPos)
mc.entity.setPos(entityIds[0], 20, 20, 20)
time.sleep(2)
mc.entity.setPos(entityIds[0], entityPos)
```
> 

## Get Position Underneath Entity
```python
 entityTilePos = mc.entity.getTilePos(entityIds[0])
print("Entity tile pos", entityTilePos)
```
> Print Position of tile entity is on.

## Set New Position Underneath Entity
```python
mc.entity.setTilePos(entityIds[0], 15, 1, 25)
time.sleep(2)
mc.entity.setTilePos(entityIds[0], entityTilePos)
```
> Change entity position


## Get Entity's Rotation
```python
entityRot = mc.entity.getRotation(entityIds[0])
mc.postToChat(entityRot)
```
> Get entity rotation.

## Get Entity's Pitch
```python
entityPitch = mc.entity.getPitch(entityIds[0])
mc.postToChat(entityPitch)
```
> Get entity pitch

## Get Entity's Direction
```python
entityDirection = mc.entity.getDirection(entityIds[0])
mc.postToChat("Entity direction = ")
mc.postToChat(entityDirection)
```
> Get entity direction

