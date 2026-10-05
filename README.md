### 1. Project Title

* **Title:** Uber Ride Request & Supply-Demand Analytics Dashboard


---

### 2. Short Description

* A business intelligence project developed using Microsoft Power BI to clean, model, and visualize real-world Uber trip request records.
* Focuses on diagnosing trip completion failures, mapping temporal and geographic demand spikes, and identifying operational supply shortages.

---

### 3. Purpose

* **Quantify Lost Booking Demand:** Measure and differentiate lost trip volume between driver-side cancellations and system-level car shortages ("No Cars Available").
* **Pinpoint Peak Demand Windows:** Analyze hourly and weekday booking trends to highlight extreme morning and evening commuter surges.
* **Identify Route-Specific Imbalances:** Contrast city center pickups against airport transit routes to uncover structural supply-demand gaps.
* **Support Operational Strategy:** Supply fleet managers with actionable KPIs to optimize driver dispatching, reduce idle transit, and adjust dynamic surge incentives.

---

### 4. Tech Stack

* **Business Intelligence & Visualization:** Microsoft Power BI Desktop
* **Data Extraction, Transformation, and Loading (ETL):** Power Query (M Language)
* **Data Modeling & Analytics:** DAX (Data Analysis Expressions)
* **Data Storage / Source Format:** Microsoft Excel (`.xlsx`) / Flat File (`.csv`)

---

### 5. Example Walkthrough

* **Use Case:** Analyzing ride failure rates during the weekday evening rush hour.
* **Filter Configuration:** Select `Pickup Point = Airport` within the `17:00 – 21:00` time window.
* **Observed Insight:** The dashboard reveals that more than 60% of airport trip requests fail due to "No Cars Available," while driver cancellations remain under 10%.
* **Operational Conclusion:** Confirms an absolute shortage of inbound cars reaching the airport rather than drivers actively rejecting airport trips.

---

### 6. Data Source

* **Dataset Name:** Uber Trip Request Records (Transactional log format)
* **File Format:** `.csv` / `.xlsx`
* **Schema Attributes:**
* `Request id`: Unique transaction identifier for each booking attempt.
* `Pickup point`: Geographic pickup location (e.g., City, Airport).
* `Driver id`: Unique identifier assigned to the servicing driver (empty if unassigned).
* `Status`: Trip outcome (`Trip Completed`, `Cancelled`, `No Cars Available`).
* `Request timestamp`: Date and time when the customer placed the ride request.
* `Drop timestamp`: Date and time when the trip ended (null for incomplete trips).



---

### 7. Features & Highlights

* **Automated ETL Pipeline:** Handled inconsistent date-time structures, managed null values, cleaned column headers, and engineered discrete time dimensions using Power Query.
* **Executive KPI Scorecards:** High-level summary cards reporting Total Bookings, Trip Completion Rate (%), Cancellation Rate (%), and Unfulfilled Demand Rate (%).
* **24-Hour Demand Profiling:** Line and area charts mapping hourly booking requests alongside completed trips to reveal real-time capacity deficits.
* **Trip Outcome Decomposition:** Donut and stacked bar charts detailing the proportion of completed trips against missed requests.
* **Corridor-Based Comparison:** Cross-location visuals illustrating how driver availability shifts between airport routes and intra-city trips.
* **Interactive Filtering:** Dynamic slicers enabling instantaneous drill-downs by date ranges, pickup points, time slots, and ride completion statuses.

---

### 8. Business Impact & Insights

* **Severe Supply Deficit at Airports (Evening Peak):** Between 5:00 PM and 9:00 PM, over 60% of airport ride requests go unfulfilled due to "No Cars Available" because cars drop passengers in the city earlier in the day and do not return to the airport hub.
* **Driver Cancellations During Morning City Rush:** Between 5:00 AM and 9:00 AM, trips originating in the city face high driver cancellation rates, likely driven by driver unwillingness to take long trips to the airport that offer lower return trip guarantees.
* **Quantifiable Revenue Leakage:** More than 55% of all incoming ride attempts fail to convert into completed trips, pointing to substantial untapped gross booking revenue.
* **Actionable Fleet Interventions:**
* Implement targeted driver bonuses for city-to-airport trips in the late afternoon to naturally increase vehicle availability for evening flight arrivals.
* Introduce airport return trip guarantees or queue-priority privileges for drivers who accept early-morning city-to-airport runs, directly cutting cancellation rates.


---

### 9.	Screenshots / Demos
Show what the dashboard looks like.
Example: ![Dashboard Preview](https://github.com/rushabh419/Uber-Dashboard/blob/main/Main%20Uber.png)
[Dashboard Preview](https://github.com/rushabh419/Uber-Dashboard/blob/main/uber%20dashboard.png)
