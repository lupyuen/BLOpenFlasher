# BLOpenFlasher: Flash Firmware to BL602 (Tested on PineCone)

TODO: Connect to PineCone USB Serial

```bash
sudo screen /dev/ttyUSB0 2000000
```

# Previous Instructions

This is open source version for flash_tools, not perfect but open source totally. The current version also require python3 env, and if not please use tools to convert dts to dtb.

# Installing dependencies
```bash
go get gopkg.in/ini.v1 github.com/pelletier/go-toml github.com/albenik/go-serial
```

# Usage
Switch BL602 to program mode by pulling-up GPIO8 during booting, connect via the uart(which is hardcode now), and then run "go run flash_tool.go". Bin files are generated and then bl602 will be programmed. 

# Other version
Initially Golang version is only for mass production program with linux. Now, there are other better options for cross platform requirement. Thanks for these contributors.  
Python version:  
https://github.com/stschake/bl60x-flash  
https://github.com/renzenicolai/bl602tool     
Rust version:  
https://github.com/spacemeowx2/blflash  
https://github.com/mkroman/bouffalo-cli   

