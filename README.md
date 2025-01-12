# Adversarial Attacks on Intrusion Detection Systems (IDS) Using CounterfactualGAN

This repository implements **black-box adversarial attacks** to mislead an Intrusion Detection System (IDS). It includes:

- **HopSkipJump**, **ZOO**, and **SignOPT** black-box attacks.
- Use of **CounterfactualGAN** to generate targeted adversarial perturbations.
- **Explainability** of adversarial examples using LIME/SHAP to identify influential features.

---

## Key Features

1. **CounterfactualGAN**: A GAN-based model to craft adversarial perturbations for targeted misclassification.
2. **Black-Box Attacks**: Implementation of HopSkipJump, ZOO, and SignOPT attacks with and without CounterfactualGAN.
3. **Explainability**: Visualize and interpret feature importance of adversarial examples.
4. **Performance Metrics**:
   - **Attack Success Rate**
   - **Query Efficiency**
   - **Perturbation Magnitude**

---

## Prerequisites

1. Python 3.8+
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
CFGANAdvGit/
├── data_for_comparison.zip     # Comparison datasets for adversarial examples
├── model_for_comparison.sav    # Pre-trained IDS model for comparison
├── hsja_for_comparison.sav     # Pre-trained HSJA attack results for comparison
├── signopt_for_comparison.sav  # Pre-trained SignOPT attack results for comparison
├── zoo_for_comparison.sav      # Pre-trained ZOO attack results for comparison
├── web_attacks_rf.model        # Trained Random Forest IDS model
├── web_attacks_libsvm_normalized.train  # Training data (normalized)
├── web_attacks_libsvm_normalized.test   # Test data (normalized)
├── web_attacks_balanced.csv    # Web attack dataset (balanced version)
├── adv_examples_inf/           # Directory containing adversarial examples (infinite perturbations)
├── adv_examples_1/             # Directory containing adversarial examples set 1
├── adv_examples_2/             # Directory containing adversarial examples set 2
├── CFGANresults.zip            # Results from the CounterfactualGAN attack
├── predicted_probabilities_adversarial_example.txt  # Predicted probabilities for adversarial examples
├── predicted_probabilities_original_example.txt     # Predicted probabilities for original examples
├── dataset.zip                # Raw dataset
└── .config                    # Configuration files for training and attacks


python train_ids.py
