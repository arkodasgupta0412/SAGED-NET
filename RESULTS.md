# Experimental Results: SAGED-Net

## TABLE I: Performance Comparison
Performance comparison on TNBC, CPM-15, CPM-17, and PanNuke using DSC, AJI, Precision, and Recall. Values for proposed method are reported as Mean ± Standard Deviation for TNBC, CPM-15 and CPM-17 and only Mean for PanNuke.

### TNBC
| Model | DSC | AJI | Precision | Recall |
| :--- | :--- | :--- | :--- | :--- |
| Roy et al. | 0.8165 | 0.6918 | - | - |
| Kang et al. | 0.8290 | 0.6110 | 0.8260 | 0.8330 |
| Mahmood et al. | 0.8441 | 0.7332 | 0.8352 | 0.8306 |
| Guan et al. | 0.8500 | 0.6920 | - | - |
| Firat et al. | 0.9075 | 0.8381 | 0.9035 | 0.9115 |
| HI-Net | 0.8242 | 0.7468 | 0.8359 | 0.8521 |
| **SAGED-Net (Ours)** | **0.9103 ± 0.0050** | **0.8431 ± 0.0076** | **0.8325 ± 0.0174** | **0.8522 ± 0.0268** |

### CPM-15
| Model | DSC | AJI | Precision | Recall |
| :--- | :--- | :--- | :--- | :--- |
| Lin et al. | 0.7513 | 0.5454 | - | - |
| Mahbod et al. | 0.7570 | 0.5460 | - | - |
| Lin et al. | 0.8070 | 0.6800 | - | - |
| U-Net | 0.7427 | 0.5940 | 0.6834 | 0.8293 |
| U-Net++ | 0.7542 | 0.6073 | 0.6993 | 0.8290 |
| HI-Net | 0.8480 | 0.7406 | 0.8962 | 0.8246 |
| **SAGED-Net (Ours)** | **0.9286 ± 0.0147** | **0.8711 ± 0.0244** | **0.8659 ± 0.0224** | **0.8950 ± 0.0310** |

### CPM-17
| Model | DSC | AJI | Precision | Recall |
| :--- | :--- | :--- | :--- | :--- |
| Lin et al. | 0.8390 | 0.7250 | - | - |
| Li et al. | 0.8660 | 0.7010 | - | - |
| Chen et al. | 0.8740 | 0.7220 | - | - |
| Chen et al. | 0.8950 | 0.7210 | - | - |
| Zhao et al. | 0.8990 | 0.7910 | - | - |
| HI-Net | 0.8894 | 0.7953 | 0.8692 | 0.8954 |
| **SAGED-Net (Ours)** | **0.9057 ± 0.0030** | **0.8328 ± 0.0048** | **0.8317 ± 0.0128** | **0.8720 ± 0.0135** |

### PanNuke
| Model | DSC | AJI | Precision | Recall |
| :--- | :--- | :--- | :--- | :--- |
| Liu et al. | 0.8325 | 0.7425 | 0.8192 | 0.8675 |
| Fan et al. | 0.8346 | 0.7909 | - | - |
| Tang et al. | 0.8350 | 0.7185 | - | - |
| Youssef et al. | 0.8760 ± 0.0046 | 0.8261 ± 0.0044 | - | 0.8891 ± 0.0030 |
| DeepLabV3+ | 0.8353 ± 0.0068 | 0.7795 ± 0.0079 | - | 0.8653 ± 0.0031 |
| HI-Net | 0.8867 | 0.7773 | 0.8293 | 0.8490 |
| **SAGED-Net (Ours)** | **0.9058** | **0.8339** | **0.9053** | **0.9062** |

<br>

## TABLE II: Ablation Study
Ablation Study of Loss Function Components across TNBC, CPM-15, CPM-17, and PanNuke. Values for proposed method are reported as Mean ± Standard Deviation for TNBC, CPM-15 and CPM-17 and only Mean for PanNuke.

| Loss Function Components | TNBC (DSC) | TNBC (AJI) | CPM-15 (DSC) | CPM-15 (AJI) | CPM-17 (DSC) | CPM-17 (AJI) | PanNuke (DSC) | PanNuke (AJI) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| ℒ<sub>spec</sub> | 0.8714 ± 0.0043 | 0.7860 ± 0.0060 | 0.8692 ± 0.0066 | 0.7808 ± 0.0091 | 0.8880 ± 0.0025 | 0.8051 ± 0.0038 | 0.8910 | 0.8114 |
| ℒ<sub>morph</sub> | 0.8976 ± 0.0058 | 0.8239 ± 0.0085 | 0.9068 ± 0.0081 | 0.8359 ± 0.0127 | 0.9035 ± 0.0024 | 0.8292 ± 0.0038 | 0.9003 | 0.8309 |
| ℒ<sub>spec</sub> + ℒ<sub>morph</sub> | 0.9067 ± 0.0051 | 0.8375 ± 0.0077 | 0.9074 ± 0.0066 | 0.8368 ± 0.0103 | 0.8987 ± 0.0050 | 0.8218 ± 0.0078 | 0.9058 | 0.8338 |
| **ℒ<sub>spatial</sub> + ℒ<sub>spec</sub> + ℒ<sub>morph</sub>** | **0.9103 ± 0.0050** | **0.8431 ± 0.0076** | **0.9286 ± 0.0147** | **0.8711 ± 0.0244** | **0.9057 ± 0.0030** | **0.8328 ± 0.0048** | **0.9058** | **0.8339** |

<br>

## TABLE III: Model Complexity
Comparison of Model Complexity (Trainable Parameters).

| Model | Parameters (M) |
| :--- | :--- |
| HI-Net | ~6.9 |
| U-Net | ~31.03 |
| Attention U-Net | ~34.87 |
| U-Net++ | ~36.63 |
| DeepLabV3+ (ResNet50) | ~40.35 |
| SAM (ViT-B) | ~91.00 |
| TransUNet | ~105.28 |
| **SAGED-Net (Ours)** | **3.79** |
