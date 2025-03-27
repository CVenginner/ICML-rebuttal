**Table 1: ROUGE-L scores (↑) for OpenLLaMA2-3B across five task-agnostic instruction-following datasets, with OpenLLaMA2-7B serving as the teacher model.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| SFT       | 24.54 (0.51) | 16.80 (0.64) | 16.15 (0.15) | 29.29 (0.13) | 27.43 (0.21) |
| KD        | 25.23 (0.44) | 18.90 (1.20) | 16.67 (0.35) | 31.68 (0.22) | 29.36 (0.13) |
| GKD       | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.79 (0.17) |
| DISTILLM  | 28.24 (0.48) | 21.00 (0.72) | 19.12 (0.53) | 37.06 (0.35) | 35.05 (0.13) |
| Ours (ABKD) | 30.24 (0.37) | 22.39 (0.62) | 20.81 (0.42) | 38.51 (0.32) | 38.66 (0.10) |

