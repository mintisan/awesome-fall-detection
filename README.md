# Awesome Fall Detection

![Awesome](https://awesome.re/badge.svg)
[![Contributions](https://img.shields.io/github/issues-pr-closed-raw/mintisan/awesome-fall-detection.svg?label=contributions)](https://github.com/mintisan/awesome-fall-detection/pulls)
[![Commits](https://img.shields.io/github/last-commit/mintisan/awesome-fall-detection.svg?label=last%20contribution)](https://github.com/mintisan/awesome-fall-detection/commits/main)
![GitHub stars](https://img.shields.io/github/stars/mintisan/awesome-fall-detection.svg?style=social)

A curated list of awesome datasets, papers, code repositories, TinyML projects, and engineering resources for wearable and sensor-based fall detection. The list focuses on IMU / accelerometer / gyroscope systems, wrist and chest wearables, public datasets, reproducible baselines, and edge deployment.

## Table of Contents

- [Dataset](#dataset)
  - [Wrist and Multi-Position Datasets](#wrist-and-multi-position-datasets)
  - [Common Benchmark Datasets](#common-benchmark-datasets)
  - [Synthetic and Generated Datasets](#synthetic-and-generated-datasets)
  - [Real-World / Restricted Datasets](#real-world--restricted-datasets)
- [Paper](#paper)
  - [Survey and Evaluation](#survey-and-evaluation)
  - [Dataset Papers](#dataset-papers)
  - [Sampling Rate and Sensor Placement](#sampling-rate-and-sensor-placement)
  - [Classical and Machine Learning](#classical-and-machine-learning)
  - [Deep Learning](#deep-learning)
  - [Edge and TinyML](#edge-and-tinyml)
  - [PaperWithCode](#paperwithcode)
- [Code](#code)
  - [Official / Author Repositories](#official--author-repositories)
  - [Reproductions and Baselines](#reproductions-and-baselines)
  - [Embedded and TinyML](#embedded-and-tinyml)
  - [Foundation Models and Tooling](#foundation-models-and-tooling)
- [Notes](#notes)
- [Contributing](#contributing)
- [License](#license)

## Dataset

### Wrist and Multi-Position Datasets

- [WEDA-FALL](https://github.com/joaojtmarques/WEDA-FALL) - Wrist Elderly Daily Activity and Fall Dataset captured with a Fitbit Sense at 50 Hz, with 40/25/10/5 Hz downsampled versions, accelerometer, gyroscope, orientation, and manually annotated fall timestamps.
- [UMAFall](https://figshare.com/articles/dataset/UMA_ADL_FALL_Dataset_zip/4214283) - Multisensor fall dataset from Universidad de Malaga with smartphone and wearable sensors at several body positions including chest, wrist, waist, ankle, and thigh.
- [UP-Fall Detection Dataset](https://sites.google.com/up.edu.mx/har-up/) - Multimodal fall dataset with IMUs, ambient sensors, cameras, EEG, and multiple body positions including neck, waist, wrist, ankle, and pocket.
- [SmartFall Dataset](https://userweb.cs.txstate.edu/~hn12/data/SmartFallDataSet/) - Smartwatch-based wrist accelerometer dataset used by the SmartFall project; includes SmartFall, SmartWatch, and Notch wrist data.
- [HR + IMU Fall Detection Dataset](https://github.com/nhoyh/HR_IMU_falldetection_dataset) - Wrist IMU and heart-rate/RR data for falls, ADLs, and near-falls, introduced with an IEEE Access 2020 paper.
- [AybuFall](https://zenodo.org/records/18175644) - IMU dataset with forehead and forearm MetaMotionS sensors at 200 Hz, covering falls, ADLs, and prayer movements for false-positive stress testing.
- [FallAllD](https://ieee-dataport.org/open-access/fallalld-comprehensive-dataset-human-falls-and-activities-daily-living) - Large multi-position dataset with neck, waist, and wrist LSM9DS1 sensors, available through IEEE DataPort.

### Common Benchmark Datasets

- [SisFall](http://sistemic.udea.edu.co/en/investigacion/proyectos/english-falls/) - Widely used waist-mounted accelerometer/gyroscope benchmark with simulated falls and ADLs.
- [KFall](https://sites.google.com/view/kfalldataset) - KAIST large-scale motion dataset for pre-impact fall detection, with frame-level fall onset and impact labels.
- [UniMiB SHAR](https://www.sal.disco.unimib.it/technologies/unimib-shar/) - Smartphone accelerometer dataset for human activity recognition and falls.
- [MobiAct / MobiFall](https://bmi.hmu.gr/the-mobiact-v2-0-dataset/) - Smartphone-based fall and activity datasets from the Hellenic Mediterranean University group.
- [UR Fall Detection Dataset](http://fenix.ur.edu.pl/~mkepski/ds/uf.html) - Dataset combining accelerometer data and depth camera sequences.
- [tFall](https://webdiis.unizar.es/~lfdb/tfall/) - Smartphone accelerometer dataset for fall detection in trouser pockets.

### Synthetic and Generated Datasets

- [LLM-Based Synthetic Fall Data](https://github.com/txst-cs-smartfall/LLM-based-synthetic-fall-data-generation) - Synthetic wearable IMU fall data generated and evaluated with LLM and diffusion approaches for fall-detection augmentation.
- [Xentim Fall Detection Sample](https://huggingface.co/datasets/xentim/fall-detection-sample) - Synthetic camera-view (not wearable) skeleton data: 384 sequences from 32 simulated falls and non-fall look-alikes, 12 virtual cameras per event, 17 COCO keypoints per frame. Free sample for internal evaluation behind an access form; the full dataset is commercial.

### Real-World / Restricted Datasets

- [FARSEEING](https://farseeingresearch.eu/) - Real-world falls from older adults; important for realistic validation, but access is restricted.

## Paper

### Survey and Evaluation

- 2012 - [Evaluation of Accelerometer-Based Fall Detection Algorithms on Real-World Falls](https://doi.org/10.1371/journal.pone.0037062) - Landmark evaluation showing the gap between simulated and real-world falls.
- 2017 - [Analysis of Public Datasets for Wearable Fall Detection Systems](https://www.mdpi.com/1424-8220/17/7/1513) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s17071513)](https://juleskreuer.eu/citation-badge/)
- 2021 - [A Feasibility Study of Smartwatches in Wearable Fall Detection Systems](https://www.mdpi.com/1424-8220/21/6/2254) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s21062254)](https://juleskreuer.eu/citation-badge/)
- 2022 - [An Analytical Comparison of Datasets of Real-World and Simulated Falls Intended for the Evaluation of Wearable Fall Alerting Systems](https://doi.org/10.1016/j.measurement.2022.111843) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1016/j.measurement.2022.111843)](https://juleskreuer.eu/citation-badge/)
- 2025 - [A Comparative Overview of Technological Advances in Fall Detection Systems for Elderly People](https://www.mdpi.com/1424-8220/25/24/7423) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s25247423)](https://juleskreuer.eu/citation-badge/)

### Dataset Papers

- 2017 - [SisFall: A Fall and Movement Dataset](https://www.mdpi.com/1424-8220/17/1/198) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s17010198)](https://juleskreuer.eu/citation-badge/)
- 2017 - [UniMiB SHAR: A Dataset for Human Activity Recognition Using Acceleration Data from Smartphones](https://www.mdpi.com/2076-3417/7/10/1101) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/app7101101)](https://juleskreuer.eu/citation-badge/)
- 2018 - [SmartFall: A Smartwatch-Based Fall Detection System Using Deep Learning](https://www.mdpi.com/1424-8220/18/10/3363) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s18103363)](https://juleskreuer.eu/citation-badge/)
- 2019 - [UP-Fall Detection Dataset: A Multimodal Approach](https://www.mdpi.com/1424-8220/19/9/1988) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s19091988)](https://juleskreuer.eu/citation-badge/)
- 2021 - [FallAllD: An Open Dataset of Human Falls and Activities of Daily Living for Classical and Deep Learning Applications](https://doi.org/10.1109/JSEN.2020.3018335) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/JSEN.2020.3018335)](https://juleskreuer.eu/citation-badge/)
- 2021 - [KFall: A Large-Scale Open Motion Dataset and Benchmark Algorithms for Detecting Pre-Impact Fall](https://www.frontiersin.org/articles/10.3389/fnagi.2021.692865/full) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3389/fnagi.2021.692865)](https://juleskreuer.eu/citation-badge/)
- 2026 - [An IMU-Based Dataset of Falls, Activities of Daily Living, and Prayer Movements (AybuFall)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12910762/) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1186/s13104-026-07679-9)](https://juleskreuer.eu/citation-badge/)

### Sampling Rate and Sensor Placement

- 2008 - [Comparison of Low-Complexity Fall Detection Algorithms for Body Attached Accelerometers](https://doi.org/10.1016/j.gaitpost.2008.01.003)
- 2016 - [An Analysis on Sensor Locations of the Human Body for Wearable Fall Detection Devices](https://www.mdpi.com/1424-8220/16/8/1161) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s16081161)](https://juleskreuer.eu/citation-badge/)
- 2016 - [How Accurately Can Your Wrist Device Recognize Daily Activities and Detect Falls?](https://www.mdpi.com/1424-8220/16/6/800) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s16060800)](https://juleskreuer.eu/citation-badge/)
- 2018 - [Analysis of a Smartphone-Based Architecture with Multiple Mobility Sensors for Fall Detection with Supervised Learning](https://www.mdpi.com/1424-8220/18/4/1155) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s18041155)](https://juleskreuer.eu/citation-badge/)
- 2018 - [On the Comparison of Wearable Sensor Data Fusion to a Single Sensor Machine Learning Technique in Fall Detection](https://www.mdpi.com/1424-8220/18/2/592) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s18020592)](https://juleskreuer.eu/citation-badge/)
- 2022 - [Deep-Learning-Based Signal Enhancement of Low-Resolution Accelerometer for Fall Detection Systems](https://doi.org/10.1109/TCDS.2021.3116228) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/TCDS.2021.3116228)](https://juleskreuer.eu/citation-badge/)
- 2022 - [A Study of the Influence of the Sensor Sampling Frequency on the Performance of Wearable Fall Detectors](https://www.sciencedirect.com/science/article/pii/S0263224122002226) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1016/j.measurement.2022.110945)](https://juleskreuer.eu/citation-badge/)
- 2026 - [The Impact of the Accelerometer Sampling Rate on ML/DL Models in Wearable Fall Detection Systems](https://www.mdpi.com/1424-8220/26/1/162) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s26010162)](https://juleskreuer.eu/citation-badge/)

### Classical and Machine Learning

- 2007 - [Evaluation of a Threshold-Based Tri-Axial Accelerometer Fall Detection Algorithm](https://doi.org/10.1016/j.gaitpost.2006.09.012)
- 2017 - [A Comparison of Accuracy of Fall Detection Algorithms](https://doi.org/10.1007/s11517-016-1504-y)
- 2018 - [Real-Life/Real-Time Elderly Fall Detection with a Triaxial Accelerometer](https://www.mdpi.com/1424-8220/18/4/1101) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s18041101)](https://juleskreuer.eu/citation-badge/)
- 2018 - [Movement Decomposition and Machine Learning-Based Fall Detection Using Wrist Wearable Device](https://doi.org/10.1109/JSEN.2018.2830337)
- 2019 - [Elderly Fall Detection Using Wearable Sensors: A Low Cost Highly Accurate Algorithm](https://doi.org/10.1109/JSEN.2019.2891128) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/JSEN.2019.2891128)](https://juleskreuer.eu/citation-badge/)
- 2024 - [Accurate and Efficient Real-World Fall Detection Using Time Series Techniques](https://www.researchgate.net/publication/382940726_Accurate_and_Efficient_Real-World_Fall_Detection_Using_Time_Series_Techniques) - Feature-free time-series classifiers on FARSEEING, FallAllD, and SisFall.
- 2025 - [A Feature Engineering Method for Smartphone-Based Fall Detection](https://www.mdpi.com/1424-8220/25/20/6500) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s25206500)](https://juleskreuer.eu/citation-badge/)

### Deep Learning

- 2018 - [Online Fall Detection Using Recurrent Neural Networks](https://arxiv.org/abs/1804.04976) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.48550/arXiv.1804.04976)](https://juleskreuer.eu/citation-badge/)
- 2020 - [A Study on the Application of Convolutional Neural Networks to Fall Detection Evaluated with Multiple Public Datasets](https://www.mdpi.com/1424-8220/20/5/1466) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s20051466)](https://juleskreuer.eu/citation-badge/)
- 2021 - [Fall Detection with CNN-Casual LSTM Network](https://www.mdpi.com/2078-2489/12/10/403) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/info12100403)](https://juleskreuer.eu/citation-badge/)
- 2022 - [Fall Detection Using Multimodal Data](https://link.springer.com/chapter/10.1007/978-3-030-98358-1_31) - UP-Fall sensor, camera, and sensor-camera fusion experiments.
- 2023 - [Patch-Transformer Network: A Wearable-Sensor-Based Fall Detection Method](https://www.mdpi.com/1424-8220/23/14/6360) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s23146360)](https://juleskreuer.eu/citation-badge/)
- 2023 - [PreFallKD: Pre-Impact Fall Detection via CNN-ViT Knowledge Distillation](https://arxiv.org/abs/2303.03634) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.48550/arXiv.2303.03634)](https://juleskreuer.eu/citation-badge/)
- 2023 - [Experimental Study: Deep Learning-Based Fall Monitoring among Older Adults with Skin-Wearable Electronics](https://www.mdpi.com/1424-8220/23/8/3983) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s23083983)](https://juleskreuer.eu/citation-badge/)
- 2023 - [Sensitivity Analysis of LSTM Networks for Fall Detection Wearable Sensors](https://doi.org/10.1109/CIoT57267.2023.10084906) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/CIoT57267.2023.10084906)](https://juleskreuer.eu/citation-badge/)
- 2023 - [TinyFallNet: A Lightweight Pre-Impact Fall Detection Model](https://www.mdpi.com/1424-8220/23/20/8459) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s23208459)](https://juleskreuer.eu/citation-badge/)
- 2024 - [Physics Sensor Based Deep Learning Fall Detection System](https://arxiv.org/abs/2403.06994) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.48550/arXiv.2403.06994)](https://juleskreuer.eu/citation-badge/)
- 2025 - [AI-Generated Fall Data: Assessing LLMs and Diffusion Model for Wearable Fall Detection](https://www.mdpi.com/1424-8220/25/16/5144) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/s25165144)](https://juleskreuer.eu/citation-badge/)
- 2025 - [Beyond Falls: A Hybrid CNN-LSTM-Attention Framework for Pre-, Transition-, and Post-Fall Detection With Wearable Inertial Sensors](https://doi.org/10.1109/ACCESS.2025.3641198) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/ACCESS.2025.3641198)](https://juleskreuer.eu/citation-badge/)
- 2026 - MadgwickFall-Net: A Lightweight Dual-Frame Feature Fusion Network for Pre-Impact Fall Detection Using Wearable IMUs - Dual-frame body/global IMU fusion for KFall pre-impact fall detection; public DOI/URL not found in the local copy.

### Edge and TinyML

- 2020 - [Deep Learning Based Fall Detection Algorithms for Embedded Systems, Smartwatches, and IoT Devices](https://www.mdpi.com/2227-7080/8/4/72) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/technologies8040072)](https://juleskreuer.eu/citation-badge/)
- 2024 - [Analyzing and Comparing Deep Learning Models on an ARM 32-bit Microcontroller for Pre-Impact Fall Detection](https://doi.org/10.1109/JSEN.2024.3364249) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1109/JSEN.2024.3364249)](https://juleskreuer.eu/citation-badge/)
- 2024 - [Edge Computing Transformers for Fall Detection in Older Adults](https://doi.org/10.1142/S0129065724500266) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.1142/S0129065724500266)](https://juleskreuer.eu/citation-badge/)
- 2025 - [Energy-Efficient Fall-Detection System Using LoRa and Hybrid Algorithms](https://www.mdpi.com/2313-7673/10/5/313) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.3390/biomimetics10050313)](https://juleskreuer.eu/citation-badge/)
- 2025 - [IMU Sensor Based Expandable Fall Detection System Design](https://doi.org/10.54370/ordubtd.1658926) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.54370/ordubtd.1658926)](https://juleskreuer.eu/citation-badge/)
- 2026 - [A Wearable System for Real-Time Fall Detection on Resource-Constrained Devices](https://doi.org/10.1109/JIOT.2025.3636894)
- 2026 - [A Pre-impact Fall Algorithm Based on a Lightweight Re-Parameters-Parallel Convolutional-TCN](https://doi.org/10.13164/re.2026.0084) [![Citation Badge](https://api.juleskreuer.eu/citation-badge.php?doi=10.13164/re.2026.0084)](https://juleskreuer.eu/citation-badge/)

### PaperWithCode

- 2019 - [UP-Fall Detection Dataset: A Multimodal Approach](https://www.mdpi.com/1424-8220/19/9/1988) | [jpnm561/HAR-UP](https://github.com/jpnm561/HAR-UP)
- 2019 - [Applying Singular Value Decomposition on Accelerometer Data for 1D CNN Based Fall Detection](https://doi.org/10.1049/el.2018.6117) | [heeryoncho/SVD_applied_fall_detection](https://github.com/heeryoncho/SVD_applied_fall_detection)
- 2020 - [Cluster-Analysis-Based User-Adaptive Fall Detection Using Fusion of Heart Rate Sensor and Accelerometer](https://doi.org/10.1109/ACCESS.2020.2969389) | [nhoyh/HR_IMU_falldetection_dataset](https://github.com/nhoyh/HR_IMU_falldetection_dataset)
- 2021 - [FallAllD: An Open Dataset of Human Falls and ADLs](https://doi.org/10.1109/JSEN.2020.3018335) | [aaqdas/FallDetection](https://github.com/aaqdas/FallDetection) (community end-to-end MCU implementation)
- 2021 - [LIMU-BERT: Unleashing the Potential of Unlabeled Data for IMU Sensing Applications](https://dl.acm.org/doi/10.1145/3485730.3485937) | [dapowan/LIMU-BERT-Public](https://github.com/dapowan/LIMU-BERT-Public)
- 2022 - [Fall Detection Using Multimodal Data](https://link.springer.com/chapter/10.1007/978-3-030-98358-1_31) | [hoangNguyen210/Fall-Detection-Research-1](https://github.com/hoangNguyen210/Fall-Detection-Research-1)
- 2022 - [Fall Detection Using Biometric Information Based on Multi-Horizon Forecasting](https://ieeexplore.ieee.org/document/9956568) | [IKKIM00/Fall_Detection_using_multihorizon_forecasting](https://github.com/IKKIM00/Fall_Detection_using_multihorizon_forecasting)
- 2023 - [Sensitivity Analysis of LSTM Networks for Fall Detection Wearable Sensors](https://doi.org/10.1109/CIoT57267.2023.10084906) | [SCorreiaPT/LSTM_SensitivityFallDetection](https://github.com/SCorreiaPT/LSTM_SensitivityFallDetection)
- 2023 - [PreFallKD: Pre-Impact Fall Detection via CNN-ViT Knowledge Distillation](https://arxiv.org/abs/2303.03634) | [brianchi0607/PREFALLKD](https://github.com/brianchi0607/PREFALLKD-PRE-IMPACT-FALL-DETECTION-VIA-CNN-VIT-KNOWLEDGE-DISTILLATION)
- 2024 - [Physics Sensor Based Deep Learning Fall Detection System](https://arxiv.org/abs/2403.06994) | [WuShaoa/SensorDataClassification-TCN](https://github.com/WuShaoa/SensorDataClassification-TCN)
- 2024 - [Accurate and Efficient Real-World Fall Detection Using Time Series Techniques](https://www.researchgate.net/publication/382940726_Accurate_and_Efficient_Real-World_Fall_Detection_Using_Time_Series_Techniques) | [mlgig/ts_fall_detection](https://github.com/mlgig/ts_fall_detection)
- 2025 - [AI-Generated Fall Data: Assessing LLMs and Diffusion Model for Wearable Fall Detection](https://www.mdpi.com/1424-8220/25/16/5144) | [txst-cs-smartfall/LLM-based-synthetic-fall-data-generation](https://github.com/txst-cs-smartfall/LLM-based-synthetic-fall-data-generation)

## Code

### Official / Author Repositories

- [jpnm561/HAR-UP](https://github.com/jpnm561/HAR-UP) - Official UP-Fall Python pipeline for database download, feature extraction, feature selection, cross-validation, and traditional ML training. ![GitHub stars](https://img.shields.io/github/stars/jpnm561/HAR-UP.svg)
- [heeryoncho/SVD_applied_fall_detection](https://github.com/heeryoncho/SVD_applied_fall_detection) - Author code for SVD + 1D-CNN fall detection on SisFall, UMAFall, and UniMiB. ![GitHub stars](https://img.shields.io/github/stars/heeryoncho/SVD_applied_fall_detection.svg)
- [IKKIM00/Fall_Detection_using_multihorizon_forecasting](https://github.com/IKKIM00/Fall_Detection_using_multihorizon_forecasting) - Original code for multi-horizon fall forecasting with TFT, 1D-CNN, and LSTM on SmartFall, Notch, DLR, and MobiAct. ![GitHub stars](https://img.shields.io/github/stars/IKKIM00/Fall_Detection_using_multihorizon_forecasting.svg)
- [hoangNguyen210/Fall-Detection-Research-1](https://github.com/hoangNguyen210/Fall-Detection-Research-1) - Code for UP-Fall multimodal fall detection with sensor features, camera CNNs, and sensor-camera fusion. ![GitHub stars](https://img.shields.io/github/stars/hoangNguyen210/Fall-Detection-Research-1.svg)
- [mlgig/ts_fall_detection](https://github.com/mlgig/ts_fall_detection) - Code and evaluation results for real-world time-series fall detection on FARSEEING, FallAllD, and SisFall. ![GitHub stars](https://img.shields.io/github/stars/mlgig/ts_fall_detection.svg)
- [brianchi0607/PREFALLKD](https://github.com/brianchi0607/PREFALLKD-PRE-IMPACT-FALL-DETECTION-VIA-CNN-VIT-KNOWLEDGE-DISTILLATION) - PyTorch implementation of CNN-ViT knowledge distillation for pre-impact fall detection on KFall. ![GitHub stars](https://img.shields.io/github/stars/brianchi0607/PREFALLKD-PRE-IMPACT-FALL-DETECTION-VIA-CNN-VIT-KNOWLEDGE-DISTILLATION.svg)
- [nhoyh/HR_IMU_falldetection_dataset](https://github.com/nhoyh/HR_IMU_falldetection_dataset) - HR + IMU wrist dataset repository for user-adaptive fall detection. ![GitHub stars](https://img.shields.io/github/stars/nhoyh/HR_IMU_falldetection_dataset.svg)
- [joaojtmarques/WEDA-FALL](https://github.com/joaojtmarques/WEDA-FALL) - Official WEDA-FALL dataset repository. ![GitHub stars](https://img.shields.io/github/stars/joaojtmarques/WEDA-FALL.svg)
- [dapowan/LIMU-BERT-Public](https://github.com/dapowan/LIMU-BERT-Public) - Public LIMU-BERT implementation for self-supervised IMU representation learning. ![GitHub stars](https://img.shields.io/github/stars/dapowan/LIMU-BERT-Public.svg)
- [SCorreiaPT/LSTM_SensitivityFallDetection](https://github.com/SCorreiaPT/LSTM_SensitivityFallDetection) - MATLAB author code for LSTM layer and cell-size sensitivity analysis in wearable fall detection. ![GitHub stars](https://img.shields.io/github/stars/SCorreiaPT/LSTM_SensitivityFallDetection.svg)

### Reproductions and Baselines

- [aaqdas/FallDetection](https://github.com/aaqdas/FallDetection) - FallAllD-based 1D-CNN with TensorFlow Lite Micro conversion and Arduino Nano 33 BLE Sense deployment. ![GitHub stars](https://img.shields.io/github/stars/aaqdas/FallDetection.svg)
- [mojtabaSefidi/Fall-Detection-System](https://github.com/mojtabaSefidi/Fall-Detection-System) - SisFall traditional ML and deep learning comparison. ![GitHub stars](https://img.shields.io/github/stars/mojtabaSefidi/Fall-Detection-System.svg)
- [SpaceMinds/FDS](https://github.com/SpaceMinds/FDS) - Educational SisFall pipeline from thresholding to KNN, SVM, and neural networks. ![GitHub stars](https://img.shields.io/github/stars/SpaceMinds/FDS.svg)
- [1saifj/Fall-Detection-System-SisFall-Dataset-Raspberry-Pi](https://github.com/1saifj/Fall-Detection-System-SisFall-Dataset-Raspberry-Pi) - SisFall LSTM/CNN-LSTM with Raspberry Pi deployment. ![GitHub stars](https://img.shields.io/github/stars/1saifj/Fall-Detection-System-SisFall-Dataset-Raspberry-Pi.svg)
- [OreoDu/sisFall](https://github.com/OreoDu/sisFall) - SisFall RNN/LSTM-style experiments. ![GitHub stars](https://img.shields.io/github/stars/OreoDu/sisFall.svg)
- [naomikgrant/SisFall_DL](https://github.com/naomikgrant/SisFall_DL) - Deep learning experiments for SisFall. ![GitHub stars](https://img.shields.io/github/stars/naomikgrant/SisFall_DL.svg)
- [chizhanyuefeng/FD-CNN](https://github.com/chizhanyuefeng/FD-CNN) - CNN-based fall detection implementation. ![GitHub stars](https://img.shields.io/github/stars/chizhanyuefeng/FD-CNN.svg)
- [chizhanyuefeng/Realtime-Fall-Detection-for-RNN](https://github.com/chizhanyuefeng/Realtime-Fall-Detection-for-RNN) - Real-time RNN fall detection reference. ![GitHub stars](https://img.shields.io/github/stars/chizhanyuefeng/Realtime-Fall-Detection-for-RNN.svg)
- [IKKIM00/fall-detection-and-predction-using-GRU-and-LSTM-with-Transfer-Learning](https://github.com/IKKIM00/fall-detection-and-predction-using-GRU-and-LSTM-with-Transfer-Learning) - SmartFall to MobiAct GRU/LSTM transfer-learning experiments. ![GitHub stars](https://img.shields.io/github/stars/IKKIM00/fall-detection-and-predction-using-GRU-and-LSTM-with-Transfer-Learning.svg)
- [xushige/HAR-Dataset-Preprocess](https://github.com/xushige/HAR-Dataset-Preprocess) - PyTorch preprocessing and model infrastructure for UniMiB, PAMAP2, WISDM, UCI-HAR, USC-HAD, and other HAR datasets. ![GitHub stars](https://img.shields.io/github/stars/xushige/HAR-Dataset-Preprocess.svg)
- [hoangNguyen210/Fall-Detection-Research-2](https://github.com/hoangNguyen210/Fall-Detection-Research-2) - UP-Fall camera-data continuation with preprocessing notebooks, mixture-of-experts models, and 3D-CNN experiments. ![GitHub stars](https://img.shields.io/github/stars/hoangNguyen210/Fall-Detection-Research-2.svg)
- [ankit1997/Fall-Detection-using-CNN](https://github.com/ankit1997/Fall-Detection-using-CNN) - TensorFlow CNN and dense baseline for accelerometer/gyroscope fall-vs-non-fall sensor data. ![GitHub stars](https://img.shields.io/github/stars/ankit1997/Fall-Detection-using-CNN.svg)
- [hwixley/Fall-Detection-Deep-Learning](https://github.com/hwixley/Fall-Detection-Deep-Learning) - PyTorch LSTM and ResNet fall-detection pipeline with sliding-window preprocessing and TFLite export. ![GitHub stars](https://img.shields.io/github/stars/hwixley/Fall-Detection-Deep-Learning.svg)
- [AdrianNunez/transformer-based-fall-detection](https://github.com/AdrianNunez/transformer-based-fall-detection) - Transformer-based UP-Fall video fall-detection baseline using camera-frame inputs. ![GitHub stars](https://img.shields.io/github/stars/AdrianNunez/transformer-based-fall-detection.svg)

### Embedded and TinyML

- [baljo/fall_detection](https://github.com/baljo/fall_detection) - Edge Impulse / Nicla Sense ME fall-detection reference project. ![GitHub stars](https://img.shields.io/github/stars/baljo/fall_detection.svg)
- [NathanielFelleke/TinyML-Fall-Detection](https://github.com/NathanielFelleke/TinyML-Fall-Detection) - TinyML fall detection project with data collection, training, and embedded inference pieces. ![GitHub stars](https://img.shields.io/github/stars/NathanielFelleke/TinyML-Fall-Detection.svg)
- [STMicroelectronics/st-mems-machine-learning-core](https://github.com/STMicroelectronics/st-mems-machine-learning-core) - ST MEMS Machine Learning Core examples and tooling. ![GitHub stars](https://img.shields.io/github/stars/STMicroelectronics/st-mems-machine-learning-core.svg)
- [harrkout/Machine_Learning_Core_STM32WL55](https://github.com/harrkout/Machine_Learning_Core_STM32WL55) - STM32WL55 + LSM6DSOX MLC reference project. ![GitHub stars](https://img.shields.io/github/stars/harrkout/Machine_Learning_Core_STM32WL55.svg)
- [xiaoweiweiyaya/ESP32_FallDetection](https://github.com/xiaoweiweiyaya/ESP32_FallDetection) - ESP32 fall-detection project. ![GitHub stars](https://img.shields.io/github/stars/xiaoweiweiyaya/ESP32_FallDetection.svg)
- [Kartik9250/Fall_detection](https://github.com/Kartik9250/Fall_detection) - Arduino/MPU-style threshold fall detection. ![GitHub stars](https://img.shields.io/github/stars/Kartik9250/Fall_detection.svg)
- [geoseiden/fall-detection-blynk](https://github.com/geoseiden/fall-detection-blynk) - IoT fall detection with Blynk integration. ![GitHub stars](https://img.shields.io/github/stars/geoseiden/fall-detection-blynk.svg)
- [tensorflow/tflite-micro](https://github.com/tensorflow/tflite-micro) - TensorFlow Lite Micro; `magic_wand` is a useful IMU template for MCU deployment. ![GitHub stars](https://img.shields.io/github/stars/tensorflow/tflite-micro.svg)

### Foundation Models and Tooling

- [yolish/har-with-imu-transformer](https://github.com/yolish/har-with-imu-transformer) - Transformer backbone for IMU human activity recognition. ![GitHub stars](https://img.shields.io/github/stars/yolish/har-with-imu-transformer.svg)
- [Hangwei12358/cross-person-HAR](https://github.com/Hangwei12358/cross-person-HAR) - Cross-person HAR generalization reference. ![GitHub stars](https://img.shields.io/github/stars/Hangwei12358/cross-person-HAR.svg)
- [rh20624/Awesome-IMU-Sensing](https://github.com/rh20624/Awesome-IMU-Sensing) - Broad IMU sensing paper and resource list. ![GitHub stars](https://img.shields.io/github/stars/rh20624/Awesome-IMU-Sensing.svg)
- [WuShaoa/SensorDataClassification-TCN](https://github.com/WuShaoa/SensorDataClassification-TCN) - FallSeqTCN / TCN-style sensor data classification code. ![GitHub stars](https://img.shields.io/github/stars/WuShaoa/SensorDataClassification-TCN.svg)
- [txst-cs-smartfall/LLM-based-synthetic-fall-data-generation](https://github.com/txst-cs-smartfall/LLM-based-synthetic-fall-data-generation) - Synthetic fall-data generation resources released with the LLM and diffusion wearable fall-detection study. ![GitHub stars](https://img.shields.io/github/stars/txst-cs-smartfall/LLM-based-synthetic-fall-data-generation.svg)

## Notes

- Many fall-detection papers report excellent results on simulated datasets but do not release official code. Treat community implementations as useful baselines, not exact reproductions.
- SisFall, KFall, and UniMiB are common academic benchmarks, but they are waist, lower-back, or phone-pocket datasets. Wrist and chest products should validate on native wrist/chest data such as WEDA-FALL, UMAFall, UP-Fall, FallAllD, or self-collected data.
- AybuFall is useful for false-positive analysis because prayer movements can resemble fall-like posture transitions while still being non-fall activities.
- For product work, evaluate with leave-one-subject-out and cross-dataset protocols whenever possible. Real-world fall data such as FARSEEING is crucial for false-alarm analysis.
- Always check dataset licenses and access rules before redistributing raw data.

## Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch, for example `feature/new-fall-resource`.
3. Add relevant papers, datasets, code, or corrections.
4. Open a pull request with a short description of why the resource belongs here.

Please prefer resources that are directly relevant to wearable, sensor-based, IMU, accelerometer, gyroscope, TinyML, or edge fall detection. Mark clearly whether a repository is official code, author code, or a community reproduction.

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
