
## Overview

This repository contains the code and documentation for a research project on **classifying Peripheral Blood Smear (PBS) images of Acute Lymphoblastic Leukemia (ALL)** using **Vision Transformers (ViT)**. The project focuses on **model explainability** and **privacy-preserving collaborative training** through **Federated Learning**.

Key features of this project:

* Fine-tuning **Vision Transformer (ViT-B/16)** for ALL image classification.
* **Explainable AI (XAI)** using:

  * **Attention Rollout** – for global interpretability of ViT attention maps.
  * **LIME** – for local interpretability on individual image predictions.
* **Federated Learning (Flower framework)** to simulate multi-institutional training while preserving patient privacy.
* Non-IID data distribution to mimic real-world heterogeneity across hospitals.



## Federated Learning Setup

* **Framework**: Flower
* **Clients**: 4 simulated hospitals
* **Model**: ViT-B/16 (pretrained on ImageNet)
* **Data distribution**: Non-IID to reflect real-world heterogeneity
* **Aggregator**: FedAvg to combine client updates into a global model

---

## Explainability Methods

| Method            | Type       | Purpose                                              |
| ----------------- | ---------- | ---------------------------------------------------- |
| Attention Rollout | Global XAI | Visualizes which patches the ViT focuses on overall. |
| LIME              | Local XAI  | Explains individual predictions on specific images.  |

---

## Results

* Achieved high classification accuracy on ALL vs Healthy PBS images.
* Attention maps highlight clinically relevant regions in PBS images.
* Federated learning maintains performance while ensuring **data privacy**.

---

## Contributing

Contributions are welcome!

* Fork the repository
* Create a feature branch (`git checkout -b feature-name`)
* Commit your changes (`git commit -m 'Add feature'`)
* Push to the branch (`git push origin feature-name`)
* Open a Pull Request

---

## References

1. Dosovitskiy et al., “An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale,” 2020.
2. T. Lin et al., “Attention Rollout: A Method for Transformer Interpretability.”
3. Ribeiro et al., “Why Should I Trust You? Explaining the Predictions of Any Classifier,” 2016.
4. Beutel et al., “Flower: A Friendly Federated Learning Framework.”

