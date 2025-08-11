# Phishing-Analysis

A brief introduction to Phishing attacks <br />

Phishing is a type of cyber attack and a form of social engineering that targets individuals through email, text messages, phone calls and other forms of communication. It is an attack that exploits the human side of cyber security rather than any kind of technical vulnerability. The common goal is to gain unauthorized access to a system, exfiltrate data or gain some sort of user credentials that can be spoofed or impersonated. <br />

Typically, these deceptive (phishing) emails or messages appearing to be from a legitimate source like an employer, bank or a trusted organization contain an attachment or malicious link when clicked would lead the user to a malicious website to trick the user into putting their credentials or download malware.
<br />
<br />

Goals of Phishing <br />
- Impersonation; poing as legitimate organizations or individuals
- Stealing sensitive information; credentials, passwords, credit card numbers, PII, senitive files
- Deliver and install malware; via attachments, embedded files, URLs etc.
- Exploit humans; human psychology, prey on motions 





Phishing Attack Types <br />


Types of Phishing <br />
- Spear Phishing: Targeted form of Phishing where an attacker tailors the message to a specific individual or organization. This requires a lot of research so an attacker can gain some form of credibility to make the attack successful.<br />
<br />

- Whaling: A type of spear phishing that targets high profile inividuals within an organization example of such indivuals are senior exeecutives, senior management because these inividuals have a higher level of authorization or access to sensitive information <br />
<br />

- Vishing: short for "voice phishing where an attacker uses phone calls or voice messages to trick individuals into revealing sensitive information. This information can include bank account details, passwords, or other personal data. Attackers often impersonate trusted organizations like banks or government agencies to gain the victim's trust. <br />
<br />

- Smishing: A phishing attack that targets individuals through SMS (Short Message Service) or text messages. The term is a combination of “SMS” and “phishing.” The attacker sends deceptive text messages to lure victims into sharing sensitive personal or financial information, clicking on malicious links, or downloading malwareware. <br />  
< br />

- Quishing: A cyberattack known as "QR code phishing" where a cybercriminal uses QR codes to trick individuals into visiting malicious websites or downloading malware onto their devices. Victim are deceived into scanning a malicious QR code which can be embedded in various forms, such as posters, emails, or even placed over legitimate QR codes, aiming to steal sensitive information like passwords, financial data, or personal details. < br />
< br />
< br />


This Phishing Analysis will be focused on Phishing emails and attachments. This will be done primarily within the Ubuntu Virtual Machine. <br />
Utilities <br />
Mozilla Thunderbird <br />
Sublime text <br />


We would require an actual email client so we can interract with email messages. <br />
We would preferrably use "Mozilla Thundrbird" which is a free and open source email client <br />
Open a terminal window > enter the command "sudo apt in stall thunderebird" <br />
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











