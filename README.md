# Yogarajan Sivakumar

**AI/ML Researcher | Mechanistic and Causal Interpretability · AI Alignment & Safety · Model Evaluation · Uncertainty Quantification and Reliability**

I’m an AI/ML researcher working on mechanistic interpretability, AI alignment and safety, model evaluation, and uncertainty quantification, with a background in trustworthy machine learning for safety-critical clinical and biomedical applications.

Across both frontier-model and medical-AI research, I keep returning to the same problem: **when does an apparently interpretable pattern reflect a real mechanism rather than merely a useful correlation, and when do we know enough about a model to trust it?** Working with ICU clinicians made the practical side of this concrete to me: predictive performance is not enough if we cannot tell when a model should be distrusted, deferred to a human, or safely overruled.

## Current research

### ICU Extubation Outcomes & Length-of-Stay Prediction — NUS × Singapore General Hospital

**First-author work in progress**

I am continuing a research collaboration with professors at the **National University of Singapore** and clinicians at **Singapore General Hospital** on interpretable machine-learning models for successful ICU extubation (whether a patient can remain safely off invasive ventilatory support) and length of stay.

The project has grown from an initial predictive-modelling study into a longer-term effort to determine what would make such a system trustworthy enough for real clinical use. Current work focuses on stronger patient-level validation, interpretability, uncertainty and failure-mode analysis while preserving meaningful clinician oversight. We are working towards **publication and eventual clinical deployment**.

*Ongoing collaboration; code and manuscript are not public yet.*

### Frontier-Model Cooperation & Steerability — Game Theory & Evolutionary Algorithms

**First-author work in progress**

I am continuing a project that began in my Master's course on game theory and evolutionary algorithms at **Stevens Institute of Technology**, now under the supervision of the professor who taught the course and with the goal of developing it towards publication.

The project studies how frontier language models behave in repeated strategic interactions using iterated Prisoner’s Dilemma experiments, behavioural strategy classification and evolutionary dynamics. The question I find most interesting is whether seemingly small differences in model behaviour or prompt framing can become qualitatively different population dynamics once many AI agents interact and are selected on performance, and how that changes the threat profile of multi-agent deployments.

*Work in progress; code and manuscript are not yet public.*

## Repositories

### [NeuroState: Gradient-Isolated Boundary Learning for Interpretable EEG Transformers](https://github.com/Yogarajan12/neurostate)

**First-author paper · IEEE MLSP 2026**

NeuroState asks a reliability question about interpretability itself: **can an auxiliary mechanism appear to train successfully while learning almost nothing?** We found that an EEG transformer's boundary head repeatedly collapsed to near-constant outputs despite the primary task continuing to learn. Across **11 controlled interventions**, directional gradient isolation was the only tested intervention that clearly prevented this collapse.

The optimisation result is the main contribution. The physiological meaning of the resulting boundaries remains deliberately scoped as preliminary rather than being inferred from an interpretable-looking signal alone.

