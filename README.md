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

<img width="1920" height="1080" alt="Untitled design (1)" src="https://github.com/user-attachments/assets/a66eccff-730e-4863-9555-7b38cd263cf0" />

