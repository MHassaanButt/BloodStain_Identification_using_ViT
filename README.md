# Hybrid Vision Transformer for Hyperspectral Imaging-based Bloodstain Classification

Hyperspectral Imaging (HSI) has recently gained attention in forensic science, particularly in bloodstain identification. Accurate recognition of bloodstains is crucial, especially when substances like ketchup or artificial blood resemble real bloodstains. Conventional chemical methods can compromise DNA analysis. In this study, we employ HSI as a non-destructive method for bloodstain detection. We introduce the hybrid-ViT model, combining 3D-CNN and Vision Transformer (ViT) capabilities. Positional encoding captures spatial information effectively. Our model outperforms state-of-the-art models with an F1-score of 0.99 on the hyper-blood dataset. This work highlights HSI and ViT's potential in forensic science for complex bloodstain identification scenarios.
This repository contains the code for the Hybrid Vision Transformer (hybrid-ViT) model, as well as the evaluation results on the Hyperblood dataset.


## Dataset

We conducted our experiments using the Hyperblood dataset, which can be accessed [here](https://zenodo.org/record/3984905).

## Model Comparison

We compared the performance of our hybrid-ViT model with five state-of-the-art models for bloodstain classification:

- **2D CNN** 
- **2D Inception (2D IN)** 
- **Hybrid CNN** 
- **Fast and Compact 3D CNN (FC3DCNN)**
- hybird-ViT (our proposed)

Our model, hybrid-ViT, outperformed these models in terms of F1-score, achieving the highest accuracy in bloodstain identification.

### Results

Here is a table summarizing the class-wise F1-scores and other performance metrics:

```plaintext
+----------------------+-----------+---------+--------------+----------+--------------+
| Classes              | 2D CNN    | 2D IN   | Hybrid CNN   | FC3DCNN  | hybrid-ViT   |
+----------------------+-----------+---------+--------------+----------+--------------+
| blood                | 0         | 98      | 98           | 94       | 99           |
| ketchup              | 60        | 99      | 95           | 94       | 99           |
| artificial blood     | 46        | 91      | 87           | 90       | 92           |
| poster paint         | 89        | 99      | 100          | 100      | 100          |
| tomato concentrate   | 65        | 92      | 90           | 84       | 96           |
| acrylic paint        | 97        | 96      | 98           | 97       | 98           |
+----------------------+-----------+---------+--------------+----------+--------------+
| Training Time (s)   | 3.40      | 25.80   | 13.34        | 13.55    | 29.52        |
| Test Time (s)       | 1.63      | 11.82   | 7.24         | 7.89     | 8.36         |
| Overall Accuracy     | 69.46     | 95.82   | 94.59        | 94.20    | 97.31        |
| Average Accuracy     | 58.21     | 95.32   | 93.95        | 93.65    | 96.73        |
| Kappa Accuracy       | 61.92     | 94.88   | 93.39        | 92.90    | 96.71        |
+----------------------+-----------+---------+--------------+----------+--------------+
```
### Model Architecture
![hassan_sensors drawio](https://github.com/MHassaanButt/BloodStain_Identification_using_ViT/assets/30599669/b197e874-116d-4f79-8e2e-1a2a66781685)


### Training and Loss Graphs
![latest_E_1_0 9_15_9_PCA_acc_loss_curve_all_models](https://github.com/MHassaanButt/BloodStain_Identification_using_ViT/assets/30599669/72aa67c1-8f5a-4d84-9378-966ea381ee1c)


Citation
If you find this work useful in your research, please consider citing our paper:
```plaintext
@article{your-paper-citation,
  title={Hybrid Vision Transformer for Hyperspectral Imaging-based Bloodstain Classification in Complex Forensic Scenarios},
  author={Your Name},
  journal={Journal of XYZ},
  year={2023},
  volume={1},
  pages={1-10},
  doi={your-doi},
}
```
