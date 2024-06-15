Issue Summary:
- Duration: The outage occurred from 11:00 AM to 1:00 PM (WAT) on a busy Monday morning. - Impact: The service was completely unavailable during this time, affecting all users. I estimated that approximately 80% of users were affected, based on the influx of complaints and support tickets.
Root Cause:
The root cause of the outage was a misconfiguration in the load balancer settings, specifically related to traffic distribution among servers in the cluster. This led to an overload of traffic on one server and a lack of availability on others.
This was fixed by adjusting the load balancer settings to evenly distribute traffic among servers.
Timeline:
- 10:45 AM: I received automated monitoring alerts indicating high server load and immediately started investigating.
- 10:50 AM: After verifying the issue, I alerted the engineering team and began troubleshooting. - 11:00 AM: Traffic was rerouted to other servers, but the problem persisted, indicating a deeper issue.
- 11:30 AM: Misleading investigation paths were taken, including checking database performance and network connectivity.
- 12:00 PM: Unable to resolve the issue internally, I escalated it to the infrastructure team for further investigation.
- 12:30 PM: The root cause was identified as a misconfiguration in the load balancer settings. - 1:00 PM: I corrected the load balancer settings, and traffic was evenly distributed among servers, resolving the issue.
Root Cause and Resolution:
The misconfiguration in the load balancer settings caused an imbalance in traffic distribution, leading to one server becoming overloaded while others remained underutilized. This was fixed by adjusting the load balancer settings to evenly distribute traffic among servers.
Corrective and Preventative Measures:
- Improvements/Fixes: I have implemented regular audits of load balancer settings to prevent similar misconfigurations. Additionally, I have set up automated monitoring and alerting for load balancer performance.
- A List Of Tasks To Address The Issue:
- Patching the load balancer configuration to ensure correct traffic distribution.
- Adding monitoring for load balancer performance metrics.
- Conducting regular audits of load balancer settings to prevent future misconfigurations.

