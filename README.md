# it21_lora_gateway
Data communication setup between Arduino LoRa Module and Raspberry pi LoRa module 

1. Devices:
    A. Sender:
      1. Arduino
      2. SX1272 LoRa module : uses the SPI pins for communication. 
      3. The Multiprotocol Radio Shield: allows to connect two communication modules at the same time to Arduino
  
  Task-1: SX1272 LoRa module over Arduino hardware setup

    B. Receiver:
      1. Raspberry pi
      2. Connection Bridge
      3. SX1272 LoRa module 


  Task-2: SX1272 LoRa module over Raspberry pi hardware setup
  
2. Libraries
  A. The library with Arduino
      SX1272 with Arduino: http://www.cooking-hacks.com/media/cooking/images/documentation/tutorial_SX1272/SX1272_library_arduino_v1.4.zip
      Note: Upload the libraries in Arduino IDE and make sure the new library appears in the Sketch->Import Library menu item of the software.
  
  B. The library with Raspberry Pi
      The SX1272 library for Raspberry Pi requires the ArduPi library and both libraries should be in the same path.
      http://www.cooking-hacks.com/media/cooking/images/documentation/tutorial_SX1272/arduPi-api_LoRa_v1_4.zip

3. Command for Installing Libraries in Raspberry pi: 
   #wget http://www.cooking-hacks.com/media/cooking/images/documentation/tutorial_SX1272/arduPi-api_LoRa_v1_4.zip && unzip -u arduPi-api_LoRa_v1_4.zip && cd cooking/examples/LoRa && chmod +x cook.sh && cd ../../..  

4. Install ArduPi and SX1272 libraries:
    #wget http://www.cooking-hacks.com/media/cooking/images/documentation/raspberry_arduino_shield/raspberrypi2.zip && unzip raspberrypi2.zip && cd cooking/arduPi && chmod +x install_arduPi && ./install_arduPi && rm install_arduPi && cd ../..
5. SX1272 Library: 
    #wget http://www.cooking-hacks.com/media/cooking/images/documentation/tutorial_SX1272/arduPi-api_LoRa_v1_4.zip && unzip -u arduPi-api_LoRa_v1_4.zip && cd cooking/examples/LoRa && chmod +x cook.sh && cd ../../.. 
6.Go to examples: 
    #cd cooking/examples/LoRa/ 

7. Compile the example:
    ./cook.sh my_example.cpp 
8. Run the sketch:
  ./my_example.cpp_exe

  Note:
  The script "cook.sh" compiles everything in their folders and the link in the examples foldes with the "_exe" executable.

    Help: ./cook.sh
    Clean: ./cook.sh -clean (It deletes all the "*.o" files. This is only necessary if you make changes in the libraries)
  
		
