# Polargraph-machine
This project stimulates a software image to paint it on any surface (with any width and height) using electric stepper motors that generates discrete angular movement to move the wires that are attached with a pen and draws the image.
The purpose of the polar drawing machine is that it could be used in education purposes and art schools in assisting the theachers by demonstrating any image, and the most important purpose of the project is that we can draw any image that we want on any surface with various dimensions.

Detailed Report: [here](https://github.com/NaNo211/Polargraph-machine/blob/db20860e17724f7c4718f5ae097af7a70a877486/202104091545%20Plotter%20Drawing%20Robot-converted.pdf)

Presentation: [here](https://github.com/NaNo211/Polargraph-machine/blob/db20860e17724f7c4718f5ae097af7a70a877486/polargraph-final-presentation.pptx)

# First Phase Goal:
Draw a 1 color image on a specific white board.


# Steps:
1. Selecting the plotter 3D design: https://www.thingiverse.com/thing:2371117/files and we used plastic for that

2. Components:
    - Arduino MEGA.
    - L293D Motor Drive Shield
    - L293D Motor Drive IC
    - 2 x 17 Stepper Motor
    - Servo Motor MG90S
    - GT2 Pulley 16 Teeth set
    - 5M GT2 Rubber belt
    - Power Supply (12v)
    - Adapter 5V/3.5A
    
3. The wiring schematic: ![this is an image](https://github.com/NaNo211/Polargraph-machine/blob/main/Polargraph-scematic.png)
   Connecting stepper motors and servo to the motor drive and attach it to the Arduino, then anttach the motors with rubber built. 
   
5. After selecting an image, we converted it to grey scale, then to SVG format.
   
4. Software used is called "processing". The link : https://processing.org 
    Thanks for Euphy we used his code for the motors and servo controllers. The package link : https://github.com/euphy/polargraphcontroller/releases/tag/2017-11-01-20-30
    We insert the the formatted image to the software, it then generates the vector path points and sends it to the microctroller.


# First Phase Output:
![this is an image](https://github.com/NaNo211/Polargraph-machine/blob/main/images/first_phase/2.jpeg)


# Second Phase Goal:
 Draw a full color image on a specific white board.


# Concept:
 According to artistic drawing and printing a colored image is produced through merging a specific set of colors with different distributions according to the color intensities in a point, so referencing to the CMYK model, we merged 4 colored pens (Cyan, Magenta, Yellow, Magenta) to draw a full color image.


# Steps:
1. After selecting an image, we insert the image Death2Sharpie alogrithm to split it to CMYK channels.
2. We attach the corresponding color pen of channel.
3. We generate the SVG format of each layer.
4. We insert the SVG for each layer to the processing software that generates the corresponging path.
5. Printing each layer independently and manually changing pen and channel 4 times.

# Second Phase Output:
![this is an image](https://github.com/NaNo211/Polargraph-machine/blob/main/images/second_phase/4.jpeg)


# Updates:
We are still updating the project as:
we are willing to implement a scrpit that will automatically split channels of an image, convert it to SVG, and insert it to the processing software with the integration of a hardware design that will switch automatically between different color pens.
The, we will integrate this project with the neural style transfer project.
For any information contact nadaSamir@student.aast.edu or nourmorse21@gmail.com.


