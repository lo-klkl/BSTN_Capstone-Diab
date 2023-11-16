EDA Results 
---
#### Table of contents
- [Demographic](#demo)
- [Traige Categorical](#tcat)
- [Triage Numerical](#tnum)
- [Patient History and Utilization](#huse)
- [Chief Complaint](#cc)
- [Prior Medical History](#pmh)
- [Medication Categories and Admission Rates Analysis](#meds)
- [Glucose Level History and Admission Rates](#glu)
- [Conclusion](#conc)
---

### <a id = 'demo'></a> Demographic

#### Age:

- **Highest Population Occurrence:** 50-59 (22.60%)
- **Lowest Population Occurrence:** 100-109 (0.13%)

**Admission Rates:**
- Highest Admission Rate: 18-29 (0.72%)
- Lowest Admission Rate: 100-109 (0.08%)

**Disparities:**
- Disparity: Higher admission rate for 18-29 compared to the highest population occurrence (50-59), and lower admission rate for 100-109 compared to the lowest population occurrence.

#### Gender:

- **Highest Population Occurrence:** Female (55.98%)
- **Lowest Population Occurrence:** Male (44.02%)

**Admission Rates:**
- Highest Admission Rate: Female (24.82%)
- Lowest Admission Rate: Male (21.19%)

**Disparities:**
- Disparity: Higher admission rate for females compared to the highest population occurrence (Female), and lower admission rate for males compared to the lowest population occurrence (Male).

#### Race:

- **Highest Population Occurrence:** White or Caucasian (48.35%)
- **Lowest Population Occurrence:** Native Hawaiian or Other Pacific Islander (0.06%)

**Admission Rates:**
- Highest Admission Rate: White or Caucasian (25.68%)
- Lowest Admission Rate: Native Hawaiian or Other Pacific Islander (0.02%)

**Disparities:**
- Disparity: Higher admission rate for White or Caucasian compared to the highest population occurrence (White or Caucasian), and lower admission rate for Native Hawaiian or Other Pacific Islander compared to the lowest population occurrence.

##### Employment Status:

- **Highest Population Occurrence:** Retired (39.97%)
- **Lowest Population Occurrence:** On Active Military Duty (0.00%)

**Admission Rates:**
- Highest Admission Rate: Retired (24.16%)
- Lowest Admission Rate: On Active Military Duty (0.00%)

**Disparities:**
- Disparity: Higher admission rate for Retired compared to the highest population occurrence (Retired), and no admission for On Active Military Duty despite being the lowest population occurrence.

#### Insurance Status:

- **Highest Population Occurrence:** Medicare (38.39%)
- **Lowest Population Occurrence:** Self pay (0.28%)

**Admission Rates:**
- Highest Admission Rate: Medicare (21.84%)
- Lowest Admission Rate: Self pay (0.27%)

**Disparities:**
- Disparity: Higher admission rate for Medicare compared to the highest population occurrence (Medicare), and lower admission rate for Self pay compared to the lowest population occurrence.

#### Interpretation of Chi-Square Test:
- For `demo_age`, the high chi-square value (7572.65) and low p-value (0.00) suggest a strong association between age and admission rates. This indicates that different age groups are not occurring randomly concerning admission rates, and there's a significant relationship between age and the likelihood of admission.

- For `demo_employstatus`, the high chi-square value (7495.23) and low p-value (0.00) indicate a strong association between employment status and admission rates. Employment status and admission rates are not occurring randomly, suggesting a significant relationship between these factors.

- For `demo_insurance_status`, the high chi-square value (5291.14) and low p-value (0.00) suggest a strong association between insurance status and admission rates. Insurance status and admission rates are not occurring randomly, indicating a significant relationship between these factors.

- For `demo_race`, the high chi-square value (2195.91) and low p-value (0.00) suggest a strong association between race and admission rates. Race and admission rates are not occurring randomly, indicating a significant relationship between these factors.

- For `demo_gender`, the chi-square value (149.39) is lower, but the p-value (2.36e-34) is still well below the significance threshold of 0.05. This suggests a significant association between gender and admission rates, though the association is relatively weaker compared to other demographic factors.

---

### <a id = 'tcat'></a> Triage Categorical

#### Triage Category - ESI:
- **Highest Population Occurrence:** Category 2 (38.17%)
- **Lowest Population Occurrence:** Category 5 (2.25%)

**Admission Rates:**
- Highest Admission Rate: Category 2 (25.92%)
- Lowest Admission Rate: Category 5 (0.02%)

**Disparities:**
- Disparity: Higher admission rate for Category 2 compared to the highest population occurrence (Category 2), and much lower admission rate for Category 5 compared to the lowest population occurrence.

#### Triage Category - Arrival Month:
- **Highest Population Occurrence:** May (10.34%)
- **Lowest Population Occurrence:** February (6.89%)

**Admission Rates:**
- Highest Admission Rate: March (4.77%)
- Lowest Admission Rate: February (3.26%)

**Disparities:**
- Disparity: Higher admission rate for March compared to the highest population occurrence (March), and lower admission rate for February compared to the lowest population occurrence.

#### Interpretation of Chi Square Test: 
- For `triage_cat_esi`, the high chi-square value (21254.59) and low p-value (0.000) suggest a strong association.
- For `triage_cat_arrivalmonth`, the chi-square value (20.16) is lower, but the p-value (0.043) is still below the significance threshold of 0.05, indicating a significant association.

---

### <a id = 'tnum'></a> Triage Numerical

#### Triage Vital Sign - Heart Rate:
- **Highest Population Occurrence:** Normal Heart Rate (85.92%)
- **Lowest Population Occurrence:** Critical Heart Rate (0.04%)

**Admission Rates:**
- Highest Admission Rate: Normal Heart Rate (39.08%)
- Lowest Admission Rate: Critical Heart Rate (0.03%)

**Disparities:**
- Disparity: Higher admission rate for Normal Heart Rate compared to the highest population occurrence (Normal Heart Rate), and much lower admission rate for Critical Heart Rate compared to the lowest population occurrence.

#### Triage Vital Sign - Systolic Blood Pressure:
- **Highest Population Occurrence:** Hypertension (High) SBP (48.47%)
- **Lowest Population Occurrence:** Hypotension (Low) SBP (0.60%)

**Admission Rates:**
- Highest Admission Rate: Hypertension (High) SBP (24.85%)
- Lowest Admission Rate: Hypotension (Low) SBP (0.48%)

**Disparities:**
- Disparity: Higher admission rate for Hypertension (High) SBP compared to the highest population occurrence (Hypertension (High) SBP), and much lower admission rate for Hypotension (Low) SBP compared to the lowest population occurrence.

#### Triage Vital Sign - Diastolic Blood Pressure:
- **Highest Population Occurrence:** Normal DBP (51.88%)
- **Lowest Population Occurrence:** Critical DBP (0.74%)

**Admission Rates:**
- Highest Admission Rate: Normal DBP (27.22%)
- Lowest Admission Rate: Critical DBP (0.44%)

**Disparities:**
- Disparity: Higher admission rate for Normal DBP compared to the highest population occurrence (Normal DBP), and much lower admission rate for Critical DBP compared to the lowest population occurrence.

#### Triage Vital Sign - Respiratory Rate:
- **Highest Population Occurrence:** Normal Respiratory Rate (97.35%)
- **Lowest Population Occurrence:** Bradypnea (Low) RR (0.02%)

**Admission Rates:**
- Highest Admission Rate: Normal Respiratory Rate (44.32%)
- Lowest Admission Rate: Bradypnea (Low) RR (0.02%)

**Disparities:**
- Disparity: Higher admission rate for Normal Respiratory Rate compared to the highest population occurrence (Normal Respiratory Rate), and much lower admission rate for Bradypnea (Low) RR compared to the lowest population occurrence.

#### Triage Vital Sign - Body Temperature:
- **Highest Population Occurrence:** Normal Temperature (95.18%)
- **Lowest Population Occurrence:** Fever (High) Temperature (2.01%)

**Admission Rates:**
- Highest Admission Rate: Normal Temperature (43.43%)
- Lowest Admission Rate: Fever (High) Temperature (1.39%)

**Disparities:**
- Disparity: Higher admission rate for Normal Temperature compared to the highest population occurrence (Normal Temperature), and much lower admission rate for Fever (High) Temperature compared to the lowest population occurrence.

#### Interpretation of Chi-Square Test: 
- For `triage_vital_dbp`, the high chi-square value (3217.93) and low p-value (0.00) suggest a strong association.
- For `triage_vital_sbp`, the high chi-square value (1630.35) and low p-value (0.00) suggest a strong association.
- For `triage_vital_temp`, the chi-square value (473.45) is higher, and the p-value (1.56e-103) is much below the significance threshold of 0.05

---

### <a id = 'huse'></a> Patient History and Utilization:
- **Previous Disposition:**
  - **Highest Population Occurrence:** Discharge (42.82%)
  - **Lowest Population Occurrence:** Send to L&D (0.01%)
  
  **Admission Rates:**
  - Highest Admission Rate: Admit (23.24%)
  - Lowest Admission Rate: Send to L&D (0.00%)

  **Disparities:**
  - Disparity: Higher admission rate for Admit compared to the highest population occurrence (Admit), and much lower admission rate for Send to L&D compared to the lowest population occurrence.

- **Number of ED Visits:**
  - **Highest Population Occurrence:** Low Prior Visits (63.10%)
  - **Lowest Population Occurrence:** High Prior Visits (1.02%)

  **Admission Rates:**
  - Highest Admission Rate: Low Prior Visits (30.07%)
  - Lowest Admission Rate: High Prior Visits (0.19%)

  **Disparities:**
  - Disparity: Higher admission rate for Low Prior Visits compared to the highest population occurrence (Low Prior Visits), and much lower admission rate for High Prior Visits compared to the lowest population occurrence.

- **Number of Admissions:**
  - **Highest Population Occurrence:** Low Prior Admissions (49.28%)
  - **Lowest Population Occurrence:** Very High Prior Admissions (0.14%)

  **Admission Rates:**
  - Highest Admission Rate: Low Prior Admissions (26.98%)
  - Lowest Admission Rate: Very High Prior Admissions (0.07%)

  **Disparities:**
  - Disparity: Higher admission rate for Low Prior Admissions compared to the highest population occurrence (Low Prior Admissions), and much lower admission rate for Very High Prior Admissions compared to the lowest population occurrence.

- **Number of Surgeries:**
  - **Highest Population Occurrence:** Low Prior Surgeries (82.52%)
  - **Lowest Population Occurrence:** High Prior Surgeries (0.06%)

  **Admission Rates:**
  - Highest Admission Rate: Low Prior Surgeries (38.64%)
  - Lowest Admission Rate: High Prior Surgeries (0.04%)

  **Disparities:**
  - Disparity: Higher admission rate for Low Prior Surgeries compared to the highest population occurrence (Low Prior Surgeries), and much lower admission rate for High Prior Surgeries compared to the lowest population occurrence.

#### Interpretation of Chi-Square Test: 
- For `huse_previousdispo`, the high chi-square value (8063.54) and low p-value (0.00) suggest a strong association.
- For `huse_n_admissions`, the high chi-square value (3709.72) and low p-value (0.00) suggest a strong association.
- For `huse_n_surgeries`, the chi-square value (609.88) is higher, and the p-value (7.27e-132) is much below the significance threshold of 0.05.
- For `huse_n_edvisits`, the chi-square value (524.73) is higher, and the p-value (2.09e-113) is much below the significance threshold of 0.05.

---

### <a id = 'cc'></a> Chief Complaint

#### Top 20 Medical Conditions by Percentage of Occurrence:
| Variable                 | Percentage of Occurrence |
|--------------------------|---------------------------|
| cc_abdominalpain         | 9.07%                     |
| cc_chestpain             | 8.52%                     |
| cc_other                 | 8.34%                     |
| cc_shortnessofbreath     | 6.79%                     |
| cc_fall                  | 3.97%                     |
| cc_backpain              | 3.30%                     |
| cc_dizziness             | 2.85%                     |
| cc_alteredmentalstatus   | 2.58%                     |
| cc_legpain               | 2.35%                     |
| cc_cough                 | 2.34%                     |
| cc_emesis                | 2.25%                     |
| cc_weakness              | 2.24%                     |
| cc_fall>65               | 1.96%                     |
| cc_alcoholintoxication   | 1.96%                     |
| cc_flankpain             | 1.48%                     |
| cc_elevatedbloodsugar... | 1.37%                     |
| cc_motorvehiclecrash     | 1.35%                     |
| cc_headache-newonset...  | 1.31%                     |
| cc_abnormallab           | 1.31%                     |
| cc_medicalproblem        | 1.24%                     |

#### Bottom 20 Medical Conditions by Percentage of Occurrence:
| Variable              | Percentage of Occurrence |
|-----------------------|---------------------------|
| cc_vaginaldischarge   | 0.05%                     |
| cc_abdominalcramping  | 0.05%                     |
| cc_rectalbleeding     | 0.05%                     |
| cc_faciallaceration   | 0.05%                     |
| cc_pelvicpain         | 0.04%                     |
| cc_motorcyclecrash    | 0.04%                     |
| cc_withdrawal-alcohol | 0.04%                     |
| cc_swallowedforeign...| 0.04%                     |
| cc_cellulitis         | 0.04%                     |
| cc_trauma             | 0.04%                     |
| cc_thumbinjury        | 0.04%                     |
| cc_tickremoval        | 0.03%                     |
| cc_conjunctivitis     | 0.03%                     |
| cc_stdcheck           | 0.03%                     |
| cc_sicklecellpain     | 0.02%                     |
| cc_bodyfluidexposure  | 0.02%                     |
| cc_foreignbodyineye   | 0.02%                     |
| cc_seizures           | 0.01%                     |
| cc_exposuretostd      | 0.01%                     |
| cc_ingestion          | 0.01%                     |

#### Top 20 Medical Conditions by Association Strength:
| Variable1              | Phi Coefficient | P-Value       |
|------------------------|-----------------|---------------|
| cc_shortnessofbreath   | 0.11            | 0.00          |
| cc_alteredmentalstatus | 0.09            | 0.00          |
| cc_chestpain           | 0.07            | 1.03e-241     |
| cc_motorvehiclecrash   | 0.06            | 1.59e-189     |
| cc_weakness            | 0.06            | 1.15e-175     |
| cc_alcoholintoxication | 0.06            | 1.54e-157     |
| cc_backpain            | 0.06            | 5.03e-155     |
| cc_strokealert         | 0.05            | 9.55e-118     |
| cc_abnormallab         | 0.05            | 3.94e-104     |
| cc_kneepain            | 0.04            | 1.64e-93      |
| cc_fever-9weeksto74...| 0.04            | 1.58e-92      |
| cc_rash                | 0.04            | 1.25e-90      |
| cc_sorethroat          | 0.04            | 1.51e-77      |
| cc_gibleeding          | 0.04            | 9.93e-74      |
| cc_breathingdifficulty | 0.04            | 8.24e-73      |
| cc_emesis              | 0.04            | 3.80e-72      |
| cc_fatigue             | 0.04            | 1.80e-68      |
| cc_hypotension         | 0.04            | 2.21e-68      |
| cc_dyspnea             | 0.04            | 1.83e-66      |
| cc_footpain            | 0.04            | 5.60e-64      |

#### Interpretation:
- Conditions like abdominal pain, chest pain, and shortness of breath are highly prevalent in the dataset.
- Medical conditions associated with higher Phi coefficients indicate a stronger association with the dataset, and the p-values confirm the statistical significance of these associations.

---

### <a id = 'pmh'></a> Prior Medical History

#### Top 20 Medical Conditions by Percentage of Occurrence:
| Variable                | Percentage of Occurrence |
|-------------------------|---------------------------|
| pmh_diabmelnoc          | 98.37%                    |
| pmh_htn                 | 76.01%                    |
| pmh_hyperlipidem        | 53.12%                    |
| pmh_unclassified        | 31.19%                    |
| pmh_mooddisorders       | 29.23%                    |
| pmh_esophgealdx         | 27.59%                    |
| pmh_otjointdx           | 23.97%                    |
| pmh_asthma              | 23.62%                    |
| pmh_anxietydisorders    | 22.16%                    |
| pmh_otnutritdx          | 21.99%                    |
| pmh_coronathero         | 21.53%                    |
| pmh_thyroiddsor         | 17.26%                    |
| pmh_dysrhythmia         | 15.92%                    |
| pmh_othnervdx           | 15.88%                    |
| pmh_chrkidneydisease    | 15.00%                    |
| pmh_backproblem         | 14.76%                    |
| pmh_anemia              | 14.52%                    |
| pmh_copd                | 14.48%                    |
| pmh_chfnonhp            | 13.48%                    |
| pmh_acutecvd            | 11.32%                    |

#### Bottom 20 Medical Conditions by Percentage of Occurrence:
| Variable                            | Percentage of Occurrence |
|-------------------------------------|---------------------------|
| pmh_lowbirthwt                      | 0.02%                     |
| pmh_prevcsectn                      | 0.02%                     |
| pmh_earlylabor                      | 0.02%                     |
| pmh_ecodesotherspecifiednec         | 0.02%                     |
| pmh_hemorrpreg                      | 0.01%                     |
| pmh_respdistres                     | 0.01%                     |
| pmh_malgenitca                      | 0.01%                     |
| pmh_otrespirca                      | 0.01%                     |
| pmh_rehab                           | 0.01%                     |
| pmh_ecodesadverseeffectsofmedicalcare| 0.01%                     |
| pmh_amniosdx                        | 0.01%                     |
| pmh_liveborn                        | 0.00%                     |
| pmh_umbilcord                       | 0.00%                     |
| pmh_poisonpsych                     | 0.00%                     |
| pmh_fetaldistrs                     | 0.00%                     |
| pmh_ecodesstruckbyagainst           | 0.00%                     |
| pmh_birthtrauma                     | 0.00%                     |
| pmh_ecodestransportnotmvt           | 0.00%                     |
| pmh_pelvicobstr                     | 0.00%                     |
| pmh_obrelatedperintrauma           | 0.00%                     |

##### Interpretation:

- The chi-square test results indicate significant associations between various medical conditions and the dataset.

- Conditions such as congestive heart failure (`pmh_chfnonhp`), chronic kidney disease (`pmh_chrkidneydisease`), coronary atherosclerosis (`pmh_coronathero`), hypertension (`pmh_htn`), dysrhythmia (`pmh_dysrhythmia`), and acute cardiovascular disease (`pmh_acutecvd`) show very high chi-square values (indicating strong associations) and extremely low p-values (statistical significance).

- Medical conditions like acute myocardial infarction (`pmh_acutemi`), conduction disorders (`pmh_conduction`), and delirium, dementia, amnestic, and other cognitive disorders (`pmh_deliriumdementiaamnesticothercognitiv`) also exhibit strong associations with the dataset, as evident from their high chi-square values and very low p-values.

- Attention deficit, conduct, disruptive behavior, and impulse control disorders (`pmh_attentiondeficitconductdisruptivebeha`) and asthma (`pmh_asthma`) are conditions with notable associations, supported by high chi-square values and low p-values.

- Conditions such as other hematologic disorders (`pmh_othematldx`), hyperlipidemia (`pmh_hyperlipidem`), and disorders of the circulatory system, not elsewhere classified (`pmh_otcirculdx`), although highly prevalent, show strong associations with the dataset, as reflected in their chi-square values and p-values.

- The statistical significance of these associations is confirmed by the very low p-values, further supporting the reliability of the observed relationships between these medical conditions and the dataset.


### <a id = 'meds'></a> Medication Categories and Admission Rates Analysis:
#### Percentage Distribution for `meds_antihyperglycemics`:
- **no_antihyperglycemics (73.17%):** A significant portion of the population in the dataset is not prescribed antihyperglycemic medications.
- **1-to-2_antihyperglycemics (22.28%):** A substantial percentage is prescribed a moderate number (1 to 2) of antihyperglycemic medications.
- **3-to-6_antihyperglycemics (4.55%):** A smaller percentage is prescribed a higher number (3 to 6) of antihyperglycemic medications.
- **7-plus_antihyperglycemics (0.00%):** Almost negligible percentage is prescribed seven or more antihyperglycemic medications.

#### Percentage Admission for `meds_antihyperglycemics`:
- **1-to-2_antihyperglycemics (18.50%):** Among those prescribed 1 to 2 antihyperglycemic medications, a notable percentage is admitted.
- **3-to-6_antihyperglycemics (4.07%):** Among those prescribed 3 to 6 antihyperglycemic medications, a smaller percentage is admitted.
- **7-plus_antihyperglycemics (0.00%):** No admissions are reported for those prescribed seven or more antihyperglycemic medications.
- **no_antihyperglycemics (23.39%):** Among those not prescribed antihyperglycemics, a significant percentage is admitted.


#### Percentage Distribution for `meds_anti-obesitydrugs`:
- **0.0 (99.97%):** The overwhelming majority of the population is not prescribed anti-obesity drugs.
- **1.0 (0.03%):** A very small percentage is prescribed anti-obesity drugs.


#### Percentage Admission for `meds_anti-obesitydrugs`:
- **0.0 (45.95%):** Among those not prescribed anti-obesity drugs, a significant percentage is admitted.
- **1.0 (0.02%):** A very small percentage of those prescribed anti-obesity drugs is admitted.


#### Percentage Distribution for `meds_hormones`:
- **no_hormones (95.04%):** The majority of the population is not prescribed hormones.
- **1-to-2_hormones (4.91%):** A smaller percentage is prescribed a moderate number (1 to 2) of hormones.
- **3-plus_hormones (0.05%):** A very small percentage is prescribed three or more hormones.

#### Percentage Admission for `meds_hormones`:
- **1-to-2_hormones (4.47%):** Among those prescribed 1 to 2 hormones, a small percentage is admitted.
- **3-plus_hormones (0.04%):** A very small percentage of those prescribed three or more hormones is admitted.
- **no_hormones (41.45%):** Among those not prescribed hormones, a significant percentage is admitted.


#### Interpretation of Chi-Square Test: 
- For `meds_antihyperglycemics`, the high chi-square value (22847.47) and low p-value (0.00) suggest a strong association.
- For `meds_anti-obesitydrugs`, the chi-square value (3.35) is higher, and the p-value (0.07) is slightly above the significance threshold of 0.05.
- For `meds_hormones`, the high chi-square value (4514.10) and low p-value (0.00) suggest a strong association.


---

### <a id = 'glu'></a> Glucose Level History and Admission Rates:
#### `hist_glucose_median`:
  - **Percentage Distribution:**
    - Normal: 77.01%
    - .>200 (high): 15.81%
    - .>300 (very high): 7.17%
  - **Admission Rates:**
    - .>200 (high): 7.03%
    - .>300 (very high): 3.45%
    - Normal: 35.53%
  - **Disparities:**
    - Higher admission rate for >200 (high) glucose level (15.81%) and >300 (very high) glucose level (7.17%), and much lower admission rate for Normal glucose level (77.01%).

#### Interpretation of Chi-Square Test: 
- For `hist_glucose_median`, the chi-square value (31.41) is higher, and the p-value (1.51e-07) is much below the significance threshold of 0.05.

---
### <a id = 'conc'></a> Conclusion:

- In general, it seems as though all of the different super columns are significantly related to the target variable (hospital admission) for diabetic patients. There doesn't seem to be huge apparent disparities when it comes to overall demographic data. 
---
