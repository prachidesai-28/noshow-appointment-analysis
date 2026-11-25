No-Show Appointment Analysis

In this project I looked at around 1.1 lakh medical appointments to see how many patients actually came and how many missed their appointment. I also checked if some neighbourhoods miss more than others.

Files in this repo
Appointment_Analysis.ipynb - the main notebook with all the code and outputs
Hospital_Appointment_Analysis.xlsx - cleaned data, status summary and neighbourhood table in Excel
chart1_status_split.png - pie chart of showed up vs no-show
chart2_neighbourhood_noshow.png - top 10 neighbourhoods with the highest no-show %
noshowappointments.csv - the original dataset
What I did

First I cleaned the data. A few rows had missing age and missing neighbourhood. I filled the age with the median and put "Unknown" for the neighbourhood. There were no duplicate rows. Gender was written in different ways like "Fml", "Male", "Othr", so I changed all of them to F, M and O. One patient had age -1, which is not possible, so I fixed that too.

After that I counted the total appointments, how many patients came and how many didn't, and how many appointments each neighbourhood had. Then I worked out the no-show percentage for every neighbourhood.

For the neighbourhood comparison I only kept areas with 500 or more appointments. Some areas had only 1 or 2 appointments, and one of them showed 100% no-show just because both its patients missed. That doesn't mean much, so I left those small areas out.

Charts

Appointment Status

Top 10 Neighbourhoods

What I found
Around 20% of appointments were missed, so roughly 1 out of every 5 patients didn't turn up.
Jardim Camburi has the most appointments by far, followed by Maria Ortiz and Resistencia.
Santos Dumont has the highest no-show rate, close to 29%, which is clearly above the average.
Itarare is worth looking at because it has a high no-show rate and also a lot of bookings, so it loses a lot of appointments overall.
The data was mostly clean. The main fixes were the gender spellings, a wrong age value and a few missing values.
How to run

Keep noshowappointments.csv in the same folder as the notebook, open Appointment_Analysis.ipynb and run all cells. You need pandas, numpy, matplotlib and openpyxl installed.
