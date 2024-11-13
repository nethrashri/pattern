# pattern


 Below is a summary of the data generation code developed for simulating usage patterns for various service groups and services, specifically designed to mimic user behaviors across different times, days, and devices. The generated dataset is saved as netflix_pattern.csv.

Code Overview
Setup and Initialization

Date Range: The code defines a date range from January 1, 2024, to July 30, 2024, with data recorded at 15-minute intervals.
Service Groups: The main service categories (Gaming, Social Media, Streaming, Shopping, Software) are defined, each with a list of associated services.
Users and Devices: Two users (user1 and user2) are defined, each using various device types like TV, Mobile, Tablet, or PC. Each user is assigned a randomly generated MAC address for device identification.
Data Generation Logic

For each timestamp in the date range, the code generates usage data for each user.
Time-Based Patterns: The code applies specific usage patterns based on the day of the week and time:
User-Specific Weekend Patterns:
user1 uses Netflix between 7 PM and 10 PM on weekends.
user2 prefers Gaming between 4 PM and 9 PM on weekends.
Weekday Patterns:
Both users have a higher probability of using "Software" services during weekday hours (9 AM to 7 PM).
General Usage Patterns:
Outside the specific patterns, the code randomly selects a service group (Gaming, Streaming, etc.) based on the time of day, day of the week, and a random factor.
Randomized Data Generation for Each Entry

For each entry, additional columns are generated to simulate realistic data, including:
usage_minutes: Randomly chosen between 1 and 200.
usage_percentage: Randomly generated between 10% and 100%.
signal_strength: A value between -60 and -40 to simulate varying Wi-Fi signal strengths.
packet_loss_rate, latency, jitter_ms, traffic_spike, bandwidth_speed_per_sec_mbps, buffer_occupancy: Randomly generated values to simulate network and device performance metrics.
Data Storage

The generated data is saved into a Pandas DataFrame with columns for user, timestamp, service group, service name, device type, and various metrics.
Finally, the DataFrame is saved as a CSV file named netflix_pattern.csv for further analysis.


