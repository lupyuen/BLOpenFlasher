# BLOpenFlasher: Flash Firmware to BL602 (Tested on PineCone)

TODO

Connect to PineCone USB Serial with Jumper set to L...

```bash
sudo screen /dev/ttyUSB0 2000000
```

Press the RST button.  We should see...

```text
helloworld
```

Restart PineCone USB Serial with Jumper set to H. Enter...

```bash
sudo go get gopkg.in/ini.v1 github.com/pelletier/go-toml github.com/albenik/go-serial

sudo go run flash_tool.go
```

Shows this error...

```text
bl602/partition/partition_cfg_2M.toml
bl602/image/partition.bin
10000
d8000
c8000
88000
0

160000
0
32000
0
0

192000
0
57000
0
0

1e9000
0
8000
0
0

1f1000
0
2000
0
0

1f3000
0
5000
0
0

1f8000
0
7000
0
0

424650540000070000000000269adf120000004657000000000000000000010000800d0000800c000080080000000000000000000200006d66670000000000000000160000000000002003000000000000000000000000000300006d656469610000000000201900000000000070050000000000000000000000000004000050534d00000000000000901e0000000000008000000000000000000000000000000500004b455900000000000000101f00000000000020000000000000000000000000000006000044415441000000000000301f000000000000500000000000000000000000000000070000666163746f7279000000801f000000000000700000000000000000000000000000ce01508b
&{bl602/partition/partition_cfg_2M.toml bl602/image/partition.bin map[]}
bl602/efuse_bootheader/efuse_bootheader_cfg.conf
bl602/builtin_imgs/blsp_boot2.bin
bl602/image/boot2image.bin
---- blk64k_erase_time = 0x4b0
0 1200 0 16 = 1200
---- blk32k_erase_cmd = 0x52
0 82 16 8 = 5373952
---- write_enable_cmd = 0x6
0 6 0 8 = 6
---- qpage_prog_cmd = 0x32
6 50 16 8 = 3276806
---- reg_read_cmd1 = 0x35
0 53 8 8 = 13568
---- de_burst_wrap_cmd = 0x77
0 119 0 8 = 119
---- hash_5 = 0x0
0 0 0 32 = 0
---- jedecid_cmd_dmy_clk = 0x0
0 0 8 8 = 0
---- cont_read_code = 0x20
0 32 16 8 = 2097152
---- de_burst_wrap_cmd_dmy_clk = 0x3
119 3 8 8 = 887
---- img_start = 0x2000
0 8192 0 32 = 8192
---- magic_code = 0x504e4642
0 1347307074 0 32 = 1347307074
---- burst_wrap_data_mode = 0x2
0 2 16 8 = 131072
---- crc_ignore = 0x0
0 0 16 1 = 0
---- write_vreg_enable_cmd = 0x50
0 80 24 8 = 1342177280
---- page_prog_cmd = 0x2
3276806 2 8 8 = 3277318
---- fast_read_qio_cmd = 0xeb
0 235 16 8 = 15400960
---- reg_write_cmd1 = 0x31
0 49 8 8 = 12544
---- de_burst_wrap_code_mode = 0x2
887 2 16 8 = 131959
---- jedecid_cmd = 0x9f
0 159 0 8 = 159
---- fast_read_qo_dmy_clk = 0x1
15400960 1 8 8 = 15401216
---- clkcfg_magic_code = 0x47464350
0 1195787088 0 32 = 1195787088
---- cache_enable = 0x1
0 1 9 1 = 512
---- fast_read_dio_cmd = 0xbb
0 187 16 8 = 12255232
---- blk64k_erase_cmd = 0xd8
5373952 216 24 8 = 3629252608
---- fast_read_qo_cmd = 0x6b
15401216 107 0 8 = 15401323
---- burst_wrap_dmy_clk = 0x3
131072 3 8 8 = 131840
---- power_down_delay = 0x3
0 3 16 8 = 196608
---- reset_cmd = 0x99
0 153 8 8 = 39168
---- qpi_fast_read_qio_cmd = 0xeb
1342177280 235 0 8 = 1342177515
---- cont_read_exit_code = 0xff
2097152 255 24 8 = 4280287232
---- hclk_div = 0x0
0 0 16 8 = 0
---- sector_erase_cmd = 0x20
3629252608 32 8 8 = 3629260800
---- exit_contread_cmd = 0xff
39168 255 16 8 = 16750848
---- hash_2 = 0x0
0 0 0 32 = 0
---- sfctrl_clk_delay = 0x1
0 1 16 8 = 65536
---- fast_read_dmy_clk = 0x1
0 1 8 8 = 256
---- no_segment = 0x1
512 1 8 1 = 768
---- qual_page_prog_addr_mode = 0x0
3277318 0 24 8 = 3277318
---- reg_read_cmd0 = 0x5
13568 5 0 8 = 13573
---- fast_read_do_dmy_clk = 0x1
12255232 1 8 8 = 12255488
---- qe_reg_index = 0x1
0 1 8 8 = 256
---- key_sel = 0x0
768 0 4 2 = 768
---- fast_read_cmd = 0xb
256 11 0 8 = 267
---- wel_reg_write_len = 0x2
0 2 16 8 = 131072
---- burst_wrap_code = 0x40
131840 64 24 8 = 1073873664
---- wel_bit_pos = 0x1
256 1 24 8 = 16777472
---- sfctrl_clk_invert = 0x1
65536 1 24 8 = 16842752
---- qpi_fast_read_dmy_clk = 0x1
267 1 24 8 = 16777483
---- flash_clk_type = 0x3
0 3 0 8 = 3
---- hash_0 = 0xdeadbeef
0 3735928559 0 32 = 3735928559
---- revision = 0x1
0 1 0 32 = 1
---- flash_clk_div = 0x1
3 1 8 8 = 259
---- aes_region_lock = 0x0
768 0 11 1 = 768
---- hash_6 = 0x0
0 0 0 32 = 0
---- page_size = 0x100
0 256 16 16 = 16777216
---- flashcfg_crc32 = 0x0
0 0 0 32 = 0
---- reset_en_cmd = 0x66
16750848 102 0 8 = 16750950
---- qe_reg_write_len = 0x1
0 1 0 8 = 1
---- qe_reg_read_len = 0x1
1 1 8 8 = 257
---- hash_ignore = 0x0
768 0 17 1 = 768
---- qpi_fast_read_cmd = 0xb
16777483 11 16 8 = 17498379
---- page_prog_time = 0x5
1200 5 16 16 = 328880
---- sign = 0x0
768 0 0 2 = 768
---- busy_reg_index = 0x0
16777472 0 16 8 = 16777472
---- clkcfg_crc32 = 0x0
0 0 0 32 = 0
---- cont_read_support = 0x1
16842752 1 8 8 = 16843008
---- chip_erase_cmd = 0xc7
3629260800 199 0 8 = 3629260999
---- fast_read_qio_dmy_clk = 0x2
15401323 2 24 8 = 48955755
---- enter_qpi_cmd = 0x38
4280287232 56 0 8 = 4280287288
---- qe_data = 0x0
196608 0 24 8 = 196608
---- hash_1 = 0x0
0 0 0 32 = 0
---- io_mode = 0x4
16843008 4 0 8 = 16843012
---- fast_read_dio_dmy_clk = 0x0
12255488 0 24 8 = 12255488
---- blk32k_erase_time = 0x4b0
0 1200 16 16 = 78643200
---- flashcfg_magic_code = 0x47464346
0 1195787078 0 32 = 1195787078
---- qe_bit_pos = 0x1
131072 1 0 8 = 131073
---- qpi_page_prog_cmd = 0x2
1342177515 2 16 8 = 1342308587
---- sector_size = 0x4
16777216 4 0 8 = 16777220
---- notload_in_bootrom = 0x0
768 0 10 1 = 768
---- cache_way_disable = 0x3
768 3 12 4 = 13056
---- crc32 = 0xdeadbeef
0 3735928559 0 32 = 3735928559
---- exit_contread_cmd_size = 0x3
16750950 3 24 8 = 67082598
---- bclk_div = 0x1
0 1 24 8 = 16777216
---- busy_reg_read_len = 0x1
257 1 24 8 = 16777473
---- exit_qpi_cmd = 0xff
4280287288 255 8 8 = 4280352568
---- sector_erase_time = 0x12c
78643200 300 0 16 = 78643500
---- busy_bit_pos = 0x0
131073 0 8 8 = 131073
---- fast_read_do_cmd = 0x3b
12255488 59 0 8 = 12255547
---- xtal_type = 0x4
16777216 4 0 8 = 16777220
---- pll_clk = 0x4
16777220 4 8 8 = 16778244
---- bootentry = 0x0
0 0 0 32 = 0
---- hash_7 = 0x0
0 0 0 32 = 0
---- qpi_jedecid_cmd = 0x9f
159 159 16 8 = 10420383
---- encrypt_type = 0x0
13056 0 2 2 = 13056
---- qpi_jedecid_dmy_clk = 0x0
10420383 0 24 8 = 10420383
---- hash_3 = 0x0
0 0 0 32 = 0
---- wel_reg_index = 0x0
16777472 0 0 8 = 16777472
---- wel_reg_read_len = 0x1
131073 1 24 8 = 16908289
---- reg_write_cmd0 = 0x1
12544 1 0 8 = 12545
---- chip_erase_time = 0x30d40
196608 200000 0 16 = 200000
---- img_len = 0x100
0 39312 0 32 = 39312
---- hash_4 = 0x0
0 0 0 32 = 0
---- mfg_id = 0xef
16777220 239 8 8 = 16838404
---- release_power_down = 0xab
16777473 171 16 8 = 27984129
---- burst_wrap_cmd = 0x77
1073873664 119 0 8 = 1073873783
---- de_burst_wrap_code = 0xf0
131959 240 24 8 = 4026663799
---- qpi_fast_read_qio_dmy_clk = 0x2
1342308587 2 8 8 = 1342309099
bl602/efuse_bootheader/efuse_bootheader_cfg.conf
bl602/bl602.bin
bl602/image/fwimage.bin
---- release_power_down = 0xab
0 171 16 8 = 11206656
---- burst_wrap_cmd = 0x77
0 119 0 8 = 119
---- de_burst_wrap_code = 0xf0
0 240 24 8 = 4026531840
---- qpi_fast_read_qio_dmy_clk = 0x2
0 2 8 8 = 512
---- blk64k_erase_time = 0x4b0
0 1200 0 16 = 1200
---- blk32k_erase_cmd = 0x52
0 82 16 8 = 5373952
---- write_enable_cmd = 0x6
0 6 0 8 = 6
---- qpage_prog_cmd = 0x32
6 50 16 8 = 3276806
---- reg_read_cmd1 = 0x35
0 53 8 8 = 13568
---- de_burst_wrap_cmd = 0x77
4026531840 119 0 8 = 4026531959
---- hash_5 = 0x0
0 0 0 32 = 0
---- jedecid_cmd_dmy_clk = 0x0
0 0 8 8 = 0
---- cont_read_code = 0x20
0 32 16 8 = 2097152
---- de_burst_wrap_cmd_dmy_clk = 0x3
4026531959 3 8 8 = 4026532727
---- img_start = 0x2000
0 8192 0 32 = 8192
---- magic_code = 0x504e4642
0 1347307074 0 32 = 1347307074
---- burst_wrap_data_mode = 0x2
119 2 16 8 = 131191
---- crc_ignore = 0x0
0 0 16 1 = 0
---- write_vreg_enable_cmd = 0x50
512 80 24 8 = 1342177792
---- page_prog_cmd = 0x2
3276806 2 8 8 = 3277318
---- fast_read_qio_cmd = 0xeb
0 235 16 8 = 15400960
---- reg_write_cmd1 = 0x31
0 49 8 8 = 12544
---- de_burst_wrap_code_mode = 0x2
4026532727 2 16 8 = 4026663799
---- jedecid_cmd = 0x9f
0 159 0 8 = 159
---- fast_read_qo_dmy_clk = 0x1
15400960 1 8 8 = 15401216
---- clkcfg_magic_code = 0x47464350
0 1195787088 0 32 = 1195787088
---- cache_enable = 0x1
0 1 9 1 = 512
---- fast_read_dio_cmd = 0xbb
0 187 16 8 = 12255232
---- blk64k_erase_cmd = 0xd8
5373952 216 24 8 = 3629252608
---- fast_read_qo_cmd = 0x6b
15401216 107 0 8 = 15401323
---- burst_wrap_dmy_clk = 0x3
131191 3 8 8 = 131959
---- power_down_delay = 0x3
0 3 16 8 = 196608
---- reset_cmd = 0x99
0 153 8 8 = 39168
---- qpi_fast_read_qio_cmd = 0xeb
1342177792 235 0 8 = 1342178027
---- cont_read_exit_code = 0xff
2097152 255 24 8 = 4280287232
---- hclk_div = 0x0
0 0 16 8 = 0
---- sector_erase_cmd = 0x20
3629252608 32 8 8 = 3629260800
---- exit_contread_cmd = 0xff
39168 255 16 8 = 16750848
---- hash_2 = 0x0
0 0 0 32 = 0
---- sfctrl_clk_delay = 0x1
0 1 16 8 = 65536
---- fast_read_dmy_clk = 0x1
0 1 8 8 = 256
---- no_segment = 0x1
512 1 8 1 = 768
---- qual_page_prog_addr_mode = 0x0
3277318 0 24 8 = 3277318
---- reg_read_cmd0 = 0x5
13568 5 0 8 = 13573
---- fast_read_do_dmy_clk = 0x1
12255232 1 8 8 = 12255488
---- qe_reg_index = 0x1
0 1 8 8 = 256
---- key_sel = 0x0
768 0 4 2 = 768
---- fast_read_cmd = 0xb
256 11 0 8 = 267
---- wel_reg_write_len = 0x2
0 2 16 8 = 131072
---- burst_wrap_code = 0x40
131959 64 24 8 = 1073873783
---- wel_bit_pos = 0x1
256 1 24 8 = 16777472
---- sfctrl_clk_invert = 0x1
65536 1 24 8 = 16842752
---- qpi_fast_read_dmy_clk = 0x1
267 1 24 8 = 16777483
---- flash_clk_type = 0x3
0 3 0 8 = 3
---- hash_0 = 0xdeadbeef
0 3735928559 0 32 = 3735928559
---- revision = 0x1
0 1 0 32 = 1
---- flash_clk_div = 0x1
3 1 8 8 = 259
---- aes_region_lock = 0x0
768 0 11 1 = 768
---- hash_6 = 0x0
0 0 0 32 = 0
---- page_size = 0x100
0 256 16 16 = 16777216
---- flashcfg_crc32 = 0x0
0 0 0 32 = 0
---- reset_en_cmd = 0x66
16750848 102 0 8 = 16750950
---- qe_reg_write_len = 0x1
11206656 1 0 8 = 11206657
---- qe_reg_read_len = 0x1
11206657 1 8 8 = 11206913
---- hash_ignore = 0x0
768 0 17 1 = 768
---- qpi_fast_read_cmd = 0xb
16777483 11 16 8 = 17498379
---- page_prog_time = 0x5
1200 5 16 16 = 328880
---- sign = 0x0
768 0 0 2 = 768
---- busy_reg_index = 0x0
16777472 0 16 8 = 16777472
---- clkcfg_crc32 = 0x0
0 0 0 32 = 0
---- cont_read_support = 0x1
16842752 1 8 8 = 16843008
---- chip_erase_cmd = 0xc7
3629260800 199 0 8 = 3629260999
---- fast_read_qio_dmy_clk = 0x2
15401323 2 24 8 = 48955755
---- enter_qpi_cmd = 0x38
4280287232 56 0 8 = 4280287288
---- qe_data = 0x0
196608 0 24 8 = 196608
---- hash_1 = 0x0
0 0 0 32 = 0
---- io_mode = 0x4
16843008 4 0 8 = 16843012
---- fast_read_dio_dmy_clk = 0x0
12255488 0 24 8 = 12255488
---- blk32k_erase_time = 0x4b0
0 1200 16 16 = 78643200
---- flashcfg_magic_code = 0x47464346
0 1195787078 0 32 = 1195787078
---- qe_bit_pos = 0x1
131072 1 0 8 = 131073
---- qpi_page_prog_cmd = 0x2
1342178027 2 16 8 = 1342309099
---- sector_size = 0x4
16777216 4 0 8 = 16777220
---- notload_in_bootrom = 0x0
768 0 10 1 = 768
---- cache_way_disable = 0x3
768 3 12 4 = 13056
---- crc32 = 0xdeadbeef
0 3735928559 0 32 = 3735928559
---- exit_contread_cmd_size = 0x3
16750950 3 24 8 = 67082598
---- bclk_div = 0x1
0 1 24 8 = 16777216
---- busy_reg_read_len = 0x1
11206913 1 24 8 = 27984129
---- exit_qpi_cmd = 0xff
4280287288 255 8 8 = 4280352568
---- sector_erase_time = 0x12c
78643200 300 0 16 = 78643500
---- busy_bit_pos = 0x0
131073 0 8 8 = 131073
---- fast_read_do_cmd = 0x3b
12255488 59 0 8 = 12255547
---- xtal_type = 0x4
16777216 4 0 8 = 16777220
---- pll_clk = 0x4
16777220 4 8 8 = 16778244
---- bootentry = 0x0
0 0 0 32 = 0
---- hash_7 = 0x0
0 0 0 32 = 0
---- qpi_jedecid_cmd = 0x9f
159 159 16 8 = 10420383
---- encrypt_type = 0x0
13056 0 2 2 = 13056
---- qpi_jedecid_dmy_clk = 0x0
10420383 0 24 8 = 10420383
---- hash_3 = 0x0
0 0 0 32 = 0
---- wel_reg_index = 0x0
16777472 0 0 8 = 16777472
---- wel_reg_read_len = 0x1
131073 1 24 8 = 16908289
---- reg_write_cmd0 = 0x1
12544 1 0 8 = 12545
---- chip_erase_time = 0x30d40
196608 200000 0 16 = 200000
---- img_len = 0x100
0 865232 0 32 = 865232
---- hash_4 = 0x0
0 0 0 32 = 0
---- mfg_id = 0xef
16777220 239 8 8 = 16838404
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

