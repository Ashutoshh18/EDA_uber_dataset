# Project Background
### Uber is a global ride-hailing platform that connects customers with drivers through its app. Since its launch in 2009, Uber has revolutionized urban transportation by providing on-demand rides, transparent pricing, and cashless payments

This project focuses on exploring 1.5 lakh booking records to understand operational efficiency and customer behavior. The analysis dives into key performance areas such as:


***Overall Booking Performance Metrics*** – Understanding the ratio of successful vs failed rides, along with a detailed breakdown of customer cancellations, driver cancellations, and incomplete rides.

**Performance by Vehicle Type*** – Evaluating demand, cancellations, breakdowns, and booking value 
across different vehicle categories.

***Financial Analysis*** – Estimating revenue earned, potential revenue lost due to cancellations or 
incomplete rides, and average revenue per ride.

***Ride Distribution by Time & Location*** – Identifying peak booking hours, popular pickup hubs, 
and demand concentration.

***Operational Growth & Retention*** – Measuring month-over-month growth (CMGR), retention rate of customers,
and long-term usage trends.

***Customer Experience & Satisfaction*** – Analyzing customer and driver ratings to assess service quality

All data inspection, cleaning, and exploratory analysis were performed in a Jupyter Notebook 
using Python and popular data analysis libraries such as:

Dataset Source (Kaggle)
Environment (Jupyter Notebook)
Tools Used (Python, Pandas, NumPy, Matplotlib, Seaborn)

# Data Stucture & Initial Checks
The dataset for this analysis was sourced from Kaggle. It is provided in a single CSV file and loaded into a Jupyter Notebook for exploration.

***Total Records:*** 148,770
***Total Columns:*** 21
***File Format:*** CSV

## Data Schema
The dataset contains the following columns:

| Column Name                        | Description |
|------------------------------------|-------------|
| Date                               | Date of the booking |
| Time                               | Time of the booking |
| Booking ID                         | Unique identifier for each ride booking |
| Booking Status                     | Status of booking (Completed, Cancelled by Customer, Cancelled by Driver, etc.) |
| Customer ID                        | Unique identifier for customers |
| Vehicle Type                       | Type of vehicle (Go Mini, Go Sedan, Auto, eBike/Bike, UberXL, Premier Sedan) |
| Pickup Location                    | Starting location of the ride |
| Drop Location                      | Destination location of the ride |
| Avg VTAT                           | Average Vehicle Time at Arrival |
| Avg CTAT                           | Average Customer Time at Arrival |
| Cancelled Rides by Customer        | Customer-initiated cancellation flag |
| Reason for Cancelling by Customer  | Reason for customer cancellation |
| Cancelled Rides by Driver          | Driver-initiated cancellation flag |
| Driver Cancellation Reason         | Reason for driver cancellation |
| Incomplete Rides                   | Incomplete ride flag |
| Incomplete Rides Reason            | Reason for incomplete rides |
| Booking Value                      | Total fare amount for the ride |
| Ride Distance                      | Distance covered during the ride (in km) |

Initial checks were performed to:

Verify missing values

Inspect data types (numeric, categorical, datetime)

Check for duplicates and inconsistencies

Ensure overall data quality before deeper analysis


# Executive Summary - Overview of findings

#### In analyzing 150,000 Uber bookings, we found that 31% of rides were cancelled. Of these, 58% were driver cancellations, followed by incomplete rides, which together represent controllable factors leading to significant revenue loss. In contrast, customer cancellations, while frequent, are largely outside of company control.

For stakeholders, the key takeaway is:

***Driver cancellations are the single largest contributor to lost revenue.***

***Incomplete rides add further controllable loss, compounding the issue.***

***Additionally, the company’s Compound Monthly Growth Rate (CMGR) is -0.37%, highlighting stagnant growth that could worsen if controllable cancellations are not addressed.***

<img width="1367" height="864" alt="Untitled design (2)" src="https://github.com/user-attachments/assets/9b2aee58-158a-4cf9-b4fa-f88a373e14c2" />

# Insights Deep dive
### Overall Booking Performance Metrics

- High cancellation rate is hurting growth
Out of 150,000 total rides, only 69% were completed successfully, meaning 31% of rides failed. Nearly 1 in 3 customers fails to complete their journey, directly impacting both revenue and customer trust.

- Driver cancellations dominate failed bookings
Of the failed bookings, 58% were due to driver cancellations, making driver behavior the largest controllable contributor to revenue loss. Targeting driver cancellation policies could unlock significant efficiency gains.

- Failure reasons reveal operational gaps
Most customer cancellations happened because drivers didn’t approach the pickup or requested cancellation. Driver cancellations were mainly due to personal emergencies or overcapacity, while incomplete rides were caused by vehicle breakdowns or unmet demand. These highlight key operational inefficiencies that, if addressed, could improve reliability and revenue.

<img width="6778" height="1960" alt="my_plot" src="https://github.com/user-attachments/assets/5154c8a5-9dc1-4484-909e-af2112409b69" />

### Peformance metrics by vehicle type

- Autos dominate bookings
Autos received 37,419 rides, followed by Go Mini (29,806) and Go Sedan (27,141), showing strong customer preference for affordable, convenient vehicles.

- High-demand vehicles face more breakdowns
Autos and Go Mini had the most breakdowns (740 and 617, respectively), causing incomplete rides and revenue loss, highlighting the need for targeted maintenance.

- Average booking value is consistent
Booking values are fairly uniform, with Go Sedan highest at ₹501.7 per ride, indicating that improving availability and reliability of popular vehicles can directly boost revenue.

<img width="1920" height="1080" alt="Untitled design (4)" src="https://github.com/user-attachments/assets/eace6b6a-08ba-4424-b647-79c12477668f" />

### Financial Analysis – Revenue Earned vs Potential Revenue and Loss Estimation

- Significant revenue loss from controllable factors
Out of a potential revenue of ₹67.37M, the company earned ₹51.61M, resulting in a revenue loss of ₹15.76M. This highlights the financial impact of controllable operational failures.

- Driver cancellations are the largest contributor to lost revenue
Driver cancellations account for 70.9% of the lost revenue, while incomplete rides contribute 29.1%, indicating that improving driver reliability could recover the majority of lost income.

- Revenue varies by vehicle type
Autos generated the most revenue (₹12.84M), followed by Go Mini (₹10.25M) and Go Sedan (₹9.35M), showing that high-demand vehicles contribute disproportionately to total earnings.

<img width="1920" height="1080" alt="Untitled design (5)" src="https://github.com/user-attachments/assets/2e4e5992-075c-4392-8941-2004f96181b6" />

### Operational CMGR % Growth Anaylysis

- Month-over-month growth fluctuates inconsistently
The month-over-month bookings show a rollercoaster pattern, with some months gaining traction (e.g., Month 3: +7.64%) and others losing ground (e.g., Month 2: -6.99%), highlighting inconsistent demand and operational volatility

- Overall growth is negative
Overall, the business is struggling to grow, with total bookings declining by -4.31% over the year, signaling stagnation that needs urgent attention.

- Compound monthly growth rate and retention signal weak momentum
The compound monthly growth rate of -0.37% and a retention rate of only 0.81% show that the company is not only failing to expand its customer base but also struggling to keep existing customers engaged, emphasizing the importance of improving service reliability and the overall customer experience.

<img width="1920" height="1080" alt="Untitled design (6)" src="https://github.com/user-attachments/assets/8c05336b-92ba-4b85-903b-5c4a5213cb70" />







