all: accelerometer

CONTIKI=../../..

### TARGET DECLARATION
TARGET = hiveMote
CPU_FAMILY = cc26xx
# CPU_FAMILY = cc13xx

### Accelerometer Used
### Options for hiveMote:
### > NO SENSOR - leave blank
### > ADXL345 (SPI or I2C)
### > MPU6050 (I2C only)
ACCELEROMETER_USED =  ADXL345
ACCELEROMETER_INTERFACE =  SPI

ifneq ($(ACCELEROMETER_USED),)
	WITH_$(ACCELEROMETER_USED)=1
	CFLAGS += -D$(ACCELEROMETER_USED)_$(ACCELEROMETER_INTERFACE)_INTERFACE=1
	CFLAGS += -DHAS_$(ACCELEROMETER_USED)=1
endif

include $(CONTIKI)/Makefile.include
