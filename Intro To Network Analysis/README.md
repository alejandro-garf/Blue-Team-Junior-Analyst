# Capstone Project
## [Certificate](https://github.com/alejandro-garf/Blue-Team-Junior-Analyst/blob/main/Intro%20To%20Vulnerability%20Management/Course%20-%20Certificate%20-%20Introduction%20to%20Vulnerability%20Management-course.pdf)
## Scenario
```
Alexis is a fictional cybersecurity company with thousands of employees. An attacker has gained unauthorized entry into its premises and has connected their laptop to an unused port on a switch. The attacker now has access to the company’s internal networks. Within the internal network, there is a central server where critical proprietary data is stored. In this capture, the attacker is attempting to collect SSH credentials that they can use to log into the central server.
```
## My Steps:

### 1. Finding the Mad Adress of the attaker 
#### - Use Wireshark to open the pcap file
#### - Typing in ssh into the display filter cuts packets that we need to inspect to 142
#### - Checked Statistics > Conversations. Saw that there are only two devices that are communicating via SSH
#### - Went back to the main screen of Wireshark and checked the first packet showing on screen
#### - Checked the ethernet details which gave the answer: 08:00:27:3d:27:5d
### 2. What is the type of attack which is taking place that allows the attacker to listen in on conversations between the central server and another host?
#### - Man in the middle attack.
### 3. What is the file which was downloaded from the central server?
#### - Went to Statistics > Protocol Hierarchy and got an overview of all the protocols used in the PCAP file
#### - Under TCP we can see that FTP traffic was captured in the PCAP file
#### - Went back to main and typed in ftp in the display filter
#### - I selected packet 550 and followed the TCP stream.
#### - Answer: Alevis_Employee_Information_Chart.csv
### 4. What department does Borden Danilevich work in?
#### - Typed ftp in the display filter
#### - Follow the TCP stream
#### - Selected Stream 1 (Opens up CSV File)
#### - The fifth column contains the department info. Did a search for “Borden” to get his department = Sales
### 5. What is the SSH password of the Domain Administrator?
#### - I checked the csv file again and looked for the word “admin.” 
#### - There were some gibberish characters in the SSH password so I removed them and got the answer = gMR<4eXf]e6W.
