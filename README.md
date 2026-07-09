# Log-Analysis with Kali Linux

## Overview
This repository contains practical web server log analysis exercises completed using Kali Linux and standard Linux command-line tools. The project demonstrates how Apache access logs can be analyzed to identify web traffic patterns, client activity, HTTP response codes, browser information, and potentially suspicious requests.

The exercises simulate tasks commonly performed by Security Operations Center (SOC) Analysts, Blue Team defenders, and Incident Responders during security investigations.

## Project Objectives
- Analyze Apache web server access logs.
- Identify HTTP request methods.
- Count unique client IP addresses.
- Determine the most active IP address.
- Identify the most requested URLs.
- Analyze HTTP response status codes.
- Examine User-Agent strings.
- Detect web crawlers such as Googlebot.
- Identify browser versions from User-Agent data.
- Develop practical Linux log analysis skills.
  
## Technologies & Tools
- Kali Linux
- Apache Access Logs
- Linux Terminal
- grep
- awk
- sed
- sort
- uniq
- wc
- cat
- head
- tail
- less
- nano
  
## Repository Structure
Web-Server-Log-Analysis/
│
├── README.md
├── Exercise-1/
│   ├── access-1.log
│   ├── Report.docx
│   └── screenshots/
│
├── Exercise-2/
│   ├── apache_logs
│   ├── Report.docx
│   └── screenshots/
│
├── Exercise-3/
│   ├── access-2.log
│   ├── Report.docx
│   └── screenshots/
│
└── images/

## Exercises
Exercise 1 – Access-1.log

- Counted HTTP GET requests
- Identified unique HTTP status codes
- Investigated CONNECT requests
- Explained HTTP status codes
- Investigated malformed request lines
- Analyzed User-Agent information
- Counted Firefox requests
  
## Exercise 2 – Apache Logs
- Counted total log entries
- Identified unique IP addresses
- Determined the most active IP address
- Identified the most requested URL
- Counted HTTP 200 responses
  
## Exercise 3 – Access-2.log
- Counted GET requests
- Identified unique IP addresses
- Counted HTTP 200 and HTTP 400 responses
- Identified the IP address that accessed the doorbell resource
- Determined the Googlebot version
- Identified the most common Firefox version
- Determined the most frequently used HTTP request method
  
## Sample Commands

Count GET requests
grep -c "GET" access-1.log

Count unique IP addresses
awk '{print $1}' access-2.log | sort | uniq | wc -l

Find the most active IP address
awk '{print $1}' access-2.log | sort | uniq -c | sort -nr

Find the most requested URL
awk '{print $7}' access-2.log | sort | uniq -c | sort -nr

Count HTTP 200 responses
awk '$9==200' access-2.log | wc -l

## Skills Demonstrated
- Linux Command Line
- Apache Log Analysis
- HTTP Protocol Analysis
- Security Monitoring
- SOC Analysis
- Incident Investigation
- Threat Hunting Fundamentals
- Blue Team Operations
  
## Learning Outcomes
Through this project, I gained practical experience in:

- Reading and interpreting Apache web server logs.
- Extracting meaningful information using Linux commands.
- Identifying normal and suspicious web traffic.
- Understanding HTTP methods, status codes, and User-Agent strings.
- Applying a structured log analysis workflow similar to that used in Security Operations Centers (SOCs).
  
## Author
Shalom Odori

Cybersecurity Intern | SOC Analyst

License
This project is published for educational and portfolio purposes.
