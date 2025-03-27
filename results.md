**Table 1: Effects of our framework using different SGO strategies (*i.e.*, On-policy (from MINILLM), Mixed (from GKD), and Adaptive Off-policy (from DISTILLM)). "Fixed" denotes that our framework uses only the original dataset for training without augmentation.**

| **Method** | **Dolly Eval** | **Self-Instruct** | **Vicuna Eval** | **Super-Natural** | **Unnatural** |
|------------|--------------|----------------|--------------|----------------|------------|
| Prior SOTA result | 25.32 (0.14) | 12.49 (0.56) | 17.30 (0.41) | 23.76 (0.38) | 25.79 (0.08) |
| Fixed (KD) + Ours | 25.65 (0.24) | 13.47 (0.42) | 16.06 (0.25) | 26.47 (0.31) | 29.32 (0.08) |
| On-policy (MiniLLM) + Ours | 25.96 (0.42) | 13.44 (0.37) | 17.32 (0.38) | 26.86 (0.26) | 29.57 (0.13) |
| Mixed (GKD) + Ours | 26.49 (0.23) | 14.62 (0.27) | 17.14 (0.26) | 27.54 (0.44)| 30.98 (0.09) |
| Adaptive Off-policy (DISTILLM) + Ours | 26.58 (0.18)</span> | 14.25 (0.25) | 17.79 (0.35) | 27.79 (0.26) | 31.13 (0.12) |

**Table 2: ROUGE-L scores (↑) for OpenLLaMA2-3B across five task-agnostic instruction-following datasets, with OpenLLaMA2-7B serving as the teacher model.**

| Method    | Dolly Eval | Self-Instruct | Vicuna Eval | Super-Natural | Unnatural |
|-----------|-----------|---------------|-------------|---------------|-----------|
| SFT       | 24.54 (0.51) | 16.80 (0.64) | 16.15 (0.15) | 29.29 (0.13) | 27.43 (0.21) |
| KD        | 25.23 (0.44) | 18.90 (1.20) | 16.67 (0.35) | 31.68 (0.22) | 29.36 (0.13) |
| SeqKD     | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.89 (0.10) |
| GKD       | 26.28 (0.43) | 18.84 (0.66) | 17.81 (0.38) | 30.92 (0.12) | 29.79 (0.17) |
| MINILLM   | 27.74 (0.45) | 20.61 (0.80) | 18.83 (0.40) | 35.31 (0.24) | 33.86 (0.16) |
| DISTILLM  | 28.24 (0.48) | 21.00 (0.72) | 19.12 (0.53) | 37.06 (0.35) | 35.05 (0.13) |
| Ours (ABKD) | 30.25 (0.37) | 22.39 (0.62) | 20.83 (0.42) | 38.51 (0.32) | 38.66 (0.10) |

**Table 3:Training Time Comparison (sec/sample).**

| Method   | Training Time (second/sample) |
|----------|---------------------------|
| SFT      | 0.344                      |
| KD       | 0.649                      |
| SeqKD    | 0.744                      |
| MiniLLM  | 4.452                      |
| GKD      | 2.078                      |
| DISTILLM | 1.331                      |
| Ours     | 0.772                      |

<p >
  <img src="https://github.com/user-attachments/assets/f2aedfd6-e79e-4149-ab17-05caae209cea" alt="dolly" width="500">
</p>

**Figure 2.** Performance of different loss functions on the validation set over the entire training process.

