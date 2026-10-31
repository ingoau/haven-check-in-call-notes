# Haven Check-in Call #2, part 2 — Jumpstart (Godot platformer) workshop — transcript

> **Machine-generated transcript.** Produced locally with [faster-whisper](https://github.com/SYSTRAN/faster-whisper) (`medium.en`, CPU, int8). It has **not** been proofread and contains mishearings (names, URLs, jargon), repeated fragments and short gaps where the model dropped speech. Where I could cross-check against the shared slides, the cleaned-up facts are in [`notes/check-in-call-2-jumpstart-workshop.md`](../notes/check-in-call-2-jumpstart-workshop.md).
>
> - **Recording:** Hack Club Haven Jumpstart workshop (Godot 2D platformer), recorded straight after check-in call #2, ~43.7 min including a short Q&A
> - **Recorded:** Sat 19 Sep 2026 15:48 UTC = **Sun 20 Sep 2026 1:48 AM AEST** (Canberra; before daylight saving began) = Sat 19 Sep 11:48 AM EDT (US Eastern)
> - **Timestamps** are `[HH:MM:SS]` from the start of the recording.
> - **Speakers:** not labelled (the transcription has no speaker diarisation). Names appear only where the speakers said them out loud.
> - **Method note:** the final text was assembled from two transcription passes of the same model (voice-activity-detection on, and off), choosing the fullest pass for each 30-second window, because each single pass skipped some stretches. Short fragments near window edges may therefore repeat or be cut. Unintelligible sections are simply missing.

---

[00:00:00] So OK, so basically, this is just the starting screen  
[00:00:11] once you download Godot.  
[00:00:12] And then we're just going to start off  
[00:00:14] by creating the project.  
[00:00:16] And then you can name this whatever you want.  
[00:00:19] I think basically, this is the base 2D platformer.  
[00:00:23] So in this workshop, I'll just show you  
[00:00:25] how to make the little character that can run around.  
[00:00:29] then after you guys can like choose some and then like change the assets and stuff so like let's say  
[00:00:36] i wanted to make like a space platformer then i would just like title it here um and then for  
[00:00:43] project path i have like a folder i have for all the games i make so if you guys want to  
[00:00:50] like organize it then you can like create a new folder um and then you can like create it here  
[00:00:56] and by the way if you guys have any questions or want me to pause along the way, you can send a chat.  
[00:01:03] And then also the settings,  
[00:01:05] there's a few different renders. The first one forward plus is a good in-between,  
[00:01:11] so we'll just use this one and then go ahead and create the game.  
[00:01:18] And then okay, so this is the main interface. It may look a little maybe overwhelming at first,  
[00:01:25] but I'm going to explain some of the different parts of it.  
[00:01:31] So first over here is the scene area.  
[00:01:37] And basically, the way Godot and a lot of different game  
[00:01:41] engines work is they have different nodes, which  
[00:01:45] are just basically things.  
[00:01:49] And they all have a ton of different properties.  
[00:01:52] You would want to use the forward plus render.  
[00:01:57] So yeah.  
[00:01:59] And then I'm going to go more into creating the specific nodes later, but they all have their own  
[00:02:02] creating the specific nodes later um but they all have their own properties and then later we  
[00:02:11] can like make a player and stuff and then down here is the file system and basically,  
[00:02:18] this is where you will have the files of the nodes and also when you add like tileset images,  
[00:02:26] which is basically like what your environment will look like or like maybe you want to create  
[00:02:30] like, or like maybe you want to create your own assets and draw like a really cool background  
[00:02:34] or animation or add sounds, then you'll find all of those in the file system here.  
[00:02:41] And then at the top, like there's a few different like modes. We're making a 2D platformer,  
[00:02:47] So we'll just go to 2D here.  
[00:02:50] And then you can see  
[00:02:52] see this very light, like, purple rectangle.  
[00:02:56] This is the game view.  
[00:02:58] So yeah, that's like the main component.  
[00:03:01] So we can get started on making it.  
[00:03:04] So first, we're going to create like an O to contain  
[00:03:08] the whole game.  
[00:03:10] So we'll click other node and then just choose  
[00:03:13] the first one which is just like the white circle um yeah and we can also rename it if you want to  
[00:03:24] be like main and then uh you should like save your project so like you can do command s or  
[00:03:31] like file save or something and then once we have our main node that will contain everything  
[00:03:38] we can go ahead and create our player. So as you can see, just looking at all the different  
[00:03:46] node types, they're all for different purposes. This one is for making a player animation and  
[00:03:52] stuff. But the one that's used most for having a player in the game is the Character Body 2D.  
[00:04:00] So you can do like under main plus and then search up this one.  
[00:04:07] And then you can also name it like player or like whatever your players name is.  
[00:04:16] And then here, like  
[00:04:21] So under the player node, so it's all like very hierarchical.  
[00:04:27] We'll do like a sprite 2D.  
[00:04:31] And this node is basically for just like making images.  
[00:04:35] And then by putting it under the player node,  
[00:04:38] then you can like add like an image.  
[00:04:42] Like for now, since this is just.  
[00:04:45] Like a quick like overview, we  
[00:04:48] can use the default image that GitHub provides,  
[00:04:52] which is over here in the file system.  
[00:04:55] is the texture, which  
[00:04:56] just like over here are the properties and then we can drag the image here  
[00:05:02] here into this box and then we can see that it appears over here in our game  
[00:05:08] view. And later on when you are like customizing your game  
[00:05:13] more you'll be able to upload like different images into the file system  
[00:05:18] and then drag it here to be the icon for your player. And at this time  
[00:05:25] Oh, by the way, is everyone doing good?  
[00:05:30] Is everyone up to a thumbs up if you're at this place?  
[00:05:39] Sorry.  
[00:05:40] Okay, the node is over here at the scene.  
[00:05:47] There's a little plus button here, and you can also press Command-A to create  
[00:05:54] the node.  
[00:05:55] nodes are just basically like the building blocks for the whole game um okay uh you can choose to  
[00:06:06] name it like whatever you think is appropriate i mean i just called the whole thing main and then  
[00:06:11] the specific player just like player um yeah uh also if you guys are just joining in now  
[00:06:20] um and you want to catch up like there's like you can also go to the link i just sent  
[00:06:26] like to catch up a little bit if you're late. Yeah anyways, I'm gonna continue.  
[00:06:33] So you can see here that the player right now has like an error. It says  
[00:06:40] the node has shape. It can't like collide. And basically we just have to add what it tells  
[00:06:48] us to do which is the collision shape 2D. So that is for later when you have your player  
[00:06:55] jumping around like the Godot engine needs to know like what the bounds of the player are so like it  
[00:07:04] won't like just fall through the floor right so under your player node you will want to do a  
[00:07:12] collision shape 2d node and there's also like polygon maybe if you have a more complex shaped  
[00:07:19] layer. But for now, just shape 2D will work. So we'll create it under here.  
[00:07:29] And then we'll have to define a shape for our collision boundary. So in the inspector area over  
[00:07:41] here we'll just do shape and then mines right now it's just a like a dough icon so it's  
[00:07:48] like just a rectangle. So I can just make a rectangle here and then you can see that  
[00:07:54] there's this box that appeared and you can use the like the red dots at the end to  
[00:08:02] make it cover your player right and then yeah and then now we have it over here at the center of the  
[00:08:12] view but um we want to move it like over here there's like this rectangle that i mentioned  
[00:08:22] earlier which is like the game view so if i were to run the game right now so you can press  
[00:08:29] play in the top right, or you can do command B. It will probably ask you which scene it wants you to  
[00:08:38] play and you can just do select current. And then you'll be able to see your little Godot  
[00:08:45] character or your little player appear on the screen. Is everyone good with this?  
[00:08:50] right now? Maybe a thumbs up or if you guys have any questions? Okay, I'm gonna move over. So,  
[00:09:05] now we have our player created and now we're going to create the environment.  
[00:09:14] Moving around in the editor view, you can just use two fingers to pan around and  
[00:09:19] and to zoom around.  
[00:09:23] You will use Command-B for playing, not D.  
[00:09:27] Or you can just press the Play button,  
[00:09:29] and then it will show your game here.  
[00:09:33] OK?  
[00:09:35] So now we're going to create the level, so what  
[00:09:39] your player is actually running around  
[00:09:45] I guess control B, but you can also press the actual button.  
[00:09:49] Yeah, OK, so now we're going to create the thing around  
[00:09:56] around it.  
[00:10:01] So under main, we're going to create a new node and then do this tile  
[00:10:08] map layer. So basically we're creating like a tile map and this is like think about like Minecraft  
[00:10:19] where you can like select different blocks and then you can like create whatever you want  
[00:10:24] instead of like having to manually build it. This tile map layer makes it so you can like  
[00:10:29] just like customize and build your own levels whatever you want for your player to like  
[00:10:34] player to like explore around really easily in so yeah we'll create tile  
[00:10:39] map layer node under the main here and then now we'll have to create the  
[00:10:48] the tileset. So we have our tile map layer here selected, right? And then on the right  
[00:10:56] in the inspector area, you want to click like this arrow right next to tileset and  
[00:11:04] then just say a new tileset. And then this is just creating like the thing like  
[00:11:11] or if I like show a tileset example, like it's like there's different blocks and things  
[00:11:23] and then you can like create your own map.  
[00:11:26] And like in a past game I made, like I made like a space platform for like a whole tileset  
[00:11:40] I just, I'm just going to do and draw your own book.  
[00:11:56] Is this okay guys? Am I still lagging? Okay. So we can just for now, we'll just find like  
[00:12:05] OK.  
[00:12:07] So we can just, for now, we'll  
[00:12:09] just find a random image of something.  
[00:12:15] I'm low key just going to take a screenshot of green for this example, to make the  
[00:12:20] tile set and then you can import it and drag the image into your file system here and  
[00:12:29] then let's just say we can name it grass and later on you'll probably want to create  
[00:12:36] folder for like your images or for your sounds and stuff but like right now we just  
[00:12:41] have it here okay um and like again to add something to your file system like  
[00:12:48] you can just drag it in everyone good with this step yes no no what's what's  
[00:13:02] the issue um well okay anyways so now we're going to add into drag it our  
[00:13:20] tile set over here right am I still lagging am I lagging you would want to  
[00:13:44] drag your in and then we'll clip so now just like we added a collision to our  
[00:13:59] player need for our time so how we'll do that is through like the house  
[00:14:19] okay it's still a one moment I'm gonna pause the recording really quick  
[00:14:28] because we cannot see your screen moving either.  
[00:14:31] Okay, so is everyone like, where do you guys, are you guys at this like tileset place?  
[00:14:49] Like, thumbs up, maybe, or chat, no. Where are you at then?  
[00:14:56] I can like resume or go back a little bit.  
[00:15:02] okay the importing the grass so here i'll just redo it so do we have the once you open like  
[00:15:14] uh sorry basically you'll want to. Select your, tile map layer and then have  
[00:15:20] the um over here on the right side there's like this little tile set place, place in the inspector area  
[00:15:30] and you want to say new and then tileset, right right? And then over here at the bottom  
[00:15:38] that you'll see this new tileset area created and then this is where we're  
[00:15:43] gonna drag our image into. So on the right in the file system I have my  
[00:15:50] tileset image which is right now just like some green and then all  
[00:15:55] All I'm doing is just dragging it here, and then into this area, and then just dropping  
[00:16:00] into this area and then just dropping it. Okay and then it'll ask you it'll ask you to  
[00:16:06] automatically create tiles and then for now we can just say yes. So is this good? Is everyone here?  
[00:16:15] Yes, send a thumbs up if you're here.  
[00:16:24] Okay, great. Now we're going to create the collision for our tile map. So we made  
[00:16:36] So we made it for our player earlier.  
[00:16:39] So if it were to fall on something, then the engine would basically know what the  
[00:16:44] bounds of the player are.  
[00:16:46] And we have to do something similar with our tileset.  
[00:16:50] So over here on the right in the inspector, you want to open this tileset area.  
[00:16:58] And then under physics layers, because this is falling under physics, we'll basically  
[00:17:03] create a new element.  
[00:17:06] And then you'll see this collision layer is created, and here.  
[00:17:11] So now that we've created this collision layer in our tile map node, we have to  
[00:17:17] apply it to the actual blocks we have here, right?  
[00:17:23] So in this, in the bottom section here in your tileset place, you'll want to head over  
[00:17:33] because we're basically painting on the collision area.  
[00:17:38] And then under paint properties,  
[00:17:40] we'll see this physics layer zero.  
[00:17:42] And this is the one that we just created over here  
[00:17:48] the inspector.  
[00:17:49] So we'll select this and then we can go ahead  
[00:17:51] and paint over all of our blocks.  
[00:17:55] And right now since we just have like the same image  
[00:17:58] for everything, it doesn't vary that much.  
[00:18:01] but let's say later on you wanted your blocks to have like lots of rounded corners or something  
[00:18:09] like if you're building like a winter themed game or something then maybe you'll like adjust  
[00:18:18] the mat the like collision mask to have like a corner um but right now it's just this  
[00:18:26] And if you guys are not finding a physics layer when you're going to your  
[00:18:31] going to your print properties, make sure to go to,  
[00:18:35] on the right, the Inspector.  
[00:18:38] And then open Tileset.  
[00:18:41] And then under Physics Layers, you'll  
[00:18:44] want to do the new element until  
[00:18:46] until you see this little collision layer thing.  
[00:18:50] And then that's the layer that we're using here.  
[00:18:58] And I'll also stare and mention,  
[00:19:00] you, if you guys like falling a little behind or something,  
[00:19:03] then you can also look at the page.  
[00:19:07] So yeah, now that we've created our tileset,  
[00:19:10] we can actually start designing our level.  
[00:19:13] So we've been in tileset, and in the bottom,  
[00:19:17] we'll want to navigate to the tile map area.  
[00:19:19] Yeah.  
[00:19:22] Sorry?  
[00:19:25] Oh, they made it.  
[00:19:29] OK, so now when we open the tile map,  
[00:19:32] we'll see a variety of different tools  
[00:19:35] that we can use to build and design our levels.  
[00:19:38] So we can mainly just use the pencil tool or the paint  
[00:19:43] tool, I guess.  
[00:19:44] And then you will want to select one of your blocks  
[00:19:49] they're all the same.  
[00:19:50] So I'll just select this first one here.  
[00:19:53] And then you can see over here  
[00:19:56] that the little block is appearing.  
[00:19:58] And then if I wanted to draw my level right now,  
[00:20:03] And I can also use other tools, I can make all of this filled area.  
[00:20:11] Yeah, and then this is where you can honestly just get as creative as you want,  
[00:20:17] like build the wildest like levels you want like maybe like flying or I don't  
[00:20:22] know like floating platforms and just things like that so yeah I'll just  
[00:20:28] design like this very simple like level I guess yeah and also if you  
[00:20:36] want to increase the size of your blocks because they may be small you  
[00:20:41] You can go to like transform under the inspector area and turn up the scale of the blocks  
[00:20:49] just like that option is also available for you guys.  
[00:20:53] So now if we're to run our game again which is the play button or you can do  
[00:20:59] command B then we can see we have our player here and the map  
[00:21:02] and the map around it.  
[00:21:04] But obviously, nothing is really happening.  
[00:21:07] The player is just floating.  
[00:21:09] So now we have to add the code for our player.  
[00:21:13] So it can actually fall and then we can press the keys  
[00:21:16] and it can jump around and stuff.  
[00:21:19] So Godot uses scripts, which is basically just a code file.  
[00:21:25] So under the player node, so select player in the scene.  
[00:21:31] And then over here at the top,  
[00:21:34] you'll see this little scroll with the green plus.  
[00:21:38] And this is creating a script to the player.  
[00:21:42] And then you will be able to code things,  
[00:21:44] and then the player will react to whatever you code.  
[00:21:48] So yeah, is everyone at this section here with the node,  
[00:21:56] and then you have your level map, a thumbs up  
[00:21:59] or something in the chat?  
[00:22:05] Yes.  
[00:22:06] Is everyone good?  
[00:22:13] Okay.  
[00:22:15] So yeah, now we're going to create our...  
[00:22:19] So for no physics layer,  
[00:22:23] you'll want to like...  
[00:22:26] Here, I can share like...  
[00:22:32] For no physics layer, you have to create it in the area before.  
[00:22:37] So you can see in this step, I can send it to you,  
[00:22:43] and then maybe you can go through it, and then it should be able to resolve.  
[00:22:48] Well, yeah, it's step five of here.  
[00:22:52] So yeah, now we're going to create our script.  
[00:22:59] So we can just name it player.gd,  
[00:23:02] And we'll also want to check the little template box  
[00:23:07] and then choose this Character, body 2D basic movement template.  
[00:23:12] And this is just going to give us a good base for our code.  
[00:23:15] And then you can go ahead and press Create.  
[00:23:19] And then we can see here that, first of all,  
[00:23:21] it's automatically switched us to the scripting area.  
[00:23:26] So if you want to go back and forth between coding  
[00:23:29] and seeing your actual game, then you can use this.  
[00:23:33] And then we can see the code here.  
[00:23:35] So it may look a little complicated,  
[00:23:38] but I'm going to go through and explain it.  
[00:23:41] And then later on, we can edit a few of the things  
[00:23:45] so the movement is better.  
[00:23:47] But just like right now, if you were to run this,  
[00:23:51] then you can actually see your player has fallen,  
[00:23:56] and you can do left and right in space to go around.  
[00:24:00] But as you can see, the movement is not the best.  
[00:24:04] Well, it depends on what you want your game to be.  
[00:24:08] If you want it to be very snappy,  
[00:24:11] the maybe this isn't the best,  
[00:24:13] but we can go and edit that later.  
[00:24:16] So now I'm gonna just go through  
[00:24:21] what the code is doing.  
[00:24:23] And it's important to understand that.  
[00:24:25] So later, when you edit it and everything,  
[00:24:28] you know what it's doing.  
[00:24:30] So here, the first line just connects it  
[00:24:34] the actual character body 2D node of the player.  
[00:24:38] And then here, we're setting some variables.  
[00:24:41] And these, we can see they're both constant.  
[00:24:44] So that means that throughout the whole game,  
[00:24:47] they won't change.  
[00:24:48] And maybe later, if you wanted to add,  
[00:24:50] like, maybe a coin counter or points  
[00:24:54] or something, those would be changing.  
[00:24:56] But throughout the game, these,  
[00:24:58] like the speed of your player  
[00:25:00] and jump velocity are always the same. So speed is just how fast your player is. You  
[00:25:06] can change it to whatever you want. Jump velocity is how high it jumps. If you had a  
[00:25:12] frog or something, maybe it would be very high. And you'll notice that this value is  
[00:25:18] actually negative. And this is because, like, the coordinate system is so that when you go higher,  
[00:25:30] it is like a more negative value. So like, let's say I want it to jump like twice as high,  
[00:25:37] then I would change this to like minus 800. Right? Yeah, so these are the variables and  
[00:25:42] and then connecting it to our player node in the scene.  
[00:25:47] And then now we have this huge function here.  
[00:25:51] And this is the bulk of it.  
[00:25:53] This is the physics, and it makes the player  
[00:25:56] fall and jump around.  
[00:25:59] So we can see here, this one is  
[00:26:02] if the player is not on the floor, then it's in the air.  
[00:26:06] So we want it to fall.  
[00:26:07] And how this does it is like it senses when it's not on the floor and then the velocity,  
[00:26:14] it will go down and, according to the gravity. And later we can edit this value. Like maybe if  
[00:26:22] your game is on a different planet, you want the gravity to be different. So yeah, this will  
[00:26:27] cause your player to fall. And then here is for jumping. So if this is basically the space  
[00:26:35] key if your space key is pressed and your player is on the floor then you  
[00:26:41] want to add to your y-velocity so like vertical your jump velocity and this is  
[00:26:47] the variable that we set at the beginning right so this will just make  
[00:26:52] it when you press the key then your player will jump up right and then  
[00:26:58] this code is for making it go right and left so we're first setting a  
[00:27:04] variable and then setting it to a direction. So if we were  
[00:27:09] clipping the left button, then it would be like minus one, and  
[00:27:14] right would be like one. And then once we set it, so we know  
[00:27:18] like which key we're pressing, then we'll check that like the  
[00:27:24] if the direction  
[00:27:25] is the like right or left, then we'll set the x velocity  
[00:27:30] which is like horizontal, right,  
[00:27:32] in that particular direction at that speed.  
[00:27:37] Does that make sense?  
[00:27:39] And then in the other case,  
[00:27:43] where you're not pressing left or right,  
[00:27:46] then you don't want your player to do anything,  
[00:27:48] right, you just want it to be still.  
[00:27:50] So this line will basically set,  
[00:27:53] make your velocity go towards zero.  
[00:27:56] So you're coming to a stop, right?  
[00:27:58] Yeah, and then this one, we'll just finish the whole thing off and then run the whole  
[00:28:02] off and then run the whole process.  
[00:28:06] Does that make sense? Does anyone have any questions  
[00:28:09] about how the code is working here?  
[00:28:11] Can you give me a thumbs up if you're good and you're caught up so far?  
[00:28:31] What's your question?  
[00:28:32] I do have one question I do have one question yes I am I have been having some trouble  
[00:28:51] understanding the move and slide function what exactly does the move and slide function  
[00:28:58] The movement, which this part or?  
[00:29:04] Move and slide, move and slide.  
[00:29:07] Oh, move and slide. This basically runs the whole process at the end.  
[00:29:12] And it will like implement all of this before.  
[00:29:16] So it's basically just like executing it at the end.  
[00:29:20] Does that make sense?  
[00:29:24] Yeah.  
[00:29:28] Thanks.  
[00:29:31] OK, so now we're going to make a few edits  
[00:29:35] to the movement of our game.  
[00:29:36] , and then you guys can go ahead and make  
[00:29:40] a lot more customizations if you want. So first I did edit like the speed and jump velocity of  
[00:29:46] my game so like if I were to run it now and I'm clicking the buttons you can see that it's like  
[00:29:53] already the movement is jumping a lot but it does seem like a bit a little bit airy. So  
[00:29:59] one thing that we couldn't change is the amount of gravity in our game. So this value here  
[00:30:07] And to change that, you'll want  
[00:30:10] to go to your very top bar and go to Project, Project  
[00:30:17] Settings.  
[00:30:18] And then here, there should be,  
[00:30:23] you can start searching gravity and under Physics 2D,  
[00:30:27] then we can see we can actually edit the amount of gravity  
[00:30:32] we want to.  
[00:30:33] So I'll just set this to like 2,500.  
[00:30:42] Yeah, so you'll submit jump start  
[00:30:44] before you organized.  
[00:30:48] So yeah, you can change the gravity here.  
[00:30:51] And then if I were to run it again,  
[00:30:53] you can see that I'm jumping,  
[00:30:55] and it's falling way quicker.  
[00:30:57] And now just the overall movement of the game  
[00:31:00] feels a lot better and snappier.  
[00:31:02] And you can change all these values to however  
[00:31:07] you can tweak around and see what you like.  
[00:31:10] And also, another thing that we can add to our game  
[00:31:14] is a moving, like the camera will follow the player.  
[00:31:20] Because right now, if we play a game and we get here,  
[00:31:23] then it's kind of the end.  
[00:31:25] What do we do now?  
[00:31:26] So what we can do is add a camera to our player.  
[00:31:30] So under our player node, we'll want to do the plus button  
[00:31:37] and search for this camera 2D node.  
[00:31:41] And we can go ahead and create it.  
[00:31:44] And now we'll want to go back to the 2D view.  
[00:31:49] And then we can see that here, like the little pink rectangle  
[00:31:54] is our new camera view.  
[00:31:56] And theenegger is like the little red plus thing.  
[00:32:02] And then you can move the camera if you want.  
[00:32:05] But I'll just have the player always at the center of it.  
[00:32:11] So now if we were to run our game,  
[00:32:13] since we have the camera attached to our player,  
[00:32:18] then you can see as I jump,  
[00:32:20] then the camera follows their player  
[00:32:22] and then you can like,  
[00:32:24] yeah, you can build the level however long you want.  
[00:32:27] And then you can just keep going.  
[00:32:29] Also like maybe like another fun thing you can add  
[00:32:34] if you want is like a little bit of camera lag.  
[00:32:37] So like as I'm moving,  
[00:32:38] the camera is like following me instantly,  
[00:32:41] but like one cool effect you can add  
[00:32:43] is like a little bit of lag.  
[00:32:45] So if you, in the, like when you select camera 2D  
[00:32:48] and then go to inspector,  
[00:32:51] you can turn on the position smoothening  
[00:32:54] and then you can like have some random value.  
[00:32:58] And then as you can see,  
[00:33:00] like there's like a little bit of lag,  
[00:33:02] which I think is just like a pretty cool effect  
[00:33:04] that you guys can add to your game if you want to.  
[00:33:08] Yeah, and at this point, this is the end of like  
[00:33:12] the base, creating the base of your platformer.  
[00:33:15] And now you guys can go crazy  
[00:33:19] and add whatever you want to it.  
[00:33:21] Like obviously right now we have like  
[00:33:23] the basic black thing, the Godot thing,  
[00:33:26] the Godot like icon.  
[00:33:28] So you guys can like pick a  
[00:33:31] theme for what you want your game to be  
[00:33:33] and maybe draw your own assets  
[00:33:36] or find your own assets online.  
[00:33:38] And there's also Godot,  
[00:33:40] You can make so many different cool add-ons and stuff.  
[00:33:45] You could add collectibles.  
[00:33:48] Say you want to make a really cool something,  
[00:33:52] you can add different things.  
[00:33:56] And for that, there's tons of tutorials online.  
[00:34:02] Just search it up, and you'll be  
[00:34:04] able to find ways to build whatever you want in Godot.  
[00:34:09] I also have some extra ideas for things you might want to add to your project before submitting  
[00:34:16] to really make it your own.  
[00:34:19] So also enemies, scoring, sound effects are really fun as well.  
[00:34:24] And this basically concludes the Jumpstart workshop.  
[00:34:28] And then once you have this, there's a file submission on the website and then  
[00:34:33] on the website, and then we'll submit. Yay!  
[00:34:40] Yay! Thank you so much, Estella, for giving this awesome workshop,  
[00:34:43] and thank you everybody for coming to this JumpStart workshop.  
[00:34:47] Do you have any other words, Estella? Can I ask one?  
[00:34:51] Uh, I don't think so. Sorry?  
[00:34:57] Oh, can I ask something? Yeah, go ahead with your question.  
[00:35:04] All right in the website you do tutorial  
[00:35:07] There was one part that said that in the original Jumpstart event website  
[00:35:12] there was more in-depth tutorials for daughters.  
[00:35:17] But there are not.  
[00:35:19] Where can we find more focused resources like  
[00:35:24] that they actually like this, the category like the  
[00:35:28] the way you all keep that in the Jumpstart house  
[00:35:31] and all that. How do we find resources like this to not just rely on L11s  
[00:35:38] and the sort of other communities that we are making?  
[00:35:42] Especially if we are already advancing the game already.  
[00:35:48] Do you recommend any resources?  
[00:35:53] Oh, like resources for adding more to your game?  
[00:35:57] Yes.  
[00:35:59] More on the story of when you add more to your game.  
[00:36:03] I was creating my first video game last year I think for like a hackathon like hack club  
[00:36:16] event in China actually I like I low-key just relied on like tutorials I found on  
[00:36:22] YouTube they're very helpful and yeah you can just go ahead and search it like on  
[00:36:28] Google and there's tons of resources. There's like a channel. I don't remember what specific  
[00:36:30] There's like a channel, I don't remember what specific videos I used  
[00:36:42] Maybe I can link some like I can add like some resources and I'll share some like in  
[00:36:49] in the Jumpstart-Haven channel after this if you guys want to take a look.  
[00:36:54] Yeah, does that answer your question?  
[00:36:59] Yeah, quite. So there was a little bit of lag again, but what I understood is that I  
[00:37:06] I'm sorry that I didn't get to address that. That was what I managed to understand.  
[00:37:15] Okay.  
[00:37:20] Well, I think that thank you everyone.  
[00:37:23] Yes.  
[00:37:26] If you need more ideas or help on what else you can add to your game, Estella said there's a lot of really awesome resources on YouTube that you can watch.  
[00:37:37] Yeah, okay, thank you.  
[00:37:39] And don't forget, everyone join the Jumpstart Haven channel. You guys can also share what you're building on your game there.  
[00:37:51] Okay, bye everybody!  
[00:37:54] Okay, thank you everyone. Bye.  
[00:38:04] Sorry, like I will still stay on call if you guys have any other questions about like Haven in  
[00:38:09] general or Jumpstart Haven but if not then you're free to leave and have an awesome day.  
[00:38:20] Bye-bye.  
[00:38:28] All right, all of you here, do you have any more questions?  
[00:38:32] If you have any questions, you can also send in the chat.  
[00:38:35] I will just be hanging out for now.  
[00:38:39] Sorry Also, I think if you have a question, please put it into the chat my computer's a bit slow  
[00:39:08] so I couldn't hear you clearly, I'm sorry.  
[00:39:16] Yeah, just just a quick question is not related. But can I ask?  
[00:39:25] I could question the chat. I'm sorry. Like I can hear you at  
[00:39:28] first and then it kind of cuts off. So please type in the  
[00:39:37] a team owner owner saying that we only need only need two participants. But in my point  
[00:39:43] of view, there should be three participants. What do you say?  
[00:39:48] Oh, I'm sorry. Could you could you ask a question and type in the chat?  
[00:39:52] Okay, okay.  
[00:39:53] Not good.  
[00:39:54] I hear it. Thank you so much.  
[00:40:12] Bye everybody.  
[00:40:14] Unless you have questions, you're free to leave as the check in call and jumpstart  
[00:40:18] workshop has ended.  
[00:40:19] who participants do you mean like at your haven event I'm a little bit  
[00:40:59] confused or do you mean like no no like is it for a jumpstart specifically  
[00:41:18] .  
[00:41:48] Okay, I'm a little bit confused because I'm not sure if this is about Haven in particular.  
[00:41:57] Please let me know if I'm like understanding your question correctly.  
[00:42:01] asking like should the team size be two people or should the team size at a  
[00:42:05] hater be three people? Is that your question? Okay, I'm hoping to understand  
[00:42:24] this correctly, but if you're asking how many people should be in a team, right  
[00:42:28] now we're trying a policy where we're  
[00:42:34] This could be subject to change, so we will confirm it in a future check-in  
[00:42:38] call, especially as we get closer to the event, but yes. And also I do want to  
[00:42:46] make clear that Haven is specifically a game jam hackathon, so if somebody wants to like make  
[00:42:52] like a hardware maybe like a macro pad to play their game or like their ownitored game console,  
[00:42:57] that's totally fine. But all participants should be shipping a game game because it needs to be  
[00:43:01] because it needs to be on itch.io.  
[00:43:04] And it's not really easy to put a heart of pride for the niche that I am so as long as it's a game. It's all good  
[00:43:13] Does that answer your question? Maybe hopefully  
[00:43:18] Okay, awesome. Thank you so much  
[00:43:21] Okay, are you all just like hanging around in the Zoom meeting? I will officially end  
[00:43:35] I will officially end the meeting for everybody. Bye everybody, see you all next week.  
