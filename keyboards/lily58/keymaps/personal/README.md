<!-- compiling doesn't work on arch because the avr-cpp version is to new -->
`qmk json2c -o my_layout.c my_layout.json` and copy keymaps array to `keymap.c`
`docker run --privileged -it --rm -v "$(pwd):/qmk_firmware" qmk compile -km personal -kb lily58`
`sudo avrdude -v -patmega32u4 -cavr109 -P/dev/ttyACM0 -b57600 -Uflash:w:".build/lily58_rev1_personal.hex":i`
