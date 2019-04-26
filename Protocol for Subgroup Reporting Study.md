## Introduction

Aim: to describe the reporting of subgroup analyses within published
results of randomized controlled trials

This review will seek to comprehensively identify registered randomized
controlled trials for pharmacological interventions for a range of
physical medical conditions, and to describe the reporting of subgroup
analyses within published results papers from these studies.

This review forms part of a wider programme of work assessing
heterogeneity of treatment effects in pharmacological interventions for
medical conditions. This overall project seeks to analyse
individual-level participant data from clinical trials, and is described
in the protocol
<https://www.crd.york.ac.uk/PROSPERO/display_record.php?RecordID=48202>.

The trials identified from clinicaltrials.gov in this review of subgroup
effects are also intended to represent the ‘denominator’ set of trials
from which the individual-participant data trials were selected for this
wider project. As such, the inclusion criteria applied to
clinicaltrials.gov in this protocol reflect the criteria applied to the
trials in the protocol above.

This protocol described here is not registered on PROSPERO as it only
concerns trial reporting and methodology (rather than analyzing disease
outcomes) and therefore falls outside the remit of PROSPERO.

## Review question

  - What proportion of randomized controlled trials of pharmacological
    interventions for physical medical conditions report results of
    subgroup analyses?

  - What subgroups are assessed in these trials?

  - What study characteristics are associated with the reporting of
    subgroup effects?

## Searches

This study seeks to accurately describe the extent of subgroup reporting
among registered trials. We will therefore search clinicaltrials.gov to
identify a set of registered trials meeting our inclusion criteria,
before going on to identify papers reporting the results of these
trials.

Clinicaltrials.gov is a database of registered clinical studies. It is
provided by the U.S National Library of Medicine. Studies are conducted
around the world. The database contains summary information on studies
and participants.

The database will be searches using the Access to Aggregate Content of
ClinicalTrials.gov (AACT) PostgreSQL database running the RPostgreSQL
package from within R software. AACT contains information about every
study registered in clinicaltrials.gov, including protocol and result
data elements. It is updated daily.

Inclusion criteria (PICOS) were applied to the trial meta-data obtained
from the database search to obtain a list of trial IDs meeting these. In
brief, we aimed to identify every trial recruiting \>300 participants of
a pharmacological or biological intervention registered after 1990 for
any of the medical conditions listed in table
1.

