# Attention Fails: Understanding Vision Transformer's Degradation in Low-Data Regimes

## Library Version

| Library | Version |
|---------|---------|
| Python | 3.12.13 |
| torch | 2.10.0+cpu |
| torchvision | 0.25.0+cpu |
| numpy | 2.0.2 |
| matplotlib | 3.10.0 |
| seaborn | 0.13.2 |
| timm | 1.0.25 |
| scikit-learn | 1.6.1 |

CUDA available: False

---

## Project Structure


```
DSAI5207_MDL_Project/
│
├── DSAI5207_MDL_Project.ipynb
│
├── data/	
│   └── cifar-100-python/
│
├── models/
│   ├── vit_standard_n10.pth
│   ├── vit_no_pos_n10.pth
│   ├── vit_fewer_heads_n10.pth
│   ├── vit_small_mlp_n10.pth
│   ├── vit_deep_mlp_n10.pth
│   └── vit_large_patch_n10.pth
│
└── outputs/
    ├── Experiment 1: Main Comparison/
    │   ├── training_curves_vit_tiny_5shots.png
    │   ├── training_curves_vit_tiny_10shots.png
    │   ├── training_curves_resnet18_5shots.png
    │   └── training_curves_resnet18_10shots.png
    │
    ├── Experiment 2: Ablation Study/
    │   ├── ablation_study_results.png
    │   ├── ablation_study_simple.png
    │   ├── all_training_curves.png
    │   ├── summary_table.png
    │   ├── training_curves_standard_n10.png
    │   ├── training_curves_no_pos_n10.png
    │   ├── training_curves_fewer_heads_n10.png
    │   ├── training_curves_small_mlp_n10.png
    │   ├── training_curves_deep_mlp_n10.png
    │   └── training_curves_large_patch_n10.png
    │
    └── Experiment 3: Attention Analysis/
        ├── attention_maps/
        │   ├── attention_maps_standard_n10.png
        │   ├── attention_maps_no_pos_n10.png
        │   ├── attention_maps_fewer_heads_n10.png
        │   ├── attention_maps_small_mlp_n10.png
        │   ├── attention_maps_deep_mlp_n10.png
        │   └── attention_maps_large_patch_n10.png
        │
        ├── layer_entropy/
        │   ├── layer_entropy_standard_n10.png
        │   ├── layer_entropy_no_pos_n10.png
        │   ├── layer_entropy_fewer_heads_n10.png
        │   ├── layer_entropy_small_mlp_n10.png
        │   ├── layer_entropy_deep_mlp_n10.png
        │   └── layer_entropy_large_patch_n10.png
        │
        ├── correlation/
        │   ├── accuracy_vs_entropy.png
        │   ├── layerwise_entropy.png
        │   └── entropy_accuracy_correlation.png
        │
        └── matrices/
            ├── attention_matrices_standard.txt
            ├── attention_matrices_no_pos.txt
            ├── attention_matrices_fewer_heads.txt
            ├── attention_matrices_small_mlp.txt
            ├── attention_matrices_deep_mlp.txt
            └── attention_matrices_large_patch.txt

```
