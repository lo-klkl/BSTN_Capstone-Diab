Dummy Column Reference
-----
After dummying columns in the [Pre-processing notebook](Notebooks/Pt2- Preprocessing.ipynb), the columns with the most instances were dropped to avoid multicollinearity and serve as a reference point. However, this also means that it can be difficult to remember if not written down. This document will serve as a reference. 

### Demographic Data
- For Age: [50-59] age bin was dropped 
- For Employ Status: Not_Employed status was dropped
- For Insurance Status: insurance_status_Federal was dropped

### Triage Numerical Data 
- For 'dum_triage_vital__normal_hr' with the most instances for 'triage_vital_hr' was dropped.
- For 'dum_triage_vital__hypertension(high)_sbp' with the most instances for 'triage_vital_sbp' was dropped.
- For 'dum_triage_vital__normal_dbp' with the most instances for 'triage_vital_dbp' was dropped.
- For 'dum_triage_vital__normal_rr' with the most instances for 'triage_vital_rr' was dropped.
- For 'dum_triage_vital__normal_temp' with the most instances for 'triage_vital_temp' was dropped.

### Hospital Usage Data 
- For 'dum_huse__prev_dispo_None' with the most instances for 'huse_previousdispo' was dropped.
- For 'dum_huse__low_prior_visit' with the most instances for 'huse_n_edvisits' was dropped.
- For 'dum_huse__low_prior_admis' with the most instances for 'huse_n_admissions' was dropped.
- For 'dum_huse__low_Surg' with the most instances for 'huse_n_surgeries' was dropped.

### Hisorical Lab Data
- The dummy column with the most instances is: dum_hist_glucose_median__Normal

### Medication Data 
- For 'dum_huse__no_antihyperglycemics' with the most instances for 'meds_antihyperglycemics' was dropped.
- For 'dum_huse__no_hormones' with the most instances for 'meds_hormones' was dropped.
