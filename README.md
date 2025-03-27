\begin{table*}[t]
\centering
% \vspace{-6pt} 
\caption{ROUGE-L scores \textbf{(↑)} for \textbf{\textit{OpenLLaMA2-3B}} across five task-agnostic instruction-following datasets, with \textbf{\textit{OpenLLaMA2-7B}} serving as the teacher model.}
\label{instruction-following performances}
\resizebox{0.85\textwidth}{!}{
\begin{tabular}{l|ccccc}
\toprule
\textbf{Method} & \textbf{Dolly Eval } & \textbf{Self-Instruct} & \textbf{Vicuna Eval } & \textbf{Super-Natural } & \textbf{Unnatural } \\
% \midrule
% GPT-2 XL (Teacher) & 26.94 (0.23) & 13.31 (0.63) & 16.23 (0.62) & 24.28 (0.43) & 29.05 (0.14) \\
\midrule 
SFT & 24.54 (0.51) &  16.80 (0.64) & 16.15 (0.15) & 29.29 (0.13) & 27.43 (0.21) \\
KD  & 25.23 (0.44)  &  18.90 (1.20) &  16.67 (0.35) &  31.68 (0.22) & 29.36 (0.13) \\
% SeqKD \cite{DBLP:journals/corr/KimR16a} &  \\
% MiniLLM  \cite{gu2024minillm} & \\
GKD   &  26.28 (0.43) & 18.84 (0.66) & 17.81 (0.38) & 30.92 (0.12) &  29.79 (0.17) \\
DISTILLM  &  28.24 (0.48) & 21.00 (0.72) & 19.12 (0.53) & 37.06 (0.35) &  35.05 (0.13) \\
Ours (ABKD) & 29.54 (0.37) & 21.39 (0.62) & 19.81 (0.42) & 37.51 (0.32)  & 37.66 (0.10) \\
\bottomrule
\end{tabular}
}
\end{table*}
