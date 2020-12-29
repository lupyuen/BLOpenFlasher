# BLOpenFlasher: Flash Firmware to BL602 (Tested on PineCone)

TODO: Connect to PineCone USB Serial

```bash
sudo screen /dev/ttyUSB0 2000000

sudo go get gopkg.in/ini.v1 github.com/pelletier/go-toml github.com/albenik/go-serial

sudo go run flash_tool.go
```

Shows...

```text
48955499 1 8 8 = 48955755
131819 80 24 8 = 1342309099
16777216 1 8 8 = 16777472
1073742711 2 16 8 = 1073873783
256 3 0 8 = 259
0 8192 0 32 = 8192
0 3735928559 0 32 = 3735928559
65540 1 8 8 = 65796
65796 1 24 8 = 16843012
exit status 1
CmdReset
/dev/ttyUSB0---RESET Module---
/dev/ttyUSB0 Next to CmdShakeHand
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdBootInfo
/dev/ttyUSB0 14:13 <-4f4b1400010000000000000003000000619dc005b9181d00
/dev/ttyUSB0 Next to CmdBootHeader
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegHeader
/dev/ttyUSB0 14:13 <-4f4b10000000012290710000357dc86e938a7a6f
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:13 <-
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:12 <-
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:14 <-
/dev/ttyUSB0 14:13 <-4f4b4f4b
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:14 <-
/dev/ttyUSB0 14:13 <-4f4b4f4b
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:14 <-
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 14:13 <-4f4b
/dev/ttyUSB0 Next to CmdSegData
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:14 <-
/dev/ttyUSB0 14:13 <-464c1402464c1402
/dev/ttyUSB0 14:13 <-464c1402
/dev/ttyUSB0 Next to ConfigReset
/dev/ttyUSB0 Next to CmdReset
/dev/ttyUSB0---RESET Module---
/dev/ttyUSB0 Next to CmdShakeHand
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 Failed to read [Res]
/dev/ttyUSB0 14:9 <-
/dev/ttyUSB0 Next to CmdReset
/dev/ttyUSB0---RESET Module---
/dev/ttyUSB0 Next to CmdShakeHand
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 Next to CmdReset
/dev/ttyUSB0---RESET Module---
/dev/ttyUSB0 Next to CmdShakeHand
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 14:0 <-
/dev/ttyUSB0 Next to CmdReset
/dev/ttyUSB0 Next to ErrorShakeHand
ErrorShakeHand can not be located!
/dev/ttyUSB0 -----Failure-----
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

