# UIDAI AadhaarLens

## Aadhaar Enrolment & Update Activity Analysis

UIDAI AadhaarLens is a data analytics project developed for the UIDAI Hackathon.

The project analyzes Aadhaar enrolment and update activity across age groups, states, districts, pincodes and dates to identify meaningful behavioural patterns, operational differences and unusual district-level activity.

---

## Problem Statement

Aadhaar enrolment and update activity varies across age groups, states, districts and activity types.

The objective of this project is to:

- Identify the major drivers of Aadhaar enrolment activity
- Understand demographic and biometric update patterns
- Compare enrolment and maintenance activity across districts
- Identify different district behavioural profiles
- Detect unusual district-level activity
- Translate analytical findings into actionable operational recommendations

---

## Key Questions

1. Which age groups drive new Aadhaar enrolment?
2. How do demographic and biometric update patterns vary geographically?
3. Which districts are enrolment-heavy versus maintenance-heavy?
4. Can districts be grouped into behavioural profiles?
5. Can unusual district activity be identified for further investigation?

---

## Dataset

The project uses the UIDAI Aadhaar Enrolment & Update dataset provided for the hackathon.

Each record represents aggregated Aadhaar activity for a particular date and geography.

### Main variables

- `date`
- `state`
- `district`
- `pincode`
- `age_0_5`
- `age_5_17`
- `age_18_greater`
- `demo_age_5_17`
- `demo_age_17_`
- `bio_age_5_17`
- `bio_age_17_`

The dataset contains aggregated activity counts rather than individual applicant records.

---

## Methodology

### 1. Data Cleaning

- Removed exported index column
- Checked missing values
- Checked negative values
- Removed duplicate activity records
- Converted dates to datetime
- Standardised state and district names
- Validated pincode formatting

### 2. Feature Engineering

Created:

- Total enrolment
- Total demographic updates
- Total biometric updates
- Total updates
- Update-to-enrolment ratio
- Child enrolment share
- Biometric share of updates
- Calendar features

### 3. Exploratory Data Analysis

The analysis covers:

- Overall activity composition
- Age-group composition
- State-level age variation
- Demographic vs biometric activity
- District-level enrolment and update pressure

### 4. District Segmentation

K-Means clustering was used to identify behavioural district profiles based on activity characteristics such as:

- Enrolment volume
- Update pressure
- Child-enrolment intensity

### 5. Anomaly Detection

District-level September activity was compared against each district's own baseline using mean and standard deviation to identify unusual activity.

---

## Key Findings

### 1. Aadhaar activity is update-heavy

Observed update activity substantially exceeds new enrolment activity, indicating that maintenance represents a major share of the recorded workload.

### 2. New enrolment is strongly child-driven

Age 0–5 contributes the largest share of new-enrolment activity.

### 3. Enrolment composition varies geographically

Major states show meaningful differences in the relative contribution of different enrolment age groups.

### 4. Districts have different operational profiles

High enrolment volume does not necessarily correspond to high update-to-enrolment activity.

### 5. District-level anomalies exist

Some districts deviate substantially from their own September activity baseline and can be treated as candidates for operational or data-quality investigation.

---

## Recommendations

### Targeted Resource Allocation

Operational capacity should be allocated according to district-specific enrolment and update pressure rather than using a one-size-fits-all strategy.

### Child Enrolment Capacity

Regions with high child-enrolment intensity can receive targeted child-focused enrolment capacity and outreach.

### Update Capacity

Maintenance-heavy districts may require greater demographic and biometric update capacity.

### Anomaly Investigation

Extreme deviations should trigger operational or data-quality checks before being interpreted as genuine changes in demand.

### Behavioural District Profiles

District personas can provide an additional planning layer beyond simple state or district rankings.

---

## Limitations

- Dataset contains aggregated activity counts rather than person-level records.
- Available dates do not form a continuous long-term time series.
- Update-to-enrolment ratio is an activity-volume indicator and not an individual-level update frequency.
- Anomalies indicate candidates for investigation and do not establish their underlying cause.

---

## Project Structure

