# 🕍Haunted_House
######
## -Members of the team:
#### Xuezhi and Xin, Xuezhi = after, Xin = before, the game isn't finished, we will continue finishing the story line.
#
#
## -What I learn:
#### I learn how to code a visual novel with options and differents endings and also having adding audios for more realistic experience and background music for differents situacions 
``` Renpy
        //here you can see some code I do to make audios works and differents options I give to the player

        label upstairs:
           scene mansionstair
           "......"
           stop sound
           show xuezhiquestion at left
           xuezhi "Haven't we reach yet?"
           show xinquestion at right
           xin "I have a felling of walking on this stair for years already"
           xuezhi "but the second floor seems so close, how are we not up there yet?"
           xin "I don't understand neither"
           xuezhi "let's just keep going I guess"
           hide xuezhiquestion
           hide xinquestion
           play sound walkonwood
         "......"
           stop sound
           show xuezhiscare at left
           xuezhi "How? How are we still not up yet?!"
           show xinscare at right
           xin "I think we are stuck on this stair, it is like a infinite loop of stair, just like the horror movies!"
           xuezhi "Oh man, I'm starting to really getting chills on me"
           xin "Now what we do?"
          
          menu:
          "Try to find the reason on your phone":
           xuezhi "Let's try to find out the reason on the phone"
           show xuezhiquestion at left
           xuezhi "It says that the loop is caused because a invisible ghost is blocking the way"
           xuezhi "If we open the camara, we may saw he through the phone and escape from he"
           xuezhi "All what we need to do is not touch the ghost or we are gonna be sent back again in the loop"
           show xuezhiangry at left
           xuezhi "Let's do this!"
           xin "Okay, so lets see where is the ghost"
           hide xuezhiangry
           hide xinscare
           show phone
          "......"
           jump gosecondfloor
          
          "Run to downstair":
           "Running back to downstair didn't work for you and you guys died because of hungry and thirsty after 1 week stuck on the stairs"
           "Bad Ending"
           return
```

#### ( Find reference in https://github.com/MxuezhiM/Haunted_House/blob/4a2b9e1e4fdb73b719e7bcf7cc1171631a33b064/script/after.rpy )
#
#
## -What can I teach:
#### I could teach people on how to do a intro animation for your game when opening the game
```Renpy
    //first you have to define your logo as a image, which in my case I did the Bandai Namco intro of year 2000 and also define the black and white image to make the blink 

    transformation    
    image black = "#000"
    image white = "#ffffff"
    image logo = "logo.png"

    //After I did a label for the transformations
    
    label splashscreen:
    scene black
    $ renpy.pause(1, hard=True)
    show white at transform_white
    $ renpy.pause(2, hard=True)

    show logo at transform_logo
    $ renpy.pause(6, hard=True)

    hide logo
    $ renpy.pause(2, hard=True)

    hide white
    $ renpy.pause(3, hard=True)

    return
    
    // And the last thing you have to do is just define the differents transformations 

    transform transform_blink:
    linear 1.0 alpha 0.2
    linear 1.0 alpha 1.0
    repeat
    
    transform transform_white:
    on show:
        alpha 0
        linear 2.0 alpha 1
    on hide:
        linear 2.0 alpha 0
   
    transform transform_blink:
    linear 1.0 alpha 0.2
    linear 1.0 alpha 1.0
    repeat
```Renpy

#### you could go to https://github.com/MxuezhiM/Haunted_House/blob/1e2f0a32a0b7c6c435458e3841e4e14544faeb87/script/intro.rpy to check the full script
#
#
## -Bibliography:
#### https://emily2.itch.io/sutemo (Assets)
#### https://stock.adobe.com/es/search?k=haunted%20mansion%20interior (Background of Mansion)
#### https://www.fesliyanstudios.com/sound-effects-search.php?q=level+open+sound (audios)
#### https://pixabay.com/music/search/horror/?genre=beats (Background Musics)
#### https://cloudnovel.net/browse/free/background/popular (Background of School)
#### https://www.renpy.org/doc/html/index.html (where I learn about Renpy)
