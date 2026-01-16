\documentclass{article}
\usepackage{amsmath, amssymb}
\usepackage{geometry}
\geometry{a4paper, margin=1in}

\title{关于素数间隙极限的一个注记}
\author{}
\date{}

\begin{document}

\maketitle

给定常数 $C \geq 0$，考虑是否存在无穷序列 $\{n_i\}$ 使得
\[
\lim_{i \to \infty} \frac{p_{n_i+1} - p_{n_i}}{\log n_i} = C,
\]
其中 $p_n$ 表示第 $n$ 个素数。

\begin{enumerate}
    \item \textbf{当 $C = 0$ 时：} 存在这样的序列。根据张益唐等人的结果，存在无穷多对素数间隙不超过 246。选取这些素数对的索引作为 $\{n_i\}$，则 $p_{n_i+1} - p_{n_i}$ 有界，而 $\log n_i \to \infty$，因此极限为 $0$。

    \item \textbf{当 $C = \infty$ 时：} 存在这样的序列。利用 Westzynthius 定理（或欧几里得构造），存在无穷多个 $n$ 使得 $p_{n+1} - p_n$ 远大于 $\log n$。选取这些 $n$ 作为子序列，可使比值趋于无穷。

    \item \textbf{当 $0 < C < \infty$ 时：} 不存在这样的序列。假设存在，则根据素数定理 $p_n \sim n \log n$，有 $\log n_i \sim \log p_{n_i}$。于是
    \[
    p_{n_i+1} - p_{n_i} \sim C \log p_{n_i}.
    \]
    但已知素数间隙的极限行为满足
    \[
    \liminf_{n \to \infty} \frac{p_{n+1} - p_n}{\log p_n} = 0, \quad 
    \limsup_{n \to \infty} \frac{p_{n+1} - p_n}{\log p_n} = \infty.
    \]
    因此，不可能存在无穷多个素数间隙渐近于 $C \log p_n$（其中 $C$ 为正有限常数）。故不存在满足条件的序列。
\end{enumerate}

综上，仅当 $C = 0$ 或 $C = \infty$ 时存在所需的序列。

\end{document}
