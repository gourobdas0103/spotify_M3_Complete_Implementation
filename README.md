# 🎵 Spotify Music Clustering & Pattern Discovery (CS-4412 M3)

This repository contains the **M3: Complete Implementation** for the CS-4412 Data Mining project.  
It demonstrates a full end-to-end pipeline for **Spotify track analysis**, expanding beyond M2 with clustering, classification, dimensionality reduction, and anomaly detection.

---

## 📌 Project Overview
- **Dataset**: ~10,000 simulated Spotify tracks (with duplicates and ratio outliers).
- **Goal**: Discover meaningful musical patterns, clusters, and anomalies.
- **Expansion**: Implements multiple techniques beyond M2, with validation and interpretation.

---

## ⚙️ Pipeline Steps
1. **Data Generation & Cleaning**
   - Simulated realistic Spotify track features (danceability, energy, acousticness, etc.).
   - Introduced and corrected **ratio outliers** (`acoustic_electronic_ratio`).
   - Deduplicated multi-genre tracks using `track_id`.

2. **Clustering (K-Means)**
   - Compared **k=2–6** clusters using **Silhouette** and **Davies-Bouldin** scores.
   - Selected **k=2** as optimal (highest Silhouette).
   - Cluster profiles interpreted via feature averages.

3. **Analytical Expansion (M3 Requirements)**
   - **PCA**: Reduced dimensionality for visualization (31% variance explained).
   - **Decision Tree**: Interpretable rules explaining cluster separation.
   - **LOF Anomaly Detection**: Identified ~10% unusual tracks.

4. **Visualization**
   - Ratio outlier correction (histograms).
   - Clustering validation metrics.
   - PCA scatter plot of clusters.
   - Energy vs. log-ratio separation.
   - Decision Tree feature importances.
   - Anomaly energy profiles.

5. **Results**
   - Cluster characterization (distinct musical profiles).
   - Key discriminating features: `ratio_log`, `energy`, `speechiness`.
   - Anomalies show higher-than-average energy.

---

## 📊 Key Findings
- **Cluster 0**: Higher energy, lower acousticness → electronic/dance-oriented tracks.
- **Cluster 1**: Higher acousticness, lower energy → acoustic/folk-oriented tracks.
- **Top Discriminators**: `ratio_log` and `energy` dominate cluster separation.
- **Anomalies**: Edge cases with unusually high energy values.

---

## 📂 Repository Structure
