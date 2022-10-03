1.	The motive behind doing this project was to perform EDA and visualize the data by creating plots.
2.	For this, I have taken a dataset called Healthcare Appointment which contains around 1 Lakh entries.
3.	To start with the project, I have imported numpy, pandas, matplotlib and seaborn libraries.
4.	Then, I have loaded the dataset into a dataframe and had a look at the dataframe to understand the data. The last column tells us whether the patient showed up on the day of the appointment while other columns stored information about the patient.
5.	I checked the shape of the data. It had 1.1 lakh entries and 18 columns.

Data Pre-Processing:
1.	I dropped the column ‘patient_id’, ‘appoinment_id’ and ‘neighbourhood’ as it has no significance.
2.	Then, I have converted data type of scheduleDay and appointmentDay to dateTime data type. ( using to_datetime(df[‘scheduleDay’]) )
3.	Then I checked for null values. (using isnull()). There were no null values.
4.	I then created two columns which contains the day of week for sch_day and app_day. ( 5 means saturday, 6 means Sunday).
5.	I also created a ‘age group’ column from age column of each group having range 20 and dropped the age column.

EDA:
1.	I used describe function to know the descriptive statistics of the data.
2.	After counting total patients on each day it is found that on Sunday there were no patients and on Saturday very few patients showed up.
3.	Then I did a bivariate analysis to look into the values of count of each columns w.r.t the count of target variable.
4.	Then I converted all categorical variables to dummy variables so that I can plot a correlation bar plot. Patients with sms received has the highest correlation with target variable.
5.	I then plotted a heatmap to see the correlation between each and every column.
6.	I also plotted a bar plot between age-group and target variable. People with age-group ‘101 - 121’ showed up very less.

Conclusion:
1.	Female patients have taken more appointments than male patients
2.	There are 99666 patients without Scholarship and out of them around 80% have come for the visit and out of the 21801 patients with Scholarship around 75% of them have come for the visit.
3.	There are around 88,726 patients without Hypertension and out of them around 78% have come for the visit and Out of the 21801 patients with Hypertension around 85% of them have come for the visit.
4.	There are around 102,584 patients without Diabetes and out of them around 80% have come for the visit and Out of the 7,943 patients with Diabetes around 83% of them have come for the visit.
5.	There are around 75,045 patients who have not received SMS and out of them around 84% have come for the visit and out of the 35,482 patients who have received SMS around 72% of them have come for the visit.
6.	There are no appointments on sunday and on saturday appointments are very less in comparision to other week days.
