Protocol for analysis of comorbidity using SAIL data
================
David A McAllister
2018-12-21

Personnel
=========

The lead for this project is David McAllister (Wellcome Trust Intermediate Clinical Fellow and Beit Fellow, Senior Clinical Lecturer in Epidemiology in the University of Glasgow and Consultant in Public Health Medicine, NHS Information Services Division, National Services Scotland). He, or a postdoctoral researcher he employs at the University of Glasgow, will conduct the analysis.

Methodological support will be provided by Sofia Dias (Professor of Health Technology, University of York). She will not work directly with the data, and so will not need access to the SAIL safe haven.

Dr Peter Hanlon, an academic primary care doctor will also conduct data analysis.

Defining comorbidity
====================

The following text on defining comorbidity is taken from the for protocol defining comorbidity in trial data. We have not, generally, changed the wording to reflect the fact that these definitions will be used in a different setting (eg changing the terminology from participants to patients) in order to make this section as close as possible to a simple “mirror” of the same section in the protocol for analysing trial data.

Concomitant medications based definitions
-----------------------------------------

We will use concomitant medications to identify comorbid conditions.

Previous studies have also used the WHO ATC criteria to define comorbid diseases, but usually in routine healthcare data with the goal being descriptive epidemiology, as in a recent paper by Huber et al.(1) We are not aware of any previous study which has used this approach for individual-level participant data from clinical trials, or to examine heterogeneity of treatment effects. To reduce non-differential misclassification bias, we have chosen definitions which we think favour specificity over sensitivity. (Table 1).

For each of the drug-based definitions in Table 1, reported concomitant medications are eligible if they were started at any time on or before starting the trial drug (or comparator) regardless of when they were stopped. Topical drugs are not included in the definitions except for M02 or S01E. Nor drugs with an inhaled or nebulised route of administration, except for R03 drugs.

This approach to defining comorbidities is a compromise between sensitivity and specificity and some misclassification is inevitable, reflecting the difficulty of inferring diagnoses from drug-usage. We have attempted to minimise the misclassification based on our understanding of clinical practice.

For example, rather than assuming all participants taking a drug in the A02B class have an acid-related disorder (Table 1) we have limited this definition to exclude participants also taking non-steroidal drugs or any drug with anti-thrombotic actions (aspirin, antiplatelets, warfarin etc). Similarly, we have not used aspirin to define cardiovascular disease because it is in widespread use for primary prevention.(2)

Moreover, while the ATC system is organised around therapeutic indications, not all indications are coded. This is because “A medicinal substance can be given more than one ATC code **ONLY** if it is available in two or more strengths or routes of administration with clearly different therapeutic uses.”(3) For example, finasteride is classified as a dermatological drug if low-dose and as a drug for benign prostatic hyperplasia if high-dose. Therefore, for a single strength and route of administration, there is only “one code, the main indication being decided on the basis of the available information.” (3)

Moreover, the “main” WHO ATC indication is not necessarily the commonest indication. For example, in a US study of drug “mentions” in a representative database, &gt;80% of mentions for gabapentin and amitriptyline were for off-label indications, predominantly pain.(4) Similarly, in a Canadian study of antidepressant use in primary care, amitriptyline was “almost exclusively prescribed for off-label indications” most commonly for pain, insomnia, and migraine.(5) These published findings are consistent with the clinical observation of members of our steering committee (and an independent epileptologist), that these drugs are predominantly used for pain. Despite this, the WHO ATC scheme does not include pain as an indication for these drugs, classifying gabapentin and pregabalin exclusively as antiepileptics and amitriptyline exclusively as an antidepressant.

Nor is there necessarily a code where routes/strengths do differ. For example, prochlorperazine is defined solely as an antipsychotic, despite being available in a buccal preparation for nausea. IN this case the accompanying note states that “The substances in this group are sometimes used for other indications in much lower doses”.

We have attempted to incorporate these nuances into the drug-based comorbidity definitions given in Table 1.

An additional complexity is caused by the fact that for certain trials, sponsors have only provided less specific codes (eg 3 or 4-character codes) and not 5-character codes which uniquely identify each class (7-character codes identifying each agent). Where this is the case, but the drug name with or without route and indication information have been provided, we will assign each potentially-relevant drug to a WHO ATC code using the US Government drug meta-thesaurus (RXNORM). Where neither the drug name, nor sufficiently detailed drug-class information is provided, we will adopt a workaround suited to each definition (Table 1). The number of trials where this approach was needed will be reported.

The proportion of participants with and without comorbid diseases based on concomitant medications with and without relevant medical histories (in trials where these have been provided) will be compared in 2x2 contingency tables. We expect to find a higher proportion with the relevant condition from the reported medical history among those participants meeting the concomitant medication definitions (eg 80% versus 10% reporting diabetes in participants taking/not taking antidiabetic medications).

We had initially planned to add skin disease to the list of diagnoses, however we found that topical therapies were very poorly recorded in the trial data and so have opted to drop this from the comorbid disease definitions.

We mapped the ATC codes to Read codes (which are used in the SAIL data) offline, using the NHS Business Authority mappings and, for some more recent drugs such as novel antidiabetic drugs, by manually mapping between ATC and Read codes. The mapping was very good, even retaining information on route. For example the read code for topical beclomethasone preparations mapped to different ATC codes to those for oral preparations.

### Table 1 Concomitant medication classes - first 6 rows only

| Condition                                                             | ATC codes | ATC label                        | Exceptions/more specific definitions/notes                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:----------|:---------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acid related disorders                                                | A02A      | ANTACIDS                         |                                                                                                                                                                                                                                      |
|                                                                       | A02B      | DRUGS FOR ACID RELATED DISORDERS | Exclude where also taking M01A ANTIINFLAMMATORY AND ANTIRHEUMATIC PRODUCTS, NON-STEROIDS, or B01 (antithrombotic) drugs                                                                                                              |
| Diabetes mellitus                                                     | A10       | DRUGS USED IN DIABETES           | Note this includes insulins and analogues, other blood glucose lowering drugs etc. It does not include cardiovascular prevention drugs We do not exclude metformin, although this is used to treat Polycystic ovary syndrome (PCOS). |
| Thromboembolic disease, atrial fibrillation or valvular heart disease | B01AA     | Vitamin K antagonists            | Do not include if only 4-level codes are available.                                                                                                                                                                                  |
|                                                                       | B01AE     | Direct thrombin inhibitors       | Do not include if only 4-level codes are available.                                                                                                                                                                                  |
|                                                                       | B01AF     | Direct factor Xa inhibitors      | Do not include if only 4-level codes are available.                                                                                                                                                                                  |

Height and weight
-----------------

We will use body mass index (BMI) where this is provided, or calculate it from the weight and height (weight in kg/height in meters-squared). Where multiple BMI measures are available, we will use the most recent BMI measurement prior to the initiation of the intervention. BMI will be standardised to the BMI in the adult population from NHANES 2015-16 (see Blood Pressure section for details). We will treat BMI as a continuous variable in the modelling.

Blood pressure
--------------

In the largest study of blood pressure, a meta-analysis of 958,074 participants from 61 prospective studies, mid-blood pressure (0.5 x DBP + 0.5 x SBP) performed slightly better than SBP alone for both stroke and ischaemic heart disease risk.(6) Consequently, we will use this measure in our models.

In a simulation study, with SBP as the outcome variable, Tobin et al demonstrated that adding a suitable constant (eg 10mmHg) for patients taking anti-hypertensive reduced bias as well as any of several more complex methods, whereas including a dummy variable for treatment introduced bias.(7) We will use this approach for SBP as a covariate in the covariate-treatment interaction models, under the assumption that the true underlying blood pressure is most relevant to the analysis. We will similarly add a constant of 5 mmHg to the diastolic blood pressure. Both constants will be added prior to calculating the mid-blood pressure.

If a participant is taking a drug from any of the following drug classes prior to initiating the study drug we will perform the correction; C02 – ANTIHYPERTENSIVES, C07 - beta-Adrenergic Blocking Agents, C08 - CALCIUM CHANNEL BLOCKERS or C09 - AGENTS ACTING ON THE RENIN-ANGIOTENSIN SYSTEM. We will perform the correction only once regardless of the number of different antihypertensive drugs any participant is taking, and regardless of whether the drug was given for hypertension or a different indication (eg a calcium channel blocker for angina).

Since blood pressure shows considerable within-person variability, we will take the mean of all measures obtained prior to initiation of the drug (ie those from screening and randomisation visits). Having done so we will standardise the blood pressure results to the adult blood pressure results from NHANES 2015-16 (Table 2).

### Table 2 Adult (aged &gt;=18) NHANES 2015-16 blood pressure averaged over (up to) 3 recordings

| Blood Pressure | Mean | Standard deviation |
|----------------|------|--------------------|
| Diastolic      | 70   | 12                 |
| Systolic       | 123  | 17                 |

For data see [*https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015*](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015).

Laboratory test based definitions
=================================

Liver impairment
----------------

We will use the Fibrosis-4 (FIB4) index to examine for the presence of liver disease. FIB4 will be calculated as follows:-

$$FIB4 = \\frac{age \\times AST}{platelet count\\times \\sqrt{ALT}} $$

Age is measured in years, AST and ALT in international units per litre and platelet counts as 10^9 platelets per litre.

This will not be calculated for patients with anaemia or known inflammatory diseases, which for the purposes of this analysis we will define as the inflammatory arthropathies and inflammatory bowel diseases. We will not include conditions which feature lower levels of systemic inflammation (eg metabolic syndrome, COPD). Operationally, any participant meeting the drug-based definition for “Inflammatory arthropathies, inflammatory bowel disease, systemic lupus erythematosus and connective tissue diseases” will not have a FIB4 calculated. For trials where inflammatory arthropathies or inflammatory bowel diseases conditions are indications, the FIB4 will not be estimated. Where these are comorbidities (defined as per concomitant medications based definitions), the participant will be assigned the median FIB4 value for the trial.

FIB4 will be standardised to FIB4 derived from component variables recorded in NHANES 2015-16 and modelled as a continuous variable.

Renal impairment
----------------

