






## Accessing Weak Password Vulnerabilities through Penetration Testing.
ECCU MSc Research paper that was submitted. 


1.	Introduction
1.1	Rationale
2.	Literature Review
3.	Methodology
3.1	Selection of penetration testing tools
3.2	Identification of Target Systems
3.3	Planning and execution
3.4	Criteria for assessment
4.	Penetration Testing Process
4.1	Reconnaissance
4.2	Enumeration
4.3	Vulnerability scanning
4.4	Exploitation & post-exploitation
5.	Results
5.1	Sample lab scenario – (Brute forcing password of SSH user)
5.2	Comparison of password strength across different types of systems.
6.	Conclusion
7.	Reference






1	Introduction
Penetration testing, also known as ethical hacking, is the practice of simulating a malicious attack on a system or network to identify and exploit vulnerabilities. Penetration testing can help assess the security posture of an organization, improve its defences, and comply with regulatory standards.
The history of penetration testing dates to the 1960s, when the US Department of Defence (DoD) initiated security audits and evaluations of its computer systems. The DoD recognized that the best way to test the security of a system was to attempt to breach it and employed teams of experts called "tiger teams" to perform simulated attacks. The tiger teams employed various techniques, such as social engineering, physical access, and network probing, to discover and exploit weaknesses in the systems. 
In the past, the emergence of the Internet and the World Wide Web created new opportunities and challenges for penetration testing. On one hand, the Internet enabled the exchange of information and tools among the penetration testing community, and facilitated the development of standards and methodologies, such as the Open-Source Security Testing Methodology Manual (OSSTMM) and the Penetration Testing Execution Standard (PTES). On the other hand, the Internet also increased the complexity and diversity of systems and networks, and introduced new types of threats, such as web-based attacks, malware, and denial-of-service attacks. Penetration testing had to adapt to the changing landscape and adopt new tools and techniques, such as web application scanners, vulnerability scanners, and exploit frameworks.
Currently, penetration testing continues to evolve and expand, as new technologies and trends emerge, such as cloud computing, mobile devices, Internet of Things (IoT), artificial intelligence, and machine learning. These technologies pose new security challenges and require new penetration testing skills and approaches, such as cloud security testing, mobile security testing, IoT security testing, and machine learning security testing. Penetration testing also faces ethical and legal issues, such as privacy, consent, and liability, and needs to follow professional codes of conduct and best practices. Moreover, penetration testing has become more accessible and democratized, as various tools and platforms are available online, such as Hack The Box, TryHackMe, and VulnHub, which allow anyone to learn and practice penetration testing skills.













1.1	Rationale
A weak password is one that can be easily guessed or cracked by an attacker, either by using common words, simple patterns, personal information, or brute-force methods. A weak password poses a serious security risk for any system or network, as it allows unauthorized access to sensitive data and resources. According to a report by Verizon, 81% of hacking-related breaches in 2017 were due to weak or stolen passwords. Therefore, it is important to identify weak passwords as part of a penetration testing process, which aims to evaluate the security of a system or network by simulating an attack from a malicious source. By identifying weak passwords, a penetration tester can demonstrate the vulnerability of the target system or network and provide recommendations for improving password security and enforcing strong password policies.
Identifying weak passwords can also help to prevent future attacks, as it can alert the system administrators or users to change their passwords to more secure ones, and to avoid reusing the same password across multiple accounts or services. Moreover, identifying weak passwords can help to raise awareness and educate users about the best practices for creating and managing passwords, such as using a combination of upper- and lower-case letters, numbers, and symbols, and using a password manager to store and generate passwords securely.





