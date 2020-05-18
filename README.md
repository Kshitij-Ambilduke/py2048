---
# **2048 The Game**

## Description:
2048 is a slide puzzle game in which by sliding numbers in the game grid a desired number (defautly 2048) is to be achieved.
Whlie the game is being played, on every valid move, a random "2" is generated in the grid wherever place in empty. The game can by played with WASD keys on the keyboard, where, W key does a up-shift, A key does a left-shift, S key does a down-shift and the D key does a right-shift. The game is made more dynamic by letting the user choose the size of the grid that they want to play in and also deciding the winning number.
It is to be noted that the winning number should always be a power of 2.

## Game Rules:
* The game starts with a grid of the size specified by the user (or default according to the input of the user). This grid has a "2" spawned randomly in the grid.
* The player has the keys WASD to move wherever she/he pleases to move.
* On every valid move, a "2" is again randomly spawn on any one of the empty part of the grid. An invalid move is a move in which no matches are made and no number is moved. If any such invalid move is played, a message saying that the move is invalid is displayed on the screen.
* When there is no possible way to move any number or match any numbers, the game has been lost and a message will be displayed on the screen.

## Platform/Software used:
* The game has been made on a Windows 8 system.
* Sublime text editor was used to edit the code.
* The code was tested on the command prompt.
* Some modules were used in the code :
  * [random2](https://pypi.org/project/random2/)
  * [msvcrt](https://docs.python.org/3/library/msvcrt.html)
  * [os](https://docs.python.org/3/library/os.html)

## About the code:
* In the beginning, it asks the user to enter the size of the grid and the winning number. If anything else than an integer is entered, the default value for the size and the winning number is taken (size=5, winning number= 2048).
> About the shifting mechanism:
  * **Right shift :**
    When the player hits the "D" button on their keyboards, it triggers the "final_right(grid)" function which performs a right shift on the current grid which is passed through the same function and returns the new grid which has been operated by a right shift.
    Following snap shows the functions used for right shift:
    
    ![Right Shift](https://github.com/Kshitij-Ambilduke/py2048/blob/master/right.PNG)
    
  * **Left shift :**
    When the player hits the "A" button on their keyboards, it triggers the "final_left(grid)" function which performs a left shift. This function takes the current grid as input and returns a grid which has been operated over by a left shift operation.
    Following snap shows the functions used for left shift:
    
    ![Left Shift](https://github.com/Kshitij-Ambilduke/py2048/blob/master/left.PNG)
    
  * **Up shift :**
    When the player hits the "W" button on their keyboards, it triggers the "final_up(grid)" function which performs an up shift. This function takes the grid rotates it in the anti-clockwise direction by 90 degrees, performs a left shit and then undo the rotation thereby giving the overall effect of an up shift.
  * **Down Shift :**
       When the player hits the "S" button on their keyboards, it triggers the "final_down(grid)" function which performs an down shift. This function takes the grid rotates it in the anti-clockwise direction by 90 degrees, performs a right shit and then undo the rotation thereby giving the overall effect of an down shift.
       Following snap shows the functions used for up and down shift:
       
       ![Up and Down Shift](https://github.com/Kshitij-Ambilduke/py2048/blob/master/uad.PNG)
       
       
**Gameplay of the game is shown below with the help of a short video.**

In the video, the first case is taken with size = 3 and winning number = 4 to show the winning case. To depict the losing case, size = 3 and winning number = 256 is taken also, to depict the invalid size , a third case is taken where "d" is input in the size of grid thereby resulting into creation of a 5x5 grid with a winning number as 2048 
___

 ![Alt Text](https://github.com/Kshitij-Ambilduke/py2048/blob/master/gameplay.gif)
 
 ## Game specifics:
 At the beginning, the game asks to enter the size of the grid and the winning number. If a proper number for the size and the winning number is not entered, the game will take the default value for the size and winning number (size=5, winning number=2048). If correct acceptable value is entered, the game will work according to the values given to it.
 It can be seen from the gif above that when a random letter is entered in the place of size, the default value for size and winning number is taken.
 In other words, if you want to play the game on default settings, just enter any invalid input at the beginning of the program and then enjoy the game!
