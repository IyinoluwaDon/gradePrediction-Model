# Validation limits

The app uses repository-relative data/model paths and isolates incompatible individual model artifacts. Pickle files must be trusted; never accept uploaded pickles. Install the training-compatible sklearn/XGBoost versions before interpreting model comparisons.

The target is G3 >= 10. G1/G2/G3 are excluded from input features. The comparison page reuses a training-style split and pretrained scaler; it is not a new independent benchmark. Full-data categorical encoding/scaling can leak information. Rebuild preprocessing in a Pipeline fitted exclusively within training folds, persist its category mapping, and use a held-out student-level evaluation before claiming generalization. Predictions are educational and should not determine student access or grades.

The bundled sklearn estimators identify their training version as 1.7.2. Runtime requirements now pin that version; newer versions can deserialize with warnings but are not a supported inference environment. The home page was rendered in the isolated review runtime; this is not an independent evaluation of every estimator.