2.	Literature review
Password security has been a significant concern in the digital age, with the increasing number of cyber-attacks and data breaches. Numerous studies have been conducted to get a grasp of the common practices, vulnerabilities, and strategies related to password security. In this literature review, we will discuss previous research on password security, common methods for password cracking, the impact of weak passwords on security, and strategies for improving password strength.
Several studies have investigated various aspects of password security. For instance, a study by Shariat et al. (2018) explored users’ password creation behaviours and found that many users still rely on weak and easily guessable passwords (Shariat, M., Al-Fuqaha, A., & Al-Mamun, M., 2018). Another study by Kang et al. (2019) analysed the effectiveness of different password policies and found that longer and complex passwords significantly improve security (Kang, J., Lee, S., & Kim, J., 2019).
Password cracking refers to the process of obtaining unauthorized access to an account by guessing or decoding a user’s password. Common methods for password cracking include brute force attacks (trying all possible combinations), dictionary attacks (using commonly used words), social engineering attacks (obtaining the password through deception), and rainbow table attacks (precomputed tables of hash values) (Chen et al., 2017).
Weak passwords pose a significant threat to information security. According to a report by Verizon Data Breach Investigations Report (DBIR) 2020, over 80% of hacking-related breaches involved using stolen or weak credentials (Verizon Enterprise Solutions, 2020). Moreover, weak passwords can lead to financial losses due to identity theft or ransomware attacks. For example, in the WannaCry ransomware attack in 2017, weak Microsoft Windows credentials were exploited to infect over 300,000 computers worldwide (BBC News, 2017).
To improve password strength and reduce vulnerabilities to cyber-attacks, several strategies have been proposed: using long and complex passwords with a combination of uppercase letters, lowercase letters, numbers, and symbols; implementing multi-factor authentication; using a reputable password manager; avoiding reusing old or easily guessable passwords; and educating users about best practices for creating strong and secure passwords (National Institute of Standards and Technology [NIST], 2017). Additionally, organizations can implement strong authentication policies such as enforcing regular password changes or implementing minimum length requirements.










3	Methodology
Penetration testing weak passwords involves reconnaissance to gather information about the target system, followed by password enumeration to identify user accounts and potential weak passwords. Password cracking techniques, such as brute force attacks and dictionary attacks, are then employed to systematically guess or generate passwords based on known patterns or character sets. Password spraying attacks and credential stuffing are utilized to test commonly used or stolen credentials against multiple accounts, while assessing the effectiveness of password policies and enforcement mechanisms. Finally, findings are documented, and actionable recommendations are provided for strengthening password security and implementing remediation efforts in collaboration with the organization's IT and security teams.

3.1	Selection of penetration testing tools
The choice of tools to assess weak passwords in a penetration test is typically determined by several factors listed below:
3.1.1	Scope and Objectives of the Test: The specific goals and scope of the penetration test influence the selection of tools. For example, if the objective is to identify weak passwords on user accounts within a Windows Active Directory environment, tools like Hydra or Mimikatz may be suitable.

3.1.2	Target Environment: The type of target environment being assessed, such as operating systems, applications, or network devices, influences the choice of tools. Different tools may be required for testing passwords on Windows, Linux, or web-based systems.

3.1.3	Testing Methodology: The methodology used for the penetration test, including reconnaissance, enumeration, password cracking, and post-exploitation techniques, informs the selection of appropriate tools at each stage of the assessment.

3.1.4	Tool Capabilities and Compatibility: The capabilities and compatibility of tools with the target environment are important considerations. Tools should be able to handle various authentication protocols, hash formats, and encryption algorithms commonly used for storing passwords.

3.1.5	Ease of Use and Automation: The usability and automation capabilities of tools play a role in their selection, especially for large-scale or repetitive password assessment tasks. User-friendly interfaces, scripting capabilities, and support for batch processing enhance efficiency and effectiveness.

3.1.6	Cost and Licensing: Considerations such as cost, licensing requirements, and availability of support may influence the choice of tools, particularly for organizations with budget constraints or specific licensing restrictions.

3.1.7	Experience and Expertise: The experience and expertise of the penetration testing team also play a crucial role in tool selection. Familiarity with certain tools, as well as proficiency in using them effectively, can significantly impact the success of the assessment.

3.2	Identification of Target Systems
Identifying a target to check for weak passwords in a penetration test involves assessing various factors to determine where weak password vulnerabilities may exist within your organization's systems and infrastructure. We will outline some steps below to help you identify a target for checking weak passwords:
3.2.1	Outline inventory of Systems and Applications: Go through the inventory of all systems, applications, and services used within your organization. This may include servers, workstations, network devices, databases, web applications, and other critical assets.
3.2.2	Prioritize High-Value Targets: Identify high-value targets that are most critical to your organization's operations and contain sensitive or confidential information. These may include servers hosting financial data, customer databases, administrative consoles, or privileged accounts.
3.2.3	Assess Authentication Mechanisms: Evaluate the authentication mechanisms used by each target system or application. Look for systems that rely solely on password-based authentication without additional layers of security, such as multi-factor authentication (MFA) or strong password policies.
3.2.4	Review Password Policies: Review the password policies implemented across your organization to determine if they align with industry best practices and security standards. Look for weaknesses in password complexity requirements, password expiration periods, and password reuse restrictions.

