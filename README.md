# F1_telemetry_analysis
This project provides an advanced technical comparison between the performance profiles of Charles Leclerc (Ferrari SF-25) and Max Verstappen (Red Bull RB21) during the 2025 Formula 1 season. By leveraging Unsupervised Machine Learning (K-Means Clustering) and custom telemetry processing, the analysis deconstructs lap times into specific dynamic factors: Speed, Traction, and Braking.

Key Features

ML-Powered Corner Categorization: Corners are automatically segmented into four physical clusters (Slow, Medium, Fast, and Power) using K-Means, allowing for a statistically sound comparison of car behavior across different racing regimes.

"Real Analysis" Data Cleaning: Implements a robust outlier rejection filter (filtering deltas >15-20 km/h) to eliminate noise caused by traffic, yellow flags, or driver errors, ensuring the results reflect pure qualifying performance.

Custom Apex Detection: Utilizes a bespoke telemetry-based peak detection algorithm to identify the true physical apex (V 
min
​	
 ) of each corner, moving beyond standard geometric track data.




 # F1 2025 Factorial Performance Analysis: LEC vs VER 🏎️📊

This repository contains an advanced telemetry analysis framework designed to benchmark Formula 1 car performance. The project focuses on the 2025 season rivalry between **Charles Leclerc (Ferrari)** and **Max Verstappen (Red Bull)**, utilizing **Unsupervised Machine Learning** to isolate pure vehicular potential from session noise.

## Project Overview
Unlike standard lap-time comparisons, this project deconstructs performance into its fundamental physical components: **Apex Speed**, **Traction**, and **Braking**. By using a factorial approach, we can identify exactly where a car gains or loses time relative to its competitor.

## Key Technical Features
- **ML-Enhanced Categorization:** Uses **K-Means Clustering** ($K=4$) to automatically segment over 200+ corner instances into dynamic regimes: *Slow (Traction)*, *Medium (Handling)*, *Fast (Downforce)*, and *Power*.
- **"Real Analysis" Filter:** A custom data-cleaning pipeline that rejects outliers (deltas >15-20 km/h) caused by traffic, yellow flags, or driver errors, ensuring a "pure qualifying" comparison.
- **Automated Apex Detection:** Implements a bespoke algorithm using `scipy.signal.find_peaks` to identify the precise physical apex ($V_{min}$) based on telemetry traces rather than static track maps.


## Tech Stack
- **Data Source:** `FastF1` API (Official Timing & Telemetry).
- **Processing:** `Pandas`, `NumPy`, `SciPy`.
- **Machine Learning:** `Scikit-learn` (StandardScaler, KMeans).
- **Visualization:** `Seaborn`, `Matplotlib`.
