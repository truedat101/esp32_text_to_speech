# ESP32 text to speech to bluetooth speaker

This project plays text to speech from an esp32 to a bluetooth speaker

ESP32 Version of [SAM](https://github.com/s-macke/SAM)

This is a modifed version of: https://github.com/tuanpmt/esp-adf-sam.git

This example plays audio generated from text `HELLO, MY NAME IS SAM.` using [SAM](https://github.com/s-macke/SAM) - Tiny Speech Synthesizer.

To run this example you need ESP32 with SPI RAM such as a WROVERB esp32. Alternatively, you may be smart enough to work out how to reduce the RAM usage of this project so it runs on an ordinary esp32. 
Let me know if you do, and I'll update to include your improvements.

You'll need to install the esp32 ADF - instructions here: https://docs.espressif.com/projects/esp-adf/en/latest/get-started/

You MUST modify main/app_main.c to specify the device name of your bluetooth speaker.

look for this line:
```
        .remote_name = "BT-12",
```

## Compile

```
git clone --recursive https://github.com/bootrino/esp32_text_to_speech.git
cd esp32_text_to_speech
make menuconfig
make flash
make monitor

```
