# Stream Splitting Moving Target Defense

## Executive Summary
Sending communications along a single channel poses certain risks to the data streams being sent. Data which runs via a single route is vulnerable to a variety of threats against confidentiality, integrity, and availability. These include the actions of human threat agents who may jeopardize any of these principles via intercepting, modifying, replaying, or outright discarding messages of importance. Also of concern is the potential threat by natural occurrences which may interrupt or delay services which remain on one communication channel at a time.

This project seeks to address these concerns by creating a point-to-point stream splitting mechanism for channeling data to protect it while in motion. This will take advantage of using multiple communication routes in parallel. As such, any potential attackers will either observe at most a meaningless fraction of the data being sent or be discouraged from attacking by the prospect of compromising multiple lines of communication. This will also provide hardening against infrastructure collapse as the system will be already prepared to swap to different data channels.

The goal of this project is to develop and prototype an interface which may be deployed across organization locations. This interface aims to provide tools for dynamically adding and removing communication channels, ensuring data encryption, and testing for communication quality. The interface will then handle encryption and balance communication channels, splitting up and reassembling data streams as necessary.

## Proposed Project Timeline
 ![alt text](https://github.com/xoBalt/Capstone-Stream-Splitting-MTD/blob/master/Gnatt%20Chart.PNG)

## Project-oriented Risk List

|Risk name (value)  | Impact     | Likelihood | Description |
|-------------------|------------|------------|-------------|
|Loss of a team member. (20)|6|2|The members job or family prevents them from completing the course. That members responsibilities will be divided amongst the remaining members.|
|Loss of communication with our Sponsor. (10)|4|1|The sponsor is assigned other obligations that take them away from this project. The team will continue with the information already supplied by the sponsor and will clearly outline any assumptions made by the team for the project.|
|Team members having other scheduling engagements. (8)|1|6| This Risk might happen a few times during the research. The team has numerous ways of communicating. This Risk might happen, but it will have no impact on the project.|
|Not having the correct technical skillset. (24)|5|6|If a team member or the team has no prior experience with the research. There will be a few times this might happen, but as a team we will gather the needed information and accomplish our tasks.|
|Programing failure (25)|8|4|The project can not proceed because of a programing failure. This project will be written using Python and most members have a good knowledge base of Python. There might be a point where the team will need to reach out and find better ways to wright aspects of the code.|
Loss of research (45)|10|2|A team member accidentally deletes a file. The team is working with a few different tools that keep saved work from being destroyed. Each team member will need to keep this practice consistent throughout the project, to ensure a minimal loss of data.|
|Failure to deliver a final project (50)|10|1|The team fails at any research. The team is excited and capable of accomplishing the tasks ahead. Each team member will need to be active throughout the project. We as a team believe that we can deliver a sound scholarly project.|





## Application Requirements

### User Stories
1. As a **network engineer**, I want all of my data links to be used concurrently to maximize bandwidth.

* Acceptance criteria: The stream splitting daemon should intelligently divide streams across links utilizing their bandwidth efficiently.

2. As a **network engineer**, I want to be able to dynamically add and remove data links.

* Acceptance criteria: The stream splitting daemon should dynacially add and remove links based on availability.

3. As a **network engineer**, I want my connection to stay up with minimal interruption, even if one of my links drops.

* Acceptance criteria: If a link loses bandwidth or goes down, the stream splitting daemon should respond automatically by limiting or stopping traffic through that link.


4. As a **network engineer**, I want my split information stream to transmit and reassemble data at a consistent rate comparable with standard network protocols.

* Acceptance criteria: The transmission speed and integrity of data falls within 10% of control tests with TCP.


5. As a **security engineer**, I want all of my data to be encrypted while in motion.

* Acceptance criteria: The data will be encrypted prior to splitting and transporting.


6. As a **security engineer**, I want my data to be randomly split between links to increase obfuscation.

* Acceptance criteria: Data will be split randomly between links. 

7. As a **security engineer**, I want to control who as access to the process.

* Acceptance criteria: The system will operate on a two-key authentication.

8. As a **security engineer**, I want to be able to set the level of security level of the data being split.

* Acceptance criteria: A flag will need to be set for data passing throught the Stream Splitting.

### [Activity Diagram](https://www.lucidchart.com/invitations/accept/ec184381-74cb-44d4-9053-03b1bd58b8c0)


## Architectural  Diagrams

#### [Level 1](https://www.lucidchart.com/invitations/accept/85a4fb6b-4c7b-486a-9fc6-2013971c1806)


#### [Level 2](https://www.lucidchart.com/invitations/accept/d02d1069-4ae7-4904-a2be-35bbf2d8029a)


#### [Level 3](https://www.lucidchart.com/invitations/accept/176e994b-ccd0-4253-b446-5c1b041db682)



## Resource Requirements
|Resource  | Dr. Hale needed?     | Investigating Team Member | Description |
|-------------------|------------|------------|-------------|
|Python|No|All|Using Python is a programming language to complete the project.|
|Criss Library|No|All|Accessing the Databases and Digital Commons at the Criss Library.|
|Raspberry Pi| No| Greg| Utilizing a Raspberry Pi in order to simulate a client connection more effectively.|
|Supporting Research|No|Greg|Existing research and software that performs a similar job and can be utilized for our purposes.

