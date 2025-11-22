# MSIN0114_Dissertation_Soil_Project
BAS_clean.xlsx

Analytical version of the internal experimental dataset (plot–season level). Contains measured nutrient balances (N, P, K, S), experimental controls (location, crop, residue, fertiliser strategy), and identifiers used to join with environmental features.


BAS_data_full_dictionary.xlsx

Data dictionary for the BAS dataset (variable names, units, and descriptions).


BMD_data_full.xlsx

Cleaned daily Bangladesh Meteorological Department panel used to engineer seasonal features (temperature, humidity, rainfall, wind, etc.).


BMD_feature_engineer.ipynb

Notebook that imputes BMD gaps, encodes agronomic seasons, derives daily metrics, and aggregates to seasonal features. Outputs BMD_summary.csv.


BMD_summary.csv

Seasonal-level meteorological features by location and season derived from BMD_data_full.xlsx.


Combine_BMD_n_NASA_features.ipynb

Notebook that merges BMD_summary.csv and NASA_summary_all.csv, harmonises names, and produces the consolidated environmental feature table.


Combine_NASA_features.ipynb

Notebook that collates site-specific NASA seasonal summaries into NASA_summary_all.csv.


Deployment and evaluation.ipynb

End-to-end loading of final models (*.pkl), generation of predictions, and test-set evaluation/plots. Demonstrates deployment in a clean session.


df_full.csv

Final modelling table at plot–season level: BAS outcomes and controls joined to the consolidated environmental features. Used to create the train/validation/test splits.


environmental_features_data_dictionary_edited.xlsx

Data dictionary for the consolidated environmental feature set.


environmental_features.csv

Merged environmental feature matrix by location–season (BMD + NASA), used as the join key for BAS.


feature_groups.pkl

Python object mapping feature names to the ten thematic groups used in Stage-1 selection.


K_bal_direct_model.pkl

Serialised final model for K balance (direct approach).


Modelling_Difference_Approach.ipynb

Training pipeline for the difference strategy (separate input and output models; subtraction to obtain balance). Includes cross-validation, tuning, and model selection.


Modelling_Direct_Approach.ipynb

Training pipeline for the direct strategy (net balance as target). Includes cross-validation, tuning, and ensemble construction.


N_bal_diff_model.pkl

Serialised final model for N balance (difference approach).


NASA_data_bogura.csv

NASA POWER daily variables for Bogura (raw/cleaned daily panel used for feature engineering).


NASA_data_cumilla.csv

NASA POWER daily variables for Cumilla.


NASA_data_muktagacha.csv

NASA POWER daily variables for Muktagacha.


NASA_data_dictionary.xlsx

Dictionary for NASA variables (definitions, units, source notes).


NASA_feature_engineer_bogura.ipynb

Site-specific NASA feature engineering for Bogura (daily → seasonal).


NASA_feature_engineer_cumilla.ipynb

Site-specific NASA feature engineering for Cumilla.


NASA_feature_engineer_muktagacha.ipynb

Site-specific NASA feature engineering for Muktagacha.


NASA_summary_all.csv

Concatenated seasonal NASA features across all three sites.


NASA_summary_bogura.csv

Seasonal NASA features for Bogura.


NASA_summary_cumilla.csv

Seasonal NASA features for Cumilla.


NASA_summary_muktagacha.csv

Seasonal NASA features for Muktagacha.


P_bal_diff_model.pkl

Serialised final model for P balance (difference approach).


S_bal_direct_model.pkl

Serialised final model for S balance (direct approach).


test_df.csv

Held-out test split at plot–season level used only for final evaluation.


train_df.csv

Training split used for model fitting and hyper-parameter tuning.


val_df.csv

Validation split used for model selection and early stopping.

