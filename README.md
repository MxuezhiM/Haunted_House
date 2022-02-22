# Haunted_House
######
## -Members of the team:
#### Xuezhi and Xin, Xuezhi = after, Xin = before, the game isn't finished, we will continue finishing the story line.
#
#
## -What I learn:
#### I learn how to code a visual novel with options and differents endings and also having adding audios for more realistic experience and background music for differents situacions ( Find reference in https://github.com/MxuezhiM/Haunted_House/blob/4a2b9e1e4fdb73b719e7bcf7cc1171631a33b064/script/after.rpy )
#
#
## -What can I teach:
#### I could teach people on how to do a intro animation for your game when opening the game
//first you have to define your logo as a image, which in my case I did the Bandai Namco intro of year 2000 and also define the black and white image to make the blink transformation
    
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
   
   transform transform_logo:
    on show:
        alpha 0 xalign 0.5 yalign 0.5
        linear 2.0 alpha 1
    on hide:
        linear 2.0 alpha 0

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