3.2.5	Evaluate User Account Management: Assess how user accounts are managed within your organization, including account provisioning, deprovisioning, and password management processes. Identify areas where weak passwords may be more prevalent, such as default passwords or shared accounts.

3.2.6	Check Historical Data: Review historical security incidents, audit findings, or password breach reports to identify systems or applications that have previously been compromised due to weak passwords. Prioritize these targets for closer scrutiny during the penetration test.

3.2.7	Test-run Password Cracking Exercises: Use automated password cracking tools, such as John the Ripper, Hashcat, or Hydra, to perform password cracking exercises against target systems. Focus on systems that are accessible to attackers and have a high likelihood of containing weak passwords.

3.2.8	Engage Red Team Tactics: Employ red team tactics, such as social engineering or phishing simulations, to gather intelligence about user passwords or password-related vulnerabilities. Use the information obtained to identify targets where weak passwords may be exploited.

3.2.9	Collaboration with IT and Security Teams: Work closely with IT and security teams to gather insights into the organization's password management practices, user behaviour, and system configurations. Leverage their expertise to identify potential targets and prioritize them for testing.

3.2.10	Document Findings and Recommendations: Document your findings and recommendations for addressing weak password vulnerabilities identified during the penetration test. Provide actionable insights to help remediate weaknesses and improve password security across the organization.

3.3	Planning and execution
3.3.1	Planning
3.3.1.1	Scope Definition: Determine the scope of the penetration test by identifying the systems, applications, and user accounts to be assessed for weak passwords. This information can be obtained from the client or through reconnaissance techniques.
3.3.1.2	Tools Selection: Choose appropriate tools for password cracking and analysis based on the target systems and password complexity. Some popular tools include John the Ripper, Hashcat, Aircrack-ng, and Hydra. Ensure that these tools are legally allowed to be used within your organization’s policies and comply with relevant laws and regulations.
3.3.1.3	Legal and Ethical Considerations: Obtain proper authorization from the organization to perform a penetration test and ensure that all activities are conducted ethically and legally. This may involve obtaining written consent from users whose accounts will be tested or implementing measures to protect their privacy.
3.3.1.4	Risk Assessment: Evaluate the potential impact of discovering weak passwords on the target systems and prioritize them based on their sensitivity and potential damage if compromised. This information can help guide your testing efforts and focus on high-value targets first.
3.3.1.5	Documentation: Create a detailed report outlining the objectives, scope, methodology, expected outcomes, risks, assumptions, constraints, dependencies, schedule, budget, resources required, stakeholders involved, communication plan, risk mitigation strategies, contingency plans, exit strategy, and any other relevant information related to your penetration test for weak password assessment.
3.3.2	Execution:
3.3.2.1	Information Gathering: Use various techniques such as social
engineering or reconnaissance to collect usernames or email addresses associated with target accounts or systems that may have weak passwords. Also use tools
like Nmap or Netstat to identify open ports and services running on target systems
that might contain vulnerable login pages or credentials stored in plaintext files
(e.g., /etc/passwd).
3.3.2.2	Password Enumeration: Use specialized tools like CrackMapExec or Metasploit to enumerate usernames and hashed passwords from various sources such as SMB shares (Samba), FTP servers (FileZilla), SQL databases (MySQL), or even memory dumps (Volatility). These tools can also help you determine which hashing algorithms were used to store these passwords so you can choose appropriate cracking methods accordingly (e.g., MD5 vs SHA-256).

3.3.2.3	Password Cracking: Use powerful GPUs or specialized hardware like ASIC miners to crack hashed passwords using brute force attacks or dictionary attacks with wordlists containing common words or phrases found in real-world dictionaries (either offline or online). You can also use rainbow tables if available for specific hash types to speed up the process significantly by precomputing hash values for common words in advance instead of generating them during runtime (which would take much longer). Additionally consider using hybrid attacks combining both dictionary words along with numbers/symbols combinations for more complex passwords if needed. Note: Be aware that cracking large numbers of hashes requires significant computational power; therefore it is essential to consider resource limitations before embarking on this task

