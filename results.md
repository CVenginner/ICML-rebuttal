
$\alpha$-$\beta$-divergence


***
**Table 1: ROUGE-L scores (↑) of different loss functions on five task-agostic instruction-following datasets. We report the average and standard
deviation of ROUGE-L scores across five random seeds \[10, 20, 30, 40, 50\].**

| **Loss Function**         | **Dolly Eval** | **Self-Instruct** | **Vicuna Eval** | **Super-Natural** | **Unnatural** |
|---------------------------|----------------|-------------------|-----------------|-------------------|---------------|
| **FKLD**                  | 23.80 (0.37)   | 10.01 (0.75)      | 15.25 (0.65)    | 17.69 (0.26)      | 18.99 (0.05)  |
| **RKLD**                  | 24.77 (0.37)   | 12.02 (0.48)      | 15.06 (0.28)    | 23.27 (0.29)      | 26.01 (0.11)  |
| **WSD**                   | 23.33 (0.52)   | 10.52 (0.47)      | 14.83 (0.61)    | 19.67 (0.13)      | 21.21 (0.21)  |
| **BDKD**        | 23.94 (0.24) | 11.83 (0.39) | 15.21 (0.23) | 19.56 (0.23) | 21.66 (0.23) |
| **Jensen's KL**     | 23.79 (0.24) | 11.52 (0.18) | 15.35 (0.80) | 21.36 (0.17) | 21.97 (0.10) |
| **AKL**       | 23.83 (0.59) | 10.87 (0.42) | 15.63 (0.66) | 20.07 (0.32) | 21.97 (0.13) |
| **AlphaNet**       | 25.13 (0.27) | 12.46 (0.46) | 15.68 (0.40) | 25.27 (0.20) | 27.56 (0.15) |
| **$\alpha$-$\beta$-divergence** | **25.65** (0.24) | **13.47** (0.42) | **16.06** (0.25) | **26.47** (0.31) | **29.32** (0.08) |


***

**Table 2: ROUGE-L scores (↑) for OpenLLaMA2-3B across five task-agnostic instruction-following datasets, with OpenLLaMA2-7B serving as the teacher model.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| SFT       | 24.54 (0.51) | 16.80 (0.64) | 16.15 (0.15) | 29.29 (0.13) | 27.43 (0.21) |
| KD        | 25.23 (0.44) | 18.90 (1.20) | 16.67 (0.35) | 31.68 (0.22) | 29.36 (0.13) |
| SeqKD     | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.89 (0.10) |
| GKD       | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.79 (0.17) |
| MINILLM   | 27.74 (0.45) | 20.61 (0.80) | 18.83 (0.40) | 35.31 (0.24) | 33.86 (0.16) |
| DISTILLM  | 28.24 (0.48) | 21.00 (0.72) | 19.12 (0.53) | 37.06 (0.35) | 35.05 (0.13) |
| Ours (ABKD) | **30.25** (0.37) | **22.39** (0.62) | **20.83** (0.42) | **38.51** (0.32) | **38.66** (0.10) |

***

**Table 3:Training Time Comparison (second/sample). SeqKD denotes supervised fine-tuning on teacher outputs.**

| Method   | Training Time (second/sample) |
|----------|---------------------------|
| SFT      | 0.344                      |
| KD       | 0.649                      |
| SeqKD    | 0.744                      |
| MiniLLM  | 4.452                      |
| GKD      | 2.078                      |
| DISTILLM | 1.331                      |
| Ours     | 0.772                      |

***


<p >
  <img src="https://github.com/user-attachments/assets/8ef32724-24a7-4684-a801-112ecca5aae6" alt="dolly" width="500">
</p>

**Figure 1.** Performance of different loss functions on the Dolly validation set over the entire training process.

***

**Table 4: ROUGE-L scores (↑) for GPT-2 (0.1B) across five task-agnostic instruction-following datasets, with GPT-2 XL (1.5B) serving as the teacher model.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| FKLD        | 23.80 (0.37) | 10.01 (0.75) | 15.25 (0.65) | 17.69 (0.26) |  18.99 (0.05) |
| RKLD        | 24.77 (0.37) | 12.02 (0.48) | 15.06 (0.28)) | 23.27 (0.29) | 26.01 (0.11) |
| AlphaNet       | 25.13 (0.27) | 12.46 (0.46) | 15.68 (0.40) | 25.67 (0.20) | 27.86 (0.15) |
| BDKD        | 23.94 (0.24) | 11.83 (0.39) | 15.21 (0.23) | 19.56 (0.23) | 21.66 (0.23) |
| Jensen's KL     | 23.79 (0.24) | 11.52 (0.18) | 15.35 (0.80) | 21.36 (0.17) | 21.97 (0.10) |
| AKL       | 23.83 (0.59) | 10.87 (0.42) | 15.63 (0.66) | 20.07 (0.32) | 21.97 (0.13) |
| Ours (ABKD) | **25.65** (0.24) | **13.47** (0.42) | **16.06** (0.25) | **26.47** (0.31) | **29.32** (0.08) |

***


