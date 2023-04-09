# Smart-trash-bins
https://www.youtube.com/channel/UC5s7DoMgMNC2AQGXQb5fd2A
Here is our Youtube channel
![image](https://github.com/qlkaaron/Smart-Trash-Bin/blob/main/img/trashbin.png)

This is a smart bin based on a Raspberry Pi. The trash will be recognised by the camera and then automatically sorted and thrown into the appropriate bin. Waste will be divided into four categories. Recyclable trash, harmful trash, kitchen trash and other trash
Yolo will be used for trash identification
The equipment we used:
Raspberry Pi 4B

Hd camera
Laptop 

# Hardware Building

The working process of the device is to use the camera to take pictures of the garbage in the area and classify it. After the photo is taken, the Raspberry Pi recongnizes the garbage category of the object through yolov5, and outputs a signal to the control servo to open the trash bin.

The whole project is divided into a shooting recognition platform and four trash bins.
![image](https://github.com/qlkaaron/Smart-Trash-Bin/blob/main/img/draft of smart trash bin.png)
Camera: This device connects to the Raspberry Pi using a USB tiny camera. The camera is fixed above the recognition area to ensure that the captured image can cover the area where the trash is placed.

Servo and driver
In this project, PCA9685 driver board is used to drive 4 MG996R servos.

How to connect:
For PCA9685:
PCA9685 can drive 16 servos at the same time. In addition to connecting to the Raspberry Pi, it needs to be powered externally with 5V to drive the servos.

Connect the VCC pin of the PCA9685 to the 3.3V pin of the Raspberry Pi.
Connect the GND pin of the PCA9685 to the GND pin of the Raspberry Pi.
Connect the SDA pin of the PCA9685 to the SDA pin of the Raspberry Pi.
Connect the SCL pin of PCA9685 to the SCL pin of Raspberry Pi.


For MG996R:
The four MG996R servos are respectively connected to the VCC pin, GND pin, and signal pin of the driver board.