| **Table 1: MeSH Terms Applied to clinicaltrials.gov database** |                                                            |                             |
| -------------------------------------------------------------- | ---------------------------------------------------------- | --------------------------- |
| **Category**                                                   | **MeSH term**                                              | **Code**                    |
|                                                                |                                                            |                             |
| Musculoskeletal                                                | Osteoporosis                                               | C05.116.198.579             |
|                                                                | Spondyloarthopathies                                       | C05.116.900.853 .625.800    |
|                                                                | Arthritis                                                  | C05.550.114                 |
|                                                                | Arthritis, Rheumatoid                                      | C05.799.114                 |
|                                                                | Gout                                                       | C05.799.414                 |
|                                                                | Osteoporosis                                               | C05.799.613                 |
|                                                                |                                                            |                             |
| Digestive system diseases                                      | CREST Syndrome                                             | C06.405.117.119.500.204     |
|                                                                | Oesophageal Achalasia                                      | C06.405.117.119.500.432     |
|                                                                | Oesophageal spasm, diffuse                                 | C06.405.117.119.500.450     |
|                                                                | Gastro-oesophageal reflux                                  | C06.405.117.119.500.484     |
|                                                                | Laryngopharyngeal reflux                                   | C06.405.117.119.500.484.500 |
|                                                                | Plummer-Vinson Syndrome                                    | C06.405.117.119.500.742     |
|                                                                | Oesophagitis                                               | C06.405.117.620             |
|                                                                | Colitis, Ulcerative                                        | C06.405.205.265.231         |
|                                                                | Inflammatory Bowel Diseases                                | C06.405.205.731             |
|                                                                | Inflammatory Bowel diseases                                | C06.405.469.432             |
|                                                                | Oesophagitis, peptic                                       | C06.405.608.348             |
|                                                                | Duodenogastric reflux                                      | C06.405.748.240             |
|                                                                | Gastritis                                                  | C06.405.748.398             |
|                                                                | Hepatitis, autoimmune                                      | C06.552.380.350.050         |
|                                                                |                                                            |                             |
| Respiratory Tract Diseases                                     | Asthma                                                     | C08.127.108                 |
|                                                                | Bronchiectasis                                             | C08.127.384                 |
|                                                                | Bronchitis, chronic                                        | C08.127.446.567             |
|                                                                | Hypertension, Pulmonary                                    | C08.381.423                 |
|                                                                | Idiopathic Interstitial Pneumonias                         | C08.381.483.487             |
|                                                                | Idiopathic Pulmonary Fibrosis                              | C08.381.483.487.500         |
|                                                                | Lung Diseases, Obstructive                                 | C08.381.495                 |
|                                                                | Pulmonary Embolism                                         | C08.381.746                 |
|                                                                | Pulmonary Fibrosis                                         | C08.381.765                 |
|                                                                | Rhinitis                                                   | C08.460.799                 |
|                                                                | Asthma                                                     | C08.674.095                 |
|                                                                | Bronchitis, Chronic                                        | C08.730.099.567             |
|                                                                |                                                            |                             |
| Otorhinolaryngologic Diseases                                  | Rhinitis, Allergic                                         | C09.603.799.315             |
|                                                                |                                                            |                             |
|                                                                | Multiple Sclerosis                                         | C10.114.375.500             |
|                                                                | Parkinsonian Disorders                                     | C10.228.140.079.862         |
|                                                                | Brain Ischaemia                                            | C10.228.140.300.150         |
|                                                                | Stroke, Lacunar                                            | C10.228.140.300.275.800     |
|                                                                | Dementia, Vascular                                         | C10.228.140.300.400         |
|                                                                | Infarction, Anterior Cerebral Artery                       | C10.228.140.300.510.200.325 |
|                                                                | Infarction, Middle Cerebral Artery                         | C10.228.140.300.510.200.387 |
|                                                                | Infarction, Posterior Cerebral Artery                      | C10.228.140.300.510.200.418 |
|                                                                | Dementia, Vascular                                         | C10.228.140.300.510.800.500 |
|                                                                | Stroke                                                     | C10.228.140.300.775         |
|                                                                | Alzheimer Disease                                          | C10.228.140.380.100         |
|                                                                | Dementia, Vascular                                         | C10.228.140.380.230         |
|                                                                | Epilepsy                                                   | C10.228.140.490             |
|                                                                | Migraine Disorders                                         | C10.228.140.546.399.750     |
|                                                                | Parkinsonian Disorders                                     | C10.228.662.600             |
|                                                                | Parkinson Disease                                          | C10.574.812                 |
|                                                                | Alzheimer Disease                                          | C10.574.945.249             |
|                                                                | Restless Leg Syndrome                                      | C10.803                     |
|                                                                |                                                            |                             |
| Male Urogenital Diseases                                       | Prostatic Hyperplasia                                      | C12.294.565.500             |
|                                                                | Diabetic Nephropathies                                     | C12.777.419.192             |
|                                                                | Urinary Bladder, Overactive                                | C12.777.829.866             |
|                                                                | Enuresis                                                   | C12.777.934.284             |
|                                                                | Urinary Incontinence                                       | C12.777.934.852             |
|                                                                |                                                            |                             |
| Female Urogenital Diseases                                     | Urinary Bladder, Overactive                                | C13.351.968.829.813         |
|                                                                | Enuresis                                                   | C13.351.968.934.252         |
|                                                                | Urinary Incontinence                                       | C13.351.968.934.814         |
|                                                                |                                                            |                             |
| Cardiovascular Diseases                                        | Atrial Fibrillation                                        | C14.280.067.198             |
|                                                                | Atrial Flutter                                             | C14.280.067.248             |
|                                                                | Heart Failure                                              | C14.280.434                 |
|                                                                | Myocardial Ischaemia                                       | C14.280.647                 |
|                                                                | Atherosclerosis                                            | C14.907.137.126.307         |
|                                                                | Peripheral Arterial Disease                                | C14.907.137.126.307.500     |
|                                                                | Coronary Artery Disease                                    | C14.907.137.126.339         |
|                                                                | Dementia, Vascular                                         | C14.907.137.126.372.500     |
|                                                                | Intermittent Claudication                                  | C14.907.137.126.669         |
|                                                                | Cerebral Infarction                                        | C14.907.253.092.477.200     |
|                                                                | Dementia, Vascular                                         | C14.907.253.560.350.500     |
|                                                                | Stroke                                                     | C14.907.253.855             |
|                                                                | Embolism and Thrombosis                                    | C14.907.355                 |
|                                                                | Pulmonary Embolism                                         | C14.907.355.350.700         |
|                                                                | Thromboembolism                                            | C14.907.355.590             |
|                                                                | Thrombosis                                                 | C14.907.355.830             |
|                                                                | Hypertension                                               | C14.907.489                 |
|                                                                | Myocardial Ischaemia                                       | C14.907.585                 |
|                                                                | Peripheral Vascular Diseases                               | C14.907.617                 |
|                                                                |                                                            |                             |
| Skin and Connective Tissue Diseases                            | Lupus Erythematosus, Systemic                              | C17.300.480                 |
|                                                                | Mixed Connective Tissue Disease                            | C17.300.540                 |
|                                                                | Rheumatic Diseases                                         | C17.300.775                 |
|                                                                | Scleroderma, Systemic                                      | C17.300.799                 |
|                                                                | Scleroderma, Systemic                                      | C17.800.784                 |
|                                                                | Scleroderma, Diffuse                                       | C17.800.784.602             |
|                                                                | Scleroderma, Limited                                       | C17.800.784.801             |
|                                                                | CREST Syndrome                                             | C17.800.784.801.500         |
|                                                                | Psoriasis                                                  | C17.800.859.675             |
|                                                                | Urticaria                                                  | C17.800.862.945             |
|                                                                |                                                            |                             |
| Nutritional and Metabolic Diseases                             | Diabetes Mellitus                                          | C18.452.394.750             |
|                                                                | Hypercholisterolaemia                                      | C18.452.584.500.500.396     |
|                                                                | Hyperlipidaemia, Familial Combined                         | C18.452.584.500.500.438     |
|                                                                | Hypertriglyceridiaemia                                     | C18.452.584.500.500.851     |
|                                                                | Hyperlipidaemia, Familial Combined                         | C18.452.648.398.450         |
|                                                                |                                                            |                             |
| Endocrine System Diseases                                      | Diabetes Mellitus, Type 1                                  | C19.246.267                 |
|                                                                | Diabetes Mellitus, Type 2                                  | C19.246.300                 |
|                                                                |                                                            |                             |
| Immune System Diseases                                         | Anti-Neutrophil Cytoplasmic Antibody-Associated Vasculitis | C20.111.193                 |
|                                                                | Antiphospholipid Syndrome                                  | C20.111.197                 |
|                                                                | Arthritis, Juvenile                                        | C20.111.198                 |
|                                                                | Arthritis, Rheumatoid                                      | C20.111.199                 |
|                                                                | Multiple Sclerosis                                         | C20.111.258.250.500         |
|                                                                | Diabetes Mellitus, Type 1                                  | C20.111.327                 |
|                                                                | Hepatitis, Autoimmune                                      | C20.111.567                 |
|                                                                | Asthma                                                     | C20.543.480.680.095         |
|                                                                | Rhinitis, Allergic                                         | C20.543.480.680.443         |

