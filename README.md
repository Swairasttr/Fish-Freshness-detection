# 🐟 AquaFresh - Fish Freshness Classification System
<img width="4536" height="3900" alt="Framework Overview" src="https://github.com/user-attachments/assets/208abc2c-5bdd-4435-a1f0-662bbb3cfad0" />

## Overview
AquaFresh is a non-destructive, real-time computer vision system that classifies fish freshness by analyzing external skin texture. Using advanced image processing techniques including LAB color space segmentation and 2D Haar Wavelet Transform, the system detects progressive texture degradation across multiple fish species (mackerel, tilapia, and tuna) under variable lighting conditions. With over 95% accuracy and minimal computational requirements, AquaFresh is designed for practical deployment in seafood supply chains and industrial quality monitoring systems.

## ✨ Key Features

- **🎯 Non-Destructive Assessment**: Evaluates freshness using only external skin texture—no physical contact or sample destruction required
- **⚡ Real-Time Processing**: Lightweight algorithm suitable for immediate quality assessment in industrial settings
- **🌍 Multi-Species Support**: Validated across mackerel, tilapia, and tuna with consistent performance
- **💡 Illumination-Invariant**: Robust performance under variable lighting conditions
- **📊 High Accuracy**: Achieves >95% classification accuracy with minimal training data
- **🔍 Early Detection**: Captures progressive texture changes from Day 1 through spoilage (11-day monitoring)

## 🛠️ Technical Approach

### Segmentation
- **Color Space**: CIE-LAB for illumination invariance
- **Algorithms**: K-means clustering and Gaussian Mixture Models (GMM)
- **Output**: Binary ROI mask isolating texture regions

### Feature Extraction
- **Transform**: Two-level 2D Haar Discrete Wavelet Transform (DWT)
- **Subband**: Level-2 horizontal detail coefficients (HL2)
- **Features**: Mean and standard deviation of wavelet coefficients

### Classification
- **Method**: Rule-based classifier with empirically calibrated thresholds
- **Categories**: 
  - FR1 (Days 1-3): Fresh
  - FR2 (Days 4-6): Moderately Fresh
  - FR3 (Days 7-11): Spoiled
- **Tie-Breaking**: Euclidean distance to class prototypes

## 📈 Applications

- Seafood supply chain quality monitoring
- Industrial fish processing facilities
- Retail freshness verification
- Portable quality assessment devices

## 🚀 Advantages Over Deep Learning

✅ No extensive labeled datasets required  
✅ Low computational overhead  
✅ Interpretable & transparent decision-making  
✅ Suitable for resource-constrained environments  
✅ Fast deployment and integration

## 📊 Performance Metrics

| Metric | Value |
|--------|-------|
| **Accuracy** | >95% |
| **Species Tested** | 3 (Mackerel, Tilapia, Tuna) |
| **Monitoring Duration** | 11 days |
| **Training Data** | Minimal required |
| **Processing Time** | Real-time capable |