3.4	Criteria for assessment
When assessing weak passwords in a penetration test, it is critical to consider various criteria to identify vulnerabilities effectively and some are outlined below:
3.4.1	Password Length: Evaluate the length of passwords to determine if they meet minimum length requirements. Longer passwords are generally more resistant to brute-force attacks.
3.4.2	Complexity: Assess the complexity of passwords by analysing the presence of different character types, such as uppercase letters, lowercase letters, numbers, and special characters. Strong passwords should include a combination of these character types.
3.4.3	Dictionary Words: Check if passwords contain dictionary words or commonly used phrases that are susceptible to dictionary-based attacks. Avoid using easily guessable words or patterns.
3.4.4	Common Patterns: Look for common patterns or sequences in passwords, such as "123456," "password," or "qwerty." These patterns are often used by individuals to create weak passwords.
3.4.5	Repetitive Characters: Identify passwords that consist of repetitive characters or sequences, such as "aaaaaa" or "123123." These passwords are easy to guess and vulnerable to brute-force attacks.
3.4.6	Default Passwords: Check for default passwords that have not been changed from their default settings. Default passwords are widely known and pose a significant security risk if left unchanged.
3.4.7	Personal Information: Evaluate passwords for the inclusion of personal information, such as names, birthdates, addresses, or phone numbers. Avoid using easily guessable information that can be obtained from social media profiles or public records.
3.4.8	Password Hashes: Analyze password hashes stored in the system or application to identify weak hashing algorithms or inadequate salt usage. Weak hashing algorithms make it easier for attackers to crack passwords using hash cracking techniques.
3.4.9	Password Policy Compliance: Assess whether passwords comply with the organization's password policy regarding length, complexity, expiration, and reuse. Non-compliant passwords may indicate weaknesses in password management practices.
3.4.10	Password Strength Tools: Utilize password strength assessment tools or libraries to automatically evaluate the strength of passwords based on established criteria. These tools can help identify weak passwords more efficiently.
3.4.11	Previous Breaches: Consider passwords that have been exposed in previous data breaches or security incidents. Check if users are using compromised passwords or if password reuse is prevalent within the organization.
3.4.12	User Behaviour: Analyze user behavior and password management practices to identify patterns of weak password creation or reuse. Educate users on best practices for creating strong passwords and encourage them to use password managers.










4	Penetration testing process.
4.4	Reconnaissance
Firstly, network scanning tools like Nmap are employed to identify active hosts and open ports within the target environment. This provides an initial understanding of the network topology and potential entry points for password assessment. Following this, enumeration tools such as Enum4linux are utilized to gather information about user accounts, including usernames, email addresses, and account types. This step helps in building a comprehensive list of potential targets for password cracking and assessment.

Secondly, authentication mechanisms used within the target environment are identified and analyzed. This includes determining whether the environment utilizes protocols such as Active Directory, LDAP, SSH keys, or web-based authentication. Information about password policies, complexity requirements, and account lockout thresholds is gathered to tailor password assessment techniques accordingly. Additionally, web application reconnaissance is performed to identify login pages, registration forms, and other authentication mechanisms within web applications. Web vulnerability scanners like OWASP ZAP or Burp Suite are employed to crawl web applications and identify potential areas for password assessment.

Lastly, social engineering techniques are employed to gather information about employees, job roles, and organizational structure. This may involve phishing emails or pretexting to extract valuable information that can be used to craft targeted password assessment campaigns. Additionally, publicly available information about the target organization, such as company websites, social media profiles, or public forums, is reviewed to identify clues about potential weak passwords. Furthermore, previous security breaches or data leaks involving the target organization are analyzed to identify leaked credentials or password hashes. By gathering this comprehensive information, penetration testers can effectively identify potential weak passwords and assess password security controls during the penetration test.

