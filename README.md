[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000274-blue)](https://doi.org/10.82901/nemar.nm000274)

# BEETL Competition 2021 Motor Imagery Dataset B — transfer learning benchmark

## Overview

Beetl2021-B is a preprocessed EEG dataset from the NeurIPS 2021 BEETL competition focused on transfer learning for motor imagery decoding. The dataset contains 32-channel EEG recordings from 2 healthy subjects performing 4-class motor imagery tasks (left hand, right hand, feet, and rest) sampled at 200 Hz. Designed to address the critical challenge of cross-subject and cross-dataset generalization in brain-computer interfaces, this dataset supports benchmarking of transfer learning and domain adaptation algorithms for motor imagery classification.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 2 |
| Channels | 32 |
| Classes | 4 |
| Trial length | 4 s |
| Sampling frequency | 200 Hz |
| Sessions | 1 |
| Total trials | 1590 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data acquired at 200 Hz sampling rate using 32 channels positioned around the motor cortex (standard 1005 montage). Online bandpass filtering (1-100 Hz) applied during acquisition. Data preprocessed with frequency-domain bandpass filtering (1-100 Hz) and organized into 4-second trials. Motor imagery paradigm with visual cues for four classes: left hand, right hand, feet, and rest. Block-wise 5-fold cross-validation employed for evaluation with cross-subject and cross-dataset assessment.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Beetl2021_B
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Beetl2021_B()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Beetl2021_B.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.48550/arXiv.2202.12950](https://doi.org/10.48550/arXiv.2202.12950)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
