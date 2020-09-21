For now this is just notes, will be writen up better later. 


# Setting up the base

## Radio
  Connect to ODIN-w2 serial port (usually the second one enumerated, at 460800). May want to clear memory (by holding SW0 for 3 seconds and giving it 1 sec before resetting) first 
  /wifi_setssid/run myssid
  /mem_store/run wifi_ap 
  /mem_store/run base
  (Restart) 

## GPS 
  In u-center, make sure the following signals make it to I2C (using CFG_MSGOUT) (assuming a moving-base setup, a fixed-base setup will be slightly different and probably involve survey-in or fixed coordinates. See the integration manual): 

*  RTCM 4072.0 Reference station PVT information
*  RTCM 1074 GPS MSM4
*  RTCM 1084 GLONASS MSM4
*  RTCM 1094 Galileo MSM4
*  RTCM 1124 BeiDou MSM4
*  RTCM 1230 GLONASS code-phase biases

I also disabled sending any NMEA to i2c (you can do this with I2C_FILTEROUT) because otherwise it was too much data (I think partially because for some reason my serial device was echoing which was generating a lot of NMEA unknown messages). 
    

# Setting up the rover

## Radio
  Connect to ODIN-w2 serial port (usually the second one enumerated, at 460800). May want to clear memory (by holding SW0 for 3 seconds and giving it 1 sec before resetting) first 
  /wifi_setssid/run myssid
  /mem_store/run wifi_sta
  /mem_store/run rover
  (Restart) 

##GPS 
  The main thing you need to do is make sure that the UBX_NAV_RELPOSNED message makes it out over UART since that's what we're reading. We also want the GNGGA message, but that's usually on by default. 



# Troubleshooting

If your I2C link is getting saturated or you get a lot of "NMEA Unknown Message" probably something is echoing your serial port back to the device, confusing it. You can disable NMEA inputs to various parts to avoid those messages. 


