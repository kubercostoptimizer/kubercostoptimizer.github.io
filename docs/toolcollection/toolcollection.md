---
layout: default
title: Tool Collection
nav_order: 5
has_children: false
permalink: /docs/toolcollection
---
# Tool Collection
---

## Tool Selection

The following surveys were initially used to collect the set of Android security papers:

1. Qiu, Junyang, Jun Zhang, Wei Luo, Lei Pan, Surya Nepal, and Yang Xiang. "A survey of Android malware detection with deep neural models." ACM Computing Surveys (CSUR) 53, no. 6 (2020): 1-36.
2. Arshad, Saba, Munam Ali Shah, Abid Khan, and Mansoor Ahmed. "Android malware detection & protection: a survey." International Journal of Advanced Computer Science and Applications 7, no. 2 (2016): 463-475.
3. Rashidi, Bahman, and Carol J. Fung. "A Survey of Android Security Threats and Defenses." J. Wirel. Mob. Networks Ubiquitous Comput. Dependable Appl. 6, no. 3 (2015): 3-35.
4. Tam, Kimberly, Ali Feizollah, Nor Badrul Anuar, Rosli Salleh, and Lorenzo Cavallaro. "The evolution of android malware and android analysis techniques." ACM Computing Surveys (CSUR) 49, no. 4 (2017): 1-41.
5. Faruki, Parvez, Ammar Bharmal, Vijay Laxmi, Vijay Ganmoor, Manoj Singh Gaur, Mauro Conti, and Muttukrishnan Rajarajan. "Android security: a survey of issues, malware penetration, and defenses." IEEE communications surveys & tutorials 17, no. 2 (2014): 998-1022.
6. Alqahtani, Ebtesam J., Rachid Zagrouba, and Abdullah Almuhaideb. "A Survey on Android Malware Detection Techniques Using Machine Learning Algorithms." In 2019 Sixth International Conference on Software Defined Systems (SDS), pp. 110-117. IEEE, 2019.
7. Souri, Alireza, and Rahil Hosseini. "A state-of-the-art survey of malware detection approaches using data mining techniques." Human-centric Computing and Information Sciences 8, no. 1 (2018): 1-22.

We appended the list with top conferences/journals based on CORE ranking and Journal Citation Reports (JCR).

The software engineering conferences/journals include:

1. International Conference on Software Engineering
2. Foundations of Software Engineering
3. Automated Software Engineering
4. International Symposium on Software Testing and Analysis
5. IEEE Transaction of Software Engineering
6. Empirical Software Engineering
7. IEEE Software
8. Journals of Systems and Software
9. Information and Software Technology
10. ACM Transactions on Software Engineering and Methodology
11. Mining Software Repositories

The security conferences/journals include:

1. ACM Conference on Computer and Communications Security
2. IEEE Symposium on Security and Privacy
3. The Network and Distributed System Security
4. USENIX Security
5. IEEE Transactions on Information Forensics and Security
6. IEEE Transactions on Dependable and Secure Computing
7. Computers & Security 
8. International Journal of Information Security Science 
9. International Journal of Information Security
10. IEEE Security & Privacy
11. Annual Computer Security Applications Conference

---

## Tool Categorization

The image below lists the categorization of Android security papers found:

![](../img/tools_mind_map.PNG)

These categories include:

1. Not Malware Detection - Papers irrelevant to malware detection
2. Generic Malware - Papers aimed to detect malware by learning features from a large set of benign and malicious applications.
3. Payload Specific - Papers aimed to targeting a specific type of payload (ex., info-leak, overlay phishing, privilege escalation)
4. Condition Detection - Papers aimed at focusing on conditions that lead to the malicious payload
5. Forced Execution - Papers aimed to force app execution into the malicious path
6. Hiding Detection - Papers aimed at flagging the difference between app behavior and its presented user interface
7. Dynamic Loading - Papers aimed at detecting dynamic code loading
8. Sandboxing - Papers aimed at creating analysis frameworks to aid researchers in analyzing malware samples
9. Repackaged Malware - Papers aimed at detecting repackaged apps
10. Inter App Attacks - Papers aimed at detecting apps that collude together to perform an attack

Details of the papers within each category can be found within this [excel file](../../../assets/data/excelsheets/Tools.xlsx).

---
