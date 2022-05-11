# M031BSP_I2C_SHT31
 M031BSP_I2C_SHT31


update @ 2022/05/11

1. use I2C0 initial SHT31 (PC1 : SCL , PC0 : SDA) , with I2C interrupt and polling flow (SHT31 is 16bit REGISTER)

check #define ENABLE_I2C_POLLING_DISCRETE , #define ENABLE_I2C_IRQ

2. base on sample code behavior

https://github.com/Sensirion/embedded-sht

3. when read data with REG : 0x2400 , need to put delay 15ms for measurement on going before start to read data

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/delay.jpg)	

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/SHT3x_table.9.jpg)	

4. below is polling LA capture with REG : 0x2400 , 

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/LA_polling_I2C_WR_24_00.jpg)	
	
below is polling LA capture to read data 

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/LA_polling_I2C_WR_24_00.jpg)	

5. below is interrupt LA capture with REG : 0x2400 , 

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/LA_interrupt_I2C_WR_24_00.jpg)	
	
6. below is log message capture ,

![image](https://github.com/released/MM031BSP_I2C_SHT31/blob/main/log.jpg)	


