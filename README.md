# F1_telemetry_analysis
This project provides an advanced technical comparison between the performance profiles of Charles Leclerc (Ferrari SF-25) and Max Verstappen (Red Bull RB21) during the 2025 Formula 1 season. By leveraging Unsupervised Machine Learning (K-Means Clustering) and custom telemetry processing, the analysis deconstructs lap times into specific dynamic factors: Speed, Traction, and Braking.

Key Features

ML-Powered Corner Categorization: Corners are automatically segmented into four physical clusters (Slow, Medium, Fast, and Power) using K-Means, allowing for a statistically sound comparison of car behavior across different racing regimes.

"Real Analysis" Data Cleaning: Implements a robust outlier rejection filter (filtering deltas >15-20 km/h) to eliminate noise caused by traffic, yellow flags, or driver errors, ensuring the results reflect pure qualifying performance.

Custom Apex Detection: Utilizes a bespoke telemetry-based peak detection algorithm to identify the true physical apex (V 
min
​	
 ) of each corner, moving beyond standard geometric track data.
