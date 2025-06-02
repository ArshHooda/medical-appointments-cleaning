# medical-appointments-cleaning
Overview
This project focuses on cleaning and preprocessing the Medical Appointment No-Shows dataset from Kaggle. The dataset contains information about patient appointments, including whether they showed up or not. The goal was to ensure the data is properly formatted, free of inconsistencies, and ready for analysis.

🔍 Dataset Information
Source: Kaggle - Medical Appointment No Shows

Records: 110,527

Columns: 14

Key Features:

PatientId - Unique patient identifier

AppointmentID - Unique appointment identifier

Gender - Patient's gender (Male/Female)

ScheduledDay - When the appointment was scheduled

AppointmentDay - Day of the appointment

Age - Patient's age

Neighbourhood - Location of the hospital

Scholarship - Whether the patient is enrolled in a welfare program (True/False)

Hipertension, Diabetes, Alcoholism - Medical conditions (True/False)

Handcap - Number of disabilities (0-4)

SMS_received - Whether the patient received an SMS reminder (True/False)

No-show - Whether the patient missed the appointment (True/False)

🧹 Data Cleaning Steps
1. Handling Missing Values
Checked for null values (df.isnull().sum()).

No missing values were found.

2. Removing Duplicates
Checked for duplicate rows (df.duplicated().sum()).

No duplicates were found.

3. Standardizing Column Names
Converted column names to lowercase.

Replaced hyphens with underscores (e.g., No-show → no_show).

4. Fixing Data Types
Datetime Conversion:

ScheduledDay and AppointmentDay were converted to datetime64[ns].

Boolean Conversion:

Scholarship, Hipertension, Diabetes, Alcoholism, SMS_received converted to bool.

Gender Standardization:

M → Male, F → Female.

No-show Column:

Yes → True, No → False.

5. Handling Age Outliers
Removed records with Age < 0 or Age > 120.

6. Final Data Type Check
Verified all columns have the correct data types (df.dtypes).

📝 Key Takeaways

✅ Standardized column names & data types

✅ Handled datetime conversion

✅ Cleaned boolean & categorical columns

✅ Removed invalid age records

✅ Verified no missing values or duplicates

The cleaned dataset is now ready for exploratory analysis, visualization, or machine learning modeling.