```text
UIDAI-AadhaarLens/
│
├── # UIDAI AadhaarLens

## Aadhaar Enrolment & Update Activity Analysis

UIDAI AadhaarLens is a data analytics project developed for the UIDAI Hackathon.

The project analyzes Aadhaar enrolment and update activity across age groups, states, districts, pincodes and dates to identify meaningful behavioural patterns, operational differences and unusual district-level activity.

---

## Problem Statement

Aadhaar enrolment and update activity varies across age groups, states, districts and activity types.

The objective of this project is to:

- Identify the major drivers of Aadhaar enrolment activity
- Understand demographic and biometric update patterns
- Compare enrolment and maintenance activity across districts
- Identify different district behavioural profiles
- Detect unusual district-level activity
- Translate analytical findings into actionable operational recommendations

---

## Key Questions

1. Which age groups drive new Aadhaar enrolment?
2. How do demographic and biometric update patterns vary geographically?
3. Which districts are enrolment-heavy versus maintenance-heavy?
4. Can districts be grouped into behavioural profiles?
5. Can unusual district activity be identified for further investigation?

---

## Dataset

The project uses the UIDAI Aadhaar Enrolment & Update dataset provided for the hackathon.

Each record represents aggregated Aadhaar activity for a particular date and geography.

### Main variables

- `date`
- `state`
- `district`
- `pincode`
- `age_0_5`
- `age_5_17`
- `age_18_greater`
- `demo_age_5_17`
- `demo_age_17_`
- `bio_age_5_17`
- `bio_age_17_`

The dataset contains aggregated activity counts rather than individual applicant records.

---

## Methodology

### 1. Data Cleaning

- Removed exported index column
- Checked missing values
- Checked negative values
- Removed duplicate activity records
- Converted dates to datetime
- Standardised state and district names
- Validated pincode formatting

### 2. Feature Engineering

Created:

- Total enrolment
- Total demographic updates
- Total biometric updates
- Total updates
- Update-to-enrolment ratio
- Child enrolment share
- Biometric share of updates
- Calendar features

### 3. Exploratory Data Analysis

The analysis covers:

- Overall activity composition
- Age-group composition
- State-level age variation
- Demographic vs biometric activity
- District-level enrolment and update pressure

### 4. District Segmentation

K-Means clustering was used to identify behavioural district profiles based on activity characteristics such as:

- Enrolment volume
- Update pressure
- Child-enrolment intensity

### 5. Anomaly Detection

District-level September activity was compared against each district's own baseline using mean and standard deviation to identify unusual activity.

---

## Key Findings

### 1. Aadhaar activity is update-heavy

Observed update activity substantially exceeds new enrolment activity, indicating that maintenance represents a major share of the recorded workload.

### 2. New enrolment is strongly child-driven

Age 0–5 contributes the largest share of new-enrolment activity.

### 3. Enrolment composition varies geographically

Major states show meaningful differences in the relative contribution of different enrolment age groups.

### 4. Districts have different operational profiles

High enrolment volume does not necessarily correspond to high update-to-enrolment activity.

### 5. District-level anomalies exist

Some districts deviate substantially from their own September activity baseline and can be treated as candidates for operational or data-quality investigation.

---

## Recommendations

### Targeted Resource Allocation

Operational capacity should be allocated according to district-specific enrolment and update pressure rather than using a one-size-fits-all strategy.

### Child Enrolment Capacity

Regions with high child-enrolment intensity can receive targeted child-focused enrolment capacity and outreach.

### Update Capacity

Maintenance-heavy districts may require greater demographic and biometric update capacity.

### Anomaly Investigation

Extreme deviations should trigger operational or data-quality checks before being interpreted as genuine changes in demand.

### Behavioural District Profiles

District personas can provide an additional planning layer beyond simple state or district rankings.

---

## Limitations

- Dataset contains aggregated activity counts rather than person-level records.
- Available dates do not form a continuous long-term time series.
- Update-to-enrolment ratio is an activity-volume indicator and not an individual-level update frequency.
- Anomalies indicate candidates for investigation and do not establish their underlying cause.

---

## Project Structure

```text
UIDAI-AadhaarLens/
│
├── # UIDAI AadhaarLens

## Aadhaar Enrolment & Update Activity Analysis

UIDAI AadhaarLens is a data analytics project developed for the UIDAI Hackathon.

The project analyzes Aadhaar enrolment and update activity across age groups, states, districts, pincodes and dates to identify meaningful behavioural patterns, operational differences and unusual district-level activity.

