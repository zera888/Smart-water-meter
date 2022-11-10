# Smart-water-meter

## Overview/Useage
smart water meter detection system (can be applied to gas and electricity meter systems). Using the text recognition function of Yolov7, regularly use the smart photography system installed next to the water meter to take pictures, and use the upload function of Bluetooth to upload the taken photos to the platform of the system. Then use the text recognition system of yolov7 in openvino to identify the water meter number and the monthly usage degree in the photo, convert it into text, output it as an xml file, write it into the database of the system, and convert it into the bill to be paid for the current month. This saves countless scribes manpower and reduces the chance of making mistakes (because of misspellings or transcription errors). Even mistakes in the proofreading process save countless manpower and time.

## Methodology / Approach

    First of all, in the hardware part, ESP32S microcontroller 30pin is used. DEVKIT V1 development board WiFi Bluetooth ioT IoT dual-core single-chip module module, with Bluetooth and IoT functions, and can be used in series with ESP32-CAM development board, connect the camera to wake up the camera at a fixed time through the system platform The lens captures the usage degree of the water meter, then uploads it to the platform through the bluetooth system, and then uses the program provided by the Openvion notebooks program set for image recognition, and then saves the result into the database in the system, and the output is sent to the bill. user.

    The control of the microprocessor is to use the Arduino program, write it into the microprocessor (ESP32S DEVKIT V1), drive the bluetooth to upload the video taken by the camera, and periodically send out a signal through the system to wake up the camera in the sleeping state to take pictures action.

    The part of the power supply is to use the solar charging board to provide power to the system, saving the problem of replacing the battery.

    The image recognition part is to use OpenVino's Edge AI technology to upload the video to the system platform, use the technical framework of YOLOv7 for image recognition, read the device number and degree of use in the photo, and save the data after confirmation. Store it in the library, wait until a specific time, convert it into a bill of payment according to the degree of use, and send it to the consumer.

    The software used is Python 3.X or above, the framework uses Pytorch, and the algorithm uses Yolov7 technology.

    The system platform can be used as a processing device through Openvino's cloud device, or Intel's 6th to 12th generation Intel® Core™ processors.

## Picture
![圖片](https://user-images.githubusercontent.com/77621980/200985177-d5384519-e9dd-46b3-83bd-b05a40ee9749.png)

## Block Diagram
![圖片](https://user-images.githubusercontent.com/77621980/200985330-426f85c4-55c2-4b23-9e6c-452f9ce6c7e2.png)

## Technologies Used

    For the local side, Intel's 6th to 12th generation Intel® Core™ processors are required.

    If it is a cloud device, you can use the Intel® Developer Cloud environment provided by Intel to work.

    The Open Model Zoo provided by Intel's Developer Cloud has pre-trained models, which can be used directly by users without the need for training.

    You can download and install openvino Toolkit from Intel Develover Cloud.

    The dataset of coco datasets.

    Yolov7's deep learning technology.

    Image framework for Pytorch.

    DEVKIT V1 development board for Arduino's ESP32S.

    Arduino's ESP32CAM camera development board and camera connector.

    Solar charging modules, solar charging panels and rechargeable batteries.

    Cloud databases such as SQL, MYSQL, etc.
