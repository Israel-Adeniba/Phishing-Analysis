# Phishing-Analysis

A brief introduction to Phishing attacks <br />

Phishing is a type of cyber attack and a form of social engineering that targets individuals through email, text messages, phone calls and other forms of communication. It is an attack that exploits the human side of cyber security rather than any kind of technical vulnerability. The common goal is to gain unauthorized access to a system, exfiltrate data or gain some sort of user credentials that can be spoofed or impersonated. <br />

Typically, these deceptive (phishing) emails or messages appearing to be from a legitimate source like an employer, bank or a trusted organization contain an attachment or malicious link when clicked would lead the user to a malicious website to trick the user into putting their credentials or downloading malware.
<br />
<br />

Goals of Phishing <br />
- Impersonation; posing as legitimate organizations or individuals
- Stealing sensitive information; credentials, passwords, credit card numbers, PII, sesnitive files
- Deliver and install malware; via attachments, embedded files, URLs etc.
- Exploit humans; human psychology, prey on motions 


Phishing Attack Types <br />

- Spear Phishing: Targeted form of Phishing where an attacker tailors the message to a specific individual or organization. This requires a lot of research so an attacker can gain some form of credibility to make the attack successful.<br />
<br />

- Whaling: A type of spear phishing that targets high profile individuals within an organization, an example of such individuals are senior executives and senior management because these individuals have a higher level of authorization or access to sensitive information <br />
<br />

- Vishing: Short for "voice phishing where an attacker uses phone calls or voice messages to trick individuals into revealing sensitive information. This information can include bank account details, passwords, or other personal data. Attackers often impersonate trusted organizations like banks or government agencies to gain the victim's trust. <br />
<br />

- Smishing: A phishing attack that targets individuals through SMS (Short Message Service) or text messages. The term is a combination of “SMS” and “phishing.” The attacker sends deceptive text messages to lure victims into sharing sensitive personal or financial information, clicking on malicious links, or downloading malware. <br />  
<br />

- Quishing: A cyberattack known as "QR code phishing" where a cybercriminal uses QR codes to trick individuals into visiting malicious websites or downloading malware onto their devices. Victims are deceived into scanning a malicious QR code that can be embedded in various forms, such as posters, emails, or even placed over legitimate QR codes, aiming to steal sensitive information like passwords, financial data, or personal details. < br />


Phishing Analysis Methodology <br />

- Identify the email as a potential Phishing attempt: Look out for common indicators like suspicious attachments, wrong spellings, urgency, links, suspicious sender addresses <br />
<br />

- Initial triage: Quickly assess and prioritize according to potential threat level. Determine the appropriate level of response, timing of response and allocation of resources for further analysis. <br />
<br />

- Analyze the email header: Examine the header for details about the sender's identity, mail servers, and the path the email took. The header contains important metadata that can be used to analyze and assess details like spoofed sender addresses, malicious IP addresses, and other anomalies. True origin can be identified and authenticity checked <br />
<br />
  
- Analyze the email body: Scrutinize the content for suspicious language, errors, formatting, call to action, requests for sensitive information, or any other social enginring red flags like scarcity, urgency, authority, trust etc.  <br />
<br />

- Analyze attachments: Check for malicious files that could harm your system and be cautious of unexpected file types like .exe, .scr, .zip, or .rar, as these are often used to deliver malware. Using malware analysis techniques like sanboxing, file signature analysis and behavioral analysis, examine attachments, file type, content and behaviour. <br />
<br />

- Verify URLs: Analyze links for suspicious domains, shortened URLs, or redirects to malicious websites. Check for HTTPS, examine the website's design, and use online tools like URLScan.io and VirusTotal. This is basically to determine their legitimacy and destination. <br />
<br />

