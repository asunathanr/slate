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

## Set Block

## Set Blocks

## Get Height

## Get Player Entity IDs

## Get Player ID

## Save Checkpoint

## Post to Chat
```python
mc.postToChat("Hello Minecraft World")
```
> Writes the message "Hello Minecraft World" to the chat window.

## Change a Setting


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


## Set Tile Position


## Change a Player Related Setting


## Get Player's Rotation


## Get Player's Pitch


## Get Player's Direction



# Entity

## Get Entity's Position

## Set Entity's Position

## Get Position Underneath Entity

## Set New Position Underneath Entity

## Get Entity's Rotation

## Get Entity's Pitch

## Get Entity's Direction