## Inclusion criteria (PICOS)

#### Population

Adult participants.

Affected by one of the medical conditions listed in table 1.

To be eligible for inclusion, trials must have either no registered
upper age limit, or an upper age limit greater than 60 years.

Trials must recruit at least 300 participants

#### Intervention

Trials must evaluate the efficacy of pharmacological or biological
interventions for one of the medical conditions listed in table 1.

Eligible medications will be classified using the World Health
Organisation Anatomic Therapeutic Classification (ATC) coding system.
ATC codes for relevant interventions are listed below. As the ATC coding
is protected by copyright we have not presented the corresponding drug
names in the form of a table, however these can be obtained from the
following source: https://www.whocc.no/atc\_ddd\_index/.

Any drug with a 7-character code starting with any of the following 3,
4, and 5-character ATC codes was defined as relevant:- A02A, A02AC,
A02BA, A02BC, A02BX, A10AB, A10AC, A10AD, A10AE, A10BA, A10BB, A10BF,
A10BG, A10BH, A10BJ, A10BK, A10BX, B01AA, B01AB, B01AC, B01AD, B01AE,
B01AF, B01AX, C01AA, C01BA, C01BB, C01BC, C01BD, C01BG, C01CA, C01CE,
C01CX, C01DA, C01DX, C01EA, C01EB, C02AA, C02AB, C02AC, C02CA, C02DB,
C02DD, C02KX, C03, C03AA, C03BA, C03BD, C03CA, C03DA, C03DB, C03XA,
C04AC, C04AD, C05AA, C05AB, C05AD, C05AE, C05BA, C07AA, C07AB, C07AG,
C08, C08CA, C08DA, C08DB, C09AA, C09CA, C09DB, C09XA, C10AA, C10AB,
C10AC, C10AD, C10AX, G04BD, G04BE, G04CA, G04CB, H05AA, H05BX, L01AA,
L01BA, L01BB, L01BC, L01CD, L01XC, L01XE, L01XX, L04AA, L04AB, L04AC,
L04AD, L04AX, M01AB, M01AC, M01AE, M01AH, M01AX, M04AA, M04AB, M04AC,
M05BA, M05BX, N03AA, N03AB, N03AF, N03AG, N03AX, N04AA, N04BA, N04BC,
N04BD, N04BX, N06DA, N06DX, R03AA, R03AC, R03BA, R03BB, R03CA, R03CC,
R03DA, R03DC, R03DX. Secondly, any intervention assigned to a drug-class
with a code exactly matching the following codes was defined as
relevant:- A02A, A02B, A10A, A10B, A10BA, A10BB, A10BF, A10BG, A10BH,
A10BJ, A10BK, A10BX, B01A, B01AB, B01AD, C01B, C02, C03A, C03AA, C03CA,
C07A, C08, C09A, C09AA, C09CA, C10A, C10AA, L04AB, M01A, M01AE, N03A,
N04BD, R03AC, R03BA, R03BB, R06A.

