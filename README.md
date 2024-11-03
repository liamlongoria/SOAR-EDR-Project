<h1>SOAR-EDR Project</h1>

<h2>Objective</h2>
Integrates a Security Orchestration, Automation, and Response (SOAR) platform (Tines) with an Endpoint Detection and Response (EDR) solution (LimaCharlie) to automate incident responses and improve cybersecurity workflow. This project demonstrates detecting and reacting to specific threats, such as unauthorized use of password recovery tools on Windows, by automating alert notifications and enabling user-driven decisions (like isolating compromised machines). It provides hands-on experience in crafting and deploying playbooks, configuring detection rules, and integrating communication channels like Slack and email for incident response.
<br />


<h2>Skills Acquired</h2>

- <b>Playbook/story creation to to facilitate and guide security response actions.</b> 
- <b>Improved ability to write rules for detection and response.</b>
- <b>Deepened understanding of telemetry by implementing cohesion between different platforms.</b>
- <b>Formatting alerts to provide important, easy to read information to investigate.</b>

<h2>Tools Used</h2>

- <b>Amazon Web Sercives Cloud Provider (AWS)</b>
- <b>Tines (SOAR)</b>
- <b>LimaCharlie (EDR)</b>
- <b>Slack and Email (Alerts)</b>

<h2>Project Walkthrough:</h2>

**Step 1:** Spun up an instance in AWS and connected to virtual machine (VM) using remote desktop protocol (RDP).

<img width="956" alt="AWSspin" src="https://github.com/user-attachments/assets/87a92032-2b68-4a76-9233-e3abd6162e35">


**Step 2:** Created installation key in LimaCharlie to enroll EDR into VM by installing LimaCharlie agent in Powershell.

<img width="957" alt="Installationkey" src="https://github.com/user-attachments/assets/5a2257cd-5bc3-4997-9212-a8beae35d6c0">


**Step 3:** Installed and ran LaZagne, a password recovery tool, which generated events in LimaCharlie.

<img width="953" alt="LasagnePS" src="https://github.com/user-attachments/assets/3292ddef-3bd8-4612-8c60-47d64b2f9277">
<img width="955" alt="LasagneProcessTL Lima" src="https://github.com/user-attachments/assets/253fd824-9fc6-47a6-9bf3-31dca7db747c">


**Step 4:** Created detection and responce rule for Lazagne events. Then ensured that events were captured in the detections section.

<img width="942" alt="EDR Detect" src="https://github.com/user-attachments/assets/b72cf6c9-bccc-4239-a722-6f1b691296ba">
<img width="938" alt="EDR Respond" src="https://github.com/user-attachments/assets/86787b0f-4884-4c81-81af-ad16c2a90aad">
<img width="953" alt="Detectsuccess" src="https://github.com/user-attachments/assets/1995ef59-9f0b-4912-942f-2aaf1007d3b2">


**Step 5:** Set up Tines and Slack, then interconnected them with LimaCharlie

<img width="956" alt="tinesdetection" src="https://github.com/user-attachments/assets/821b2137-5e75-4696-b9bb-379a60581d4d">


**Step 6:** Created a playbook/story in Tines, which sends a Slack message and an email containing information about the detection from LimaCharlie. It would then generate a prompt asking if we want to isolate the machine. From there, automation is created to isolate the machine based on the user responce.

![Longo-SOAR-EDR Project-storyboard](https://github.com/user-attachments/assets/9c00c2c5-5878-4f65-ab55-1ed54aeaf045)


**Step 7:** Test ran the playbook/story and responded yes to the user prompt to isolate the machine.

<img width="956" alt="slackalertwithisolate_fin" src="https://github.com/user-attachments/assets/2dfb537f-c1a9-4dfe-869b-4e1d45e2ab37">
<img width="955" alt="emailtines_final" src="https://github.com/user-attachments/assets/fe893fb9-2ff5-416f-be4c-1a7d3879983f">
<img width="956" alt="Userprompt_fin" src="https://github.com/user-attachments/assets/e037d3e2-9020-4162-bcbb-a87d70d407f5">
<img width="953" alt="isolatedsensor" src="https://github.com/user-attachments/assets/4cdf99d6-850f-42e1-9671-4714c86b6226">













