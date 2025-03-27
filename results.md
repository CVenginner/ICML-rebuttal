**Table 1: ROUGE-L scores (↑) for OpenLLaMA2-3B across five task-agnostic instruction-following datasets, with OpenLLaMA2-7B serving as the teacher model.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| SFT       | 24.54 (0.51) | 16.80 (0.64) | 16.15 (0.15) | 29.29 (0.13) | 27.43 (0.21) |
| KD        | 25.23 (0.44) | 18.90 (1.20) | 16.67 (0.35) | 31.68 (0.22) | 29.36 (0.13) |
| SeqKD     | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.89 (0.10) |
| GKD       | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.79 (0.17) |
| MINILLM   | 27.74 (0.45) | 20.61 (0.80) | 18.83 (0.40) | 35.31 (0.24) | 33.86 (0.16) |
| DISTILLM  | 28.24 (0.48) | 21.00 (0.72) | 19.12 (0.53) | 37.06 (0.35) | 35.05 (0.13) |
| Ours (ABKD) | 30.25 (0.37) | 22.39 (0.62) | 20.83 (0.42) | 38.51 (0.32) | 38.66 (0.10) |


## Table: Effects of Our Framework Using Different SGO Strategies

**Caption:** Effects of our framework using different SGO strategies (*i.e.*, On-policy, Mixed, and Adaptive Off-policy). "Fixed" denotes that our framework uses only the original dataset for training without augmentation. Following [Ko et al., 2024](#), in the mixed strategy, we apply the on-policy optimization method with a probability of 0.5. Otherwise, we sample from the fixed dataset.

**Table:**

| **Method** | **Dolly Eval** | **Self-Instruct** | **Vicuna Eval** | **Super-Natural** | **Unnatural** |
|------------|--------------|----------------|--------------|----------------|------------|
| **Prior SOTA result** | 25.32 (0.14) | 12.49 (0.56) | 17.30 (0.41) | 23.76 (0.38) | 25.79 (0.08) |
| **Fixed (KD) + Ours** | 25.65 (0.24) | 13.47 (0.42) | 16.06 (0.25) | 26.47 (0.31) | 29.32 (0.08) |
| **On-policy (MiniLLM) + Ours** | 25.96 (0.42) | 13.44 (0.37) | <span style="background-color:#EAF1F9">17.32 (0.38)</span> | 26.86 (0.26) | 29.57 (0.13) |
| **Mixed (GKD) + Ours** | <span style="background-color:#EAF1F9">26.49 (0.23)</span> | <span style="background-color:#C0D6EC"><strong>14.62</strong> (0.27)</span> | 17.14 (0.26) | <span style="background-color:#EAF1F9">27.54 (0.44)</span> | <span style="background-color:#EAF1F9">30.98 (0.09)</span> |
| **Adaptive Off-policy (DISTILLM) + Ours** | <span style="background-color:#C0D6EC"><strong>26.58</strong> (0.18)</span> | <span style="background-color:#EAF1F9">14.25 (0.25)</span> | <span style="background-color:#C0D6EC"><strong>17.79</strong> (0.35)</span> | <span style="background-color:#C0D6EC"><strong>27.79</strong> (0.26)</span> | <span style="background-color:#C0D6EC"><strong>31.13</strong> (0.12)</span> |