4.5	Enumeration
Performing enumeration for assessing weak passwords in a penetration test involves a systematic approach to gather information about user accounts, authentication mechanisms, and password policies. Firstly, identify the target systems and applications to be assessed, including user accounts on servers, databases, web applications, and network services. Next, enumerate user accounts and groups using tools like enum4linux or LDAP queries, and discover active hosts and open ports on the network to identify potential targets for password assessment. Once the targets are identified, analyze the services and protocols running on these systems to understand the authentication mechanisms in use.

Secondly, utilize a combination of brute-force and dictionary-based password cracking techniques to guess passwords and assess their strength. Perform brute-force attacks against services like Telnet, FTP, or SSH using tools such as Hydra or Medusa. Additionally, conduct dictionary attacks using custom wordlists or publicly available dictionaries to guess passwords based on common words, phrases, or patterns. Simulate social engineering attacks, such as phishing or pretexting, to gather information about user passwords or password-related security practices.

Lastly, analyze the results of enumeration and password cracking attempts to identify weak passwords, default passwords, or passwords that do not comply with password policies. 




4.6	Vulnerability scanning
Firstly, selecting the right tools is crucial, such as Nessus, OpenVAS, or Nexpose, which offer password auditing capabilities. These tools are instrumental in identifying vulnerabilities related to password security within the target environment. Secondly, customization of scan policies is essential to focus specifically on password-related vulnerabilities. This involves configuring the scan to check for weak password policies, default credentials, and common password patterns. By tailoring the scan policies, testers can effectively target areas where weak passwords may be exploited.

Once the scanning process is initiated, authenticated scans are performed using valid credentials for user accounts with varying levels of privilege. This allows testers to assess password security controls on different systems accurately. After analyzing the scan results, vulnerabilities related to weak passwords are identified, including weak password policies, default credentials, password reuse, and easily guessable passwords. Testers prioritize these vulnerabilities based on severity and potential impact, focusing on high-risk findings first to address immediate security concerns.

Lastly, actionable recommendations are provided based on the identified vulnerabilities. These recommendations may include implementing stronger password policies, enforcing password complexity requirements, and conducting user awareness training on password best practices. Regular vulnerability scans are encouraged to continuously assess password security controls and identify newly introduced vulnerabilities. By incorporating vulnerability scanning for weak passwords as part of routine security assessments, organizations can maintain a strong security posture and mitigate the risk of unauthorized access due to weak passwords.

4.7	Exploitation and post-exploitation
Exploiting weak passwords involves several key steps to gain unauthorized access and assess overall security vulnerabilities. Initially, thorough enumeration and target identification are crucial, focusing on identifying the target system or network segment and conducting reconnaissance to gather pertinent information about user accounts, domain names, and network services. Employing tools like Nmap, enum4linux, or LDAP queries aids in enumerating users, groups, and network shares, laying the groundwork for subsequent exploitation.

Password cracking serves as a pivotal phase, where tools such as Hydra, Medusa, or John the Ripper are utilized to crack weak or default passwords. Password dictionaries, crafted based on common passwords, wordlists, or patterns, facilitate this process. The objective is to successfully crack passwords offline using captured password hashes or online against login prompts, allowing for credential harvesting and subsequent authentication attempts. With compromised credentials at hand, penetration testers proceed to authenticate into the target Windows system, attempting to access it through remote login methods like RDP, SSH, or WinRM.

Subsequent stages encompass privilege escalation, lateral movement, and persistence establishment, facilitating deeper access within the network and ensuring prolonged control over the compromised system. Post-exploitation activities entail gathering additional insights into the target environment, including sensitive data exploration and analysis of system configurations. Throughout the exercise, meticulous documentation and reporting are paramount, detailing weak passwords identified, successful exploitation attempts, and comprehensive recommendations for remediation. It is imperative to conduct all activities ethically, with explicit permission and adherence to legal and ethical guidelines, prioritizing the security and privacy of the target organization's data and systems at every step.











5	Results
5.1	Sample lab Scenario – Brute forcing password of SSH user on Debian target
Step 1: Open both machines Parrot(client & Target) and Metasploitable, then confirm IP addresses of both nodes using the command:
$ ifconfig
Step 2: Perform an NMAP scan to get the list of open ports on the target machine, using the command shown below
$ nmap -sS -sV 192.168.10.3 (the IP address of the target machine)

Step 3: On confirming port 22/tcp that is running SSH service with version Openssh 4.7, open the MSF Console in the terminal by typing the below command:
msfconsole
 
