# Covert Commuication Channels dataset
Dataset of wireless Covert Communication Channels (CCCs) for the IEEE 802.11 standard (WiFi).

## Objectives
Undetectability and reliability are the main goals of wireless covert communication channel. Also, the hardware overhead to enable the CCC must be minimum to be stealthy.

## Characteristics
+ Acquisitions are received downconverted IQ samples using a Software Defined Radio (SDR) board bladeRF xA9.
+ Transmission signals are created in Matlab following the physical layer (PHY) specifications.
+ A frame of the transmitted signal is composed of a preamble and the payload.
+ The preamble is composed of 320 IQ samples.
+ The payload is an OFDM-QPSK signal of 320 IQ samples.
+ The total frame size is 640 IQ samples.
+ In each transmitted signal there are 1024 frames (each has 640 samples), so 655,360 samples.

## License
See licence file LICENCE.txt

## Datasets SMA
+ 8 different SNR leves

### HT-free
+ Clean signal

### Amplitud Modulation Short Training Sequence Hardare Trojan (AM STS HT)
+ three different AM (alpha) mangitudes, 5%, 10% and 15%

### Phase Shift Keying Short Training Sequence Hardare Trojan (PSK STS HT)
+ three different cases (beta), 8, 6, and 4 bits per frame
+ 8-bits per frame (implemented)
+ 6-bits (TODO)
+ 4-bits (TODO)