- Contextual Examination: Perform a holistic analysis by considering the organization’s broader environment and any recent security incidents to assess the credibility of a phishing email. Review patterns in reported cases, check ticketing systems for similar incidents, and analyze the email copy along with identified IoCs or artifacts. Use these findings to conduct a threat hunt across the organization’s email system, identifying related attempts and recurring themes—such as sender addresses or threat actor tactics—to enable more proactive and efficient implementation of defensive measures. <br />
<br />

 - Defense measures: Upon detection of a phishing attempt, determine whether to apply proactive measures, reactive measures, or both—depending on its success.<br />
 Reactive measures are taken when the phishing attempt succeeds. These include activating incident response procedures for containment, mitigation, and remediation. For example, if a user is successfully phished and credentials are compromised, immediate actions may include temporarily disabling their account, reviewing login history, resetting credentials, and conducting further investigation to limit damage.<br />
   Proactive measures focus on preventing future incidents. These may involve implementing technical controls such as advanced email filtering, DNS blacklisting, and endpoint protection based on identified IoCs and artifacts. Additionally, proactive efforts should include educating users on phishing awareness, providing clear guidelines for recognizing suspicious emails, and ensuring employees know how to quickly report incidents to the SOC. <br /> 
<br />

- Documentation and Reporting: Maintain accurate, detailed records in tickets, including findings, verdicts, and actions taken, to ensure future justification and traceability of decisions. <br />
<br />

This Phishing Analysis will focus on Phishing emails and it's attachments, conducted primarily within the Ubuntu Virtual Machine. <br />

<h1> Utilities </h1>
- Mozilla Thunderbird <br />
- Sublime text <br />
<br />

We require an actual email client to interact with email messages, preferrably "Mozilla Thundrbird", a free and open source option <br />
Open a terminal window > enter the command "sudo apt install thunderebird" <br />
<br />
<br />
<img src="https://i.imgur.com/dSLezVY.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
Thunderbird installation complete
<img src="https://i.imgur.com/1EhwdWY.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
Installation confirmation on Desktop
<img src="https://i.imgur.com/1zPH9DR.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
Now that thunderbird has been installed, any ".eml or e-mail" files are automatically associated with the application <br />
Letts open up an email file <br />
On the desktop Open the Phishing Analysis folder > Header Analysis > Open sample1.eml  <br />
<img src="https://i.imgur.com/2cLl122.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
We need to be able to open email messages with linked images without automatically blocking them <br />
Open thunderird > Privacy & Security > Check "Allow remote content in messages <br />
<img src="https://i.imgur.com/1THnbZB.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />

To do some manual email file and header analysis, we need a text and code editor not just to rely on the terminal for the full analysis <br />
We would be installing Sublime Text, an editor for code and different types of markup <br />
Open Firefox > search "sublime text" > Click the first result > Install for linux <br />
<img src="https://i.imgur.com/mlu34cO.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
<img src="https://i.imgur.com/SNtXrli.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
To install Sublime text, we would run the "gpg key" and install the package. <br />
Copy the GPG key, paste in the terminal <br />
Select the channek to use  by copying the "Stable" command <br />
<img src="https://i.imgur.com/K5lXqni.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
<img src="https://i.imgur.com/efniIwm.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
<img src="https://i.imgur.com/6cE2pTM.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
Run the "sudo apt-get update" command and the "sudo apt-get install sublime-text" command'<br />
<img src="https://i.imgur.com/9cD5dxK.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
<img src="https://i.imgur.com/xbnHt99.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
<img src="https://i.imgur.com/1tILb5b.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />
To confirm the installation of Sublime text, click the applications menu <br />
<img src="https://i.imgur.com/IFQvONu.png" height="80%" width="80%" alt="Building a SOC Lab Steps"/>
<br />
<br />


How to use Header Analysis to determine sender's identity and assess sender's legitimacy
To view email headers in some email clients
For Thunderbird; Click view > Message Source > 

For Gmail; Click the menu icon > Click Download message to download a ".eml" file of the email OR Click Show original 







