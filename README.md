# Covert Communication Channels based on Hardware Trojans: open-source dataset and AI-based detection
Dataset of Hardware-Trojan (HT) based Covert Channels (HT-CCs) for the IEEE 802.11 (WiFi) standard.

## License
See licence file LICENCE.txt

## Datasets arhitecture
The dataset contains for 8 different SNR values, ranging from 1dB to 29dB with a step of 4dB, 5 × 2000 frames labelled to 1 out of 5 classes, namely CC-free (HT0-CC) and CC-infected (HTX-CC, X={1, · · · , 4}). The data set contains two acquisitions for each element of the data set. The second acquisition was obtained immediately after the first one, with no other parameters changing between one acquisition and the other. The second acquisition is marked with an underscore in the naming of the file.

### Naming convention
Files are named according to the following convention:

First acquisition:
rxSig_<SNR value>dB_HT<HTCC attack>.mat

Seconf acquisition:
rxSig_<SNR value>dB_HT<HTCC attack>.mat

SNR value: ranging from 1dB to 29dB with a step of 4dB, i.e., 1 = 1db, 2 = 5db, 3 = 9dB, 4 = 13dB, 5 = 17dB, 6 = 21dB, 7 = 25dB, 8 = 29dB.

## Hardware Platform
Acquisitions are received downconverted IQ samples using a Software Defined Radio (SDR) board bladeRF xA9.
