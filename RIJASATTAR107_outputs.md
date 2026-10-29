# RIJASATTAR107 — Outputs

## Output 1

```
Roll number: 107
Random seed: 7
HOG cell size: (16, 16)
SIFT grid: 6 x 6
Expected HOG features: 1764
Expected SIFT features: 4608
```

## Output 2

```

Training image shape: (400, 128, 128)
Training label shape: (400,)
Class counts: {'Eosinophil': 100, 'Monocyte': 100, 'Neutrophil': 100, 'Platelet': 100}

Validation image shape: (120, 128, 128)
Validation label shape: (120,)
Class counts: {'Eosinophil': 30, 'Monocyte': 30, 'Neutrophil': 30, 'Platelet': 30}

Test image shape: (120, 128, 128)
Test label shape: (120,)
Class counts: {'Eosinophil': 30, 'Monocyte': 30, 'Neutrophil': 30, 'Platelet': 30}
```

![Output 2](outputs_images/output_2_1.png)

## Output 3

```
Training HOG shape: (400, 1764)
Validation HOG shape: (120, 1764)
HOG feature length: 1764

HOG hand calculation:
Cells per direction: 8
Blocks per direction: 7
Features per block: 36
Total features: 1764
```

![Output 3](outputs_images/output_3_2.png)

```
      C  Validation accuracy  Validation macro-F1
0   0.1             0.766667              0.75871
1   1.0             0.766667              0.75871
2  10.0             0.766667              0.75871
```

```
Selected C: 0.1
HOG validation accuracy: 0.7666666666666667
HOG validation macro-F1: 0.7587100213219616
```

![Output 3](outputs_images/output_3_3.png)

## Output 4

```
Average keypoints: 73.605
Minimum keypoints: 11
Maximum keypoints: 179
Images with zero keypoints: 0
```

![Output 4](outputs_images/output_4_4.png)

```
Normal SIFT produces variable-length features because different images can have different numbers of keypoints.
Training SIFT shape: (400, 4608)
Validation SIFT shape: (120, 4608)
SIFT feature length: 4608
Hand calculation: 6 x 6 = 36 grid points
Total features: 36 x 128 = 4608
```

```
      C  Validation accuracy  Validation macro-F1
0   0.1             0.708333             0.697227
1   1.0             0.700000             0.690255
2  10.0             0.700000             0.690255
```

```
Selected C: 0.1
SIFT validation accuracy: 0.7083333333333334
SIFT validation macro-F1: 0.6972273394920168
```

![Output 4](outputs_images/output_4_5.png)

## Output 5

```
Q4: Test-set robustness results
```

```
        Model           Condition  Accuracy  Macro-F1
0   HOG + SVM               Clean    0.7500    0.7527
1   HOG + SVM  Rotated 20 degrees    0.6750    0.6666
2   HOG + SVM      Gaussian noise    0.3333    0.2551
3  SIFT + SVM               Clean    0.6917    0.6895
4  SIFT + SVM  Rotated 20 degrees    0.6583    0.6548
5  SIFT + SVM      Gaussian noise    0.6833    0.6792
```

```
Accuracy comparison
```

```
Condition    Clean  Gaussian noise  Rotated 20 degrees
Model                                                 
HOG + SVM   0.7500          0.3333              0.6750
SIFT + SVM  0.6917          0.6833              0.6583
```

![Output 5](outputs_images/output_5_6.png)

```

Accuracy drop under Rotated 20 degrees:
Model
HOG + SVM     0.0750
SIFT + SVM    0.0333
dtype: float64

Accuracy drop under Gaussian noise:
Model
HOG + SVM     0.4167
SIFT + SVM    0.0083
dtype: float64

Use these measured values to decide which model was more robust.
```

## Output 6

```

 HOG + SVM
Clean — most frequent confusion: Monocyte predicted as Eosinophil | count: 9
Rotated 20 degrees — most frequent confusion: Eosinophil predicted as Monocyte | count: 14
Gaussian noise — most frequent confusion: Eosinophil predicted as Monocyte | count: 28

 SIFT + SVM
Clean — most frequent confusion: Eosinophil predicted as Monocyte | count: 12
Rotated 20 degrees — most frequent confusion: Eosinophil predicted as Monocyte | count: 14
Gaussian noise — most frequent confusion: Eosinophil predicted as Monocyte | count: 13
```

## Output 7

```
=======================================================
COMPUTER VISION ASSIGNMENT — ROLL NUMBER 107
=======================================================

Personal settings
Random seed: 7
HOG cell size: (16, 16)
SIFT grid: 6 x 6

Feature lengths
HOG: 1764
SIFT: 4608

Selected hyperparameters
HOG C: 0.1
SIFT C: 0.1

Validation results
HOG accuracy: 0.7667
HOG macro-F1: 0.7587
SIFT accuracy: 0.7083
SIFT macro-F1: 0.6972

Robustness table
```

```
        Model           Condition  Accuracy  Macro-F1
0   HOG + SVM               Clean    0.7500    0.7527
1   HOG + SVM  Rotated 20 degrees    0.6750    0.6666
2   HOG + SVM      Gaussian noise    0.3333    0.2551
3  SIFT + SVM               Clean    0.6917    0.6895
4  SIFT + SVM  Rotated 20 degrees    0.6583    0.6548
5  SIFT + SVM      Gaussian noise    0.6833    0.6792
```

```

Remember to use these actual outputs in your report.
```
