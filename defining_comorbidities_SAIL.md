Protocol for analysis of comorbidity using SAIL data
================
David A McAllister
2018-11-09

Personnel
=========

The lead for this project is David McAllister (Wellcome Trust Intermediate Clinical Fellow and Beit Fellow, Senior Clinical Lecturer in Epidemiology in the University of Glasgow and Consultant in Public Health Medicine, NHS Information Services Division, National Services Scotland). He, or a postdoctoral researcher he employs at the University of Glasgow, will conduct the analysis.

Methodological support will be provided by Sofia Dias (Professor of Health Technology, University of York). She will not work directly with the data, and so will not need access to the SAIL safe haven.

Dr Peter Hanlon, an academic primary care doctor will also conduct data analysis.

Defining comorbidity
====================

The following text on defining comorbidity is taken from the for protocol defining comorbidity in trial data. We have not changed the wording to reflect the fact that these definitions will be used in a different setting (eg changing the terminology from participants to patients) in order to make this section as close as possible to a simple “mirror” of the same section in the protocol for analysing trial data.

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

An additional complexity is caused by the fact that for certain trials, sponsors have only provided less specific codes (eg 3 or 4-character codes) and not 5-character codes which uniquely identify each class (7-character codes identifying each agent). Where this is the case, but the drug name with or without route and indication information have been provided, we will assign each potentially-relevant drug to a WHO ATC code using the US Government drug metathesaurus (RXNORM). Where neither the drug name, nor sufficiently detailed drug-class information is provided, we will adopt a workaround suited to each definition (Table 1). The number of trials where this approach was needed will be reported.

The proportion of participants with and without comorbid diseases based on concomitant medications with and without relevant medical histories (in trials where these have been provided) will be compared in 2x2 contingency tables. We expect to find a higher proportion with the relevant condition from the reported medical history among those participants meeting the concomitant medication definitions (eg 80% versus 10% reporting diabetes in participants taking/not taking antidiabetic medications).

We had initially planned to add skin disease to the list of diagnoses, however we found that topical therapies were very poorly recorded in the trial data and so have opted to drop this from the comorbid disease definitions.

We mapped the ATC codes to Read codes (which are used in the SAIL data) offline, using the NHS Business Authority mappings and, for some more recent drugs such as novel antidiabetic drugs, by manually mapping between ATC and Read codes. The mapping was very good, even retaining information on route. For example the read code for topical beclamethasone preparations mapped to different ATC codes to those for oral preparations.

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

For the main comparison between trial and primary care data we will use the concomittant medication based definitions. This is because the recording of BMI, blood pressure, AST, ALT, platelets and haemoglobin are likely to be less consistent and less reliably coded than concomittant medication definitions. The non-concomittant medication based components will be included in secondary analysis if these are found to be recorded in a reasonable proportion of patients. We will identify the Read codes for these components in an iterative process, to attempt to obtain the most complete data available.

Estimate incidence of subsequent events
---------------------------------------

We will choose one or more index condition(s) for this analysis where that condition is common, where comorbidity among people with that condition is also common, and where there is some evidence from my (separate) analysis of trial data that treatment efficacy may differ by comorbidity status.

For these selected index conditions, we will fit time to event models for events of interest (hospitalisations and deaths). We will fit Cox proportional hazard models (or possibly parametric survival models) treating competing events as censoring events (ie these are cause-specific hazard ratios). We will include age, sex and comorbidities in the modelling. Continuous measures of comorbidity (eg FIB-4) will be treated as continuous variables, with fractional polynomials or cubic splines to allow for non-linearity. We will include main terms and interactions only where these both improve model fit and have an appreciable effect size (eg a hazard ratio of less than 0.96 or more than 1.04 for binary variables/per standard deviation in continuous variables).

Where small numbers of participants have a comorbidity we will drop that from the main analysis. We will also explore whether inclusion of specific comorbidities or comorbiditity counts (as a score) is a better predictor of subsequent events.

Summarise comorbidity correlations
----------------------------------

If time permits we will also estimate correlations between comorbidities in hierarchical multivariate probit models. The models will include age, sex and index condition as covariates and will be fit in a Bayesian framework using an approch similar to that descibed by Pollock et al (12). The output of this work will be in the form of network diagrams illustrating the correlation between comorbidities for different index conditions.

Time period for analysis
------------------------

We conducted a preliminary inspection of the SAIL data to determine the number of patients with a prescription for **any** of the drugs of interest (including "excluded" drugs aspirin, amitriptyline etc). This was done prior to examining specific comorbid conditions, it was also done prior to identifying which patients had the index conditions (and indeed prior to specifying the Read codes for the index conditions). On conducting this analysis we found that the number of patients was low prior to 2010 and plateaued in 2011. For this reason we specified the 2011 to 2012 time period to identify concomittant diseases.

Age and sex characteristics for comparison
==========================================

In the primary analysis we will compare comorbidity counts in the SAIL and trial datasets having standardised the SAIL data to the number of trial participants with each indication in each age and sex band. Briefly, for each indication, we will apply proportions with each comorbidity count for each age and sex specific stratum to the age and sex distribution in the trial data to get the expected comorbidity counts for each statum, then sum this across strata. This is analagous to direct standardisation. As the numbers are expected to be large, we do not plan to estimate confidence intervals for the main analysis.

The Read codes for each indication will be specified, and will not be changed after they are uploaded to the SAIL secure analysis platform.

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
