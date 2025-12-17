# F1_telemetry_analysis
This project provides an advanced technical comparison between the performance profiles of Charles Leclerc (Ferrari SF-25) and Max Verstappen (Red Bull RB21) during the 2025 Formula 1 season. By leveraging Unsupervised Machine Learning (K-Means Clustering) and custom telemetry processing, the analysis deconstructs lap times into specific dynamic factors: Speed, Traction, and Braking.

Key Features

ML-Powered Corner Categorization: Corners are automatically segmented into four physical clusters (Slow, Medium, Fast, and Power) using K-Means, allowing for a statistically sound comparison of car behavior across different racing regimes.

"Real Analysis" Data Cleaning: Implements a robust outlier rejection filter (filtering deltas >15-20 km/h) to eliminate noise caused by traffic, yellow flags, or driver errors, ensuring the results reflect pure qualifying performance.

Custom Apex Detection: Utilizes a bespoke telemetry-based peak detection algorithm to identify the true physical apex (V 
min
​	
 ) of each corner, moving beyond standard geometric track data.




 # F1 2025 Performance Analysis: LEC vs VER 🏎️📊

Progetto di analisi telemetrica avanzata che confronta le prestazioni di **Charles Leclerc (Ferrari)** e **Max Verstappen (Red Bull)** durante la stagione 2025. Il core del progetto utilizza il **Machine Learning** per isolare il potenziale puro delle vetture, eliminando il rumore statistico.

## 🚀 Key Highlights
- **Unsupervised ML (K-Means):** Categorizzazione automatica delle curve in 4 cluster dinamici (Slow, Medium, Fast, Power) basata su telemetria reale.
- **Real Analysis Filter:** Algoritmo proprietario per la rimozione degli outlier (delta >15km/h) causati da traffico o errori, garantendo dati "pure qualifying".
- **Apex Detection:** Identificazione fisica dell'apice della curva tramite *peak detection* sulla traccia della velocità minima ($V_{min}$).

## 🛠️ Tech Stack
- **Languages:** Python
- **Libraries:** FastF1 (Data Source), Pandas, NumPy, SciPy
- **ML & Stats:** Scikit-learn (StandardScaler, KMeans)
- **Visualization:** Seaborn, Matplotlib

## 📈 Insights Generati
Il modello ha rivelato che la **Ferrari SF-24** eccelle nella velocità di percorrenza a centro curva (+3.34 km/h nelle medie), mentre la **Red Bull RB21** domina in efficienza frenante e stabilità aerodinamica ad alto carico, permettendo a Verstappen di tornare sul gas prima nonostante una $V_{min}$ inferiore.

## 📂 Struttura del Repository
- `F1_Analysis_Notebook.ipynb`: Il motore principale dell'analisi.
- `/plots`: Esportazione dei grafici (Heatmap fattoriali e Delta Speed).
- `/data`: (Opzionale) Script per il caching dei dati FastF1.

---
*Developed for advanced motorsport data driving and performance benchmarking.*
