
# Voice-Controlled Robot With the ESP32

Build your own voice-controlled robot - all you will need is an ESP32 and Microphone board (and some motors etc...).





I'm using a microphone breakout board that I've built myself based around the ICS-43434 - but any microphone board will work. The code has been written so that you can either use an I2S microphone or an analogue microphone using the built-in ADC.

I would recommend using an I2S microphone if you have one as they have a lot better noise characteristics.



Other I2S microphones are equally suitable. Boards based around the INMP441 work very well.

The voice recognition is carried out using a model trained with TensorFlow and runs on the ESP32 using TensorFlow Lite. A pre-trained model is included in the Firmware folder so you can get up and running straight away.

There are two folders in this repo `model` and `firmware` check the `README.md` file in each one for complete details.

## Model

Jupyter notebooks for creating a TensorFlow Lite model for "wake word" recognition.

A pre-trained model has already been generated and added to the firmware folder.

If you want to train your own, I added a couple of extra folders to the training data they are available here:

## Firmware

ESP32 firmware built using Platform.io. This runs the neural network trying to detect the words `Up`, `Down`, `Forward` and `Backward`.

The code assumes there are two continuous servos attached to the board such as the FS90R servo - these are readily available from various suppliers and you can normally buy them with wheels as well.

# 3dPrinting

This contains the 3d models that I used to build my 2 wheeled robot. It's designed around the FS90R continuous servos and a cylindrical power bank.
