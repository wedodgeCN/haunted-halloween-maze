 


> Open this page at [https://arcade.makecode.com/#tutorial:https://makecode.com/_edJfkPLMcEPy](https://arcade.makecode.com/#tutorial:https://makecode.com/_edJfkPLMcEPy)

# Haunted Maze!

```blocks
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player)

controller.moveSprite(mySprite)

game.over(false)

scene.onOverlapTile(SpriteKind.Player, assets.tile`transparency16`, function (sprite, location) {
})
scene.cameraFollowSprite(mySprite)
tiles.setTilemap(tilemap`level1`)

info.startCountdown(10)

mySprite = 0
```

```template
```


## Step 1
You've found the haunted maze in the **Castle of Code and Curiosities**! 
This tutorial will teach you how to create your own spooky maze game!

## Step 2
We need a character to explore our maze. To add a character sprite, open the 
``||sprites.Sprites||`` code block menu and find the 
``||variables.set mySprite to||`` block. 
Drag it into the workspace, inside the ``||loops.on start||`` block.

## Step 3
Click the **gray box** in the ``||variables.set mySprite to||`` block and 
draw an image for your character. It could be anything, from a spooky ghost 
or a silly clown to a silly ghost or a spooky clown. 

Click the ▶ button to see your character appear on screen!

## Step 4
Your sprite looks great, but they can't do much just yet. To change that, 
open the ``||conroller.Controller||`` menu and drag a 
``||move mySprite with buttons||`` block under the 
``||variables.set mySprite to||`` block, but still inside the 
``||loops.on start||`` block.

## Step 5
Next, we're going to make our maze. Open the ``||scene.Scene||`` menu and find 
the ``||scene.set tilemap to||`` block. Drag that under the 
``||controller.move mySprite with buttons||`` block.

## Step 6
Click the **gray square** in the ``||scene.set tilemap to||`` block to begin 
drawing a maze. Select one tile from your options to be the floor, and a 
different tile for the walls. Create a maze, being sure to leave a path from 
the begining to the end. 

Click the green **Done** button when you're happy with your maze.

## Step 7
Click the ▶ button to test your game! See what happens when you move your 
character off screen or over a wall.

## Step 8
To make your walls solid, click the image of your maze in the 
``||scene.set tilemap to||`` block. In the editor, find the **Draw walls** 
button (it looks kind of like a wall with the corner missing) and click it. 
It should turn red. Now draw over all your wall tiles; you should see them 
turn red when you do. Click **Done** again when you're finished. 

## Step 9
We should also make sure the camera stays focused on your character. Open the 
``||scene.Scene||`` menu again, and add a ``||scene.camera follow sprite||`` 
block to the ``||loops.on start||`` block.

## Step 10
Now let's add a start and finish location to our maze. Go back into the tilemap 
editor and find tiles that you want to use as the starting point and goal of 
your maze. Use each block exactly one time, and place them where you want 
players to start and finish the maze.

## Step 11
Open the ``||scene.Scene||`` menu again and find the 
``||scene.place mySprite on top of random||`` block. Add that to the 
``||loops.on start||`` container and click the dropdown menu at the end. 
Find your **start** tile and select it.

## Step 12
Now, open the ``||scene.Scene||`` menu again and find the 
``||scene.on sprite of kind Player overlaps||`` block. Drag that into the 
workspace, **outside** of the ``||loops.on start||`` loop. Click the 
dropdown and find your **finish** tile. Click it.

## Step 13
Open the ``||game.Game||`` menu and find the ``||game.game over <LOSE>||`` block. 
Drag that into the ``||scene.on sprite of kind Player overlaps||`` block. Click
the ``||game.<LOSE>||`` toggle to switch it to ``||game.<WIN>||``. 

## Step 14
Click the ▶ button to test your game! Find your way from the start to the finish.

## Step 15
To add some difficulty, let's put a countdown in the game. Now, players will 
have a limited amount of time to find and reach the exit.

Open the ``||info.Info||`` menu and drag the ``||info.start countdown||`` block 
into the bottom of the ``||loops.on start||`` loop. Try out different time 
limits to find one that is fun but challenging.

## Step 16
And just like that, you've done it! You created your own maze game from scratch!
When you click the **Finish!** button, you'll have a chance to publish and share 
your game.

Have a happy Halloween!

```assetjson
{
 "README.md": " ",
 "assets.json": "",
 "images.g.jres": {
     "transparency16": {
         "data": "hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true
     },
     "tile3": {
         "data": "hwQQABAAAADM/M/MzPzPzHf3d3d393d3d/d3d3f3fHfM/8zMzPzMzP//////////fHd3/Hx3d/zMzMz/zMzM////////////zPzMzMzMz8zM/MzMzPzPzP//////////z8zM/M/MzPz//////////8zM/8zMzP/M/////////////////////w==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile1"
     },
     "tile6": {
         "data": "hwQQABAAAAB8x//8zM/P/HzHz/zMz//PfP9//MzP/8z/z3/8zP/////Hf/zM/8/Mf8d//Pz///9/x3/8/8/MzHzHf/z/zMzMfMfP//////98x///zMzM/3zH/393d3f8fPf///////98/8/MzPzMzPz/d3d3/3d3/H93d3d/d3fPzMzM/M/MzA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile4"
     },
     "tile1": {
         "data": "hwQQABAAAAB8x///zP/P/3zHz/zM/8//fMd//Mz///9/zH/8/P//////f/z//8//fMx//M//z/98x8/8z/zP/3zHz//P/M//fMf//8z8z/98x8//zP/P/3zHf/zMz///f8d//MzP/////3/8/8/P/3z3f/zMz8//fMd//MzPz/98x8/8zP/P/w==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile"
     },
     "tile4": {
         "data": "hwQQABAAAADPzMzM/M/MzPx/d3d3f3d3/P93d3f/d3d8/8/MzPzMzHz3////////fMf/f3d3d/x8x///zMzM/3zHz///////fMd//P/MzMx/x3/8/8/MzH/Hf/z8/////8d//Mz/z8z/z3/8zP///3z/f/zMz//MfMfP/MzP/898x//8zM/P/A==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile2"
     },
     "tile5": {
         "data": "hwQQABAAAAD/////////////////////zMz/zMzM/8z//////////8/MzPzPzMz8///////////M/MzMzPzPzMz8zMzMzM/M///////////MzMz/zMzM/3x3d/x8d3f8///////////M/8zMzPzMzHf3d3d393x3d/d3d3f3d3fM/M/MzPzPzA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile3"
     },
     "tile7": {
         "data": "hwQQABAAAAD//P/M//98x//8/8zP/HzH////zM/3fMf////Pz/fM9//8///P9/////z//M/3zMf//M/8z/x8x//8z/z//HzH//zPzP//fMf//P/M//x8x////MzP93zH///8zM/3fPf//Pz/z/f////8/MzP93/H//z8zM/3fMf//P/Mz/x8xw==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile5"
     },
     "tile8": {
         "data": "hwQQABAAAADP/PzMz/98x/z//MzP/HzHzP/8zM/3/8f////Mz/f8/8z8/8zP93z/////z8/3fPfMzPz/z/d898zMzP/P93zH///////8fMf/zMzM//98x893d3f3/3zH////////f8fMzM/MzPz/x3d3/3d3d//Pd3f3d3d398/MzPzPzMzM/A==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile6"
     },
     "tile9": {
         "data": "hwQQABAAAADMzPzPzMzM/Hd393d3d/fPd3f/d3d3/8/MzM/MzPz/x////////3/Hz3d3d/f/fMf/zMzM//98x////////HzHzMzM/8/3fMfMzPz/z/d89////8/P93z3zPz/zM/3fP/////Mz/f8/8z//MzP9//H/P/8zM/8fMfP/PzMz/98xw==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile7"
     },
     "tile2": {
         "data": "hwQQABAAAADMzMzMzMzMzMzMzMzMzMzMzMzMzM/MzMzM/MzMzM/MzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMz8zMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzPzMzMzMzMzM/MzPzMzMzM/MzMzMzMzMzMzMzM/MzMzMzMzMzMzMzMzMzMzA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile0"
     },
     "tile10": {
         "data": "hwQQABAAAAD////////////////////////MzMz/zMz////////////8zMzMzMz8//z8/////////PzMzMzPzP/8/3zMzM/M//z/zPf//////PzM/8zMzP/8/MzPd3fH//z8z893//////z/z/f/zP///MzP98x3//z8zP/8fHf//P/M//98xw==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile8"
     },
     "tile11": {
         "data": "hwQQABAAAAD//P/M//98x//8/Mz//Hx3///8zM/3zHf///z/z/f/zP/8/M/Pd/////z8zM93d8f//PzM/8zMzP/8/8z3//////z/fMzMz8z//PzMzMzPzP/8/P////////zMzMzMzPz/////////////zMzM/8zM/////////////////////w==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile9"
     },
     "tile13": {
         "data": "hwQQABAAAADMzMzMzMzPzMzMzMzM/PbMzMz8//+vZs/MzG9mZvZq9sz8ZqqqZs/2zG+mmZlq9s/Mb5qZmcn2zMxvmpnZyfbMzG+amdnJ9szMb5rZncn2zMxvppmZbPbM/Ppmqqpmz8xvpm9mZvbMzPxm/P//z8zMzG/PzMzMzMzM/MzMzMzMzA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile11"
     },
     "tile12": {
         "data": "hwQQABAAAADMzMzMzMzMzMzMzMzM/M/MzMzMzPxP9MzMzMzMT9S0z8zMzP9F0bTPzMz/VRXdtM/M/FFV3d20z8wfEVVV1LTPzN8RVVVEtM/M/N1VVUS0z8zM/91VRLTPzMzM/0tEtM/MzMzMv0u0z8zMzMz8v/vMzMzMzMz8/8zMzMzMzMzMzA==",
         "mimeType": "image/x-mkcd-f4",
         "tilemapTile": true,
         "displayName": "myTile10"
     },
     "level1": {
         "id": "level1",
         "mimeType": "application/mkcd-tilemap",
         "data": "MTAxMDAwMTAwMDA0MDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTA2MDMwMjAyMDUwMjAyMDIwMjAyMDIwMjAyMDIwMjAyMDUwMzAyMDIwNTAyMDIwMjAyMDIwMjAyMDIwMjAyMDIwNTAzMDIwMjA4MDIwMjBhMDcwNzA3MDcwNzA4MDIwMjA1MDMwMjAyMDIwMjAyMDUwMjAyMDIwMjAyMDIwMjAyMDUwMzAyMDIwMjAyMDIwNTAyMDIwMjAyMDIwMjAyMDIwNTAzMDIwMjBhMDcwNzA4MDcwODAyMDIwOTA3MDcwNzA1MDMwMjAyMDUwMjAyMDIwMjAyMDIwMjAyMDIwMjAyMDUwMzAyMDIwNTAyMDIwMjAyMDIwMjAyMDIwMjAyMDIwNTAzMDcwNzA4MDcwODAyMDIwOTA3MDcwNzBiMDIwMjA1MDMwMjAyMDIwMjAyMDIwMjAyMDIwMjAyMDMwMjAyMDUwMzAyMDIwMjAyMDIwMjAyMDIwMjAyMDIwMzAyMDIwNTAzMDIwMjBhMDcwNzA3MDcwNzA4MDIwMjA5MDcwNzA1MDMwMjAyMDUwMjAyMDIwMjAyMDIwMjAyMDIwMjAyMDUwMzAyMDIwNTAyMDIwMjAyMDIwMjAyMDIwMjAyMGMwNTA5MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA3MDcwNzA4MjIyMjIyMjIyMjIyMjIyMjAyMjAwMDAwMDAwMDAwMjAwMjIwMDAwMDAwMDAwMDIwMDIyMDAwMjIyMjIyMDIyMDAyMDAwMDAyMDAwMDAwMjAwMjAwMDAwMjAwMDAwMDIwMDIyMDIyMjIwMjIwMjIyMjAyMjAwMDAwMDAwMDAwMjAwMjIwMDAwMDAwMDAwMDIwMjIyMjIyMDAyMjIyMDIyMDAyMDAwMDAwMDAwMDAyMjAwMjAwMDAwMDAwMDAwMjIwMDIyMDIyMjIyMjAwMjIyMjAyMjAwMDAwMDAwMDAwMjAwMjIwMDAwMDAwMDAwMDIwMjIyMjIyMjIyMjIyMjIyMg==",
         "tileset": [
             "myTiles.transparency16",
             "myTiles.tile1",
             "myTiles.tile2",
             "myTiles.tile3",
             "myTiles.tile4",
             "myTiles.tile5",
             "myTiles.tile6",
             "myTiles.tile7",
             "myTiles.tile8",
             "myTiles.tile9",
             "myTiles.tile10",
             "myTiles.tile11",
             "myTiles.tile12"
         ],
         "displayName": "level1"
     },
     "*": {
         "mimeType": "image/x-mkcd-f4",
         "dataEncoding": "base64",
         "namespace": "myTiles"
     }
 }
```
