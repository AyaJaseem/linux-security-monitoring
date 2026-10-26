# Linux Security Monitoring

## About
This is a small project I worked on to learn more about Linux security and log monitoring.

I used Ubuntu and the Elastic Stack to collect system logs and monitor failed SSH login attempts. I also created a dashboard in Kibana to view the results.

## Tools
- Ubuntu Linux 20.04 LTS
- Elasticsearch 8.19.23
- Kibana 8.19.23
- Elastic Agent 8.19.23
- SSH

## Setup and Configuration

### 1. Environment Setup
The lab was set up using an Ubuntu Linux virtual machine running Ubuntu 20.04.6 LTS.

The following tools were installed and configured:
- Elasticsearch 8.19.23
- Kibana 8.19.23
- Elastic Agent 8.19.23

### 2. Elasticsearch Setup
Installed Elasticsearch on Ubuntu and verified that the service was running. Elasticsearch was used to store and index the collected log events.

### 3. Kibana Setup
Installed Kibana and connected it to Elasticsearch. Kibana was used to search, inspect, and visualize the collected security events.

### 4. Elastic Agent Configuration
Configured Elastic Agent to collect Linux system and authentication logs and send them to Elasticsearch for analysis.

### 5. Log Analysis
Used Kibana Discover to inspect authentication events and identify failed SSH login attempts. The authentication events were available in the `logs-system.auth-default` data stream.

### 6. Dashboard Configuration
Created a Kibana dashboard named **Failed SSH Login Monitoring** to visualize failed login attempts and review usernames and source IP addresses.

## What I Did
- Set up Elasticsearch and Kibana.
- Configured Elastic Agent to collect system and authentication logs.
- Checked SSH login attempts in Kibana.
- Created a dashboard to show failed login attempts.
- Added charts to view usernames and source IP addresses.

## Testing
I tested the setup by attempting to log in using a username that does not exist.

The login was rejected, and the failed attempts appeared in Kibana.

Test username: `wronguser789`

Source IP: `127.0.0.1`

## What I Learned
This project helped me practice working with Linux, understand authentication logs, and learn how to use Kibana to monitor security events.

## Dashboard Screenshots

### Screenshot 1
![Kibana Dashboard 1](./failed-ssh-dashboard%201.png)

### Screenshot 2
![Kibana Dashboard 2](./failed-ssh-dashboard.2.png)

### Screenshot 3
![Kibana Dashboard 3](./failed-ssh-dashboard.3.png)

### Screenshot 4
![Kibana Dashboard 4](./failed-ssh-dashboard.4.png)

## Results
- Successfully configured Elasticsearch and Kibana for Linux security monitoring.
- Collected Ubuntu system and authentication logs using Elastic Agent.
- Generated failed SSH login events during testing.
- Verified that failed login events appeared in Kibana.
- Created a Kibana dashboard to visualize failed login attempts by username and source IP address.

## Conclusion
This project provided hands-on experience with Linux log monitoring, Elasticsearch, Kibana, and basic security event analysis. It helped me understand how SIEM tools can be used to monitor authentication activity and investigate failed SSH login attempts.

## Security Note
This project was created for educational purposes in a controlled lab environment. Sensitive information should not be uploaded to GitHub.
