
# ADS1115

[![ADS1115](ADS1115_I2CADC.png)](https://store.ncd.io/product/ads1115-16-bit-4-channel-precision-analog-to-digital-converter-i2c-mini-module/)

# ADS1115
ADS1115 is a 16-Bit 4-Channel Precision Analog to Digital Converter I2C Mini Module.
This Device is available from www.ncd.io

[SKU: ADS1115_I2CS]

(https://store.ncd.io/product/ads1115-16-bit-4-channel-precision-analog-to-digital-converter-i2c-mini-module/)

This Sample code can be used with  Arduino.

Hardware needed to interface ADS1115 16-Bit 4-Channel Precision Analog to Digital Converter with Arduino
1. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-nano/">Arduino Nano</a>
2. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-micro-with-i2c-expansion-port/">Arduino Micro</a>
3. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-uno/">Arduino uno</a>
4. <a href="https://store.ncd.io/product/dual-i2c-shield-for-arduino-due-with-modular-communications-interface/">Arduino Due</a>
5. <a href="https://store.ncd.io/product/ads1115-16-bit-4-channel-precision-analog-to-digital-converter-i2c-mini-module/">ADS1115 16-Bit 4-Channel Precision Analog to Digital Converter</a>
6. <a href="https://store.ncd.io/product/i%C2%B2c-cable/">I2C Cable</a>

ADS1115 :

ADS1115 is a 4 Channel 16 bit resolution Analog to digital Converter. This ADC can be used as four single ended and two differential inputs analog to digital converter, signal channel differential analog to digital converter or single channel comparator. 
The ADC board has 2 address jumpers, which can be used to set upto 4 different I2C addresses. 

Applications:

•Portable Instrumentation

•Battery Voltage and Current Monitoring

•Temperature Measurement Systems

•Consumer Electronics

•Factory Automation and Process Control

## Arduino
Download and install Arduino Software (IDE) on your machine. Steps to install Arduino are provided at:

https://www.arduino.cc/en/Main/Software

Download (or git pull) the code and double click the file to run the program.
Compile and upload the code on Arduino IDE and see the output on Serial Monitor.

How to Use the ADS1115 Arduino Library
The ADS1115 has a number of settings, which can be configured based on user requirements.
1. Gain Settings : ADS1115 supports upto 8 gain settings and these gain settings can be changed using this function

    ads.setGain(GAIN_TWO);          // 2x gain   +/- 2.048V  1 bit = 0.0625mV (default)
    
2. Mode of Operation : ADS1115 has two mode of operation, one is Continuous conversion mode and other one is Power-down single-shot mode. If you are using this ADC in a battery powered application, you should use Power-down single-shot mode.
The mode of operation setting can be changed using this function

    ads.setMode(MODE_CONTIN);  
    
3. Sample rate : ADS1115 supports upto 860 SMPS settings, these settings can be changed based on number of sample required in a second. If you have a application where you need the data really quick in the minimum possible time you can use the higher number of samples setting. If you need high accuracy data without any time constraint, in that case you can use low SMPS setting. In general application you can keep the SMPS number in middle.
You can change the SMSP using this function

    ads.setRate(RATE_128);
 
 Reading ADS1115 in differential mode : To read the ADC input in differential mode you can use this function
 
    result01 = ads.Measure_Differential(01);
    
 In this setting you will need to connect your ADC input at channel 0 and channel 1. The ADS1115 will read the voltage difference between these two inputs.
 
 Reading ADS1115 In single ended Mode : To read the ADC input in single ended mode you can use this function
 
    adc0 = ads.Measure_SingleEnded(0);
    
  In this case it will read the voltage at ADC input channel 0 and at ADC input channel 1
