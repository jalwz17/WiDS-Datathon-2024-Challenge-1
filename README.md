# WiDS-Datathon-2024-Challenge-1

Women in Data Science (WiDS) Worldwide is on a mission to increase participation of women in data science to benefit societies worldwide.

Gilead Sciences is the sponsor for this year’s WiDS Datathon. They provided a rich, real-world dataset which contains information about demographics, diagnosis and treatment options, and insurance provided about patients who were diagnosed with breast cancer from 2015-2018. The dataset originated from Health Verity, one of the largest healthcare data ecosystems in the US. It was enriched with third party geo-demographic data to provide views into the socio economic aspects that may contribute to health equity. For this challenge, the dataset was then further enriched with zip code level toxicology data NASA/Columbia University.

**Challenge task:**
You will be asked to predict if the patients received metastatic cancer diagnosis within 90 days of screening.

The WiDS Datathon 2024 focuses on a prediction task using a roughly 39k record dataset (split into training and test sets) representing patients and their characteristics (age, race, BMI, zip code), their diagnosis and treatment information (breast cancer diagnosis code, metastatic cancer diagnosis code, metastatic cancer treatments, … etc.), their geo (zip-code level) demographic data (income, education, rent, race, poverty, …etc), as well as toxic air quality data (Ozone, PM25 and NO2) that tie health outcomes to environmental conditions. Each row in the data corresponds a single patient and her Diagnosis Period. Your task is to assess whether the likelihood of the patient’s Diagnosis Period being less than 90 days is predictable using these characteristics and information about the patient.

You are provided with two datasets:
(1) the training dataset train.csv where the observed values of the outcome [Diagnosis Period being Less Than 90 Days] for each row is provided
(2) the test dataset test.csv where we withhold the observed values of the outcome for each row

**Target**
DiagPeriodL90D: Diagnosis Period Less Than 90 Days. This is an indication of whether the cancer was diagnosed within 90 Days.

**Columns**
patient_id - Unique identification number of patient

patient_race - Asian, African American, Hispanic or Latino, White, Other Race

payer_type - payer type at Medicaid, Commercial, Medicare on the metastatic date

patient_state - Patient State (e.g. AL, AK, AZ, AR, CA, CO etc…) on the metastatic date

patient_zip3 - Patient Zip3 (e.g. 190) on the metastatic date

patient_age - Derived from Patient Year of Birth (index year minus year of birth)

patient_gender - F, M on the metastatic date

bmi - If Available, will show available BMI information (Earliest BMI recording post metastatic date)

breast_cancer_diagnosis_code - ICD10 or ICD9 diagnoses code

breast_cancer_diagnosis_desc - ICD10 or ICD9 code description. This column is raw text and may require NLP/ processing and cleaning

metastatic_cancer_diagnosis_code - ICD10 diagnoses code

metastatic_first_novel_treatment - Generic drug name of the first novel treatment (e.g. "Cisplatin") after metastatic diagnosis

metastatic_first_novel_treatment_type - Description of Treatment (e.g. Antineoplastic) of first novel treatment after metastatic diagnosis

region - Region of patient location

division - Division of patient location

population - An estimate of the zip code's population.

density - The estimated population per square kilometer.

age_median - The median age of residents in the zip code.

male - The percentage of residents who report being male (e.g. 55.1).

female - The percentage of residents who report being female (e.g. 44.9).

married - The percentage of residents who report being married (e.g. 44.9).

family_size - The average size of resident families (e.g. 3.22).

income_household_median - Median household income in USD.

income_household_six_figure - Percentage of households that earn at least $100,000 (e.g. 25.3)

home_ownership - Percentage of households that own (rather than rent) their residence.

housing_units - The number of housing units (or households) in the zip code.

home_value - The median value of homes that are owned by residents.

rent_median - The median rent paid by renters.

education_college_or_above - The percentage of residents with at least a 4-year degree.

labor_force_participation - The percentage of residents 16 and older in the labor force.

unemployment_rate - The percentage of residents unemployed.

race_white - The percentage of residents who report their race White.

race_black - The percentage of residents who report their race as Black or African American.

race_asian - The percentage of residents who report their race as Asian.

race_native - The percentage of residents who report their race as American Indian and Alaska Native.

race_pacific - The percentage of residents who report their race as Native Hawaiian and Other Pacific Islander.

race_other - The percentage of residents who report their race as Some other race.

race_multiple - The percentage of residents who report their race as Two or more races.

hispanic - The percentage of residents who report being Hispanic. Note: Hispanic is considered to be an ethnicity and not a race.

age_under_10 - The percentage of residents aged 0-9.

age_10_to_19 - The percentage of residents aged 10-19.

age_20s - The percentage of residents aged 20-29.

age_30s - The percentage of residents aged 30-39.

age_40s - The percentage of residents aged 40-49.

age_50s - The percentage of residents aged 50-59.

age_60s - The percentage of residents aged 60-69.

age_70s - The percentage of residents aged 70-79.

age_over_80 - The percentage of residents aged over 80.

divorced - The percentage of residents divorced.

never_married - The percentage of residents never married.

widowed - The percentage of residents never widowed.

family_dual_income - The percentage of families with dual income earners.

income_household_under_5 - The percentage of households with income under $5,000.

income_household_5_to_10 - The percentage of households with income from $5,000-$10,000.

income_household_10_to_15 - The percentage of households with income from $10,000-$15,000.

income_household_15_to_20 - The percentage of households with income from $15,000-$20,000.

income_household_20_to_25 - The percentage of households with income from $20,000-$25,000.

income_household_25_to_35 - The percentage of households with income from $25,000-$35,000.

income_household_35_to_50 - The percentage of households with income from $35,000-$50,000.

income_household_50_to_75 - The percentage of households with income from $50,000-$75,000.

income_household_75_to_100 - The percentage of households with income from $75,000-$100,000.

income_household_100_to_150 - The percentage of households with income from $100,000-$150,000.

income_household_150_over - The percentage of households with income over $150,000.

income_individual_median - The median income of individuals in the zip code.

poverty - The median value of owner occupied homes.

rent_burden - The median rent as a percentage of the median renter's household income.

education_less_highschool - The percentage of residents with less than a high school education.

education_highschool - The percentage of residents with a high school diploma but no more.

education_some_college - The percentage of residents with some college but no more.

education_bachelors - The percentage of residents with a bachelor's degree (or equivalent) but no more.

education_graduate - The percentage of residents with a graduate degree.

education_stem_degree - The percentage of college graduates with a Bachelor's degree or higher in a Science and Engineering (or related) field.

self_employed - The percentage of households reporting self-employment income on their 2016 IRS tax return.

farmer - The percentage of households reporting farm income on their 2016 IRS tax return.

disabled - The percentage of residents who report a disability.

limited_english - The percentage of residents who only speak limited English.

commute_time - The median commute time of resident workers in minutes.

health_uninsured - The percentage of residents who report not having health insurance.

veteran - The percentage of residents who are veterans.

ozone - Annual Ozone (O3) concentration data at Zip3 level. This data shows how air quality data may impact health.

PM25 - Annual Fine Particulate Matter (PM2.5) concentration data at Zip3 level. This data shows how air quality data may impact health.

N02 - Annual Nitrogen Dioxide (NO2) concentration data at Zip3 level. This data shows how air quality data may impact health.
