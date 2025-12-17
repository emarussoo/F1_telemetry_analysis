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
