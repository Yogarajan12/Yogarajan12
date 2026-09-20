# Yogarajan Sivakumar

**AI/ML Researcher | Mechanistic Interpretability · AI Safety · Uncertainty-Aware and Trustworthy ML**

I’m an AI/ML researcher working on mechanistic interpretability, AI safety and uncertainty-aware machine learning, with a background in high-stakes clinical and biomedical ML.

I’m especially interested in a question that keeps recurring across my work: **when does an apparently interpretable pattern reflect a real mechanism rather than merely a useful correlation?** Working with ICU clinicians made the practical side of that question concrete to me: predictive performance is not enough if we cannot tell when a model should be distrusted, deferred to a human, or safely overruled.

## Current research

### ICU Extubation Outcomes & Length-of-Stay Prediction — NUS × Singapore General Hospital

I am continuing a research collaboration with professors at the National University of Singapore and clinicians at Singapore General Hospital on building statistical machine-learning models for ICU extubation outcomes and length of stay.

The project has grown from an initial predictive-modelling study into a longer-term effort to determine what would make such a system trustworthy enough for real clinical use. Current work focuses on stronger patient-level validation, interpretability, uncertainty and failure-mode analysis, while preserving meaningful clinician oversight. We are working towards publication and eventual clinical deployment.

*Ongoing collaboration; code and manuscript are not yet public.*

### Frontier-Model Cooperation & Steerability — Game Theory & Evolutionary Algorithms

I am continuing a project that began in my Master's course on game theory and evolutionary algorithms at Stevens Institute of Technology, now under the supervision of the professor who taught the course and with the goal of developing it into a research artifact.

The project uses iterated Prisoner’s Dilemma experiments, behavioural strategy classification and evolutionary dynamics to study how frontier language models behave in repeated strategic interactions. I am particularly interested in framing sensitivity, strategic stability and steerability, and what these behaviours may imply for future multi-agent AI systems.

*Work in progress; code and manuscript are not yet public, though some thoughts have been shared on Lesswrong.*

## Selected repositories

### NeuroState: Gradient-Isolated Boundary Learning for Interpretable EEG Transformers

**First-author paper · IEEE MLSP 2026**

NeuroState studies a failure mode in which an auxiliary boundary head inside an EEG transformer collapses to nearly constant outputs during joint training. Across 11 controlled interventions, directional gradient isolation was the only tested intervention that produced clearly non-degenerate boundaries. The optimisation result is the main contribution; the physiological interpretation of the learned boundaries remains deliberately scoped as preliminary.

[Accepted Manuscript](https://github.com/Yogarajan12/neurostate/blob/main/paper/NeuroState__Gradient_Isolated_Boundary_Learning_for_Interpretable_EEG_Transformers.pdf) · [Code](https://github.com/Yogarajan12/neurostate) 

### Uncertainty-Aware Cancer Drug Response Prediction

Built a dual-encoder graph neural network for drug-response prediction across 177K GDSC1 molecular and genomic measurements, reaching Pearson r = 0.909, then added split conformal prediction to produce calibrated prediction intervals rather than point predictions alone.

[Code](https://github.com/Yogarajan12/conformal-drug-response) · [Report](https://github.com/Yogarajan12/conformal-drug-response/blob/main/report/)

### Diffusion-Based Uncertainty for Fetal Ultrasound

Tested whether diffusion reconstruction error could identify medical-image cases a classifier should defer rather than answer confidently. The proposed signal supported selective prediction, but performed poorly on important comparative and out-of-distribution tests; that negative result became part of the conclusion rather than something to hide.

[Code](https://github.com/Yogarajan12/quality-gated-fetal-ultrasound) · [Report](https://github.com/Yogarajan12/quality-gated-fetal-ultrasound/blob/main/report/)

## Recent research

### Mechanistic Interpretability of Reasoning Models

Completed an empirical mechanistic-interpretability project in September 2026 studying representation geometry, reasoning-versus-answer activations, measurement validity and causal interventions in reasoning-distilled language models.

A manuscript from this work is currently under double-blind workshop review. 

## Collaborative research

### RLHFless

Co-authored work on serverless infrastructure for reinforcement learning from human feedback, aimed at reducing redundant compute and improving the efficiency of preference-training experiments. My contribution formed part of a broader collaborative systems effort.

[Paper — arXiv:2602.22718](https://arxiv.org/abs/2602.22718)

## Other work

- **Auditing Model Interpretability and Robustness** — compared statistical and deep-learning models across clinical tasks using SHAP, Grad-CAM, attention analysis and targeted model editing to examine where explanation methods are informative and where they can mislead.
- **Calibrated clinical scheduling** — combined no-show prediction with cost-aware overbooking and fairness analysis.
- **Multivariate gait modelling** — compared classical and deep sequence models for interpretable biomechanical analysis.
- **Manufacturing anomaly detection & data quality** — developed confident-learning and anomaly-detection pipelines for semiconductor sensor data at Infineon Technologies.

## Background

**M.S. Computer Engineering, AI Specialisation**  
Stevens Institute of Technology, 2026 · Provost Scholarship

**B.Eng. Electrical Engineering (Honours)**  
National University of Singapore, 2024

Previous research and industry roles include **LLM Researcher** at the Algoverse AI Research Program, **AI Research Fellow** at the Stevens Institute for Artificial Intelligence and Research, **Research Assistant** at the National University of Singapore, and **Machine Learning & Data Analytics Intern** at Infineon Technologies.