#### Comparison

Comparison must be either placebo, standard or usual care, or an
alternative pharmacological agent.

We will exclude trials where the comparator is the same pharmacological
agent as the intervention (e.g. trials comparing different doses of the
same medication), or for an intervention within the same ATC class.

#### Outcome

Trials must report the efficacy of the trial agent for the conditions in
question.

Given the broad inclusion criteria (i.e. any medical condition) the
range of potential outcomes will be large. We will consider any clinical
outcome related to the index condition. Papers assessing
cost-effectiveness or quality of life will only be included if they also
assess clinical outcomes.

#### Study design

Only randomsied controlled trials will be eligible for inclusion.
Studies must have a parallel design. Randomisation must be at the level
of the individual participant (i.e. cluster randomized trials will be
excluded).

Trials must be registered after 1990

## Screening and study selection

By applying the above inclusion criteria to the clinicaltrials.gov
database using AACT, we will obtain a list of registered trials that
meet these criteria. We will then identify all published results related
to these studies, and from these published papers, determine which
report subgroup effects.

The identification of studies will be carried out in two stages,
described in detail below. Briefly, we will initially identify all
PubMed indexed publications related to registered trials meeting the
inclusion criteria outlined above. We will then manually screen these to
identify all results papers reporting subgroup analyses.

#### Identification of registered trials from clinicatrials.gov

Clinicaltrials.gov maintains within the database detailed of PubMed IDs
(PMID) of all publications related to registered trials.

In addition, PubMed has a facility to search by trial registration
number.

We used both of these methods to identify any PubMed indexed publication
pertaining to any of the trials identified from the AACT database.

#### Identification and screening of related publications

Titles and abstracts of all papers will be manually screened by one
reviewer to identify papers reporting trial results. Only papers can be
identified as not reporting results (e.g. baseline characteristics
papers, observational analyses etc.) will be excluded at this stage. All
results papers will be retained for full text screening. No assessment
of subgroup reporting will be made at the abstract screening stage. If
the nature of a paper is not clear from title or abstract, it will be
retained for full text screening. A random sample of 500 abstracts will
be screened by a second review and a kappa statistic of agreement
calculated.