Now we are going to search for ssh_login Auxiliaries by using the Search command in msfconsole as you can see in the image below. 
search ssh
 

Input the auxiliary/scanner/ssh/ssh_login from the results, to use this module:
msf6 > use auxiliary/scanner/ssh/ssh_login
Check for options available to set our target, using the command below.
msf6 > (auxiliary/scanner/ssh/ssh_login) > show options 
 
Step 4: Set the required options and launch the attack.
set RHOST 192.168.10.3
set THREADS 3
set STOP_ON_SUCCESS true
set VERBOSE true
 
 
After these options are set now we are going to use a PASSWORD list as the program doesn’t have one. So, to show you the attack successful I have created a password list that contains usernames and passwords, separated by space as it says in the image above for USERPASS_FILE.
Now set the password list with the command set, as shown in the image below:
set USERPASS_FILE <path to the password list>
 
 
Step 5: We are all set to go and now we can launch the attack and watch each attempt on the terminal, to launch the attack use run the command. After typing the run command it will start brute forcing into the system and when the attack is successful it will return the password and username. as you can see in the image below the default password for Metasploitable 2 is msfadmin and username also msfadmin and it had been successful.
 
 
5.2	Comparison of password strength across different systems
Password strength requirements and implementations vary across different systems, including desktops, servers, and mobile operating systems, reflecting the unique security considerations and usage patterns of each platform. Desktop operating systems, such as Windows and macOS, often enforce robust password policies to protect user accounts and sensitive data. For example, Windows systems typically require passwords to meet complexity criteria, including minimum length, character diversity, and expiration periods. Users may be prompted to create strong passwords containing a mix of uppercase and lowercase letters, numbers, and special characters. Similarly, macOS incorporates features like password strength meters to guide users in creating secure passwords, emphasizing the importance of strong authentication to safeguard personal and business data.

In contrast, server operating systems prioritize password security to protect critical infrastructure and network resources from unauthorized access. Servers commonly employ stringent password policies tailored to organizational requirements, often enforced through group policy settings or configuration directives. For instance, Linux servers may utilize tools like Pluggable Authentication Modules (PAM) to enforce password complexity rules, including minimum length and character diversity. Additionally, server administrators may implement multi-factor authentication (MFA) or password rotation policies to mitigate the risk of credential compromise and unauthorized access to sensitive systems and data.

Mobile operating systems, such as iOS and Android, face unique challenges in balancing security with usability due to the prevalence of mobile devices in everyday life. Password strength requirements on mobile platforms aim to strike a balance between security and user convenience, considering factors like device form factor, touch screen input, and user behaviour. For example, iOS devices offer biometric authentication options like Touch ID and Face ID, reducing reliance on traditional passwords for device access. Android devices may enforce password complexity requirements, similar to desktop and server systems, but may also incorporate features like Smart Lock to streamline authentication based on user context and device proximity. Overall, password strength implementations on mobile operating systems prioritize usability while ensuring adequate protection against unauthorized access to personal and sensitive data stored on mobile devices.







Conclusion
The assessment of weak password vulnerabilities within a penetration test is a critical aspect of ensuring the overall security posture of an organization's systems and networks. By systematically identifying and exploiting weak passwords, penetration testers can uncover potential entry points for attackers and highlight areas in need of strengthening. Using enumeration, password cracking techniques, and exploitation, weaknesses in password policies, user behaviors, and system configurations can be revealed, enabling organizations to implement targeted remediation measures and enhance their resilience against unauthorized access. Moving forward, continuous evaluation and improvement of password security practices, coupled with robust authentication mechanisms and user education, are essential components of a proactive defense strategy to mitigate the risks associated with weak passwords and safeguard sensitive information from malicious actors.

References
Weidman, G. (2014). Penetration testing: A Hands-On Introduction to Hacking. No Starch Press.

Kim, P. (2018). The Hacker Playbook 3: Practical Guide to Penetration Testing. Secure Planet LLC

GeeksforGeeks. (2024, April 17). Brute Force Attack in Metasploit. https://www.geeksforgeeks.org/brute-force-attack-in-metasploit/

Allsopp, W. (2017). Advanced Penetration Testing: Hacking the World’s Most Secure Networks. Wiley





