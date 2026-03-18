# writings

A collection of academic work I'm proud of — theses, projects, and papers spanning machine learning, quantitative finance, sports analytics, and quantum computing. Written during my time at the Norwegian School of Economics (NHH) and the University of Oslo (UiO).

---

## Contents

### [BAN-THE — Exploiting the Index Effect on OSEBX using Machine Learning](./BANTHE%20-%20Exploiting%20the%20Index%20Effect%20on%20OSEBX%20using%20Machine%20Learning.pdf)
> Master's thesis · Norwegian School of Economics (NHH) · Autumn 2023 · with Arne Jordåen

The Oslo Stock Exchange Benchmark Index (OSEBX) rebalances its composition periodically — and when stocks enter or leave an index, their prices move predictably. This thesis asks: can we exploit that? Using XGBoost and Generalized Linear Models (GLM), we predict index additions and deletions up to 100 days in advance with >94% accuracy, then build active trading portfolios around those predictions. The best GLM portfolio outperformed the OSEBX by **0.95% per month (11.4% annualised)**, with significant alpha surviving Fama-French 3-factor risk adjustment. The thesis covers the full pipeline — from the theoretical index effect literature, through ML model development, to portfolio backtesting over 2010–2022.

---

### [FYS-STK3155 Project 1 — The Great Regression](./FYS-STK3155%20PROJECT%201%20-%20The%20Great%20Regression.pdf)
> Applied Data Analysis and Machine Learning (FYS-STK3155) · University of Oslo · with Bror Johannes Tidemand Ruud & Adne Rolstad

A deep dive into regression methods and the bias-variance tradeoff. We approximate the notoriously tricky Runge function using Ordinary Least Squares, Ridge, and LASSO regression across polynomial degrees 1–20, then benchmark five gradient descent variants (standard GD, momentum, AdaGrad, RMSProp, and ADAM). ADAM wins. LASSO with degree 10 hits an MSE of 0.0028. Regularisation is shown to be essential for taming polynomial overfitting, and the theoretical derivations are worked out alongside the numerical experiments.

---

### [FYS-STK3155 Project 2 — Neural Networking](./FYS-STK3155%20PROJECT%202%20-%20NEURAL%20NETWORKING.pdf)
> Applied Data Analysis and Machine Learning (FYS-STK3155) · University of Oslo · with Bror Johannes Tidemand Ruud & Adne Rolstad

We build feed-forward neural networks from scratch — no PyTorch shortcuts — and benchmark them on regression (Runge function) and classification (FashionMNIST). The custom FFNN achieves an MSE of **2.96 × 10⁻⁶** on the Runge function, blowing Ridge regression's 1.90 × 10⁻³ out of the water, and reaches 89.5% accuracy on FashionMNIST. We also implement RNNs with LSTM and GRU layers, comparing activation functions (Leaky ReLU beats sigmoid and ReLU), optimisers (ADAM at η = 0.01 is the pick), and regularisation strategies across architectures.

---

### [FYS-STK3155 Project 3 — Predicting Footballer Market Value using Machine Learning](./FYS-STK3155%20PROJECT%203%20-%20Predicting%20Footballer%20Market%20Value%20using%20Machine%20Learning.pdf)
> Applied Data Analysis and Machine Learning (FYS-STK3155) · University of Oslo · with Bror Johannes Tidemand Ruud & Adne Rolstad

Can you put a number on Haaland? This project uses a Transfermarkt dataset of 278,558 player-valuation instances to predict footballer market values using Ridge regression, FFNNs, and recurrent networks (LSTM/GRU). The jump from static to temporal modelling is dramatic: Ridge regression tops out at R² = 0.51, while LSTM/GRU architectures hit **R² ≈ 0.976** with an RMSE of ~€245k. As a fun stress test, the best model was used to predict the starting lineups for the 2024 UEFA Champions League Final.

---

### [FYS5419 Project 1 — A VQE Study of the Lipkin Interaction](./FYS5419%20PROJECT%201%20-%20A%20VQE%20Study%20of%20the%20Lipkin%20Interaction.pdf)
> Quantum Computing and Quantum Machine Learning (FYS5419) · University of Oslo

The Variational Quantum Eigensolver (VQE) is one of the most promising near-term quantum algorithms. This project applies it to the Lipkin-Meshkov-Glick (LMG) model — a classic many-body quantum system — to find ground-state energies of increasingly complex systems (N = 2 and N = 4 fermions). Starting from single-qubit Bell state entanglement and working up through avoided crossings and phase transitions, VQE results are compared against exact diagonalisation. Agreement is excellent for smaller systems (error ~10⁻¹¹), with residual error growing for N = 4 due to the more complex optimization landscape. Implemented in PennyLane and Qiskit.

---

## About

These are projects I worked on and am proud of. The machine learning work spans finance, physics, and football. The quantum computing work gets into territory I genuinely find fascinating. Everything is written in Python unless noted otherwise.

If any of it is useful to you, great.
