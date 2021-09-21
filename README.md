 


> Open this page at [https://wedodgecn.github.io/haunted-halloween-maze/](https://wedodgecn.github.io/haunted-halloween-maze/)

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

##Step 16
And just like that, you've done it! You created your own maze game from scratch!
When you click the **Finish!** button, you'll have a chance to publish and share 
your game.

Have a happy Halloween!