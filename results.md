
***

**Table 1: Training Time Comparison (second/sample) for distilling GPT-2 XL (1.5B) into GPT-2 (0.1B).**

| Method   | Training Time (second/sample) |
|----------|---------------------------|
| SFT      | 0.344                      |
| KD       | 0.649                      |
| MiniLLM  | 4.452                      |
| GKD      | 2.078                      |
| DISTILLM | 1.331                      |
|AlphaNet|  0.882 |
| Ours     | 0.768                      |

***

<p >
  <img src="https://github.com/user-attachments/assets/1cb9788c-5328-4f95-b2d5-ceaf5b32a134" alt="dolly" width="500">
</p>

**Figure 1: Performance of different loss functions on the Dolly validation set over the entire training process.**

***

**Table 2: ROUGE-L scores (↑) of different loss functions on five task-agostic instruction-following datasets when distilling GPT-2 XL (1.5B) into GPT-2 (0.1B). We report the average and standard
deviation of ROUGE-L scores across five random seeds \[10, 20, 30, 40, 50\].**

| **Loss Function**         | **Dolly Eval** | **Self-Instruct** | **Vicuna Eval** | **Super-Natural** | **Unnatural** |
|---------------------------|----------------|-------------------|-----------------|-------------------|---------------|
| **FKLD**                  | 23.80 (0.37)   | 10.01 (0.75)      | 15.25 (0.65)    | 17.69 (0.26)      | 18.99 (0.05)  |
| **RKLD**                  | 24.77 (0.37)   | 12.02 (0.48)      | 15.06 (0.28)    | 23.27 (0.29)      | 26.01 (0.11)  |
| **WSD**                   | 23.33 (0.52)   | 10.52 (0.47)      | 14.83 (0.61)    | 19.67 (0.13)      | 21.21 (0.21)  |
| **BDKD**        | 23.94 (0.24) | 11.83 (0.39) | 15.21 (0.23) | 19.56 (0.23) | 21.66 (0.23) |
| **Jensen's KL**     | 23.79 (0.24) | 11.52 (0.18) | 15.35 (0.80) | 21.36 (0.17) | 21.97 (0.10) |
| **AKL**       | 23.83 (0.59) | 10.87 (0.42) | 15.63 (0.66) | 20.07 (0.32) | 21.97 (0.13) |
| **AlphaNet**       | 25.13 (0.27) | 12.46 (0.46) | 15.64 (0.40) | 25.27 (0.20) | 27.56 (0.15) |
| **Ours** | **25.65** (0.24) | **13.47** (0.42) | **16.06** (0.25) | **26.47** (0.31) | **29.32** (0.08) |


***

**Table 3: ROUGE-L scores (↑) on five task-agnostic instruction-following datasets when distilling OpenLLaMA2-7B into OpenLLaMA2-3B.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| SFT       | 24.54 (0.51) | 16.80 (0.64) | 16.15 (0.15) | 29.29 (0.13) | 27.43 (0.21) |
| FKLD        | 25.23 (0.44) | 18.90 (1.20) | 16.67 (0.35) | 31.68 (0.22) | 29.36 (0.13) |
| RKLD   | 27.74 (0.45) | 20.61 (0.80) | 18.83 (0.40) | 35.31 (0.24) | 33.86 (0.16) |
| Jensen's KL       | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.79 (0.17) |
| BDKD       | 26.78 (0.53) | 18.94 (0.68) | 17.81 (0.52) | 32.15 (0.34) | 30.89 (0.24)  |
| AKL       | 26.38 (0.41) | 17.69 (0.46) | 16.72 (0.48) | 33.02 (0.16) | 31.29 (0.08) |
| DISTILLM  | 28.24 (0.48) | 21.00 (0.72) | 19.12 (0.53) | 37.06 (0.35) | 35.05 (0.13) |
| AlphaNet  | 28.11 (0.29) | 21.30 (0.63) | 18.70 (0.23) | 37.86 (0.44) | 35.40 (0.17) |
| Ours (ABKD) | **30.25** (0.37) | **22.39** (0.62) | **20.83** (0.42) | **38.51** (0.32) | **38.66** (0.10) |

***

