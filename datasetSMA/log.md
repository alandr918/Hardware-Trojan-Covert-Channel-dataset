# Log
Label of the files and meaning:
+ Received signal after AFE digitizing
+ At N dB of SNR
+ Type of Hardware Trojan (HT)
+ Parameter variance
```
    rxSig_<N>dB_HT<0,1,2,...,6>_<a5,a10,a15,b4,b6,b8>
```

## HT-free
```
    rxSig_1dB_HT0_a0 ... rxSig_8dB_HT0_a0
```

## AM STS HT
+ alpha (a), i.e., amplitud modulation of corrupted subcarriers at 10%
```
    rxSig_1dB_HT1_a10 ... rxSig_8dB_HT1_a10
```

## PSK STS HT
+ beta (b), i.e., number of leaked bits per frame, equal to 8-bits
```
    rxSig_1dB_HT2_b8 ... rxSig_8dB_HT2_b8
```