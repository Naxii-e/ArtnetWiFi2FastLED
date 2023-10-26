# ArtnetWiFi2FastLED
[ArtnetWifi](https://github.com/rstephan/ArtnetWifi)を使用し受信したDMX512パケットをFastLED(NeoPixel)用シグナルに変換し、WS2812Bなどを操作することが出来ます。

## Envs
- ESP32-WROOM-32
- WS2812B
- FastLED 3.6.0
- ArtnetWifi 1.5.1

## Max channels
1 universe(<=512ch)を超えるLEDは、現段階では制御できません。
最大LED数はRGBの場合は、
```
MaxLeds = NumberOfChannels * LedNums
```
で求めることが出来ます。
`NumberOfChannels`はチャンネルに対するLEDの数となり、WS2811のようなLED 3つに対し1つのアドレスを持つ場合は、`3`となります。

## Art-Net Credits
Art-Net™ Designed by and Copyright Artistic Licence
[Art-Net](https://www.artisticlicence.com/WebSiteMaster/User%20Guides/art-net.pdf)
