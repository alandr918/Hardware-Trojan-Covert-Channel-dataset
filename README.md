# Covert Communication Channels based on Hardware Trojans: open-source dataset
Dataset of Hardware-Trojan (HT) based Covert Channels (HT-CCs) for the IEEE 802.11 (WiFi) standard.

## License
See licence file LICENCE.txt

## Reference Paper
Please reference the following paper when using the dataset:
> A. R. Díaz-Rizo, A. Abdelazim, H. Aboushady and H.-G. Stratigopoulos, "Covert Communication Channels Based On Hardware Trojans : Open-Source Dataset and AI-based Detection," 2024 IEEE International Symposium on Hardware Oriented Security and Trust (HOST), Washington DC, United States of America, May 2024.

## Datasets arhitecture
+ The dataset has 80 dataset elements organized in 5 classes, namely CC-free (HT0-CC) and CC-infected (HTX-CC, X={1, · · · , 4}), each class has 16 elements.
+ Those 16 elements are 8 acquisitions for different SNR values ranging from 1dB to 29dB with a step of 4dB, 2 acquisitions for each SNR value. The second acquisition was obtained immediately after the first one, with no other parameters changing between one acquisition and the other. The second acquisition is marked with an underscore in the naming of the file.
+ Each dataset element has 2000 frames and it is the concatenation of ten 200-frames sub-acquisitions.

### Naming convention
Files are named according to the following convention:

First acquisition:
```
rxSig_<SNR value>dB_HT<HTCC attack>.mat
```

Second acquisition:
```
rxSig_<SNR value>dB_HT<HTCC attack>_.mat
```
+ SNR value: ranging from 1dB to 29dB with a step of 4dB, i.e., <1>=SNR of 1db, <2>=SNR of 5db, <3>=SNR of 9dB, <4>=SNR of 13dB, <5>=SNR of 17dB, <6>=SNR of 21dB, <7>=SNR of 25dB, <8>=SNR of 29dB.
+ HTCC attack: HTCC-free (HT0-CC) and HTCC-infected (HTX-CC, X={1, · · · , 4}).

### HT0-CC
The HT0-CC is the benchmark CC-free transmission according to the WiFi standard.

### HT1-CC
The HT1-CC is the Amplitude Modulation (AM) Short Training Sequence (STS) HT attak based on the paper
> A. R. Díaz-Rizo, H. Aboushady and H.-G. Stratigopoulos, "Leaking Wireless ICs via Hardware Trojan-Infected Synchronization," in IEEE Transactions on Dependable and Secure Computing, vol. 20, no. 5, pp. 3845-3859, 1 Sept.-Oct. 2023, doi: 10.1109/TDSC.2022.3218507.

The amplitude modulation value alpha is set to 10%.

### HT2-CC
The HT2-CC is the PSK STF HT attack based on the paper
> J. Classen, M. Schulz and M. Hollick, "Practical covert channels for WiFi systems," in Proceedings of 2015 IEEE Conference on Communications and Network Security (CNS), Florence, Italy, 2015, pp. 209-217, doi: 10.1109/CNS.2015.7346830.

The implemented version is leaking 8 bits per OFDM PPDU.

### HT3-CC
The HT3-CC is the Dirty Constellation attack based on paper
> A. Dutta, D. Saha, D. Grunwald and D. Sicker, "Secret Agent Radio: Covert Communication through Dirty Constellations," in Information Hiding, M. Kirchner and D. Ghosal, Eds., Berlin, Heidelberg, 2013,
pp. 160–175, Springer Berlin Heidelberg, doi: 10.1007/978-3-642-36373-3_11.

The implemented version of this attack has an embedding frequency of 5 subcarriers per OFDM symbol, where each OFDM symbol comprises 48 data subcarriers. Each dirty subcarrier is leaking 2 bits; therefore, we are leaking 10 bits per OFDM symbol,

### HT4-CC
The HT4-CC is the AM analog/RF attack based on paper
> K. S. Subramani, N. Helal, A. Antonopoulos, A. Nosratinia and Y. Makris, "Amplitude-Modulating Analog/RF Hardware Trojans in Wireless Networks: Risks and Remedies," in IEEE Transactions on Information Forensics and Security, vol. 15, pp. 3497-3510, 2020, doi: 10.1109/TIFS.2020.2990792.

Due to SPI limitations, the implemented version of the attack is a digitally-emulated version of the AM analog/RF attack. It leaks 8 bits per transmitted frame.

## Hardware Platform
Acquisitions are received downconverted IQ samples using a Software Defined Radio (SDR) board bladeRF xA9.