Full texts will be obtained for all results papers (or where the nature
of a paper could not be determined from title/abstract screening). Both
manual screening and automatic screening of the full text for key terms
related to subgroups will be used to assess each full text. This process
will be carried out as follows:

  - One reviewer will manually screen each full text to confirm (i) that
    it is a results paper and (ii) determine if results are reported by
    subgroups.

  - Each full text will also be screened by an automatic search of the
    manuscript text and tables using the following regular expression
    (regex) search “sub-group|subgroup|strata|(by
    baseline)|subpopulation”

  - All papers identified by the automatic screening will undergo
    duplicate manual review to confirm the presence of absence of
    subgroup reporting.

All papers identified as containing subgroup results will be retained
for data extraction.

## Data extraction

#### Subgroup names

For each results paper, the presence or absence of subgroup analysis
will be recorded. Where subgroups are reported, we will also record
whether these analyses are described as pre-specified within the
manuscript text, and whether the authors report a p-value for
interaction. These features are recommended in the reporting of subgroup
effects.

Where the results of subgroup analyses are reported in tables, these
will be converted into a standard format. This will include the names of
each subgroup (e.g. age, sex), and the levels (e.g. above or below 60
years, male/female, etc.).

Where the subgroup results are presented in figures, the subgroup names
and levels will be extracted and formatted similarly to the tables.

Where the subgroup results are reported in the manuscript text, these
will be extracted verbatim and processed to assess subgroup names and
levels.

Where the manuscript text refers to subgroup analyses displayed in an
appendix, these will be retrieved and extracted in the same way as
described above.

Where an entire manuscript reports a sub-group restricted analysis (eg
only on older people, only in people with diabetes) the main results
will be extracted for later comparison with the non-subgroup results
from the main manuscript. In addition, any further sub-group comparisons
within the sub-group paper will be extracted.

These extracted data will then be synthesized into a single database
detailing what subgroups are assessed within each registered trial.

#### Trial characteristics

Data on trial characteristics (intervention, comparison, indication,
number of participants, phase, number of arms, sponsor, eligibility
criteria, year registered, year completed) will be extracted directly
from the trial registration on clinicaltrials.gov. These data will be
merged with the extraction of subgroup reporting from the published
literature.

## Quality assessment/risk of bias

For each of the studies reporting subgroups, we will assess whither
these analyses were pre-specified or carried out post-hoc. We will also
record whether the authors report a p-value for interaction, as is
recommended in the reporting of subgroup effects. As such, we will
assess the quality/risk of bias of the subgroup reporting specifically,
not the trial as a whole.

## Analysis and synthesis

The unit of analysis will be individual trials, rather than individual
publications. This is because some trials will report subgroups in a
separate manuscript from the main trial result.

For the full set of registered trials, we will calculate:

  - The proportion of registered trials for which published results are
    available.

  - The proportion of trials with published results that include
    assessment of treatment efficacy in specific subgroups.

  - The proportion of trials which report sub-groups as part of overall
    results papers and those in manuscripts dedicated to examining
    specific sub-groups.

We will also calculate the number of subgroups reported by each trial.

After describing the overall proportion of trials reporting subgroups,
we will analyse the relationship between trial characteristics and:

  - The presence of subgroup analyses

  - The number of subgroups analysed

  - The specific subgroups that are analysed

We will describe the overall associations between the following trial
characteristics and the publication of subgroup analyses:

  - Organ system

  - Drug class

  - Trial sponsor

  - Type of sponsor (industry, NIH, other)

  - Year of registration

  - Sample size

  - Statistical significance of the primary outcome reported in the
    study (i.e. positive or negative overall result of primary outcome)

  - Type of primary outcome measure – event-type data yes/no

  - Study results posted on clinicaltrials.gov

All associations will be presented unadjusted, and having adjusted for
trial size and drug class in logistic regression models. We will also
plot the cumulative incidence of sub-group reporting and informed by
this analysis will conduct a sensitivity analysis restricted to trials
based on the time from completion to the final search (eg 2 years).

For each subgroup reported in the trials (e.g. age, sex, ethnicity,
measure of disease severity etc.) we will record which trials report
each subgroup according to year of trial registration and sponsor. We
will stratify these findings by drug class. We will present the findings
in a form of a heatmap or similar. This will allow assessment of how
commonly each specific subgroup is assessed, and how this varies between
drug classes and index conditions.
