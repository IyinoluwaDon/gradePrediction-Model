# Student Grade Prediction Explorer

A Streamlit application and notebook project using the UCI Student Performance data for mathematics and Portuguese courses. The target is derived from final grade `G3`: scores of 10/20 or higher are Pass and scores below 10 are Fail. The workflow compares logistic regression and random forest baselines and includes an XGBoost classifier for the extended experiments; saved estimators and preprocessing artifacts power the prediction interface.

`app.py` presents exploration, model comparison, and prediction pages. `notebook/` contains the analysis and training workflow; `requirements.txt` pins the app stack; `VALIDATION.md` documents the artifact checks.

## Run

```sh
python -m pip install -r requirements.txt
streamlit run app.py
```

The notebook encodes categorical fields and trains/evaluates the classifiers on student-course records. `notebook/model.ipynb` documents the target construction, feature choices, model comparisons, and saved artifacts for both subject datasets.