[Accepted Manuscript](https://github.com/Yogarajan12/neurostate/blob/main/paper/NeuroState__Gradient_Isolated_Boundary_Learning_for_Interpretable_EEG_Transformers.pdf) · [Code](https://github.com/Yogarajan12/neurostate)

### [Uncertainty-Aware Cancer Drug Response Prediction](https://github.com/Yogarajan12/conformal-drug-response)

**Course project · Data Acquisition, Modelling and Analysis: Deep Learning**

Built a dual-encoder graph neural network for cancer drug-response prediction across **177K GDSC1 measurements**, reaching Pearson **r = 0.909**. I then used split conformal prediction to turn point estimates into statistically calibrated prediction intervals.

The broader question was one of **reliable self-reporting**: a strong prediction is much more useful in a high-stakes setting if the system can also communicate how much confidence we should place in it.

[Code](https://github.com/Yogarajan12/conformal-drug-response) · [Report](https://github.com/Yogarajan12/conformal-drug-response/blob/main/report/)

### [Diffusion-Based Uncertainty for Fetal Ultrasound](https://github.com/Yogarajan12/quality-gated-fetal-ultrasound)

**Course project · Probabilistic Generative Modelling and Learning**

Built a quality-gated fetal-ultrasound classifier that could **abstain and defer uncertain cases to a human** rather than force a prediction. I tested diffusion reconstruction uncertainty as an independent quality signal alongside classifier confidence.

The most useful result was partly negative: although selective prediction worked, diffusion uncertainty itself ranked classification errors substantially worse than simpler uncertainty baselines and largely failed at out-of-distribution detection. I kept that failure in the conclusion because knowing which confidence signals *not* to trust is part of building a trustworthy deferral system.

[Code](https://github.com/Yogarajan12/quality-gated-fetal-ultrasound) · [Report](https://github.com/Yogarajan12/quality-gated-fetal-ultrasound/blob/main/report/)

### [Calibrated Clinical Scheduling — No-Show Prediction & Overbooking Optimisation](https://github.com/Yogarajan12/clinic-overbooking-optimization)

**Course project · Applied Modelling and Optimization**

Combined patient-specific no-show prediction with a constrained overbooking optimiser, then stress-tested policies for **cost, overflow risk, calibration, distribution shift and subgroup fairness** across more than 8.6M simulated slot outcomes.

One of the more useful lessons was that the lowest-cost policy was not automatically the most patient-centred or fairest, and the predictive model itself exposed a meaningful calibration gap. The project therefore became less about finding a single "optimal" schedule and more about making uncertainty, service-level constraints and fairness explicit in the decision rule.

[Code](https://github.com/Yogarajan12/clinic-overbooking-optimization) · [Report](https://github.com/Yogarajan12/clinic-overbooking-optimization/blob/main/report/project_report.pdf)

### [Interpretable Multivariate Gait Modelling](https://github.com/Yogarajan12/gait-bracing-classification)

**Course project · Pattern Recognition and Classification**

Compared **Random Forests, Hidden Markov Models, attention-based LSTMs and Spatio-Temporal Graph Convolutional Networks** for classifying joint-angle dynamics under different bracing conditions, including subject-level generalisation tests.

Beyond classification performance, I used feature importance, hidden-state structure, gradient-based saliency and temporal attention to ask whether predictions could be related back to recognisable biomechanical patterns; such as which joints and phases of the gait cycle carried the discriminative signal.

[Code](https://github.com/Yogarajan12/gait-bracing-classification) · [Report](https://github.com/Yogarajan12/gait-bracing-classification/blob/main/report/Sivakumar_Yogarajan_CPE646_Project_Report.pdf)

## Recent research

### Mechanistic Interpretability of Reasoning Models

**First-author paper · completed September 2026 · under double-blind workshop review**

Completed an empirical AI alignment and mechanistic-interpretability project testing how much confidence we should place in simple activation-space descriptions of model behaviour.

The work compared independently reconstructed representation directions, reasoning versus final-answer activations, behavioural measurement, predictive adequacy and causal interventions. A recurring lesson was that **reproducibility is not the same thing as mechanism**: a representation can be strikingly stable while still being incomplete or sensitive to how it is constructed.

*The manuscript and identifying repository link are withheld while double-blind review is ongoing.*

## Collaborative research

### [RLHFless: Serverless Computing for Efficient RLHF](https://arxiv.org/abs/2602.22718)

Co-authored work on serverless infrastructure for reinforcement learning from human feedback. RLHFless addresses wasted compute from repeated prefill, changing response lengths and static resource allocation during synchronous RLHF training, achieving up to **1.35× speedup and 44.8% lower cost** in the reported experiments.

My contribution was primarily to the experimental side of the project, running evaluations and validating that the reported results held consistently across the tested settings, during a summer **AI Research Fellowship at the Stevens Institute for Artificial Intelligence and Research**. Now under review for ACM Symposium on Cloud Computing 2026.

[Paper — arXiv:2602.22718](https://arxiv.org/abs/2602.22718)

## Other work

- **Auditing Model Interpretability and Robustness** — compared statistical and deep-learning models across tabular, imaging and language-based clinical tasks using feature attribution, attention analysis and targeted model editing. The central question was when additional model complexity buys enough predictive value to justify the corresponding loss of transparency.

- **Manufacturing Anomaly Detection & Data Quality** — developed confident-learning and Gaussian-mixture anomaly-detection pipelines for semiconductor sensor data at **Infineon Technologies**, treating mislabelling and distribution anomalies as reliability problems rather than noise to average over.

## Background

**M.S. Computer Engineering, AI Specialisation**  
Stevens Institute of Technology, 2026 · Provost Scholarship

**B.Eng. Electrical Engineering (Honours)**  
National University of Singapore, 2024

Previous research and industry roles include the **Algoverse AI Research Program**, an **AI Research Fellowship** at the Stevens Institute for Artificial Intelligence and Research, a **Research Assistantship** at the National University of Singapore's Control, Intelligent Systems & Robotics group, and a **Machine Learning & Data Analytics Internship** at Infineon Technologies.
