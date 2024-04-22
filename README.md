# SPERO Dataset
SPERO(Simultaneous Power/EM Side-channel RASC and oscilloscope dataset) is a side-channel dataset follows the format and structure of the popular side-channel attack dataset called ASCAD. The structure of SPERO is shown below, 

![dataset](https://github.com/YunkaiUF/SPERO/assets/126429160/3c5ca934-15ae-4748-a4b6-592bcfb34c00)

We collected 2000-feature power/EM traces for the third subkey of the first round of unmasked and masked AES encryptions. Since each subkey of unmasked/masked AES consists of 8 bits, there are a total of 256 possible subkey values. For each subkey value, we have gathered 256 traces, where the plaintext at position 3 varies from 0x00 to 0xFF. Consequently, there are a total of 131072 (256x256x2) power/EM traces for both unmasked and masked AES encryption. In these 131072 traces, the first 100000 of EM/power traces have been organized into the profiling folder, while the remaining 31072 traces have been placed in the testing folder. Furthermore, each power/EM trace is labeled sequentially and accompanied by essential information, including the label's sequence number, channel, and plaintext value. In the end, we also upload included a tutorial text to guide users in opening the files using the provided Python script.

# Experiment setup
In our experiments, we gather EM and power traces at the same time when the attack target is encrypting data. The target board is Arduino UNO and its core frequency is 16MHz. The sampling speed of our oscilloscope MDO3102 is set to 100MS/s in the unmasked AES experiment and 500MS/s in the masked AES experiment. The sampling speed of RASCv3 is 160MS/s in both masked/unmasked experiment. 

# RASC
RASC (short for, remote access to a side-channel platform), an external miniature monitor, that performs side-channel analysis for offensive (e.g., secret extraction) and defensive purposes (e.g., disassembly and malware detection) on a target chip. The first version of RASC was introduced by Stern et al. in 2019[1], and the upgrade version (RASCv2) was first presented by Bai et al. in 2022[2]. For generating SPERO dataset, we use the third version of RASC (RASCv3) and the comparison with RASCv2 and traditional side-channel instruments, such as oscilloscope is included in our paper. 

# Unmasked AES code
The unmasked AES code could be found in [3].

# Masked AES code
The masked AES code could be found in [4].

# References
[1] A. Stern, K. Yang, J. Vosatka, A. Duncan, J. Park, D. Forte, and M. Tehranipoor, “Rasc: Enabling remote access to side-channels for mission critical systems,” GOMACTech, 2019.
[2] Y. Bai, A. Stern, J. Park, M. Tehranipoor, and D. Forte, “Rascv2: Enabling remote access to side-channels for mission critical and iot systems,” ACM Transactions on Design Automation of Electronic Systems
(TODAES), vol. 27, no. 6, pp. 1–25, 2022.
[3] “tinyaes,” https://github.com/kokke/tiny-AES-c
[4] “CENSUS,” https://github.com/CENSUS/masked aes-c/tree/main
