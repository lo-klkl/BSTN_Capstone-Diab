I will segment these numerical columns as shown below. These values for the various conditions were pulled from the Mayo Clinic. The purpose of converting these numerical columns 
is to make it easier to understand what they mean in the context of medical triage information. I plan to keep this here as a reference to understand what the newly generated labels
mean in terms of their numeric origins. 

Doing this will make it easier to create visualizations that are easier to understand and also pre-process the data for one-hot encoding for later modeling purposes. 

---

I will segment these columns as shown below. These values for the various conditions were pulled from the Mayo Clinic and also from the study by [Raza,S.](https://www.sciencedirect.com/science/article/pii/S2772442522000430).  

triage_vital_hr (heart rate):
- Normal: 60 - 100 bpm
- Tachycardia (high): >100 bpm
- Bradycardia (low): <60 bpm
- Critical (extreme values): <30 bpm or >160 bpm

triage_vital_sbp (systolic blood pressure):
- Normal: 90 - 120 mmHg
- Hypotension (low): <90 mmHg
- Pre-hypertension: 120 - 140 mmHg
- Hypertension (high): >140 mmHg
- Critical (extreme values): <70 mmHg or >180 mmHg

triage_vital_dbp (diastolic blood pressure):
- Normal: 60 - 80 mmHg
- Hypotension (low): <60 mmHg
- Pre-hypertension: 80 - 90 mmHg
- Hypertension (high): >90 mmHg
- Critical (extreme values): <40 mmHg or >120 mmHg

triage_vital_rr (respiratory rate):
- Normal: 12 - 20 breaths per minute
- Tachypnea (high): >20 breaths per minute
- Bradypnea (low): <12 breaths per minute
- Critical (extreme values): <8 breaths per minute or >30 breaths per minute

triage_vital_temp (temperature):
- Normal body temperature: 97 - 99.5 degrees Fahrenheit
- Hypothermia (low): <97 degrees Fahrenheit
- Fever (high): >99.5 degrees Fahrenheit
- Critical (extreme values): <90 degrees Fahrenheit or >106 degrees Fahrenheit

huse_n_edvisits (prior hospital visits):
- No prior visits: 0
- Low prior visits: 1 - 10
- Moderate prior visits: 11 - 50
- High prior visits: >50

huse_n_admissions (prior hospital admissions):
- Low prior admissions: 1 - 10
- Moderate prior admissions: 11 - 20
- High prior admissions: 21 - 30
- Very high prior admissions: >30

huse_n_surgeries (prior surgeries):
- No prior surgeries: 0
- Low prior surgeries: 1 - 10
- Moderate prior surgeries: 11 - 20
- High prior surgeries: >20

hist_glucose_median
- "Normal" if <= 200 mg/dL
- ">200(high)" if > 200 and <= 300 mg/dL
- ">300(very high)" if > 300 mg/dL
- **for this data, we will be following the guide put forth by [Raza](https://www.sciencedirect.com/science/article/pii/S2772442522000430)
