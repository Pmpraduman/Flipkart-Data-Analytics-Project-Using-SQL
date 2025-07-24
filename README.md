# Flipkart-Data-Analytics-Project-Using-SQL
<img width="666" height="375" alt="Flipkart logo" src="https://github.com/user-attachments/assets/665dbc33-2639-42c7-8ee6-bf12e0371214" />

#  Overview

### **As a Product Manager, I built this project to simulate how product teams at leading e-commerce platforms like Flipkart use data to understand user behavior, optimize conversion funnels, improve logistics, and drive business growth. The entire project is powered purely by SQL and showcases my ability to derive actionable insights from raw data — without relying on any external BI tools or dashboards.**


# Objectives
### ●  Track user signups and activity (DAU, WAU, MAU) to analyze growth. 
### ●  Map the full conversion funnel from views to purchases using SQL. 
### ●  Identify top-performing products and detect high return/cancellation patterns. 
### ●  Analyze traffic sources to measure marketing effectiveness. 
### ●  Evaluate delivery performance and user retention trends. 
### ●  Drive all insights using raw SQL — without any BI tools 

# Dataset  
The data for this project is sourced from self-generated data

#  Schema

```sql
DROP TABLE IF EXISTS user_activity;
CREATE TABLE user_activity (
    activity_id SERIAL PRIMARY KEY,
    user_id INT NOT NULL,
    session_id VARCHAR(100),
    activity_date DATE,
    activity_time TIME,
    device_type VARCHAR(50),               -- e.g., 'Mobile', 'Desktop'
    platform VARCHAR(20),                  -- 'App' or 'Web'
    source VARCHAR(100),                   -- 'Organic', 'Google Ads', etc.
    referral_user_id INT,                  -- If user was referred
    is_new_user BOOLEAN,
    page_viewed VARCHAR(100),
    click_event BOOLEAN,
    product_id INT,
    added_to_cart BOOLEAN,
    purchased BOOLEAN,
    coupon_used BOOLEAN,
    order_value DECIMAL(10,2),             -- Order amount
    returned BOOLEAN,                      -- Whether the product was returned
    session_duration_seconds INT           -- Duration of session
);
 SELECT * From user_activity;



#   Business Problems and Solutions
