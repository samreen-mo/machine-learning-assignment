# machine-learning-assignment
Machine Learning Assignment Code for Submission
Machine Learning Analysis on the effect of Congestion Pricing on Public Bus Performance in New York City

Analysis of MTA bus segment speeds (Oct–Dec 2024 vs Oct–Dec 2025) to test whether
New York's 2025 congestion pricing explains where and when bus speeds improved (RQ1),
and machine-learning models (Logistic Regression, Decision Tree, Random Forest) to
predict slow bus segments (RQ2).

## Data
Datasets for Oct-Dec 2024 and 2025 have been uploaded in the releases section of the repository. 
Also, the original link to download the CSV exports of each year from New York State Open Data is as given below:
- MTA Bus Route Segment Speeds: 2023–2024 — https://data.ny.gov/Transportation/MTA-Bus-Route-Segment-Speeds-2023-2024/58t6-89vi
- MTA Bus Route Segment Speeds: Beginning 2025 — https://data.ny.gov/Transportation/MTA-Bus-Route-Segment-Speeds-Beginning-2025/kufs-yh3x

## Running
Install the libraries: pip install pandas numpy matplotlib seaborn scikit-learn
Download both CSV files into the notebook's folder, and set the file names in the first code cell.
Run all cells. It takes about 4 minutes, with random seed 42.

## Key findings
Bus speeds rose slightly more inside the zone, but Manhattan routes just outside it improved even more. The gain was also no larger when the toll was highest. The toll does not explain the pattern.
A random forest predicts slow segments better than simpler models: ROC-AUC 0.937 on an unseen month. Location is the strongest predictor.