Some of the trials may have been conducted in countries or sites where creatinine levels have not been standardised to an isotope dilution mass spectrometry (IDMS) reference measurement procedure. Therefore we will use the “Creatinine Standardization Recommendations (for countries or regions that are introducing or have not completed standardization of creatinine calibration)” from the NIDDK recommendations (<https://www.niddk.nih.gov/health-information/communication-programs/nkdep/laboratory-evaluation/glomerular-filtration-rate/creatinine-standardization/recommendations>).

This means that we will use the “Original Modification of Diet in Renal Disease (MDRD) Study equation for routine methods that have not been calibrated to be traceable to IDMS” and the “CKD-EPI or IDMS-traceable MDRD Study equation for estimating GFR in adults” for laboratory results where the creatinine measurement “has its calibration traceable to IDMS”. For consistency, we will use the IDMS-traceable MDRD Study equation (GFR (mL/min/1.73 m2) = 175 × (Scr)<sup>-1.154</sup> × (Age)<sup>-0.203</sup> × (0.742 if female) × (1.212 if African American) in the latter case.

The eGFR estimated from either method is normalized to 1.73 m² body surface area. As per the NIDDK guidance for providers (<https://www.niddk.nih.gov/health-information/professionals/clinical-tools-patient-education-outreach/ckd-drug-dosing-providers>) we will adjust for body surface area for people who are “very large or very small”. We will define these groups as having a height, weight or BMI below the 10<sup>th</sup> or above the 90<sup>th</sup> centile based on data from NHANES 2015-2016.

### Table 3 Quantiles for Height and Weight for NHANES 2015-2016

| Quantile                   | Weight (kg) | Height (cm) | BMI |
|----------------------------|-------------|-------------|-----|
| 10<sup>th</sup> percentile | 58          | 155         | 22  |
| 90<sup>th</sup> percentile | 111         | 182         | 38  |

For data see <https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015>

We estimate body surface area using the Mosteller equation(8) and use this to adjust the eGFR as per the NIDDK recommendation (eGFR/1.73m<sup>2</sup> x estimated BSA = eGFR).

Having derived the eGFR we will standardise this to eGFR derived from creatinine measured in NHANES 2015-16 using the IDMS-traceable MDRD Study equation (as the creatinine measure in NHANES is IDMS-standardised) and model it as a continuous variable.

Although for clinical reporting eGFR levels above 60 are simply reported as “&gt;=60” we will not similarly truncate our values, as we are allowing for non-linearity in the modelling.

Anaemia
-------

Since the relationship between haemoglobin and disease states is markedly non-linear (with haemoglobin levels above and below the normal range considered abnormal), we will model haemoglobin using a dichotomous variable for anaemia present/absent, and use an additional continuous term for the severity of anaemia. We propose to define anaemia as per the WHO definitions (<http://apps.who.int/iris/bitstream/10665/85839/3/WHO_NMH_NHD_MNM_11.1_eng.pdf> ). This defines anaemia using Hb in g/dl as follows.

### Table 4 Anaemia

|                                | Not anaemia | Mild anaemia | Moderate anaemia |
|--------------------------------|-------------|--------------|------------------|
| Non-pregnant women (≥15 years) | ≥12         | &lt;12       | &lt;11           |
| Men (≥15 years)                | ≥13         | &lt;13       | &lt;11           |

We will use the “Not anaemia” threshold to define anaemia as present/absent. For the continuous component of the variable we will standardise Haemoglobin to the NHANES 2015-16 laboratory results (<https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Laboratory&CycleBeginYear=2015>).

Diagnostic code mapping
-----------------------

Each of the diagnoses above has been mapped to the closest available WHO ICD-10 codes and US Clinical Classifications Software codes.(11) The latter is an established aggregation system for ICD-10CM and ICD-10 codes for use in health services research.

Statistical analysis
====================

Prevalence of separate comorbidities
------------------------------------

For each condition, we will estimate the prevalence of each comorbidity using simple proportions. Continuous variables, unless specified otherwise above, will be dichotomised at the 75<sup>th</sup> centile.

Comorbidity count
-----------------

We will calculate a comorbidity count for each patient based on obesity, renal impairment, liver impairment, anaemia and each of the concomitant medicine derived terms. Although there are a number of comorbidity counting methods described in the existing literature, the coefficients for these were derived based on the prediction of outcomes such as healthcare utilisation and/or mortality.(10) We are not aware of any comorbidity score with weightings based on treatment efficacy. Consequently, we will use a simple summation of the categorical (0/1) and continuous variables, with a view to capturing a measure of the total “multimorbid” burden. For continuous variables, we will standardise the variable so that the 75<sup>th</sup> centile is scored 1 and the 25<sup>th</sup> centile scored zero.

For the comorbidity count calculation, the concomitant medication definition pairs will be collapsed into a single condition.

### Table 5 Combining concomitant medication based definitions

| Definition 1 | Definition 2             |
|--------------|--------------------------|
| Pain         | Migraine                 |
| Pain         | Rheumatologic conditions |

We will summarise these counts as the proportion of patients with each comorbidity count, stratified by index condition, age and sex.

For the main comparison between trial and primary care data we will use the concomitant medication based definitions. This is because the recording of BMI, blood pressure, AST, ALT, platelets and haemoglobin are likely to be less consistent and less reliably coded than concomitant medication definitions. The non-concomitant medication based components will be included in secondary analysis if these are found to be recorded in a reasonable proportion of patients. We will identify the Read codes for these components in an iterative process, to attempt to obtain the most complete data available.

Estimate incidence of subsequent events
---------------------------------------

We will choose one or more index condition(s) for this analysis where that condition is common, where comorbidity among people with that condition is also common, and where there is some evidence from my (separate) analysis of trial data that treatment efficacy may differ by comorbidity status.

For these selected index conditions, we will fit time to event models for events of interest (hospitalisations and deaths). We will fit Cox proportional hazard models (or possibly parametric survival models) treating competing events as censoring events (ie these are cause-specific hazard ratios). We will include age, sex and comorbidities in the modelling. Continuous measures of comorbidity (eg FIB-4) will be treated as continuous variables, with fractional polynomials or cubic splines to allow for non-linearity. We will include main terms and interactions only where these both improve model fit and have an appreciable effect size (eg a hazard ratio of less than 0.96 or more than 1.04 for binary variables/per standard deviation in continuous variables).

Where small numbers of participants have a comorbidity we will drop that from the main analysis. We will also explore whether inclusion of specific comorbidities or comorbiditity counts (as a score) is a better predictor of subsequent events.

Summarise comorbidity correlations
----------------------------------

If time permits we will also estimate correlations between comorbidities in hierarchical multivariate probit models. The models will include age, sex and index condition as covariates and will be fit in a Bayesian framework using an approach similar to that described by Pollock et al (12). The output of this work will be in the form of network diagrams illustrating the correlation between comorbidities for different index conditions.

Time period for analysis
------------------------

We conducted a preliminary inspection of the SAIL data to determine the number of patients with a prescription for **any** of the drugs of interest (including "excluded" drugs aspirin, amitriptyline etc). This was done prior to examining specific comorbid conditions, it was also done prior to identifying which patients had the index conditions (and indeed prior to specifying the Read codes for the index conditions). On conducting this analysis we found that the number of patients was low prior to 2010 and plateaued in 2011. For this reason we specified the 2011 to 2012 time period to identify concomitant diseases.

After this analysis, we identified an error in the concomitant medication coding (a three character ATC code was inadvertently treated as a 4-character ATC code) and updated the definitions accordingly. This was done at the same time that the Read code definitions of index conditions were written (see below). Both the Read code definitions of index conditions and the updated concomitant medication definitions will be uploaded to the SAIL platform together. As such, this change in drug-definitions was done prior to identifying the patients who have each index condition.

Denominator population
----------------------

The denominator population will be defined as those patients identified as being registered with a GP (defined using the SAIL algorithm for defining registered patients) throughout all of 2011. Of these, each patient will be assigned to one or more index conditions (Table 6) according to the list of Read codes at the foot of this document (Table A1). The patients will be defined as having the diagnosis if these codes were recorded in any of the records. For all of the index conditions except myocardial infarction and arthroplasty we will not impose any time restrictions. We chose not to do so as these are all chronic diseases.

In a sensitivity analysis we will also include in the denominator those patients who were not registered throughout 2011 because they died during that year. Lower comorbidity counts in the primary care population could result from including such patients (because a prescription may not have been issued during the period when they were alive) or excluding such patients (because these are likely to be the sickest patients). Therefore, we opted to exclude them for the main analysis because patients expected to die within a year would be unlikely to be included in many clinical trials.

We derived our read codes from existing code lists whenever these were available. Sources included QOF Read codes as well as non-QOf lists from [ClinicalCodes.org](https://clinicalcodes.rss.mhs.man.ac.uk/) as well as codes from the [Barnett et al 2012](https://doi.org/10.1016/S0140-6736(12)60240-2) paper.

Note that the groups are not necessarily mutually exclusive as some patients will have more than one of the eligible diagnoses.

Table 6 List of index conditions
--------------------------------

| Condition                                 |  Number of Read codes|
|:------------------------------------------|---------------------:|
| Alzheimer's Disease                       |                     9|
| Asthma                                    |                    85|
| Atrial Fibrillation                       |                    11|
| Axial Spondyloarthritis                   |                     5|
| Benign Prostatic Hyperplasia              |                     5|
| Chronic Idiopathic Urticaria (CIU)        |                     1|
| Dementia (any)                            |                    52|
| Diabetes Mellitus, Type 2                 |                    50|
| Epilepsy                                  |                    98|
| Erectile dysfunction                      |                    19|
| Hypertension                              |                    61|
| Hypertension, Pulmonary                   |                     3|
| Inflammatory bowel disease                |                    44|
| Migraine                                  |                    38|
| Osteoarthritis                            |                   128|
| Osteoporosis                              |                    71|
| Parkinson's disease (all)                 |                    21|
| Parkinson's disease (excluding secondary) |                    11|
| Psoriasis                                 |                    31|
| Psoriatic arthropathy                     |                     7|
| Pulmonary Disease, Chronic Obstructive    |                    45|
| Pulmonary fibrosis                        |                    12|
| Restless legs syndrome                    |                     1|
| Rheumatoid arthritis                      |                    51|
| Systemic Lupus Erythematosus              |                    12|
| Thromboembolism                           |                    95|

Where there are multiple definitions in the above table (eg Dementia (Alzheimer's) and Dementia (any), the following definitions will be used for the primary and secondary analyses respectively.

Table 7 Multiple diagnostic criteria, primary and secondary analyses
--------------------------------------------------------------------

| Primary analysis                          | Secondary analysis        |
|-------------------------------------------|---------------------------|
| Alzheimer's Disease                       | Dementia (any)            |
| Parkinson's disease (excluding secondary) | Parkinson's disease (all) |

We have generally avoided using drugs as part of the definition of index conditions to avoid the risk of biasing the findings towards patients who are more likely to be prescribed drugs, by making having received a drug part of the inclusion criterion. However, in the case of migraine, the definition includes one or more of the listed Read codes for migraine **as well** as a prescription for a migraine drug (WHO ATC code N02C, as per the concomitant medication analysis). Similarly, we required the thromboembolism definition to include a prescription of an anticoagulant drug (B01AA, B01AE or B01AF as per the concomitant medication analysis.)

Two of the index diagnoses relate to events rather than chronic illnesses; myocardial infarction and arthroplasty (knee and hip). These episodes will be defined using hospital episode data (coded via ICD10 and OPCS respectively.) The codes for myocardial infarction are ICD-10 codes I21 and I22. The codes for hip and knee arthroplasty are those described by The National Joint Registry (NJR) as being suitable for translating NJR procedures into OPCS codes (<http://www.njrcentre.org.uk/njrcentre/Portals/0/Documents/England/Data%20collection%20forms/OPCS%20Procedure%20codes%20relevant%20to%20NJRv4.pdf>) (Table A2). In both cases we will define the patient as having the index condition if any of the relevant codes were included in any position from 2012-01-01 to 2012-12-01 for patients defined as being in the denominator population. We had previously selected a 3-month period but opted to extend this to include more patients. This decision was taken before calculating comorbidity counts for myocardial infarction adn/or hip arthroplasty.

Age and sex standardisation
===========================

In the primary analysis we will compare comorbidity counts in the SAIL and trial datasets having standardised the SAIL data to the number of trial participants with each indication in each age and sex band. Briefly, for each indication, we will apply proportions with each comorbidity count for each age and sex specific stratum to the age and sex distribution in the trial data to get the expected comorbidity counts for each stratum, then sum this across strata. This is analogous to direct standardisation. As the numbers are expected to be large, we do not plan to estimate confidence intervals for the main analysis.

The trial-specific strata will be obtained from summary statistics for the sex-specific age distributions from each trial. The age distributions have been summarised using truncated normal distributions. These distributions were used in preference to simple counts to avoid concerns about disclosiveness (eg if only 5 patients were aged &lt;40 in a trial, this could in theory be disclosive). The truncated normal distribution was found to describe the distribution well for all of the trials. A truncated normal distribution was chosen over a normal distribution to reflect the fact that many trials impose age cut-offs for trial participation.

References
==========

1.  Huber CA, Szucs TD, Rapold R, Reich O. Identifying patients with chronic conditions using pharmacy data in Switzerland: an updated mapping approach to the classification of medications. BMC Public Health. 2013 Oct 30;13:1030.

2.  Stuntz M, Bernstein B. Recent trends in the prevalence of low-dose aspirin use for primary and secondary prevention of cardiovascular disease in the United States, 2012–2015. Prev Med Rep. 2016 Dec 28;5:183–6.

3.  WHO Collaborating Centre for Drug Statistics Methodology. ATC classification index with DDDs. 2015.

4.  Radley DC, Finkelstein SN, Stafford RS. Off-label prescribing among office-based physicians. Arch Intern Med. 2006 May 8;166(9):1021–6.

5.  Wong J, Motulsky A, Abrahamowicz M, Eguale T, Buckeridge DL, Tamblyn R. Off-label indications for antidepressants in primary care: descriptive study of prescriptions from an indication based electronic prescribing system. BMJ. 2017 Feb 21;356:j603.

6.  Age-specific relevance of usual blood pressure to vascular mortality: a meta-analysis of individual data for one million adults in 61 prospective studies. The Lancet. 2002 Dec 14;360(9349):1903–13.

7.  Tobin Martin D., Sheehan Nuala A., Scurrah Katrina J., Burton Paul R. Adjusting for treatment effects in studies of quantitative traits: antihypertensive therapy and systolic blood pressure. Stat Med. 2005 Sep 8;24(19):2911–35.

8.  Mosteller RD. Simplified calculation of body-surface area. N Engl J Med. 1987 Oct 22;317(17):1098.

9.  Royston P. The use of fractional polynomials to model interactions between treatment and continuous covariates in clinical trials. In: ResearchGate \*I**n**t**e**r**n**e**t* . *c**i**t**e**d*2018*A**p\*\*r\*6 . Available from: [https://www.researchgate.net/publication/4998077\\\_The\\\_use\\\_of\\\_fractional\\\_polynomials\\\_to\\\_model\\\_interactions\\\_between\\\_treatment\\\_and\\\_continuous\\\_covariates\\\_in\\\_clinical\\\_trials](https://www.researchgate.net/publication/4998077_The_use_of_fractional_polynomials_to_model_interactions_between_treatment_and_continuous_covariates_in_clinical_trials)

10. Yurkovich M, Avina-Zubieta JA, Thomas J, Gorenchtein M, Lacaille D. A systematic review identifies valid comorbidity indices derived from administrative health data. J Clin Epidemiol. 2015 Jan;68(1):3–14.

11. Agency for Healthcare Research and Quality. Clinical Classifications Software for ICD-10 Data \*I**n**t**e**r**n**e**t* . 2012 *c**i**t**e**d*2015*D**e\*\*c\*31 . Available from: [http://www.ahrq.gov/research/data/hcup/icd10usrgd.html\\\#elix](http://www.ahrq.gov/research/data/hcup/icd10usrgd.html#elix)

12. Pollock, Laura J., Reid Tingley, William K. Morris, Nick Golding, Robert B. O’Hara, Kirsten M. Parris, Peter A. Vesk, and Michael A. McCarthy. “Understanding Co-Occurrence by Modelling Species Simultaneously with a Joint Species Distribution Model (JSDM).” Methods in Ecology and Evolution 5, no. 5 (May 1, 2014): 397–406. <https://doi.org/10.1111/2041-210X.12180>.

Appendix Diagnostic codes
=========================

Table A1 Read codes for index diagnoses
---------------------------------------

| Read code | Description                                                                                                           | Condition                                 |
|:----------|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| 66h..     | Dementia monitoring                                                                                                   | Dementia (any)                            |
| 6AB..     | Dementia annual review                                                                                                | Dementia (any)                            |
| E000.     | Uncomplicated senile dementia                                                                                         | Dementia (any)                            |
| E001.     | Presenile dementia                                                                                                    | Dementia (any)                            |
| E0010     | Uncomplicated presenile dementia                                                                                      | Dementia (any)                            |
| E0011     | Presenile dementia with delirium                                                                                      | Dementia (any)                            |
| E0012     | Presenile dementia with paranoia                                                                                      | Dementia (any)                            |
| E0013     | Presenile dementia with depression                                                                                    | Dementia (any)                            |
| E001z     | Presenile dementia NOS                                                                                                | Dementia (any)                            |
| E002.     | Senile dementia with depressive or paranoid features                                                                  | Dementia (any)                            |
| E0020     | Senile dementia with paranoia                                                                                         | Dementia (any)                            |
| E0021     | Senile dementia with depression                                                                                       | Dementia (any)                            |
| E002z     | Senile dementia with depressive or paranoid features NOS                                                              | Dementia (any)                            |
| E003.     | Senile dementia with delirium                                                                                         | Dementia (any)                            |
| E004.     | Arteriosclerotic dementia                                                                                             | Dementia (any)                            |
| E0040     | Uncomplicated arteriosclerotic dementia                                                                               | Dementia (any)                            |
| E0041     | Arteriosclerotic dementia with delirium                                                                               | Dementia (any)                            |
| E0042     | Arteriosclerotic dementia with paranoia                                                                               | Dementia (any)                            |
| E0043     | Arteriosclerotic dementia with depression                                                                             | Dementia (any)                            |
| E004z     | Arteriosclerotic dementia NOS                                                                                         | Dementia (any)                            |
| E012.     | Other alcoholic dementia                                                                                              | Dementia (any)                            |
| E02y1     | Drug-induced dementia                                                                                                 | Dementia (any)                            |
| E041.     | Dementia in conditions EC                                                                                             | Dementia (any)                            |
| Eu00.     | \[X\]Dementia in Alzheimer's disease                                                                                  | Dementia (any)                            |
| Eu000     | \[X\]Dementia in Alzheimer's disease with early onset                                                                 | Dementia (any)                            |
| Eu001     | \[X\]Dementia in Alzheimer's disease with late onset                                                                  | Dementia (any)                            |
| Eu002     | \[X\]Dementia in Alzheimer's dis, atypical or mixed type                                                              | Dementia (any)                            |
| Eu00z     | \[X\]Dementia in Alzheimer's disease, unspecified                                                                     | Dementia (any)                            |
| Eu01.     | \[X\]Vascular dementia                                                                                                | Dementia (any)                            |
| Eu010     | \[X\]Vascular dementia of acute onset                                                                                 | Dementia (any)                            |
| Eu011     | \[X\]Multi-infarct dementia                                                                                           | Dementia (any)                            |
| Eu012     | \[X\]Subcortical vascular dementia                                                                                    | Dementia (any)                            |
| Eu013     | \[X\]Mixed cortical and subcortical vascular dementia                                                                 | Dementia (any)                            |
| Eu01y     | \[X\]Other vascular dementia                                                                                          | Dementia (any)                            |
| Eu01z     | \[X\]Vascular dementia, unspecified                                                                                   | Dementia (any)                            |
| Eu02.     | \[X\]Dementia in other diseases classified elsewhere                                                                  | Dementia (any)                            |
| Eu020     | \[X\]Dementia in Pick's disease                                                                                       | Dementia (any)                            |
| Eu021     | \[X\]Dementia in Creutzfeldt-Jakob disease                                                                            | Dementia (any)                            |
| Eu022     | \[X\]Dementia in Huntington's disease                                                                                 | Dementia (any)                            |
| Eu023     | \[X\]Dementia in Parkinson's disease                                                                                  | Dementia (any)                            |
| Eu024     | \[X\]Dementia in human immunodef virus \[HIV\] disease                                                                | Dementia (any)                            |
| Eu025     | \[X\]Lewy body dementia                                                                                               | Dementia (any)                            |
| Eu02y     | \[X\]Dementia in other specified diseases classif elsewhere                                                           | Dementia (any)                            |
| Eu02z     | \[X\] Unspecified dementia                                                                                            | Dementia (any)                            |
| Eu041     | \[X\]Delirium superimposed on dementia                                                                                | Dementia (any)                            |
| F110.     | Alzheimer's disease                                                                                                   | Dementia (any)                            |
| F1100     | Alzheimer's disease with early onset                                                                                  | Dementia (any)                            |
| F1101     | Alzheimer's disease with late onset                                                                                   | Dementia (any)                            |
| F111.     | Pick's disease                                                                                                        | Dementia (any)                            |
| F112.     | Senile degeneration of brain                                                                                          | Dementia (any)                            |
| F116.     | Lewy body disease                                                                                                     | Dementia (any)                            |
| Fyu30     | \[X\]Other Alzheimer's disease                                                                                        | Dementia (any)                            |
| Eu00.     | \[X\]Dementia in Alzheimer's disease                                                                                  | Alzheimer's Disease                       |
| Eu000     | \[X\]Dementia in Alzheimer's disease with early onset                                                                 | Alzheimer's Disease                       |
| Eu001     | \[X\]Dementia in Alzheimer's disease with late onset                                                                  | Alzheimer's Disease                       |
| Eu002     | \[X\]Dementia in Alzheimer's dis, atypical or mixed type                                                              | Alzheimer's Disease                       |
| Eu00z     | \[X\]Dementia in Alzheimer's disease, unspecified                                                                     | Alzheimer's Disease                       |
| F110.     | Alzheimer's disease                                                                                                   | Alzheimer's Disease                       |
| F1100     | Alzheimer's disease with early onset                                                                                  | Alzheimer's Disease                       |
| F1101     | Alzheimer's disease with late onset                                                                                   | Alzheimer's Disease                       |
| Fyu30     | \[X\]Other Alzheimer's disease                                                                                        | Alzheimer's Disease                       |
| 173A.     | Exercise induced asthma                                                                                               | Asthma                                    |
| 173c.     | Occupational asthma                                                                                                   | Asthma                                    |
| 173d.     | Work aggravated asthma                                                                                                | Asthma                                    |
| 1780      | Aspirin induced asthma                                                                                                | Asthma                                    |
| 1O2..     | Asthma confirmed                                                                                                      | Asthma                                    |
| 663d.     | Emergency asthma admission since last appointment                                                                     | Asthma                                    |
| 663e.     | Asthma restricts exercise                                                                                             | Asthma                                    |
| 6.63E+02  | Asthma sometimes restricts exercise                                                                                   | Asthma                                    |
| 6.63E+03  | Asthma severely restricts exercise                                                                                    | Asthma                                    |
| 663f.     | Asthma never restricts exercise                                                                                       | Asthma                                    |
| 663h.     | Asthma - currently dormant                                                                                            | Asthma                                    |
| 663j.     | Asthma - currently active                                                                                             | Asthma                                    |
| 663m.     | Asthma accident and emergency attendance since last visit                                                             | Asthma                                    |
| 663n.     | Asthma treatment compliance satisfactory                                                                              | Asthma                                    |
| 663N.     | Asthma disturbing sleep                                                                                               | Asthma                                    |
| 663N0     | Asthma causing night waking                                                                                           | Asthma                                    |
| 663N1     | Asthma disturbs sleep weekly                                                                                          | Asthma                                    |
| 663N2     | Asthma disturbs sleep frequently                                                                                      | Asthma                                    |
| 663O.     | Asthma not disturbing sleep                                                                                           | Asthma                                    |
| 663O0     | Asthma never disturbs sleep                                                                                           | Asthma                                    |
| 663p.     | Asthma treatment compliance unsatisfactory                                                                            | Asthma                                    |
| 663P.     | Asthma limiting activities                                                                                            | Asthma                                    |
| 663q.     | Asthma daytime symptoms                                                                                               | Asthma                                    |
| 663Q.     | Asthma not limiting activities                                                                                        | Asthma                                    |
| 663r.     | Asthma causes night symptoms 1 to 2 times per month                                                                   | Asthma                                    |
| 663s.     | Asthma never causes daytime symptoms                                                                                  | Asthma                                    |
| 663t.     | Asthma causes daytime symptoms 1 to 2 times per month                                                                 | Asthma                                    |
| 663u.     | Asthma causes daytime symptoms 1 to 2 times per week                                                                  | Asthma                                    |
| 663U.     | Asthma management plan given                                                                                          | Asthma                                    |
| 663v.     | Asthma causes daytime symptoms most days                                                                              | Asthma                                    |
| 663V.     | Asthma severity                                                                                                       | Asthma                                    |
| 663P.     | Asthma limiting activities                                                                                            | Asthma                                    |
| 663q.     | Asthma daytime symptoms                                                                                               | Asthma                                    |
| 663r.     | Asthma causes night symptoms 1 to 2 times per month                                                                   | Asthma                                    |
| 663u.     | Asthma causes daytime symptoms 1 to 2 times per week                                                                  | Asthma                                    |
| 663v.     | Asthma causes daytime symptoms most days                                                                              | Asthma                                    |
| 663V0     | Occasional asthma                                                                                                     | Asthma                                    |
| 663V1     | Mild asthma                                                                                                           | Asthma                                    |
| 663V2     | Moderate asthma                                                                                                       | Asthma                                    |
| 663V3     | Severe asthma                                                                                                         | Asthma                                    |
| 663w.     | Asthma limits walking up hills or stairs                                                                              | Asthma                                    |
| 663W.     | Asthma prophylactic medication used                                                                                   | Asthma                                    |
| 663x.     | Asthma limits walking on the flat                                                                                     | Asthma                                    |
| 663y.     | Number of asthma exacerbations in past year                                                                           | Asthma                                    |
| 66Y5.     | Change in asthma management plan                                                                                      | Asthma                                    |
| 66Y9.     | Step up change in asthma management plan                                                                              | Asthma                                    |
| 66YA.     | Step down change in asthma management plan                                                                            | Asthma                                    |
| 66YC.     | Absent from work or school due to asthma                                                                              | Asthma                                    |
| 66YE.     | Asthma monitoring due                                                                                                 | Asthma                                    |
| 66YJ.     | Asthma annual review                                                                                                  | Asthma                                    |
| 66YK.     | Asthma follow-up                                                                                                      | Asthma                                    |
| 66YP.     | Asthma night-time symptoms                                                                                            | Asthma                                    |
| 66YQ.     | Asthma monitoring by nurse                                                                                            | Asthma                                    |
| 66YR.     | Asthma monitoring by doctor                                                                                           | Asthma                                    |
| 8793      | Asthma control step 0                                                                                                 | Asthma                                    |
| 8794      | Asthma control step 1                                                                                                 | Asthma                                    |
| 8795      | Asthma control step 2                                                                                                 | Asthma                                    |
| 8796      | Asthma control step 3                                                                                                 | Asthma                                    |
| 8797      | Asthma control step 4                                                                                                 | Asthma                                    |
| 8798      | Asthma control step 5                                                                                                 | Asthma                                    |
| 8B3j.     | Asthma medication review                                                                                              | Asthma                                    |
| 8CR0.     | Asthma clinical management plan                                                                                       | Asthma                                    |
| 8791      | Further asthma - drug prevent.                                                                                        | Asthma                                    |
| 9hA..     | Exception reporting: asthma quality indicators                                                                        | Asthma                                    |
| H3120     | Chronic asthmatic bronchitis                                                                                          | Asthma                                    |
| H33..     | Asthma                                                                                                                | Asthma                                    |
| H330.     | Extrinsic (atopic) asthma                                                                                             | Asthma                                    |
| H3300     | Extrinsic asthma without status asthmaticus                                                                           | Asthma                                    |
| H3301     | Extrinsic asthma with status asthmaticus                                                                              | Asthma                                    |
| H330z     | Extrinsic asthma NOS                                                                                                  | Asthma                                    |
| H331.     | Intrinsic asthma                                                                                                      | Asthma                                    |
| H3310     | Intrinsic asthma without status asthmaticus                                                                           | Asthma                                    |
| H3311     | Intrinsic asthma with status asthmaticus                                                                              | Asthma                                    |
| H331z     | Intrinsic asthma NOS                                                                                                  | Asthma                                    |
| H332.     | Mixed asthma                                                                                                          | Asthma                                    |
| H333.     | Acute exacerbation of asthma                                                                                          | Asthma                                    |
| H334.     | Brittle asthma                                                                                                        | Asthma                                    |
| H33z.     | Asthma unspecified                                                                                                    | Asthma                                    |
| H33z0     | Status asthmaticus NOS                                                                                                | Asthma                                    |
| H33z1     | Asthma attack                                                                                                         | Asthma                                    |
| H33z2     | Late-onset asthma                                                                                                     | Asthma                                    |
| H33zz     | Asthma NOS                                                                                                            | Asthma                                    |
| H35y6     | Sequoiosis (red-cedar asthma)                                                                                         | Asthma                                    |
| H35y7     | Wood asthma                                                                                                           | Asthma                                    |
| H47y0     | Detergent asthma                                                                                                      | Asthma                                    |
| 14AN.     | H/O: atrial fibrillation                                                                                              | Atrial Fibrillation                       |
| 3272      | ECG: atrial fibrillation                                                                                              | Atrial Fibrillation                       |
| 662S.     | Atrial fibrillation monitoring                                                                                        | Atrial Fibrillation                       |
| 6A9..     | Atrial fibrillation annual review                                                                                     | Atrial Fibrillation                       |
| G573.     | Atrial fibrillation and flutter                                                                                       | Atrial Fibrillation                       |
| G5730     | Atrial fibrillation                                                                                                   | Atrial Fibrillation                       |
| G5732     | Paroxysmal atrial fibrillation                                                                                        | Atrial Fibrillation                       |
| G5733     | Non-rheumatic atrial fibrillation                                                                                     | Atrial Fibrillation                       |
| G5734     | Permanent atrial fibrillation                                                                                         | Atrial Fibrillation                       |
| G5735     | Persistent atrial fibrillation                                                                                        | Atrial Fibrillation                       |
| G573z     | Atrial fibrillation and flutter NOS                                                                                   | Atrial Fibrillation                       |
| XabRZ     | Axial spondyloarthritis                                                                                               | Axial Spondyloarthritis                   |
| N100.     | Ankylosing spondylitis                                                                                                | Axial Spondyloarthritis                   |
| X7023     | Ankylosing spondylitis with organ / system involvement                                                                | Axial Spondyloarthritis                   |
| X7024     | Ankylosing spondylitis with multisystem involvement                                                                   | Axial Spondyloarthritis                   |
| X701x     | Juvenile ankylosing spondylitis                                                                                       | Axial Spondyloarthritis                   |
| K20..     | Benign prostatic hypertrophy                                                                                          | Benign Prostatic Hyperplasia              |
| K200.     | Prostatic hyperplasia unspecified                                                                                     | Benign Prostatic Hyperplasia              |
| K201.     | Prostatic hyperplasia of the lateral lobe                                                                             | Benign Prostatic Hyperplasia              |
| K202.     | Prostatic hyperplasia of the medial lobe                                                                              | Benign Prostatic Hyperplasia              |
| K20z.     | Prostatic hyperplasia NOS                                                                                             | Benign Prostatic Hyperplasia              |
| Xa8EX     | Chronic idiopathic urticaria                                                                                          | Chronic Idiopathic Urticaria (CIU)        |
| 66A3.     | Diabetic on diet only                                                                                                 | Diabetes Mellitus, Type 2                 |
| 66A4.     | Diabetic on oral treatment                                                                                            | Diabetes Mellitus, Type 2                 |
| 66Ao.     | Diabetes type 2 review                                                                                                | Diabetes Mellitus, Type 2                 |
| C1074     | NIDDM with peripheral circulatory disorder                                                                            | Diabetes Mellitus, Type 2                 |
| C109.     | Non-insulin dependent diabetes mellitus                                                                               | Diabetes Mellitus, Type 2                 |
| C1090     | Non-insulin-dependent diabetes mellitus with renal comps                                                              | Diabetes Mellitus, Type 2                 |
| C1091     | Non-insulin-dependent diabetes mellitus with ophthalm comps                                                           | Diabetes Mellitus, Type 2                 |
| C1092     | Non-insulin-dependent diabetes mellitus with neuro comps                                                              | Diabetes Mellitus, Type 2                 |
| C1093     | Non-insulin-dependent diabetes mellitus with multiple comps                                                           | Diabetes Mellitus, Type 2                 |
| C1094     | Non-insulin dependent diabetes mellitus with ulcer                                                                    | Diabetes Mellitus, Type 2                 |
| C1095     | Non-insulin dependent diabetes mellitus with gangrene                                                                 | Diabetes Mellitus, Type 2                 |
| C1096     | Non-insulin-dependent diabetes mellitus with retinopathy                                                              | Diabetes Mellitus, Type 2                 |
| C1097     | Non-insulin dependent diabetes mellitus - poor control                                                                | Diabetes Mellitus, Type 2                 |
| C1099     | Non-insulin-dependent diabetes mellitus without complication                                                          | Diabetes Mellitus, Type 2                 |
| C109A     | Non-insulin dependent diabetes mellitus with mononeuropathy                                                           | Diabetes Mellitus, Type 2                 |
| C109B     | Non-insulin dependent diabetes mellitus with polyneuropathy                                                           | Diabetes Mellitus, Type 2                 |
| C109C     | Non-insulin dependent diabetes mellitus with nephropathy                                                              | Diabetes Mellitus, Type 2                 |
| C109D     | Non-insulin dependent diabetes mellitus with hypoglyca coma                                                           | Diabetes Mellitus, Type 2                 |
| C109E     | Non-insulin depend diabetes mellitus with diabetic cataract                                                           | Diabetes Mellitus, Type 2                 |
| C109F     | Non-insulin-dependent d m with peripheral angiopath                                                                   | Diabetes Mellitus, Type 2                 |
| C109G     | Non-insulin dependent diabetes mellitus with arthropathy                                                              | Diabetes Mellitus, Type 2                 |
| C109H     | Non-insulin dependent d m with neuropathic arthropathy                                                                | Diabetes Mellitus, Type 2                 |
| C109J     | Insulin treated Type 2 diabetes mellitus                                                                              | Diabetes Mellitus, Type 2                 |
| C109K     | Hyperosmolar non-ketotic state in type 2 diabetes mellitus                                                            | Diabetes Mellitus, Type 2                 |
| C10F.     | Type 2 diabetes mellitus                                                                                              | Diabetes Mellitus, Type 2                 |
| C10F0     | Type 2 diabetes mellitus with renal complications                                                                     | Diabetes Mellitus, Type 2                 |
| C10F1     | Type 2 diabetes mellitus with ophthalmic complications                                                                | Diabetes Mellitus, Type 2                 |
| C10F2     | Type 2 diabetes mellitus with neurological complications                                                              | Diabetes Mellitus, Type 2                 |
| C10F3     | Type 2 diabetes mellitus with multiple complications                                                                  | Diabetes Mellitus, Type 2                 |
| C10F4     | Type 2 diabetes mellitus with ulcer                                                                                   | Diabetes Mellitus, Type 2                 |
| C10F5     | Type 2 diabetes mellitus with gangrene                                                                                | Diabetes Mellitus, Type 2                 |
| C10F6     | Type 2 diabetes mellitus with retinopathy                                                                             | Diabetes Mellitus, Type 2                 |
| C10F7     | Type 2 diabetes mellitus - poor control                                                                               | Diabetes Mellitus, Type 2                 |
| C10F9     | Type 2 diabetes mellitus without complication                                                                         | Diabetes Mellitus, Type 2                 |
| C10FA     | Type 2 diabetes mellitus with mononeuropathy                                                                          | Diabetes Mellitus, Type 2                 |
| C10FB     | Type 2 diabetes mellitus with polyneuropathy                                                                          | Diabetes Mellitus, Type 2                 |
| C10FC     | Type 2 diabetes mellitus with nephropathy                                                                             | Diabetes Mellitus, Type 2                 |
| C10FD     | Type 2 diabetes mellitus with hypoglycaemic coma                                                                      | Diabetes Mellitus, Type 2                 |
| C10FE     | Type 2 diabetes mellitus with diabetic cataract                                                                       | Diabetes Mellitus, Type 2                 |
| C10FF     | Type 2 diabetes mellitus with peripheral angiopathy                                                                   | Diabetes Mellitus, Type 2                 |
| C10FG     | Type 2 diabetes mellitus with arthropathy                                                                             | Diabetes Mellitus, Type 2                 |
| C10FH     | Type 2 diabetes mellitus with neuropathic arthropathy                                                                 | Diabetes Mellitus, Type 2                 |
| C10FJ     | Insulin treated Type 2 diabetes mellitus                                                                              | Diabetes Mellitus, Type 2                 |
| C10FK     | Hyperosmolar non-ketotic state in type 2 diabetes mellitus                                                            | Diabetes Mellitus, Type 2                 |
| C10FL     | Type 2 diabetes mellitus with persistent proteinuria                                                                  | Diabetes Mellitus, Type 2                 |
| C10FM     | Type 2 diabetes mellitus with persistent microalbuminuria                                                             | Diabetes Mellitus, Type 2                 |
| C10FN     | Type 2 diabetes mellitus with ketoacidosis                                                                            | Diabetes Mellitus, Type 2                 |
| C10FP     | Type 2 diabetes mellitus with ketoacidotic coma                                                                       | Diabetes Mellitus, Type 2                 |
| C10FQ     | Type 2 diabetes mellitus with exudative maculopathy                                                                   | Diabetes Mellitus, Type 2                 |
| C10FR     | Type 2 diabetes mellitus with gastroparesis                                                                           | Diabetes Mellitus, Type 2                 |
| 1473      | H/O: epilepsy                                                                                                         | Epilepsy                                  |
| 1B1W.     | Transient epileptic amnesia                                                                                           | Epilepsy                                  |
| 1O30.     | Epilepsy confirmed                                                                                                    | Epilepsy                                  |
| 667..     | Epilepsy monitoring                                                                                                   | Epilepsy                                  |
| 6671      | Initial epilepsy assessment                                                                                           | Epilepsy                                  |
| 6672      | Follow-up epilepsy assessment                                                                                         | Epilepsy                                  |
| 6673      | Epilepsy associated problems                                                                                          | Epilepsy                                  |
| 6674      | Fit frequency                                                                                                         | Epilepsy                                  |
| 6675      | Last fit                                                                                                              | Epilepsy                                  |
| 6676      | Epilepsy treatment changed                                                                                            | Epilepsy                                  |
| 6677      | Epilepsy treatment started                                                                                            | Epilepsy                                  |
| 6678      | Nocturnal epilepsy                                                                                                    | Epilepsy                                  |
| 6679      | Epilepsy control good                                                                                                 | Epilepsy                                  |
| 667D.     | Epilepsy control poor                                                                                                 | Epilepsy                                  |
| 667E.     | Epilepsy care arrangement                                                                                             | Epilepsy                                  |
| 667G.     | Epilepsy restricts employment                                                                                         | Epilepsy                                  |
| 667H.     | Epilepsy prevents employment                                                                                          | Epilepsy                                  |
| 667J.     | Epilepsy impairs education                                                                                            | Epilepsy                                  |
| 667K.     | Epilepsy limits activities                                                                                            | Epilepsy                                  |
| 667L.     | Epilepsy does not limit activities                                                                                    | Epilepsy                                  |
| 667M.     | Epilepsy management plan given                                                                                        | Epilepsy                                  |
| 667N.     | Epilepsy severity                                                                                                     | Epilepsy                                  |
| 667Q.     | 1 to 12 seizures a year                                                                                               | Epilepsy                                  |
| 667R.     | 2 to 4 seizures a month                                                                                               | Epilepsy                                  |
| 667S.     | 1 to 7 seizures a week                                                                                                | Epilepsy                                  |
| 667T.     | Daily seizures                                                                                                        | Epilepsy                                  |
| 667V.     | Many seizures a day                                                                                                   | Epilepsy                                  |
| 667W.     | Emergency epilepsy treatment since last appointment                                                                   | Epilepsy                                  |
| 667X.     | No epilepsy drug side effects                                                                                         | Epilepsy                                  |
| 667Z.     | Epilepsy monitoring NOS                                                                                               | Epilepsy                                  |
| 8B66.     | Anticonvulsant therapy                                                                                                | Epilepsy                                  |
| 8BIF.     | Epilepsy medication review                                                                                            | Epilepsy                                  |
| Eu803     | \[X\]Acquired aphasia with epilepsy \[Landau - Kleffner\]                                                             | Epilepsy                                  |
| F1321     | Progressive myoclonic epilepsy                                                                                        | Epilepsy                                  |
| F25..     | Epilepsy                                                                                                              | Epilepsy                                  |
| F250.     | Generalised nonconvulsive epilepsy                                                                                    | Epilepsy                                  |
| F2500     | Petit mal (minor) epilepsy                                                                                            | Epilepsy                                  |
| F2501     | Pykno-epilepsy                                                                                                        | Epilepsy                                  |
| F2502     | Epileptic seizures - atonic                                                                                           | Epilepsy                                  |
| F2503     | Epileptic seizures - akinetic                                                                                         | Epilepsy                                  |
| F2504     | Juvenile absence epilepsy                                                                                             | Epilepsy                                  |
| F2505     | Lennox-Gastaut syndrome                                                                                               | Epilepsy                                  |
| F250y     | Other specified generalised nonconvulsive epilepsy                                                                    | Epilepsy                                  |
| F250z     | Generalised nonconvulsive epilepsy NOS                                                                                | Epilepsy                                  |
| F251.     | Generalised convulsive epilepsy                                                                                       | Epilepsy                                  |
| F2510     | Grand mal (major) epilepsy                                                                                            | Epilepsy                                  |
| F2511     | Neonatal myoclonic epilepsy                                                                                           | Epilepsy                                  |
| F2512     | Epileptic seizures - clonic                                                                                           | Epilepsy                                  |
| F2513     | Epileptic seizures - myoclonic                                                                                        | Epilepsy                                  |
| F2514     | Epileptic seizures - tonic                                                                                            | Epilepsy                                  |
| F2515     | Tonic-clonic epilepsy                                                                                                 | Epilepsy                                  |
| F2516     | Grand mal seizure                                                                                                     | Epilepsy                                  |
| F251y     | Other specified generalised convulsive epilepsy                                                                       | Epilepsy                                  |
| F251z     | Generalised convulsive epilepsy NOS                                                                                   | Epilepsy                                  |
| F252.     | Petit mal status                                                                                                      | Epilepsy                                  |
| F253.     | Grand mal status                                                                                                      | Epilepsy                                  |
| F254.     | Partial epilepsy with impairment of consciousness                                                                     | Epilepsy                                  |
| F2540     | Temporal lobe epilepsy                                                                                                | Epilepsy                                  |
| F2541     | Psychomotor epilepsy                                                                                                  | Epilepsy                                  |
| F2542     | Psychosensory epilepsy                                                                                                | Epilepsy                                  |
| F2543     | Limbic system epilepsy                                                                                                | Epilepsy                                  |
| F2544     | Epileptic automatism                                                                                                  | Epilepsy                                  |
| F2545     | Complex partial epileptic seizure                                                                                     | Epilepsy                                  |
| F254z     | Partial epilepsy with impairment of consciousness NOS                                                                 | Epilepsy                                  |
| F255.     | Partial epilepsy without impairment of consciousness                                                                  | Epilepsy                                  |
| F2550     | Jacksonian, focal or motor epilepsy                                                                                   | Epilepsy                                  |
| F2551     | Sensory induced epilepsy                                                                                              | Epilepsy                                  |
| F2552     | Somatosensory epilepsy                                                                                                | Epilepsy                                  |
| F2553     | Visceral reflex epilepsy                                                                                              | Epilepsy                                  |
| F2554     | Visual reflex epilepsy                                                                                                | Epilepsy                                  |
| F2555     | Unilateral epilepsy                                                                                                   | Epilepsy                                  |
| F2556     | Simple partial epileptic seizure                                                                                      | Epilepsy                                  |
| F255y     | Partial epilepsy without impairment of consciousness OS                                                               | Epilepsy                                  |
| F255z     | Partial epilepsy without impairment of consciousness NOS                                                              | Epilepsy                                  |
| F257.     | Kojevnikov's epilepsy                                                                                                 | Epilepsy                                  |
| F258.     | Post-ictal state                                                                                                      | Epilepsy                                  |
| F259.     | Early infant epileptic encephalopathy wth suppression bursts                                                          | Epilepsy                                  |
| F25A.     | Juvenile myoclonic epilepsy                                                                                           | Epilepsy                                  |
| F25B.     | Alcohol-induced epilepsy                                                                                              | Epilepsy                                  |
| F25C.     | Drug-induced epilepsy                                                                                                 | Epilepsy                                  |
| F25D.     | Menstrual epilepsy                                                                                                    | Epilepsy                                  |
| F25E.     | Stress-induced epilepsy                                                                                               | Epilepsy                                  |
| F25F.     | Photosensitive epilepsy                                                                                               | Epilepsy                                  |
| F25X.     | Status epilepticus, unspecified                                                                                       | Epilepsy                                  |
| F25y.     | Other forms of epilepsy                                                                                               | Epilepsy                                  |
| F25y0     | Cursive (running) epilepsy                                                                                            | Epilepsy                                  |
| F25y1     | Gelastic epilepsy                                                                                                     | Epilepsy                                  |
| F25y2     | Locl-rlt(foc)(part)idiop epilep&epilptic syn seiz locl onset                                                          | Epilepsy                                  |
| F25y3     | Complex partial status epilepticus                                                                                    | Epilepsy                                  |
| F25y4     | Benign Rolandic epilepsy                                                                                              | Epilepsy                                  |
| F25y5     | Panayiotopoulos syndrome                                                                                              | Epilepsy                                  |
| F25yz     | Other forms of epilepsy NOS                                                                                           | Epilepsy                                  |
| F25z.     | Epilepsy NOS                                                                                                          | Epilepsy                                  |
| Fyu50     | \[X\]Other generalized epilepsy and epileptic syndromes                                                               | Epilepsy                                  |
| Fyu51     | \[X\]Other epilepsy                                                                                                   | Epilepsy                                  |
| Fyu52     | \[X\]Other status epilepticus                                                                                         | Epilepsy                                  |
| Fyu59     | \[X\]Status epilepticus, unspecified                                                                                  | Epilepsy                                  |
| SC200     | Traumatic epilepsy                                                                                                    | Epilepsy                                  |
| E2273     | Erectile dysfunction                                                                                                  | Erectile dysfunction                      |
| Xaa8r     | Erectile dysfunction due to diabetes mellitus                                                                         | Erectile dysfunction                      |
| X400F     | Drug-induced impotence                                                                                                | Erectile dysfunction                      |
| X400G     | Endocrine impotence                                                                                                   | Erectile dysfunction                      |
| X400H     | Neuropathic impotence                                                                                                 | Erectile dysfunction                      |
| Xa24H     | Arteriopathic impotence                                                                                               | Erectile dysfunction                      |
| X400I     | Psychogenic impotence                                                                                                 | Erectile dysfunction                      |
| K27y1     | Impotence of organic origin                                                                                           | Erectile dysfunction                      |
| XaXgw     | C/O erectile dysfunction                                                                                              | Erectile dysfunction                      |
| 7A6G5     | Ligation of penile veins for impotence                                                                                | Erectile dysfunction                      |
| X74UL     | Provision of device for impotence                                                                                     | Erectile dysfunction                      |
| X74UM     | Provision of penile vacuum constriction device                                                                        | Erectile dysfunction                      |
| X74UN     | Provision of penile tension band device                                                                               | Erectile dysfunction                      |
| X77lU     | Physiological tests for impotence                                                                                     | Erectile dysfunction                      |
| X77lV     | Nocturnal penile tumescence                                                                                           | Erectile dysfunction                      |
| X77lW     | Corporeal veno-occlusive function                                                                                     | Erectile dysfunction                      |
| X77lX     | Intracavernous injection test using vaso-active agent                                                                 | Erectile dysfunction                      |
| X71FJ     | Advice on technique for impotence                                                                                     | Erectile dysfunction                      |
| X30HR     | Penile revascularisation for impotence                                                                                | Erectile dysfunction                      |
| 662G.     | Hypertensive treatm.changed                                                                                           | Hypertension                              |
| 662O.     | On treatment for hypertension                                                                                         | Hypertension                              |
| 662P.     | Hypertension monitoring                                                                                               | Hypertension                              |
| 662q.     | Trial reduction of antihypertensive therapy                                                                           | Hypertension                              |
| 662r.     | Trial withdrawal of antihypertensive therapy                                                                          | Hypertension                              |
| 8B26.     | Antihypertensive therapy                                                                                              | Hypertension                              |
| 8BL0.     | Patient on maximal tolerated antihypertensive therapy                                                                 | Hypertension                              |
| 8CR4.     | Hypertension clinical management plan                                                                                 | Hypertension                              |
| F4042     | Blind hypertensive eye                                                                                                | Hypertension                              |
| F4213     | Hypertensive retinopathy                                                                                              | Hypertension                              |
| F4504     | Ocular hypertension                                                                                                   | Hypertension                              |
| G2...     | Hypertensive disease                                                                                                  | Hypertension                              |
| G20..     | Essential hypertension                                                                                                | Hypertension                              |
| G200.     | Malignant essential hypertension                                                                                      | Hypertension                              |
| G201.     | Benign essential hypertension                                                                                         | Hypertension                              |
| G202.     | Systolic hypertension                                                                                                 | Hypertension                              |
| G203.     | Diastolic hypertension                                                                                                | Hypertension                              |
| G20z.     | Essential hypertension NOS                                                                                            | Hypertension                              |
| G21..     | Hypertensive heart disease                                                                                            | Hypertension                              |
| G210.     | Malignant hypertensive heart disease                                                                                  | Hypertension                              |
| G2100     | Malignant hypertensive heart disease without CCF                                                                      | Hypertension                              |
| G2101     | Malignant hypertensive heart disease with CCF                                                                         | Hypertension                              |
| G210z     | Malignant hypertensive heart disease NOS                                                                              | Hypertension                              |
| G211.     | Benign hypertensive heart disease                                                                                     | Hypertension                              |
| G2110     | Benign hypertensive heart disease without CCF                                                                         | Hypertension                              |
| G2111     | Benign hypertensive heart disease with CCF                                                                            | Hypertension                              |
| G211z     | Benign hypertensive heart disease NOS                                                                                 | Hypertension                              |
| G21z.     | Hypertensive heart disease NOS                                                                                        | Hypertension                              |
| G21z0     | Hypertensive heart disease NOS without CCF                                                                            | Hypertension                              |
| G21z1     | Hypertensive heart disease NOS with CCF                                                                               | Hypertension                              |
| G21zz     | Hypertensive heart disease NOS                                                                                        | Hypertension                              |
| G22..     | Hypertensive renal disease                                                                                            | Hypertension                              |
| G220.     | Malignant hypertensive renal disease                                                                                  | Hypertension                              |
| G221.     | Benign hypertensive renal disease                                                                                     | Hypertension                              |
| G222.     | Hypertensive renal disease with renal failure                                                                         | Hypertension                              |
| G22z.     | Hypertensive renal disease NOS                                                                                        | Hypertension                              |
| G23..     | Hypertensive heart and renal disease                                                                                  | Hypertension                              |
| G230.     | Malignant hypertensive heart and renal disease                                                                        | Hypertension                              |
| G231.     | Benign hypertensive heart and renal disease                                                                           | Hypertension                              |
| G232.     | Hypertensive heart&renal dis wth (congestive) heart failure                                                           | Hypertension                              |
| G233.     | Hypertensive heart and renal disease with renal failure                                                               | Hypertension                              |
| G234.     | Hyperten heart&renal dis+both(congestv)heart and renal fail                                                           | Hypertension                              |
| G23z.     | Hypertensive heart and renal disease NOS                                                                              | Hypertension                              |
| G24..     | Secondary hypertension                                                                                                | Hypertension                              |
| G240.     | Secondary malignant hypertension                                                                                      | Hypertension                              |
| G2400     | Secondary malignant renovascular hypertension                                                                         | Hypertension                              |
| G240z     | Secondary malignant hypertension NOS                                                                                  | Hypertension                              |
| G241.     | Secondary benign hypertension                                                                                         | Hypertension                              |
| G2410     | Secondary benign renovascular hypertension                                                                            | Hypertension                              |
| G241z     | Secondary benign hypertension NOS                                                                                     | Hypertension                              |
| G244.     | Hypertension secondary to endocrine disorders                                                                         | Hypertension                              |
| G24z.     | Secondary hypertension NOS                                                                                            | Hypertension                              |
| G24z0     | Secondary renovascular hypertension NOS                                                                               | Hypertension                              |
| G24z1     | Hypertension secondary to drug                                                                                        | Hypertension                              |
| G24zz     | Secondary hypertension NOS                                                                                            | Hypertension                              |
| G2y..     | Other specified hypertensive disease                                                                                  | Hypertension                              |
| G2z..     | Hypertensive disease NOS                                                                                              | Hypertension                              |
| G672.     | Hypertensive encephalopathy                                                                                           | Hypertension                              |
| Gyu2.     | \[X\]Hypertensive diseases                                                                                            | Hypertension                              |
| Gyu20     | \[X\]Other secondary hypertension                                                                                     | Hypertension                              |
| Gyu21     | \[X\]Hypertension secondary to other renal disorders                                                                  | Hypertension                              |
| G410.     | Primary pulmonary hypertension                                                                                        | Hypertension, Pulmonary                   |
| X2036     | Sporadic primary pulmonary hypertension                                                                               | Hypertension, Pulmonary                   |
| X2037     | Familial primary pulmonary hypertension                                                                               | Hypertension, Pulmonary                   |
| 14C4.     | H/O: colitis                                                                                                          | Inflammatory bowel disease                |
| J08z9     | Orofacial Crohn's disease                                                                                             | Inflammatory bowel disease                |
| J40..     | Regional enteritis - Crohn's disease                                                                                  | Inflammatory bowel disease                |
| J400.     | Regional enteritis of the small bowel                                                                                 | Inflammatory bowel disease                |
| J4000     | Regional enteritis of the duodenum                                                                                    | Inflammatory bowel disease                |
| J4001     | Regional enteritis of the jejunum                                                                                     | Inflammatory bowel disease                |
| J4002     | Crohn's disease of the terminal ileum                                                                                 | Inflammatory bowel disease                |
| J4003     | Crohn's disease of the ileum unspecified                                                                              | Inflammatory bowel disease                |
| J4004     | Crohn's disease of the ileum NOS                                                                                      | Inflammatory bowel disease                |
| J4005     | Exacerbation of Crohn's disease of small intestine                                                                    | Inflammatory bowel disease                |
| J400z     | Crohn's disease of the small bowel NOS                                                                                | Inflammatory bowel disease                |
| J401.     | Regional enteritis of the large bowel                                                                                 | Inflammatory bowel disease                |
| J4010     | Regional enteritis of the colon                                                                                       | Inflammatory bowel disease                |
| J4011     | Regional enteritis of the rectum                                                                                      | Inflammatory bowel disease                |
| J4012     | Exacerbation of Crohn's disease of large intestine                                                                    | Inflammatory bowel disease                |
| J401z     | Crohn's disease of the large bowel NOS                                                                                | Inflammatory bowel disease                |
| J402.     | Regional ileocolitis                                                                                                  | Inflammatory bowel disease                |
| J40z.     | Regional enteritis NOS                                                                                                | Inflammatory bowel disease                |
| J41..     | Idiopathic proctocolitis                                                                                              | Inflammatory bowel disease                |
| J410.     | Ulcerative proctocolitis                                                                                              | Inflammatory bowel disease                |
| J4100     | Ulcerative ileocolitis                                                                                                | Inflammatory bowel disease                |
| J4101     | Ulcerative colitis                                                                                                    | Inflammatory bowel disease                |
| J4102     | Ulcerative rectosigmoiditis                                                                                           | Inflammatory bowel disease                |
| J4103     | Ulcerative proctitis                                                                                                  | Inflammatory bowel disease                |
| J4104     | Exacerbation of ulcerative colitis                                                                                    | Inflammatory bowel disease                |
| J410z     | Ulcerative proctocolitis NOS                                                                                          | Inflammatory bowel disease                |
| J411.     | Ulcerative (chronic) enterocolitis                                                                                    | Inflammatory bowel disease                |
| J412.     | Ulcerative (chronic) ileocolitis                                                                                      | Inflammatory bowel disease                |
| Jyu40     | \[X\]Other Crohn's disease                                                                                            | Inflammatory bowel disease                |
| Jyu41     | \[X\]Other ulcerative colitis                                                                                         | Inflammatory bowel disease                |
| N0310     | Arthropathy in ulcerative colitis                                                                                     | Inflammatory bowel disease                |
| N0454     | Juvenile arthritis in ulcerative colitis                                                                              | Inflammatory bowel disease                |
| J08z9     | Orofacial Crohn's disease                                                                                             | Inflammatory bowel disease                |
| J40..     | Regional enteritis - Crohn's disease                                                                                  | Inflammatory bowel disease                |
| J4002     | Crohn's disease of the terminal ileum                                                                                 | Inflammatory bowel disease                |
| J4003     | Crohn's disease of the ileum unspecified                                                                              | Inflammatory bowel disease                |
| J4004     | Crohn's disease of the ileum NOS                                                                                      | Inflammatory bowel disease                |
| J4005     | Exacerbation of Crohn's disease of small intestine                                                                    | Inflammatory bowel disease                |
| J400z     | Crohn's disease of the small bowel NOS                                                                                | Inflammatory bowel disease                |
| J4012     | Exacerbation of Crohn's disease of large intestine                                                                    | Inflammatory bowel disease                |
| J401z     | Crohn's disease of the large bowel NOS                                                                                | Inflammatory bowel disease                |
| Jyu40     | \[X\]Other Crohn's disease                                                                                            | Inflammatory bowel disease                |
| N0311     | Arthropathy in Crohn's disease                                                                                        | Inflammatory bowel disease                |
| N0453     | Juvenile arthritis in Crohn's disease                                                                                 | Inflammatory bowel disease                |
| F26..     | Migraine                                                                                                              | Migraine                                  |
| XaXkr     | Migraine induced by oestrogen contraceptive                                                                           | Migraine                                  |
| F261.     | Migraine without aura                                                                                                 | Migraine                                  |
| F261z     | Common migraine NOS                                                                                                   | Migraine                                  |
| F260.     | Migraine with aura                                                                                                    | Migraine                                  |
| X007J     | Migraine with typical aura                                                                                            | Migraine                                  |
| X007K     | Migraine with prolonged aura                                                                                          | Migraine                                  |
| F26y0     | Hemiplegic migraine                                                                                                   | Migraine                                  |
| X007L     | Familial hemiplegic migraine                                                                                          | Migraine                                  |
| X007M     | Non-familial hemiplegic migraine                                                                                      | Migraine                                  |
| F2623     | Basilar migraine                                                                                                      | Migraine                                  |
| X007N     | Migraine aura without headache                                                                                        | Migraine                                  |
| F2624     | Ophthalmic migraine                                                                                                   | Migraine                                  |
| F26y1     | Ophthalmoplegic migraine                                                                                              | Migraine                                  |
| X007O     | Retinal migraine                                                                                                      | Migraine                                  |
| X007Q     | Alternating hemiplegia of childhood                                                                                   | Migraine                                  |
| X007R     | Status migrainosus                                                                                                    | Migraine                                  |
| X007S     | Migraine with ischaemic complication                                                                                  | Migraine                                  |
| Xa07H     | Migraine - menstrual                                                                                                  | Migraine                                  |
| F2610     | Atypical migraine                                                                                                     | Migraine                                  |
| F262.     | Migraine variants                                                                                                     | Migraine                                  |
| F262z     | Migraine variant NOS                                                                                                  | Migraine                                  |
| F26y.     | Other forms of migraine                                                                                               | Migraine                                  |
| F26yz     | Other forms of migraine NOS                                                                                           | Migraine                                  |
| F26y3     | Complicated migraine                                                                                                  | Migraine                                  |
| F26z.     | Migraine NOS                                                                                                          | Migraine                                  |
| Fyu53     | \[X\]Other migraine                                                                                                   | Migraine                                  |
| 1474      | H/O: migraine                                                                                                         | Migraine                                  |
| XaXkv     | H/O migraine with aura                                                                                                | Migraine                                  |
| F260.     | Classical migraine                                                                                                    | Migraine                                  |
| X007J     | Migraine with typical aura                                                                                            | Migraine                                  |
| X007K     | Migraine with prolonged aura                                                                                          | Migraine                                  |
| F26y0     | Hemiplegic migraine                                                                                                   | Migraine                                  |
| X007L     | Familial hemiplegic migraine                                                                                          | Migraine                                  |
| X007M     | Non-familial hemiplegic migraine                                                                                      | Migraine                                  |
| F2623     | Basilar migraine                                                                                                      | Migraine                                  |
| X007N     | Migraine aura without headache                                                                                        | Migraine                                  |
| F2624     | Ophthalmic migraine                                                                                                   | Migraine                                  |
| 585O.00   | Quantitative ultrasound scan of heel - result osteoporotic                                                            | Osteoporosis                              |
| 58E4.00   | Forearm DXA scan result osteoporotic                                                                                  | Osteoporosis                              |
| 58E8.00   | Heel DXA scan T score                                                                                                 | Osteoporosis                              |
| 58EA.00   | Heel DXA scan result osteoporotic                                                                                     | Osteoporosis                              |
| 58EA.00   | Heel DXA scan result osteoporotic                                                                                     | Osteoporosis                              |
| 58EE.00   | Hip DXA scan T score                                                                                                  | Osteoporosis                              |
| 58EG.00   | Hip DXA scan result osteoporotic                                                                                      | Osteoporosis                              |
| 58EG.00   | Hip DXA scan result osteoporotic                                                                                      | Osteoporosis                              |
| 58EK.00   | Lumbar spine DXA scan T score                                                                                         | Osteoporosis                              |
| 58EM.00   | Lumbar DXA scan result osteoporotic                                                                                   | Osteoporosis                              |
| 58EM.00   | Lumbar DXA scan result osteoporotic                                                                                   | Osteoporosis                              |
| 58ES.00   | Femoral neck DEXA scan T score                                                                                        | Osteoporosis                              |
| 58EV.00   | Femoral neck DEXA scan result osteoporotic                                                                            | Osteoporosis                              |
| 7230A     | OSTEOPOROSIS                                                                                                          | Osteoporosis                              |
| 7230B     | OSTEOPOROSIS SENILIS                                                                                                  | Osteoporosis                              |
| 7230D     | VERTEBRAL OSTEOPOROSIS                                                                                                | Osteoporosis                              |
| 7230PM    | OSTEOPOROSIS POSTMENOPAUSAL                                                                                           | Osteoporosis                              |
| 7230PT    | OSTEOPOROSIS POST-TRAUMATIC                                                                                           | Osteoporosis                              |
| N330.00   | Osteoporosis                                                                                                          | Osteoporosis                              |
| N330.00   | Osteoporosis                                                                                                          | Osteoporosis                              |
| N330000   | Osteoporosis; unspecified                                                                                             | Osteoporosis                              |
| N330000   | Osteoporosis; unspecified                                                                                             | Osteoporosis                              |
| N330100   | Senile osteoporosis                                                                                                   | Osteoporosis                              |
| N330100   | Senile osteoporosis                                                                                                   | Osteoporosis                              |
| N330200   | Postmenopausal osteoporosis                                                                                           | Osteoporosis                              |
| N330200   | Postmenopausal osteoporosis                                                                                           | Osteoporosis                              |
| N330300   | Idiopathic osteoporosis                                                                                               | Osteoporosis                              |
| N330300   | Idiopathic osteoporosis                                                                                               | Osteoporosis                              |
| N330400   | Dissuse osteoporosis                                                                                                  | Osteoporosis                              |
| N330400   | Dissuse osteoporosis                                                                                                  | Osteoporosis                              |
| N330500   | Drug-induced osteoporosis                                                                                             | Osteoporosis                              |
| N330500   | Drug-induced osteoporosis                                                                                             | Osteoporosis                              |
| N330600   | Postoophorectomy osteoporosis                                                                                         | Osteoporosis                              |
| N330600   | Postoophorectomy osteoporosis                                                                                         | Osteoporosis                              |
| N330700   | Postsurgical malabsorption osteoporosis                                                                               | Osteoporosis                              |
| N330700   | Postsurgical malabsorption osteoporosis                                                                               | Osteoporosis                              |
| N330800   | Localized osteoporosis - Lequesne                                                                                     | Osteoporosis                              |
| N330800   | Localized osteoporosis - Lequesne                                                                                     | Osteoporosis                              |
| N330900   | Osteoporosis in multiple myelomatosis                                                                                 | Osteoporosis                              |
| N330900   | Osteoporosis in multiple myelomatosis                                                                                 | Osteoporosis                              |
| N330A00   | Osteoporosis in endocrine disorders                                                                                   | Osteoporosis                              |
| N330A00   | Osteoporosis in endocrine disorders                                                                                   | Osteoporosis                              |
| N330B00   | Vertebral osteoporosis                                                                                                | Osteoporosis                              |
| N330B00   | Vertebral osteoporosis                                                                                                | Osteoporosis                              |
| N330C00   | Osteoporosis localized to spine                                                                                       | Osteoporosis                              |
| N330C00   | Osteoporosis localized to spine                                                                                       | Osteoporosis                              |
| N330D00   | Osteoporosis due to corticosteroids                                                                                   | Osteoporosis                              |
| N330D00   | Osteoporosis due to corticosteroids                                                                                   | Osteoporosis                              |
| N330z00   | Osteoporosis NOS                                                                                                      | Osteoporosis                              |
| N330z00   | Osteoporosis NOS                                                                                                      | Osteoporosis                              |
| N331200   | Postoophorectomy osteoporosis with pathological fracture                                                              | Osteoporosis                              |
| N331200   | Postoophorectomy osteoporosis with pathological fracture                                                              | Osteoporosis                              |
| N331300   | Osteoporosis of disuse with pathological fracture                                                                     | Osteoporosis                              |
| N331300   | Osteoporosis of disuse with pathological fracture                                                                     | Osteoporosis                              |
| N331400   | Postsurgical malabsorption osteoporosis with path fracture                                                            | Osteoporosis                              |
| N331500   | Drug-induced osteoporosis with pathological fracture                                                                  | Osteoporosis                              |
| N331600   | Idiopathic osteoporosis with pathological fracture                                                                    | Osteoporosis                              |
| N331600   | Idiopathic osteoporosis with pathological fracture                                                                    | Osteoporosis                              |
| N331800   | Osteoporosis + pathological fracture lumbar vertebrae                                                                 | Osteoporosis                              |
| N331900   | Osteoporosis + pathological fracture thoracic vertebrae                                                               | Osteoporosis                              |
| N331A00   | Osteoporosis + pathological fracture cervical vertebrae                                                               | Osteoporosis                              |
| N331B00   | Postmenopausal osteoporosis with pathological fracture                                                                | Osteoporosis                              |
| N331M00   | Fragility fracture due to unspecified osteoporosis                                                                    | Osteoporosis                              |
| N331N00   | Fragility fracture                                                                                                    | Osteoporosis                              |
| NyuB000   | \[X\]Other osteoporosis with pathological fracture                                                                    | Osteoporosis                              |
| NyuB000   | \[X\]Other osteoporosis with pathological fracture                                                                    | Osteoporosis                              |
| NyuB100   | \[X\]Other osteoporosis                                                                                               | Osteoporosis                              |
| NyuB100   | \[X\]Other osteoporosis                                                                                               | Osteoporosis                              |
| NyuB200   | \[X\]Osteoporosis in other disorders classified elsewhere                                                             | Osteoporosis                              |
| NyuB800   | \[X\]Unspecified osteoporosis with pathological fracture                                                              | Osteoporosis                              |
| NyuB800   | \[X\]Unspecified osteoporosis with pathological fracture                                                              | Osteoporosis                              |
| 147F.     | History of Parkinson's disease                                                                                        | Parkinson's disease (all)                 |
| 297A.     | O/E - Parkinsonian tremor                                                                                             | Parkinson's disease (all)                 |
| 2987      | O/E -Parkinson flexion posture                                                                                        | Parkinson's disease (all)                 |
| 2994      | O/E-festination-Parkinson gait                                                                                        | Parkinson's disease (all)                 |
| A94y1     | Syphilitic parkinsonism                                                                                               | Parkinson's disease (all)                 |
| Eu023     | \[X\]Dementia in Parkinson's disease                                                                                  | Parkinson's disease (all)                 |
| F11x9     | Cerebral degeneration in Parkinson's disease                                                                          | Parkinson's disease (all)                 |
| F12..     | Parkinson's disease                                                                                                   | Parkinson's disease (all)                 |
| F120.     | Paralysis agitans                                                                                                     | Parkinson's disease (all)                 |
| F121.     | Parkinsonism secondary to drugs                                                                                       | Parkinson's disease (all)                 |
| F123.     | Postencephalitic parkinsonism                                                                                         | Parkinson's disease (all)                 |
| F124.     | Vascular parkinsonism                                                                                                 | Parkinson's disease (all)                 |
| F12W.     | Secondary parkinsonism due to other external agents                                                                   | Parkinson's disease (all)                 |
| F12X.     | Secondary parkinsonism, unspecified                                                                                   | Parkinson's disease (all)                 |
| F12z.     | Parkinson's disease NOS                                                                                               | Parkinson's disease (all)                 |
| F1303     | Parkinsonism with orthostatic hypotension                                                                             | Parkinson's disease (all)                 |
| Fyu20     | \[X\]Other drug-induced secondary parkinsonism                                                                        | Parkinson's disease (all)                 |
| Fyu21     | \[X\]Other secondary parkinsonism                                                                                     | Parkinson's disease (all)                 |
| Fyu22     | \[X\]Parkinsonism in diseases classified elsewhere                                                                    | Parkinson's disease (all)                 |
| Fyu29     | \[X\]Secondary parkinsonism, unspecified                                                                              | Parkinson's disease (all)                 |
| Fyu2B     | \[X\]Secondary parkinsonism due to other external agents                                                              | Parkinson's disease (all)                 |
| 147F.     | History of Parkinson's disease                                                                                        | Parkinson's disease (excluding secondary) |
| 297A.     | O/E - Parkinsonian tremor                                                                                             | Parkinson's disease (excluding secondary) |
| 2987      | O/E -Parkinson flexion posture                                                                                        | Parkinson's disease (excluding secondary) |
| 2994      | O/E-festination-Parkinson gait                                                                                        | Parkinson's disease (excluding secondary) |
| Eu023     | \[X\]Dementia in Parkinson's disease                                                                                  | Parkinson's disease (excluding secondary) |
| F11x9     | Cerebral degeneration in Parkinson's disease                                                                          | Parkinson's disease (excluding secondary) |
| F12..     | Parkinson's disease                                                                                                   | Parkinson's disease (excluding secondary) |
| F120.     | Paralysis agitans                                                                                                     | Parkinson's disease (excluding secondary) |
| F12z.     | Parkinson's disease NOS                                                                                               | Parkinson's disease (excluding secondary) |
| F1303     | Parkinsonism with orthostatic hypotension                                                                             | Parkinson's disease (excluding secondary) |
| Fyu22     | \[X\]Parkinsonism in diseases classified elsewhere                                                                    | Parkinson's disease (excluding secondary) |
| 14F2.     | H/O: psoriasis                                                                                                        | Psoriasis                                 |
| M160.     | Psoriatic arthropathy                                                                                                 | Psoriasis                                 |
| M1600     | Psoriasis spondylitica                                                                                                | Psoriasis                                 |
| M1601     | Distal interphalangeal psoriatic arthropathy                                                                          | Psoriasis                                 |
| M160z     | Psoriatic arthropathy NOS                                                                                             | Psoriasis                                 |
| M161.     | Other psoriasis                                                                                                       | Psoriasis                                 |
| M1610     | Psoriasis unspecified                                                                                                 | Psoriasis                                 |
| M1611     | Psoriasis annularis                                                                                                   | Psoriasis                                 |
| M1612     | Psoriasis circinata                                                                                                   | Psoriasis                                 |
| M1613     | Psoriasis diffusa                                                                                                     | Psoriasis                                 |
| M1614     | Psoriasis discoidea                                                                                                   | Psoriasis                                 |
| M1615     | Psoriasis geographica                                                                                                 | Psoriasis                                 |
| M1616     | Guttate psoriasis                                                                                                     | Psoriasis                                 |
| M1617     | Psoriasis gyrata                                                                                                      | Psoriasis                                 |
| M1618     | Psoriasis inveterata                                                                                                  | Psoriasis                                 |
| M1619     | Psoriasis ostracea                                                                                                    | Psoriasis                                 |
| M161A     | Psoriasis palmaris                                                                                                    | Psoriasis                                 |
| M161B     | Psoriasis plantaris                                                                                                   | Psoriasis                                 |
| M161C     | Psoriasis punctata                                                                                                    | Psoriasis                                 |
| M161D     | Pustular psoriasis                                                                                                    | Psoriasis                                 |
| M161E     | Psoriasis universalis                                                                                                 | Psoriasis                                 |
| M161F     | Psoriasis vulgaris                                                                                                    | Psoriasis                                 |
| M161G     | Acrodermatitis continua                                                                                               | Psoriasis                                 |
| M161H     | Erythrodermic psoriasis                                                                                               | Psoriasis                                 |
| M161z     | Psoriasis NOS                                                                                                         | Psoriasis                                 |
| M16y.     | Other psoriasis and similar disorders                                                                                 | Psoriasis                                 |
| M16y0     | Scalp psoriasis                                                                                                       | Psoriasis                                 |
| M16z.     | Psoriasis and similar disorders NOS                                                                                   | Psoriasis                                 |
| Myu30     | \[X\]Other psoriasis                                                                                                  | Psoriasis                                 |
| N0452     | Juvenile arthritis in psoriasis                                                                                       | Psoriasis                                 |
| Nyu13     | \[X\]Other psoriatic arthropathies                                                                                    | Psoriasis                                 |
| N0452     | Juvenile arthritis in psoriasis                                                                                       | Psoriatic arthropathy                     |
| M1600     | Psoriasis spondylitica                                                                                                | Psoriatic arthropathy                     |
| M1601     | Distal interphalangeal psoriatic arthropathy                                                                          | Psoriatic arthropathy                     |
| M1602     | Arthritis mutilans                                                                                                    | Psoriatic arthropathy                     |
| Nyu13     | \[X\]Other psoriatic arthropathies                                                                                    | Psoriatic arthropathy                     |
| M160.     | Psoriatic arthropathy                                                                                                 | Psoriatic arthropathy                     |
| M160z     | Psoriatic arthropathy NOS                                                                                             | Psoriatic arthropathy                     |
| 66YB.     | Chronic obstructive pulmonary disease monitoring                                                                      | Pulmonary Disease, Chronic Obstructive    |
| 66Yd.     | COPD accident and emergency attendance since last visit                                                               | Pulmonary Disease, Chronic Obstructive    |
| 66YD.     | Chronic obstructive pulmonary disease monitoring due                                                                  | Pulmonary Disease, Chronic Obstructive    |
| 66Ye.     | Emergency COPD admission since last appointment                                                                       | Pulmonary Disease, Chronic Obstructive    |
| 66Yf.     | Number of COPD exacerbations in past year                                                                             | Pulmonary Disease, Chronic Obstructive    |
| 66Yg.     | Chronic obstructive pulmonary disease disturbs sleep                                                                  | Pulmonary Disease, Chronic Obstructive    |
| 66Yh.     | Chronic obstructive pulmonary disease does not disturb sleep                                                          | Pulmonary Disease, Chronic Obstructive    |
| 66Yi.     | Multiple COPD emergency hospital admissions                                                                           | Pulmonary Disease, Chronic Obstructive    |
| 66YI.     | COPD self-management plan given                                                                                       | Pulmonary Disease, Chronic Obstructive    |
| 66YL.     | Chronic obstructive pulmonary disease follow-up                                                                       | Pulmonary Disease, Chronic Obstructive    |
| 66YM.     | Chronic obstructive pulmonary disease annual review                                                                   | Pulmonary Disease, Chronic Obstructive    |
| 66YS.     | Chronic obstructive pulmonary disease monitoring by nurse                                                             | Pulmonary Disease, Chronic Obstructive    |
| 66YT.     | Chronic obstructive pulmonary disease monitoring by doctor                                                            | Pulmonary Disease, Chronic Obstructive    |
| 8CR1.     | Chronic obstructive pulmonary disease clini management plan                                                           | Pulmonary Disease, Chronic Obstructive    |
| H3...     | Chronic obstructive pulmonary disease                                                                                 | Pulmonary Disease, Chronic Obstructive    |
| H3121     | Emphysematous bronchitis                                                                                              | Pulmonary Disease, Chronic Obstructive    |
| H3122     | Acute exacerbation of chronic obstructive airways disease                                                             | Pulmonary Disease, Chronic Obstructive    |
| H312z     | Obstructive chronic bronchitis NOS                                                                                    | Pulmonary Disease, Chronic Obstructive    |
| H32..     | Emphysema                                                                                                             | Pulmonary Disease, Chronic Obstructive    |
| H320.     | Chronic bullous emphysema                                                                                             | Pulmonary Disease, Chronic Obstructive    |
| H3200     | Segmental bullous emphysema                                                                                           | Pulmonary Disease, Chronic Obstructive    |
| H3201     | Zonal bullous emphysema                                                                                               | Pulmonary Disease, Chronic Obstructive    |
| H3202     | Giant bullous emphysema                                                                                               | Pulmonary Disease, Chronic Obstructive    |
| H3203     | Bullous emphysema with collapse                                                                                       | Pulmonary Disease, Chronic Obstructive    |
| H320z     | Chronic bullous emphysema NOS                                                                                         | Pulmonary Disease, Chronic Obstructive    |
| H321.     | Panlobular emphysema                                                                                                  | Pulmonary Disease, Chronic Obstructive    |
| H322.     | Centrilobular emphysema                                                                                               | Pulmonary Disease, Chronic Obstructive    |
| H32y.     | Other emphysema                                                                                                       | Pulmonary Disease, Chronic Obstructive    |
| H32y0     | Acute vesicular emphysema                                                                                             | Pulmonary Disease, Chronic Obstructive    |
| H32y1     | Atrophic (senile) emphysema                                                                                           | Pulmonary Disease, Chronic Obstructive    |
| H32y2     | MacLeod's unilateral emphysema                                                                                        | Pulmonary Disease, Chronic Obstructive    |
| H32yz     | Other emphysema NOS                                                                                                   | Pulmonary Disease, Chronic Obstructive    |
| H32z.     | Emphysema NOS                                                                                                         | Pulmonary Disease, Chronic Obstructive    |
| H36..     | Mild chronic obstructive pulmonary disease                                                                            | Pulmonary Disease, Chronic Obstructive    |
| H37..     | Moderate chronic obstructive pulmonary disease                                                                        | Pulmonary Disease, Chronic Obstructive    |
| H38..     | Severe chronic obstructive pulmonary disease                                                                          | Pulmonary Disease, Chronic Obstructive    |
| H39..     | Very severe chronic obstructive pulmonary disease                                                                     | Pulmonary Disease, Chronic Obstructive    |
| H3y..     | Other specified chronic obstructive airways disease                                                                   | Pulmonary Disease, Chronic Obstructive    |
| H3y0.     | Chronic obstruct pulmonary dis with acute lower resp infectn                                                          | Pulmonary Disease, Chronic Obstructive    |
| H3y1.     | Chron obstruct pulmonary dis wth acute exacerbation, unspec                                                           | Pulmonary Disease, Chronic Obstructive    |
| H3z..     | Chronic obstructive airways disease NOS                                                                               | Pulmonary Disease, Chronic Obstructive    |
| H4640     | Chronic emphysema due to chemical fumes                                                                               | Pulmonary Disease, Chronic Obstructive    |
| Hyu3.     | \[X\]Chronic lower respiratory diseases                                                                               | Pulmonary Disease, Chronic Obstructive    |
| Hyu30     | \[X\]Other emphysema                                                                                                  | Pulmonary Disease, Chronic Obstructive    |
| Hyu31     | \[X\]Other specified chronic obstructive pulmonary disease                                                            | Pulmonary Disease, Chronic Obstructive    |
| F13z2     | Ekbom syndrome                                                                                                        | Restless legs syndrome                    |
| 14G1.     | H/O: rheumatoid arthritis                                                                                             | Rheumatoid arthritis                      |
| F3712     | Polyneuropathy in rheumatoid arthritis                                                                                | Rheumatoid arthritis                      |
| F3964     | Myopathy due to rheumatoid arthritis                                                                                  | Rheumatoid arthritis                      |
| G5yA.     | Rheumatoid carditis                                                                                                   | Rheumatoid arthritis                      |
| G5y8.     | Rheumatoid myocarditis                                                                                                | Rheumatoid arthritis                      |
| H570.     | Rheumatoid lung                                                                                                       | Rheumatoid arthritis                      |
| N04..     | Rheumatoid arthritis and other inflammatory polyarthropathy                                                           | Rheumatoid arthritis                      |
| N040.     | Rheumatoid arthritis                                                                                                  | Rheumatoid arthritis                      |
| N0400     | Rheumatoid arthritis of cervical spine                                                                                | Rheumatoid arthritis                      |
| N0401     | Other rheumatoid arthritis of spine                                                                                   | Rheumatoid arthritis                      |
| N0402     | Rheumatoid arthritis of shoulder                                                                                      | Rheumatoid arthritis                      |
| N0403     | Rheumatoid arthritis of sternoclavicular joint                                                                        | Rheumatoid arthritis                      |
| N0404     | Rheumatoid arthritis of acromioclavicular joint                                                                       | Rheumatoid arthritis                      |
| N0405     | Rheumatoid arthritis of elbow                                                                                         | Rheumatoid arthritis                      |
| N0406     | Rheumatoid arthritis of distal radio-ulnar joint                                                                      | Rheumatoid arthritis                      |
| N0407     | Rheumatoid arthritis of wrist                                                                                         | Rheumatoid arthritis                      |
| N0408     | Rheumatoid arthritis of MCP joint                                                                                     | Rheumatoid arthritis                      |
| N0409     | Rheumatoid arthritis of PIP joint of finger                                                                           | Rheumatoid arthritis                      |
| N040A     | Rheumatoid arthritis of DIP joint of finger                                                                           | Rheumatoid arthritis                      |
| N040B     | Rheumatoid arthritis of hip                                                                                           | Rheumatoid arthritis                      |
| N040C     | Rheumatoid arthritis of sacro-iliac joint                                                                             | Rheumatoid arthritis                      |
| N040D     | Rheumatoid arthritis of knee                                                                                          | Rheumatoid arthritis                      |
| N040E     | Rheumatoid arthritis of tibio-fibular joint                                                                           | Rheumatoid arthritis                      |
| N040F     | Rheumatoid arthritis of ankle                                                                                         | Rheumatoid arthritis                      |
| N040G     | Rheumatoid arthritis of subtalar joint                                                                                | Rheumatoid arthritis                      |
| N040H     | Rheumatoid arthritis of talonavicular joint                                                                           | Rheumatoid arthritis                      |
| N040J     | Rheumatoid arthritis of other tarsal joint                                                                            | Rheumatoid arthritis                      |
| N040K     | Rheumatoid arthritis of 1st MTP joint                                                                                 | Rheumatoid arthritis                      |
| N040L     | Rheumatoid arthritis of lesser MTP joint                                                                              | Rheumatoid arthritis                      |
| N040M     | Rheumatoid arthritis of IP joint of toe                                                                               | Rheumatoid arthritis                      |
| N040N     | Rheumatoid vasculitis                                                                                                 | Rheumatoid arthritis                      |
| N040P     | Seronegative rheumatoid arthritis                                                                                     | Rheumatoid arthritis                      |
| N040Q     | Rheumatoid bursitis                                                                                                   | Rheumatoid arthritis                      |
| N040R     | Rheumatoid nodule                                                                                                     | Rheumatoid arthritis                      |
| N040S     | Rheumatoid arthritis - multiple joint                                                                                 | Rheumatoid arthritis                      |
| N040T     | Flare of rheumatoid arthritis                                                                                         | Rheumatoid arthritis                      |
| N041.     | Felty's syndrome                                                                                                      | Rheumatoid arthritis                      |
| N042.     | Other rheumatoid arthropathy + visceral/systemic involvement                                                          | Rheumatoid arthritis                      |
| N0421     | Rheumatoid lung disease                                                                                               | Rheumatoid arthritis                      |
| N0422     | Rheumatoid nodule                                                                                                     | Rheumatoid arthritis                      |
| N042z     | Rheumatoid arthropathy + visceral/systemic involvement NOS                                                            | Rheumatoid arthritis                      |
| N043.     | Juvenile rheumatoid arthritis - Still's disease                                                                       | Rheumatoid arthritis                      |
| N0430     | Juvenile rheumatoid arthropathy unspecified                                                                           | Rheumatoid arthritis                      |
| N0431     | Acute polyarticular juvenile rheumatoid arthritis                                                                     | Rheumatoid arthritis                      |
| N0432     | Pauciarticular juvenile rheumatoid arthritis                                                                          | Rheumatoid arthritis                      |
| N0433     | Monarticular juvenile rheumatoid arthritis                                                                            | Rheumatoid arthritis                      |
| N043z     | Juvenile rheumatoid arthritis NOS                                                                                     | Rheumatoid arthritis                      |
| N047.     | Seropositive errosive rheumatoid arthritis                                                                            | Rheumatoid arthritis                      |
| N04X.     | Seropositive rheumatoid arthritis, unspecified                                                                        | Rheumatoid arthritis                      |
| N04y2     | Adult-onset Still's disease                                                                                           | Rheumatoid arthritis                      |
| N0455     | Juvenile rheumatoid arthritis                                                                                         | Rheumatoid arthritis                      |
| Nyu43     | \[X\]Other forms of systemic lupus erythematosus                                                                      | Systemic Lupus Erythematosus              |
| H57y4     | Lung disease with systemic lupus erythematosus                                                                        | Systemic Lupus Erythematosus              |
| K01x4     | Nephrotic syndrome in systemic lupus erythematosus                                                                    | Systemic Lupus Erythematosus              |
| K0B40     | Renal tubulo-interstitial disorder in SLE                                                                             | Systemic Lupus Erythematosus              |
| N000.     | Systemic lupus erythematosus                                                                                          | Systemic Lupus Erythematosus              |
| N0000     | Disseminated lupus erythematosus                                                                                      | Systemic Lupus Erythematosus              |
| N0002     | Drug-induced systemic lupus erythematosus                                                                             | Systemic Lupus Erythematosus              |
| N0003     | Systemic lupus erythematosus with organ or sys involv                                                                 | Systemic Lupus Erythematosus              |
| N0004     | Systemic lupus erythematosus with pericarditis                                                                        | Systemic Lupus Erythematosus              |
| N000z     | Systemic lupus erythematosus NOS                                                                                      | Systemic Lupus Erythematosus              |
| F371.     | Polyneuropathy in collagen vascular disease                                                                           | Systemic Lupus Erythematosus              |
| F3961     | Myopathy due to disseminated lupus erythematosus                                                                      | Systemic Lupus Erythematosus              |
| 14A8.00   | H/O: thrombo-embolism                                                                                                 | Thromboembolism                           |
| 14A8100   | H/O: Deep Vein Thrombosis                                                                                             | Thromboembolism                           |
| 14A8.11   | H/O: embolism                                                                                                         | Thromboembolism                           |
| 14A8.12   | H/O: thrombosis                                                                                                       | Thromboembolism                           |
| 14AC.00   | H/O: pulmonary embolus                                                                                                | Thromboembolism                           |
| G401.00   | Pulmonary embolism                                                                                                    | Thromboembolism                           |
| G401000   | Post operative pulmonary embolus                                                                                      | Thromboembolism                           |
| G401100   | Recurrent pulmonary embolism                                                                                          | Thromboembolism                           |
| G401.11   | Infarction - pulmonary                                                                                                | Thromboembolism                           |
| G401.12   | Pulmonary embolus                                                                                                     | Thromboembolism                           |
| G41y100   | Thromboembolic pulmonary hypertension                                                                                 | Thromboembolism                           |
| G74..00   | Arterial embolism and thrombosis                                                                                      | Thromboembolism                           |
| G740.00   | Embolism and thrombosis of the abdominal aorta                                                                        | Thromboembolism                           |
| G740.11   | Aortic bifurcation syndrome                                                                                           | Thromboembolism                           |
| G740.12   | Aortoiliac obstruction                                                                                                | Thromboembolism                           |
| G740.13   | Leriche's syndrome                                                                                                    | Thromboembolism                           |
| G740.14   | Saddle embolus                                                                                                        | Thromboembolism                           |
| G741.00   | Embolism and thrombosis of the thoracic aorta                                                                         | Thromboembolism                           |
| G74..11   | Arterial embolus and thrombosis                                                                                       | Thromboembolism                           |
| G74..12   | Thrombosis - arterial                                                                                                 | Thromboembolism                           |
| G74..13   | Arterial embolic and thrombotic occlusion                                                                             | Thromboembolism                           |
| G742.00   | Embolism and thrombosis of an arm or leg artery                                                                       | Thromboembolism                           |
| G742000   | Embolism and thrombosis of the brachial artery                                                                        | Thromboembolism                           |
| G742100   | Embolism and thrombosis of the radial artery                                                                          | Thromboembolism                           |
| G742200   | Embolism and thrombosis of the ulnar artery                                                                           | Thromboembolism                           |
| G742300   | Embolism and thrombosis of an arm artery NOS                                                                          | Thromboembolism                           |
| G742400   | Embolism and thrombosis of the femoral artery                                                                         | Thromboembolism                           |
| G742500   | Embolism and thrombosis of the popliteal artery                                                                       | Thromboembolism                           |
| G742600   | Embolism and thrombosis of the anterior tibial artery                                                                 | Thromboembolism                           |
| G742700   | Embolism and thrombosis of the dorsalis pedis artery                                                                  | Thromboembolism                           |
| G742800   | Embolism and thrombosis of the posterior tibial artery                                                                | Thromboembolism                           |
| G742900   | Embolism and thrombosis of a leg artery NOS                                                                           | Thromboembolism                           |
| G742A00   | Post radiological embolism of upper limb artery                                                                       | Thromboembolism                           |
| G742B00   | Post radiological embolism of lower limb artery                                                                       | Thromboembolism                           |
| G742z00   | Peripheral arterial embolism and thrombosis NOS                                                                       | Thromboembolism                           |
| G743.00   | Embolism and thrombosis of other and unspec parts aorta                                                               | Thromboembolism                           |
| G74y.00   | Embolism and thrombosis of other specified artery                                                                     | Thromboembolism                           |
| G74y000   | Embolism and/or thrombosis of the common iliac artery                                                                 | Thromboembolism                           |
| G74y100   | Embolism and/or thrombosis of the internal iliac artery                                                               | Thromboembolism                           |
| G74y200   | Embolism and/or thrombosis of the external iliac artery                                                               | Thromboembolism                           |
| G74y300   | Embolism and thrombosis of the iliac artery unspecified                                                               | Thromboembolism                           |
| G74y500   | Embolism and thrombosis of the subclavian artery                                                                      | Thromboembolism                           |
| G74y600   | Embolism and thrombosis of the splenic artery                                                                         | Thromboembolism                           |
| G74y700   | Embolism and thrombosis of the axillary artery                                                                        | Thromboembolism                           |
| G74y800   | Embolism and thrombosis of the coeliac artery                                                                         | Thromboembolism                           |
| G74y900   | Embolism and thrombosis of the hepatic artery                                                                         | Thromboembolism                           |
| G74yz00   | Embolism and thrombosis of other arteries NOS                                                                         | Thromboembolism                           |
| G74z.00   | Arterial embolism and thrombosis NOS                                                                                  | Thromboembolism                           |
| G801.00   | Deep vein phlebitis and thrombophlebitis of the leg                                                                   | Thromboembolism                           |
| G801000   | Phlebitis of the femoral vein                                                                                         | Thromboembolism                           |
| G801100   | Phlebitis of the popliteal vein                                                                                       | Thromboembolism                           |
| G801.11   | Deep vein thrombosis                                                                                                  | Thromboembolism                           |
| G801.12   | Deep vein thrombosis; leg                                                                                             | Thromboembolism                           |
| G801.13   | DVT - Deep vein thrombosis                                                                                            | Thromboembolism                           |
| G801200   | Phlebitis of the anterior tibial vein                                                                                 | Thromboembolism                           |
| G801400   | Phlebitis of the posterior tibial vein                                                                                | Thromboembolism                           |
| G801500   | Deep vein phlebitis of the leg unspecified                                                                            | Thromboembolism                           |
| G801600   | Thrombophlebitis of the femoral vein                                                                                  | Thromboembolism                           |
| G801700   | Thrombophlebitis of the popliteal vein                                                                                | Thromboembolism                           |
| G801800   | Thrombophlebitis of the anterior tibial vein                                                                          | Thromboembolism                           |
| G801900   | Thrombophlebitis of the dorsalis pedis vein                                                                           | Thromboembolism                           |
| G801A00   | Thrombophlebitis of the posterior tibial vein                                                                         | Thromboembolism                           |
| G801B00   | Deep vein thrombophlebitis of the leg unspecified                                                                     | Thromboembolism                           |
| G801C00   | Deep vein thrombosis of leg related to air travel                                                                     | Thromboembolism                           |
| G801D00   | Deep vein thrombosis of lower limb                                                                                    | Thromboembolism                           |
| G801E00   | Deep vein thrombosis of leg related to intravenous drug use                                                           | Thromboembolism                           |
| G801F00   | Deep vein thrombosis of peroneal vein                                                                                 | Thromboembolism                           |
| G801G00   | Recurrent deep vein thrombosis                                                                                        | Thromboembolism                           |
| G801z00   | Deep vein phlebitis and thrombophlebitis of the leg NOS                                                               | Thromboembolism                           |
| G802000   | Thrombosis of vein of leg                                                                                             | Thromboembolism                           |
| G81..00   | Portal vein thrombosis                                                                                                | Thromboembolism                           |
| G82..00   | Other venous embolism and thrombosis                                                                                  | Thromboembolism                           |
| G820.00   | Budd - Chiari syndrome (hepatic vein thrombosis)                                                                      | Thromboembolism                           |
| G820.11   | Hepatic vein thrombosis                                                                                               | Thromboembolism                           |
| G821.00   | Thrombophlebitis migrans                                                                                              | Thromboembolism                           |
| G822.00   | Embolism and thrombosis of the vena cava                                                                              | Thromboembolism                           |
| G822000   | Thrombosis of inferior vena cava                                                                                      | Thromboembolism                           |
| G823.00   | Embolism and thrombosis of the renal vein                                                                             | Thromboembolism                           |
| G824.00   | Axillary vein thrombosis                                                                                              | Thromboembolism                           |
| G825.00   | Thrombosis of subclavian vein                                                                                         | Thromboembolism                           |
| G826.00   | Thrombosis of internal jugular vein                                                                                   | Thromboembolism                           |
| G827.00   | Thrombosis of external jugular vein                                                                                   | Thromboembolism                           |
| G82y.00   | Other embolism and thrombosis                                                                                         | Thromboembolism                           |
| G82z.00   | Embolism and thrombosis NOS                                                                                           | Thromboembolism                           |
| G82z000   | Embolus of vein NOS                                                                                                   | Thromboembolism                           |
| G82z011   | Embolism of vein NOS                                                                                                  | Thromboembolism                           |
| G82z100   | Thrombosis of vein NOS                                                                                                | Thromboembolism                           |
| G82zz00   | Embolism and thrombosis NOS                                                                                           | Thromboembolism                           |
| G8y4.00   | Postthrombotic syndrome                                                                                               | Thromboembolism                           |
| Gyu8200   | \[X\]Embolism and thrombosis of other specified veins                                                                 | Thromboembolism                           |
| SP12200   | Post operative deep vein thrombosis                                                                                   | Thromboembolism                           |
| SP32100   | Thromboembolism after infusion                                                                                        | Thromboembolism                           |
| ZV12800   | \[V\] Personal history deep vein thrombosis                                                                           | Thromboembolism                           |
| ZV12811   | \[V\] Personal history DVT- deep vein thrombosis                                                                      | Thromboembolism                           |
| ZV12900   | \[V\] Personal history of pulmonary embolism                                                                          | Thromboembolism                           |
| X7039     | Spondylosis                                                                                                           | Osteoarthritis                            |
| X703j     | Cervical spondylosis                                                                                                  | Osteoarthritis                            |
| N119.     | Cervical spondylosis with radiculopathy                                                                               | Osteoarthritis                            |
| N1190     | Single-level cervical spondylosis with radiculopathy                                                                  | Osteoarthritis                            |
| N1191     | Two-level cervical spondylosis with radiculopathy                                                                     | Osteoarthritis                            |
| N1192     | Multiple-level cervical spondylosis with radiculopathy                                                                | Osteoarthritis                            |
| XE1Ev     | Cervical spondylosis with myelopathy                                                                                  | Osteoarthritis                            |
| N1110     | Single-level cervical spondylosis with myelopathy                                                                     | Osteoarthritis                            |
| N1111     | Two-level cervical spondylosis with myelopathy                                                                        | Osteoarthritis                            |
| N1112     | Multiple-level cervical spondylosis with myelopathy                                                                   | Osteoarthritis                            |
| N11A.     | Cervical spondylosis with vascular compression                                                                        | Osteoarthritis                            |
| XE1Eu     | Cervical spondylosis without myelopathy                                                                               | Osteoarthritis                            |
| N1100     | Single-level cervical spondylosis without myelopathy                                                                  | Osteoarthritis                            |
| N1101     | Two-level cervical spondylosis without myelopathy                                                                     | Osteoarthritis                            |
| N1102     | Multiple-level cervical spondylosis without myelopathy                                                                | Osteoarthritis                            |
| N110.     | Cervical spondylosis (& \[without myelopathy\]) or (osteoarthritis cervical spine)                                    | Osteoarthritis                            |
| X70Cw     | Thoracic spondylosis                                                                                                  | Osteoarthritis                            |
| N11B.     | Thoracic spondylosis with radiculopathy                                                                               | Osteoarthritis                            |
| N11B0     | Single-level thoracic spondylosis with radiculopathy                                                                  | Osteoarthritis                            |
| N11B1     | Two-level thoracic spondylosis with radiculopathy                                                                     | Osteoarthritis                            |
| N11B2     | Multiple-level thoracic spondylosis with radiculopathy                                                                | Osteoarthritis                            |
| N113.     | Thoracic spondylosis with myelopathy                                                                                  | Osteoarthritis                            |
| N1130     | Single-level thoracic spondylosis with myelopathy                                                                     | Osteoarthritis                            |
| N1131     | Two-level thoracic spondylosis with myelopathy                                                                        | Osteoarthritis                            |
| N1132     | Multiple-level thoracic spondylosis with myelopathy                                                                   | Osteoarthritis                            |
| XE1Ew     | Thoracic spondylosis without myelopathy                                                                               | Osteoarthritis                            |
| N1120     | Single-level thoracic spondylosis without myelopathy                                                                  | Osteoarthritis                            |
| N1121     | Two-level thoracic spondylosis without myelopathy                                                                     | Osteoarthritis                            |
| N1122     | Multiple-level thoracic spondylosis without myelopathy                                                                | Osteoarthritis                            |
| N112.     | Thoracic spondylosis (& \[without myelopathy\])                                                                       | Osteoarthritis                            |
| XaE3C     | Lumbosacral spondylosis                                                                                               | Osteoarthritis                            |
| X703k     | Lumbar spondylosis                                                                                                    | Osteoarthritis                            |
| N11C.     | Lumbosacral spondylosis with radiculopathy                                                                            | Osteoarthritis                            |
| N11C0     | Single-level lumbosacral spondylosis with radiculopathy                                                               | Osteoarthritis                            |
| N11C1     | Two-level lumbosacral spondylosis with radiculopathy                                                                  | Osteoarthritis                            |
| N11C2     | Multiple-level lumbosacral spondylosis with radiculopathy                                                             | Osteoarthritis                            |
| N115.     | Lumbosacral spondylosis with myelopathy                                                                               | Osteoarthritis                            |
| N1150     | Single-level lumbosacral spondylosis with myelopathy                                                                  | Osteoarthritis                            |
| N1151     | Two-level lumbosacral spondylosis with myelopathy                                                                     | Osteoarthritis                            |
| N1152     | Multiple-level lumbosacral spondylosis with myelopathy                                                                | Osteoarthritis                            |
| XE1Ex     | Lumbosacral spondylosis without myelopathy                                                                            | Osteoarthritis                            |
| N1140     | Single-level lumbosacral spondylosis without myelopathy                                                               | Osteoarthritis                            |
| N1141     | Two-level lumbosacral spondylosis without myelopathy                                                                  | Osteoarthritis                            |
| N1142     | Multiple-level lumbosacral spondylosis without myelopathy                                                             | Osteoarthritis                            |
| N11y.     | Other spondyloses and allied disorders                                                                                | Osteoarthritis                            |
| Nyu62     | \[X\]Other spondylosis with myelopathy                                                                                | Osteoarthritis                            |
| Nyu63     | \[X\]Other spondylosis with radiculopathy                                                                             | Osteoarthritis                            |
| Nyu64     | \[X\]Other spondylosis                                                                                                | Osteoarthritis                            |
| XE1Ey     | Spondylosis NOS                                                                                                       | Osteoarthritis                            |
| N11z0     | Spondylosis without myelopathy, NOS                                                                                   | Osteoarthritis                            |
| N11z1     | Spondylosis with myelopathy, NOS                                                                                      | Osteoarthritis                            |
| N114.     | (Lumbosacral spondylosis \[& without myelopathy\]) or (degeneration of lumbar spine)                                  | Osteoarthritis                            |
| N11z.     | (Spondylosis NOS) or (osteoarthritis spine)                                                                           | Osteoarthritis                            |
| XE1HM     | (Spondyloses: \[cervical\] or \[lumbar\] or \[sacral\]) or (arthritis - spine) or (osteoarthritis - spine)            | Osteoarthritis                            |
| X703A     | Osteoarthritis of spinal facet joint                                                                                  | Osteoarthritis                            |
| X703F     | Osteoarthritis of first carpometacarpal joint                                                                         | Osteoarthritis                            |
| X703G     | Osteoarthritis of finger joint                                                                                        | Osteoarthritis                            |
| X703H     | Osteoarthritis of distal interphalangeal joint                                                                        | Osteoarthritis                            |
| N05zH     | Osteoarthritis NOS, of distal interphalangeal joint of finger                                                         | Osteoarthritis                            |
| X703I     | Osteoarthritis of proximal interphalangeal joint                                                                      | Osteoarthritis                            |
| N05zG     | Osteoarthritis NOS, of proximal interphalangeal joint of finger                                                       | Osteoarthritis                            |
| X703J     | Osteoarthritis of metacarpophalangeal joint of finger                                                                 | Osteoarthritis                            |
| X7035     | Finger osteoarthritis NOS                                                                                             | Osteoarthritis                            |
| X703K     | Osteoarthritis of hip                                                                                                 | Osteoarthritis                            |
| N05zJ     | Osteoarthritis NOS, of hip                                                                                            | Osteoarthritis                            |
| X703L     | Osteoarthritis of knee                                                                                                | Osteoarthritis                            |
| XaYQD     | Patellofemoral osteoarthritis                                                                                         | Osteoarthritis                            |
| N05zL     | Osteoarthritis NOS, of knee                                                                                           | Osteoarthritis                            |
| N0514     | Localised, primary osteoarthritis of the hand                                                                         | Osteoarthritis                            |
| N0524     | Localised, secondary osteoarthritis of the hand                                                                       | Osteoarthritis                            |
| N0534     | Localised osteoarthritis, unspecified, of the hand                                                                    | Osteoarthritis                            |
| N0539     | Arthrosis of first carpometacarpal joint, unspecified                                                                 | Osteoarthritis                            |
| XM1NQ     | Osteoarthritis of metacarpophalangeal joint                                                                           | Osteoarthritis                            |
| Xa3gQ     | Osteoarthritis - hand joint                                                                                           | Osteoarthritis                            |
| N0535     | (Otto's pelvis) or (hip osteoarthitis NOS) or (localised osteoarthritis, unspecified, of the pelvic region and thigh) | Osteoarthritis                            |
| N0507     | Heberden's nodes with arthropathy                                                                                     | Osteoarthritis                            |
| N0503     | Bouchard's nodes with arthropathy                                                                                     | Osteoarthritis                            |
| XE1DW     | Generalised osteoarthritis of the hand                                                                                | Osteoarthritis                            |
| N0501     | (Heberdens' nodes) or (Bouchards' nodes) or (generalised osteoarthritis of the hand)                                  | Osteoarthritis                            |
| N0614     | Traumatic arthropathy of the hand                                                                                     | Osteoarthritis                            |
| N061G     | Traumatic arthropathy of metacarpophalangeal joint                                                                    | Osteoarthritis                            |
| N061H     | Traumatic arthropathy of proximal interphalangeal joint of finger                                                     | Osteoarthritis                            |
| N061J     | Traumatic arthropathy of distal interphalangeal joint of finger                                                       | Osteoarthritis                            |
| N061K     | Traumatic arthropathy-hip                                                                                             | Osteoarthritis                            |
| N061M     | Traumatic arthropathy-knee                                                                                            | Osteoarthritis                            |
| N11y2     | Neuropathic spondylopathy                                                                                             | Osteoarthritis                            |
| N0604     | Kaschin-Beck disease of the hand                                                                                      | Osteoarthritis                            |
| N0544     | Oligoarticular osteoarthritis, unspecified, of hand                                                                   | Osteoarthritis                            |
| N05zF     | Osteoarthritis NOS, of metacarpophalangeal joint                                                                      | Osteoarthritis                            |
| N05zL     | Osteoarthritis NOS, of knee                                                                                           | Osteoarthritis                            |
| XE1Dd     | Osteoarthritis NOS, of the hand                                                                                       | Osteoarthritis                            |
| X7034     | Thumb osteoarthritis NOS                                                                                              | Osteoarthritis                            |
| N05z4     | Osteoarthritis NOS: \[hand\] or \[finger\] or \[thumb\]                                                               | Osteoarthritis                            |
| N05z5     | Osteoarthritis NOS: \[pelvic region and/or thigh\] or \[hip\]                                                         | Osteoarthritis                            |
| XE1DV     | Osteoarthrosis                                                                                                        | Osteoarthritis                            |
| XaIna     | Exacerbation of osteoarthritis                                                                                        | Osteoarthritis                            |
| X703Q     | Secondary osteoarthritis                                                                                              | Osteoarthritis                            |
| N050.     | Generalised osteoarthritis                                                                                            | Osteoarthritis                            |
| N0500     | Generalised osteoarthritis of unspecified site                                                                        | Osteoarthritis                            |
| N0502     | Generalised osteoarthritis of multiple sites                                                                          | Osteoarthritis                            |
| N050z     | Generalised osteoarthritis NOS                                                                                        | Osteoarthritis                            |
| N0505     | Secondary multiple arthrosis                                                                                          | Osteoarthritis                            |
| N0619     | Traumatic arthropathy of multiple sites                                                                               | Osteoarthritis                            |
| N0609     | Kaschin-Beck disease of multiple sites                                                                                | Osteoarthritis                            |
| X7038     | Idiopathic osteoarthritis                                                                                             | Osteoarthritis                            |
| N0506     | Erosive osteoarthrosis                                                                                                | Osteoarthritis                            |
| N054.     | Oligoarticular osteoarthritis, unspecified                                                                            | Osteoarthritis                            |
| N0540     | Oligoarticular osteoarthritis, unspecified, of unspecified sites                                                      | Osteoarthritis                            |
| N0545     | Oligoarticular osteoarthritis, unspecified, of the pelvic region and thigh                                            | Osteoarthritis                            |
| N0549     | Oligoarticular osteoarthritis, unspecified, of multiple sites                                                         | Osteoarthritis                            |
| N054z     | Osteoarthritis of more than one site, unspecified, NOS                                                                | Osteoarthritis                            |
| XE1Da     | Osteoarthritis NOS                                                                                                    | Osteoarthritis                            |
| XE1Gm     | Osteoarthritis -multiple joint                                                                                        | Osteoarthritis                            |
| N05z.     | \[Joint degeneration\] or \[osteoarthritis NOS\]                                                                      | Osteoarthritis                            |
| X703E     | Osteoarthritis of wrist                                                                                               | Osteoarthritis                            |
| N05zE     | Osteoarthritis NOS, of wrist                                                                                          | Osteoarthritis                            |
| XaEGd     | Localised, primary osteoarthritis of the wrist                                                                        | Osteoarthritis                            |
| N0515     | Localised, primary osteoarthritis of the pelvic region and thigh                                                      | Osteoarthritis                            |
| XE1DX     | Localised, secondary osteoarthritis of the pelvic region and thigh                                                    | Osteoarthritis                            |
| XE1DY     | Localised osteoarthritis, unspecified, of the pelvic region and thigh                                                 | Osteoarthritis                            |
| N0615     | Traumatic arthropathy of the pelvic region and thigh                                                                  | Osteoarthritis                            |
| N061E     | Traumatic arthropathy of distal radioulnar joint                                                                      | Osteoarthritis                            |
| N061F     | Traumatic arthropathy-wrist                                                                                           | Osteoarthritis                            |
| N0605     | Kaschin-Beck disease of the pelvic region and thigh                                                                   | Osteoarthritis                            |
| N05zD     | Osteoarthritis NOS, of distal radioulnar joint                                                                        | Osteoarthritis                            |
| N05zE     | Osteoarthritis NOS, of wrist                                                                                          | Osteoarthritis                            |
| XE1De     | Osteoarthritis NOS, pelvic region/thigh                                                                               | Osteoarthritis                            |
| N05z3     | Osteoarthritis NOS: \[of the forearm\] or \[wrist\]                                                                   | Osteoarthritis                            |
| H563.00   | idiopathic fibrosing alveolitis                                                                                       | Pulmonary fibrosis                        |
| H563.11   | Hamman?ich syndrome                                                                                                   | Pulmonary fibrosis                        |
| H563.12   | cryptogenic fibrosing alveolitis                                                                                      | Pulmonary fibrosis                        |
| H563.13   | Idiopathic pulmonary fibrosis                                                                                         | Pulmonary fibrosis                        |
| H563100   | diffuse pulmonary fibrosis                                                                                            | Pulmonary fibrosis                        |
| H563200   | Pulmonary fibrosis                                                                                                    | Pulmonary fibrosis                        |
| H563z     | Idiopathic fibrosing alveolitis                                                                                       | Pulmonary fibrosis                        |
| H563z00   | idiopathic fibrosing alveolitis NOS                                                                                   | Pulmonary fibrosis                        |
| X102v     | Usual interstitial pneumonitis                                                                                        | Pulmonary fibrosis                        |
| X102w     | Desquamative interstitial pneum                                                                                       | Pulmonary fibrosis                        |
| XE0Yb     | Cryptogenic fibrosing alveoliti                                                                                       | Pulmonary fibrosis                        |
| XE0Zr     | Idiopath. fibrosing alveolitis                                                                                        | Pulmonary fibrosis                        |

Table A2 OPCS codes for Hip and knee arthroplasty
-------------------------------------------------

| Type | definition\_or\_label | Item  | Code | Description of procedure (W) codes                                                             |
|:-----|:----------------------|:------|:-----|:-----------------------------------------------------------------------------------------------|
| Knee | Defining codes        | K1.1  | O181 | Primary hybrid prosthetic replacement knee joint using cement                                  |
| Knee | Defining codes        | K1.2  | O188 | Hybrid prosthetic replacement knee joint using cement, Other Specified                         |
| Knee | Defining codes        | K1.3  | O189 | Hybrid prosthetic replacement knee joint using cement, unspecified                             |
| Knee | Defining codes        | K1.4  | W401 | Primary total prosthetic replacement of knee joint using cement                                |
| Knee | Defining codes        | K1.5  | W408 | Total prosthetic replacement of knee joint using cement, Other specified                       |
| Knee | Defining codes        | K1.6  | W409 | Total prosthetic replacement of knee joint using cement, unspecified                           |
| Knee | Defining codes        | K1.7  | W411 | Primary total prosthetic replacement of knee joint not using cement                            |
| Knee | Defining codes        | K1.8  | W418 | Total prosthetic replacement of knee joint not using cement, Other specified                   |
| Knee | Defining codes        | K1.9  | W419 | Total prosthetic replacement of knee joint not using cement, Unspecified                       |
| Knee | Defining codes        | K1.10 | W421 | Primary total prosthetic replacement of knee joint NEC                                         |
| Knee | Defining codes        | K1.11 | W428 | Other total prosthetic replacement of knee joint, Other specified                              |
| Knee | Defining codes        | K1.12 | W429 | Other total prosthetic replacement of knee joint, Unspecified                                  |
| Hip  | Defining codes        | H1.1  | W371 | Primary total prosthetic replacement of hip joint using cement                                 |
| Hip  | Defining codes        | H1.2  | W378 | Total prosthetic replacement of hip joint using cement, Other specified                        |
| Hip  | Defining codes        | H1.3  | W379 | Total prosthetic replacement of hip joint using cement, Unspecified                            |
| Hip  | Defining codes        | H1.4  | W381 | Primary total prosthetic replacement of hip joint not using cement                             |
| Hip  | Defining codes        | H1.5  | W388 | Total prosthetic replacement of hip joint not using cement, Other specified                    |
| Hip  | Defining codes        | H1.6  | W389 | Total prosthetic replacement of hip joint not using cement, Unspecified                        |
| Hip  | Defining codes        | H1.7  | W391 | Primary total prosthetic replacement of hip joint NEC                                          |
| Hip  | Defining codes        | H1.8  | W398 | Other specified hybrid prosthetic replacement of hip joint using cemented acetabular component |
| Hip  | Defining codes        | H1.9  | W399 | Unspecified hybrid prosthetic replacement of hip joint using cemented acetabular component     |
| Hip  | Defining codes        | H1.14 | W931 | Primary hybrid prosthetic replacement of hip joint using cemented acetabular component         |
| Hip  | Defining codes        | H1.15 | W938 | Other specified hybrid prosthetic replacement of hip joint using cemented acetabular component |
| Hip  | Defining codes        | H1.16 | W939 | Unspecified hybrid prosthetic replacement of hip joint using cemented acetabular component     |
| Hip  | Defining codes        | H1.17 | W941 | Primary hybrid prosthetic replacement of hip joint using cemented femoral component            |
| Hip  | Defining codes        | H1.18 | W948 | Other specified hybrid prosthetic replacement of hip joint using cemented femoral component    |
| Hip  | Defining codes        | H1.19 | W949 | Unspecified hybrid prosthetic replacement of hip joint using cemented femoral component        |
| Hip  | Defining codes        | H1.20 | W951 | Primary hybrid prosthetic replacement of hip joint using cement NEC                            |
| Hip  | Defining codes        | H1.21 | W958 | Other specified hybrid prosthetic replacement of hip joint using cement                        |
| Hip  | Defining codes        | H1.22 | W959 | Unspecified hybrid prosthetic replacement of hip joint using cement                            |

We discovered that those compound codes (which required both anatomical and procedure codes for a definition) that we had previously planned to use to identify arthroplasty were not present in the BioBank dataset. Before examining whether or not they were present in SAIL, we excluded these codes from the definitions for hip and knee arthroplasty.
