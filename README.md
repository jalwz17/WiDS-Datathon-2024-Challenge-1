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
