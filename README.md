# Building Amazon FreeRTOS firmware for Domain Tech Summit Workshop

This repository contains Amazon FreeRTOS code that pushes sensor data to the shadow and also controls WS2812 addressable LEDs on the board according to the desired shadow configuration. 



In order to compile the code in the Cloud9 environment please execute following sections:

- [Setting up Cloud9 Environment](./Cloud9.md)
- [Installing ESP32 toolchain](./ToolchainSetup.md)
- [Compiling Amazon FreeRTOS code](./CompilingWorkshopFW.md)
- [Uploading compiled firmware to ESP32 development board](./FlashingFW.md)


Shadow structure is following:

```json
{
    "sensors": {
        "temperature": 34.1,
	"pressure": 928.0,
	"humidity": 43.4,
	"illuminance": 530.1        
	},
    "buttons": {
    	"button1": 0,
    	"button2": 1,
    	"button3": 0,
    	"button4": 0
    },
    "leds": [
    	{
    		"red": 15,
    		"green": 0,
    		"blue": 0
    	},
    	{
    		"red": 0,
    		"green": 15,
    		"blue": 0
    	},
    	{
    		"red": 0,
    		"green": 0,
    		"blue": 15
    	},
    	{
    		"red": 15,
    		"green": 15,
    		"blue": 0
    	},
    	{
    		"red": 0,
    		"green": 15,
    		"blue": 15
    	}
    ]
	}
}
```
