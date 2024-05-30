**This machine learning project extracts the archived webserver logs from the windows logger server and converts it into clean structured dataframes leveraging pandas python library to perform malicious network traffic analysis tracking down the indicators of attacks/compromise which includes dns analysis, bad IP's, weird port connections
user behaviour analysis, restricted hosts, user agents etc. The results are produced in a visualized analytics form using matplotlib and seaborn libraries for presenting it to the stakeholders and end clients. Lastly, it creates a REST API service to produce the meaningful analytical results based on the network traffic analysis performed. This automation piece can be extended other types of logs such as zeek, suricata etc. with some minor tweaks. The aim of this project is to detect the anomalies from the logs to hunt and track the threat actors to decrease the dwell time of the cybersecurity incident.**

The steps are broken down as follows with sample hosts, user agents, IP addresses, ports and domain names:

1. Parse the http.log file in each folder line by line. You will have to ignore some rows on the top.
2. Create a data frame of all the cleaned required data. 
3. See how many of the Destination Computers have Mozilla Requests (Mozilla/4.0) and for Opera/9 for each folder.
4. Each unique ip is a request. unique source and unique destination pair. Output that in
formation on the screen. Make it so the IP entry is configurable.
192.168.202.76 to 192.168.28.102 would be unique
192.168.202.79 to 192.168.229 would be unique
5. What are the different ports the traffic is going to. Destination IP would follow a port number. What are these ports used for. You will have a different answer for each port. once you have a list you can use google. Make it so the port search configurable.
6. How many times does each folder go to amazon. Make folder search configurable.
7.  How many times do you encounter a request from an unknown host. Example below that does not have a domain name.
192.168.61.10 1084 112.121.178.189 80 1 GET 112.121.178.189
8. sharq1.com and linguaflair.de are in the banned host list trigger an alert when you see this host. Make it so the banned ports can be configurable. You can either save it in a list or a file to make it configurable.
9. Was google.com visited at all in any of the logs
10. Take the above data and perform an analytic analysis using the AI algorithms you know and plot your analysis. Make sure the analysis is detailed so it can be explained to a non technical person. 
11. Create a service that takes in a cleaned file and performs the analytics and returns some analytic results. This analytic could be any ones that you have studied. 
