# writings

A collection of academic work I'm proud of — theses, projects, and papers spanning machine learning, quantitative finance, operations research, sports analytics, and quantum computing. Written during my time at the Norwegian School of Economics (NHH) and the University of Oslo (UiO).

---

## Contents

### [BAN-THE — Exploiting the Index Effect on OSEBX using Machine Learning](./BANTHE%20-%20Exploiting%20the%20Index%20Effect%20on%20OSEBX%20using%20Machine%20Learning.pdf)
> Master's thesis · Norwegian School of Economics (NHH) · Autumn 2023 · with Arne Jordåen

The Oslo Stock Exchange Benchmark Index (OSEBX) rebalances its composition periodically — and when stocks enter or leave an index, their prices move predictably. This thesis asks: can we exploit that? Using XGBoost and Generalized Linear Models (GLM), we predict index additions and deletions up to 100 days in advance with >94% accuracy, then build active trading portfolios around those predictions. The best GLM portfolio outperformed the OSEBX by **0.95% per month (11.4% annualised)**, with significant alpha surviving Fama-French 3-factor risk adjustment. The thesis covers the full pipeline — from the theoretical index effect literature, through ML model development, to portfolio backtesting over 2010–2022.

---

### [BAN401 Project 2 — Applied Programming and Data Analysis for Business](./BAN401%20Project%202.pdf)
> Applied Programming and Data Analysis for Business (BAN401) · Norwegian School of Economics (NHH) · Autumn 2023

A multi-part business-analytics assignment combining Python, R, and SQL. The headline component is a written piece on the use of Python in the healthcare sector — covering data collection, preprocessing, prediction, classification, and decision-making, with case studies on Amazon Comprehend Medical (cancer screening), AiCure (treatment adherence), Qventus (operational efficiency), and Paige (cancer diagnostics). The remaining problems work through Python and R coding exercises and design a relational database from scratch, including ER-modelling, SQL DDL, table relationships, and seed data.

---

### [BAN402 Project 1 — Decision Modelling in Business](./BAN402%20Project%201.pdf)
> Decision Modelling in Business (BAN402) · Norwegian School of Economics (NHH) · Autumn 2023

The first of three optimization projects, focused on linear programming in **AMPL** with the CPLEX solver. Across four parts we formulate LP models from business descriptions, analyse binding versus non-binding constraints in optimal solutions, and probe sensitivity and infeasibility. Each part starts from a written problem definition and ends with a working `.mod`/`.dat` formulation and an interpretation of the solver output.

---

### [BAN402 Project 2 — Decision Modelling in Business](./BAN402%20Project%202.pdf)
> Decision Modelling in Business (BAN402) · Norwegian School of Economics (NHH) · Autumn 2023

The second BAN402 project moves from pure LP into model selection and **mixed-integer linear programming**. Part A picks the right formulation from a menu of 11 candidate models (Set Covering, Facility Location, etc.) and reasons about feasibility. Part B works through model modifications to handle constraints tailored to specific characters in the problem narrative (Nils, Lisa, Abel). Parts C and D build MILP models for a refinery-style production problem — crude-oil inventory, saleable-product demand, an emergency-score objective — and analyse what changes when the situation does.

---

### [BAN402 Project 3 — Decision Modelling in Business](./BAN402%20Project%203.pdf)
> Decision Modelling in Business (BAN402) · Norwegian School of Economics (NHH) · Autumn 2023

The final BAN402 project covers three applied OR problems. Part A fits a **Holt linear (double-exponential) smoothing forecast** by optimising MAPE directly as the AMPL objective, jointly recovering γ and β; the model is then used to forecast Q1 2023. Part B is an organ-transplant location problem with fairness constraints on the number of transplant centres per district. Part C is a day-ahead electricity-market problem: building supply/demand curves, choosing system prices, and picking the most profitable block bid. Part D rounds it out with a smaller modelling exercise.

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

### [Quant Awards — Exploiting the Index Effect on the Oslo Stock Exchange Benchmark Index using Machine Learning](./Quant%20Awards%20-%20Egil%20Furnes%20-%20Norwegian%20School%20of%20Economics.pdf)
> Working paper · Norwegian School of Economics (NHH) · 2025

A condensed, paper-length successor to the master's thesis above, reframed around a sharper thesis: in benchmark-event trading, the most accurate classifier is not the most useful one. A naive persistence model scores 95.1% accuracy but predicts zero trades. The paper introduces a **conditional posterior-probability threshold** that deliberately trades a little accuracy for more actionable signal, applied to logistic GLM and XGBoost classifiers using only OSEBX rule-book inputs (turnover, free float, sector, lagged membership). Out-of-sample AUROC exceeds 0.97 across 26 rebalancing events from 2010–2023, and the resulting long–short overlays generate significant Fama–French three-factor alpha — with the XGBoost variant remaining significant even when squeezed into a 2% tracking-error enhanced-index sleeve.

---

## About

These are projects I worked on and am proud of. The machine learning work spans finance, physics, and football. The operations-research and business-analytics work covers LP/MILP modelling, forecasting, and database design. The quantum computing work gets into territory I genuinely find fascinating. Everything is written in Python unless noted otherwise (BAN402 uses AMPL/CPLEX; BAN401 mixes Python, R, and SQL).

If any of it is useful to you, great.
