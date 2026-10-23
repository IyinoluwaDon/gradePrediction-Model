# Student Grade Prediction Explorer

A Streamlit educational application that explores student records and compares saved models for a pass/fail target derived from the final grade. It includes separate mathematics and Portuguese model artifacts.

## What is included

- Data exploration and model-comparison pages
- Prediction interface using saved preprocessing/model artifacts
- Smoke check for Streamlit startup and pinned model dependencies

## Run locally

```sh
python -m pip install -r requirements.txt
streamlit run app.py
```

## Verify

The GitHub Actions workflow performs a Streamlit app smoke check. To reproduce model evaluation, inspect and run the notebooks with their data and pinned requirements; evaluation leakage must be addressed first.

## Repository map

`app.py` contains the Streamlit interface. `notebook/` contains the analysis and training work. `requirements.txt` records app dependencies; `VALIDATION.md` describes artifact checks.

## Evidence and limitations

The app smoke check passed locally and saved models were exercised with the pinned scikit-learn/XGBoost stack. These checks do not independently validate student-outcome prediction.

Historical student data and saved artifacts require provenance/licensing review. Preprocessing leakage and the absence of an independent cohort evaluation limit the reported metrics. Do not use predictions for admissions, discipline or other consequential decisions.

## License

No repository license file is included. Unless the project owner adds a license, do not assume the code, data or model artifacts may be redistributed or reused. Verify third-party data and model terms separately.
