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

## Execution Guide
### 1. Run Cells 1-10

Execute all cells from **Cell 1** to **Cell 10** sequentially.

### 2. Run Cell 11 (Main Execution)

When running **Cell 11**, you will be prompted to select an experiment:

| Option | Experiment |
|--------|------------|
| [1] | Main Comparison (ViT vs ResNet) |
| [2] | Ablation Study |
| [3] | Attention Analysis |
| [4] | Run all (may take a long time) |

**For example:**

Enter choice (1-4): 2

Enter shots per class (default=10): 10


### 3. Visualization Modules

After completing the experiments, run the following visualization modules:

#### 3.1 Best Validation Accuracy Module

Fill in the `accuracies` list with the **best validation accuracy (%)** for each of the 6 ViT variants from the result of **Experiment 2: Ablation Study**, then compute the **change** (difference) relative to the first variant and run the module.

#### 3.2 Attention Entropy Module

Fill in the `'Entropy'` column with the **average attention entropy values** for each of the 6 ViT variants from the result of **Experiment 3: Attention Analysis**, then run the module.

#### 3.3 Training Process Module

Fill in the **training process data** for all 6 ViT variants from the result of **Experiment 2: Ablation Study**, then run the module.

#### 3.4 Attention Visualization Module

Run the **Attention Visualization** module directly to generate **complete attention matrix numerical values** for all ViT variants, and then use the attention matrix numerical values to create the heatmap.

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
        │   ├── attention_matrices_standard.txt
        │   ├── attention_matrices_no_pos.txt
        │   ├── attention_matrices_fewer_heads.txt
        │   ├── attention_matrices_small_mlp.txt
        │   ├── attention_matrices_deep_mlp.txt
        │   └── attention_matrices_large_patch.txt
        └── heatmap/
            └── figure_all_variants_attention_heatmaps.png
```