---

## Problem Statement

Aadhaar enrolment and update activity varies across age groups, states, districts and activity types.

The objective of this project is to:

- Identify the major drivers of Aadhaar enrolment activity
- Understand demographic and biometric update patterns
- Compare enrolment and maintenance activity across districts
- Identify different district behavioural profiles
- Detect unusual district-level activity
- Translate analytical findings into actionable operational recommendations

---

## Key Questions

1. Which age groups drive new Aadhaar enrolment?
2. How do demographic and biometric update patterns vary geographically?
3. Which districts are enrolment-heavy versus maintenance-heavy?
4. Can districts be grouped into behavioural profiles?
5. Can unusual district activity be identified for further investigation?

---

## Dataset

The project uses the UIDAI Aadhaar Enrolment & Update dataset provided for the hackathon.

Each record represents aggregated Aadhaar activity for a particular date and geography.

### Main variables

- `date`
- `state`
- `district`
- `pincode`
- `age_0_5`
- `age_5_17`
- `age_18_greater`
- `demo_age_5_17`
- `demo_age_17_`
- `bio_age_5_17`
- `bio_age_17_`

The dataset contains aggregated activity counts rather than individual applicant records.

---

## Methodology

### 1. Data Cleaning

- Removed exported index column
- Checked missing values
- Checked negative values
- Removed duplicate activity records
- Converted dates to datetime
- Standardised state and district names
- Validated pincode formatting

### 2. Feature Engineering

Created:

- Total enrolment
- Total demographic updates
- Total biometric updates
- Total updates
- Update-to-enrolment ratio
- Child enrolment share
- Biometric share of updates
- Calendar features

### 3. Exploratory Data Analysis

The analysis covers:

- Overall activity composition
- Age-group composition
- State-level age variation
- Demographic vs biometric activity
- District-level enrolment and update pressure

### 4. District Segmentation

K-Means clustering was used to identify behavioural district profiles based on activity characteristics such as:

- Enrolment volume
- Update pressure
- Child-enrolment intensity

### 5. Anomaly Detection

District-level September activity was compared against each district's own baseline using mean and standard deviation to identify unusual activity.

---

## Key Findings

### 1. Aadhaar activity is update-heavy

Observed update activity substantially exceeds new enrolment activity, indicating that maintenance represents a major share of the recorded workload.

### 2. New enrolment is strongly child-driven

Age 0–5 contributes the largest share of new-enrolment activity.

### 3. Enrolment composition varies geographically

Major states show meaningful differences in the relative contribution of different enrolment age groups.

### 4. Districts have different operational profiles

High enrolment volume does not necessarily correspond to high update-to-enrolment activity.

### 5. District-level anomalies exist

Some districts deviate substantially from their own September activity baseline and can be treated as candidates for operational or data-quality investigation.

---

## Recommendations

### Targeted Resource Allocation

Operational capacity should be allocated according to district-specific enrolment and update pressure rather than using a one-size-fits-all strategy.

### Child Enrolment Capacity

Regions with high child-enrolment intensity can receive targeted child-focused enrolment capacity and outreach.

### Update Capacity

Maintenance-heavy districts may require greater demographic and biometric update capacity.

### Anomaly Investigation

Extreme deviations should trigger operational or data-quality checks before being interpreted as genuine changes in demand.

### Behavioural District Profiles

District personas can provide an additional planning layer beyond simple state or district rankings.

---

## Limitations

- Dataset contains aggregated activity counts rather than person-level records.
- Available dates do not form a continuous long-term time series.
- Update-to-enrolment ratio is an activity-volume indicator and not an individual-level update frequency.
- Anomalies indicate candidates for investigation and do not establish their underlying cause.

---

## Project Structure

```text
UIDAI-AadhaarLens/
│
├── UIDAI_Analysis.ipynb
├── UIDAI.csv
├── UIDAI_AadhaarLens_Final_Report.pdf
├── README.md
├── requirements.txt
└── .gitignore.ipynb
├── UIDAI.csv
├── UIDAI_AadhaarLens_Final_Report.pdf
├── README.md
├── requirements.txt
└── .gitignore.ipynb
├── UIDAI.csv
├── UIDAI_AadhaarLens_Final_Report.pdf
├── README.md
├── requirements.txt
└── .gitignore
