# SPERO
SPERO(Simultaneous Power/EM Side-channel RASC and oscilloscope dataset) is a side-channel dataset follows the format and structure of the popular side-channel attack dataset called ASCAD. As shown in Figure, 


![dataset (3)](https://github.com/YunkaiUF/SPERO/assets/126429160/5d8b6b96-b11d-4ad4-a195-d5ceea74d36e)


we collected 2000-feature power/EM traces for the third subkey of the first round of unmasked and masked AES encryptions. Since each subkey of unmasked/masked AES consists of 8 bits, there are a total of 256 possible subkey values. For each subkey value, we have gathered 256 traces, where the plaintext at position 3 varies from 0x00 to 0xFF. Consequently, there are a total of 131072 (256$\times$256$\times$2) power/EM traces for both unmasked and masked AES encryption. In these 131072 traces, the first 100000 of EM/power traces have been organized into the profiling folder, while the remaining 31072 traces have been placed in the testing folder. Furthermore, each power/EM trace is labeled sequentially and accompanied by essential information, including the label's sequence number, channel, and plaintext value. Lastly, we have included a tutorial text to guide users in opening the files using the provided Python script.
