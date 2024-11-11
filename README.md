# Catching-Z-s


# Description 
My project is a platform video game programmed in Microsoft Makecode Arcade. It is made for Gen Z end-users to address poor sleeping schedules. It offers a bed-time video game to help the end-user relax and fall asleep. It's also meant to be fun!

# Technologies used
Microsoft MakeCode Arcade Programming Software
Python Programming Language 
Computer 
Mobile Phone
Note: external code libraries are not needed as MakeCode Arcade contains internal libraries e.g. Inputs, Loops and some Advanced Extensions.

# Features 
The aim of the game is to advance through each level by Catching Z's (the rewards) and avoiding enemies (sleep inhibitors) to reach the bed at the end of each level, signifying a "good night sleep".
In order to achieve this, the main features that I make use of are functions, conditional statements, boolean logics and others. 

# Set Up
1. Install Git and clone the MakeCode Arcade repo
2. Install Python libraries (no code libraries needed as they are embedded in MakeCode Arcade)
2. Install Dependancies (not needed for MakeCode Arcade)
3. Start a local server to launch Makecode Arcade 
4. Optional: you can try to run the game on physical hardware as well.

# Usage 
An example of the usage of my code can be seen in the below programming:

def on_a_pressed():
    if GenZ.vy == 0:
        GenZ.vy = -225
controller.A.on_event(ControllerButtonEvent.PRESSED, on_a_pressed)

This is a function that makes the player move in an upward direction when the a-button is pressed. 

A second example of the usage of my code can be seen below:

def on_on_update():
    GenZ.set_image(img("""
        . . . . . 5 5 5 . . . . . . . . 
                . . . . 5 d d d . . . . . . . . 
                . . . 5 5 d d d . . . . . . . . 
                . . 5 5 . . d . . d . . . . . . 
                . . . . 9 9 9 9 9 . . . . . . . 
                . . . d . 9 9 9 . . . . . . . . 
                . . . . . 9 9 9 . . . . . . . . 
                . . . . . 9 9 9 . . . . . . . . 
                . . . . . 3 3 3 . . . . . . . . 
                . . . . . 3 . 3 . . . . . . . . 
                . . . . 3 3 . 3 . . . . . . . . 
                . . . 3 . . 3 . . . . . . . . . 
                . . d . . d . . . . . . . . . . 
                . . . . . . . . . . . . . . . . 
                . . . . . . . . . . . . . . . . 
                . . . . . . . . . . . . . . . .
    """))
    # Conditional statement for if GenZ is moving forward
    if GenZ.vy < 0:
        GenZ.set_image(img("""
            . . . . 5 . . . . . . 5 . . . . 
                        . . . . 5 5 . 5 . 5 5 . . . . . 
                        . . . . . 5 5 5 5 5 . . . . . . 
                        . . . . . . d d d . . . . . . . 
                        . . . . d . d d d . d . . . . . 
                        . . . . 9 . . d . . 9 . . . . . 
                        . . . . . 9 9 9 9 9 . . . . . . 
                        . . . . . . 9 9 9 . . . . . . . 
                        . . . . . . 9 9 9 . . . . . . . 
                        . . . . . . 9 9 9 . . . . . . . 
                        . . . . . . 3 3 3 . . . . . . . 
                        . . . . . . 3 3 3 . . . . . . . 
                        . . . . . . 3 . 3 . . . . . . . 
                        . . . . . 3 . . . 3 . . . . . . 
                        . . . . d . . . . . d . . . . . 
                        . . . . . . . . . . . . . . . .
        """))
    elif GenZ.vy > 0:
        # Conditional statement for if GenZ moving backward
        GenZ.set_image(img("""
            . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . d . . 5 . 5 . . 
                        . . . d . . . . 9 . . 5 5 5 . . 
                        . . . 3 . . . . . 9 . 5 5 5 . . 
                        . . . 3 3 3 9 9 9 9 . d d 5 . . 
                        . . . d . 3 9 9 9 9 d d d 5 . . 
                        . . . 3 3 3 9 9 d 9 . d d 5 . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . . 
                        . . . . . . . . . . . . . . . .
        """))
    else:
        pass
    if GenZ.vx < 0:
        # Then the original sprite image flips
        GenZ.image.flip_x()
game.on_update(on_on_update)

The above lines of code animate my sprite depending on the direction of their movements (left, right, up and down) to enhance the user experience.


# Project Status
Stil in progress.

# Room for Improvement
I would try to implement more stretch goals in future.

# Acknowledgements
Thank you to the teaching team and my peers for supporting my development in this project.
