# Performing the Audit

Below is the audit checklist template. Finish each section until completion. Some options and categories may not be applicable so use what makes the most sense for your organization. This is not an exhaustive list, use your common sense on what to add yourself.

> [!IMPORTANT]
> It's important to note that audits begin as an investigative and documentary process. You'll be collecting lots of information and learnign about the current state of security long before any discussions of how to improve them. After the first audit of your organization, subsequent audits will be simpler as the process will have already been established and practiced.

<br>

# 1. Assess assets

<br>

## 1.1 Assets of value

Cooperate with relevant leadership in your organization to assess what information and assets are important to protect. This could include digital access to bank accounts, cryptocurrency wallets, codebases of product software, HR records, storage of files including private organizational and operational documents, etc.  

You'll want to use a spreadsheet to enter each category discovered. Here is an example template to use:

<br>

<table>
  <tr>
    <th>Asset</th>
    <th>URL(s)</th>
    <th>Risk if compromised</th>
    <th>Severity</th>
    <th>2FA</th>
    <th>SSO</th>
    <th>Admins</th>
    <th>Primary users</th>
  </tr>

  <tr>
    <td>Google Workspace<br><sub><i>(Or any other collaboration and storage tools)</i></sub></td>
    <td>*.google.com</td>
    <td>Access, copy, and destroy all organizational documents</td>
    <th>VERY HIGH</td>
    <td>Enforced</td>
    <td>Not used</td>
    <td>CTO, Alice</td>
    <td>*</td>
  </tr>

  <tr>
    <td>Github<br><sub><i>(Or any other code repositories)</i></sub></th>
    <td>github.com/organization_name</td>
    <td>
      <ul>
        <li>Github actions</li>
        <li>control CI bot and access associated hosted instance</li>
        <li>steal private code in private repos</li>
      </ul>
    </td>
    <td>HIGH</td>
    <td>Enforced</td>
    <td>Not used</td>
    <td>Alice</td>
    <td>Alice, Bob, Charlie </td>
  </tr>

  <tr>
    <td>Bitwarden<br><sub><i>(Or any other password management tool)</i></sub></th>
    <td>bitwarden.com</td>
    <td>Access to all shared passwords</td>
    <td>HIGH</td>
    <td>Not used</td>
    <td>Not used</td>
    <td>Bob</td>
    <td>*</td>
  </tr>

  <tr>
    <td>Mattermost<br><sub><i>(Or any other internal communications service)</i></sub></th>
    <td>mattermost.com/organization</td>
    <td>
      <ul>
        <li>Impersonation</li>
        <li>Elevated phishing</li>
      </ul>
    </td>
    <td>HIGH</td>
    <td>Not used</td>
    <td>Not used</td>
    <td>Alice</td>
    <td>*</td>
  </tr>

  
  <tr>
    <td>Intuit<br><sub><i>(Or any other payroll and payment service)</i></sub></th>
    <td>Intuit.com</td>
    <td>
      <ul>
        <li>Theft of funds</li>
        <li>Leak of contractor details</li>
      </ul>
    </td>
    <td>HIGH</td>
    <td>Not used</td>
    <td>Not used</td>
    <td>Bob</td>
    <td>*</td>
  </tr>

  
</table>

<br>

> [!NOTE]
> You'll need to either work with existing leadership / administrators and/or submit an organization-wide questionnaire to discover the assets and access levels to those assets for each individual in the organization. This is covered in the next step.

<br>

## 1.2 Asset access / questionnaire

<p>In order to effectively catalogue what access is given and discover discrepencies you should submit a questionnaire organization-wide. It's recommended this be done by those in leadership that are already trusted to avoid misunderstandings and distrust.</p>

<p>Your questionnaire will want to address what software, products, services, platforms, storage, servers, providers, etc are used by different teams inside the organization and what access is provided to them at what levels.</p>

<p>You can also use your questionnaire to poll individuals in the organization on their habits and current security state. An example template is provided below. You may want to add or remove sections depending on your needs.</p>

<br>

> #### Employee Security Inventory
> 
> This questionnaire is intended to collect information on the current state of access to resources inside the organization to suggest potential improvements and options that keep everyone safe. Feel free to answer honestly and do not hesitate to ask for help if you are having trouble answering a question.
>
> <i>* Indicates required question</i>
>

> 
> 1. What OS do you primarily use on your main device for work? *
>
> - [ ] Linux
> - [ ] macOS
> - [ ] Windows
> - [ ] Other: _______

<br>

> 2. Are you running the latest version of your OS available through the relevant update services? *
> - [ ] Yes
> - [ ] No

<br>

> 3. Are your accounts secured with a strong password *
> - at least 8 characters
> - contains uppercase
> - contains lowercase
> - contains digits
> - contains symbols
> - [ ] Yes
> - [ ] No

<br>

> 4. Do you use Disk Encryption (OS or 3rd party software)? *
> - [ ] Yes
> - [ ] No

<br>

> 5. Do you use a Password Manager? *
> - [ ] Yes
> - [ ] No

<br> 

> 6. Do you use at least one weak password (less than 8 characters or easy to remember)? *
> - [ ] Yes
> - [ ] No

<br> 

> 7. Do you use a Firewall? *
> If you're unsure if you use a firewall or not, check your device (note: Mac OS has a built in firewall, iPhones do not) or ask for assistance with this question. 
> - [ ] Yes
> - [ ] No

<br> 

> 8. Do you have a backup of your files? *
> Note: Google Drive Sync would not be considered a proper backup as it syncs malicious changes and deletions as well. 
> - [ ] Yes
> - [ ] No

<br> 

> 9. If you have a backup drive, is your drive encrypted?
> - [ ] Yes
> - [ ] No

<br> 

> 10. Do you use a provided organizational account on your personal or work smartphone? *
> <i>(e.g. Gmail, Slack, Github)</i>
> - [ ] Yes
> - [ ] No

<br> 

> ##### Smartphone Inventory

<br> 

> 11. Do you use difficult or 6+ digit codes to lock your smartphone? *
> - [ ] Yes
> - [ ] No

<br> 

> 12. Do you use a pattern to unlock your smartphone? *
> - [ ] Yes
> - [ ] No

<br> 

> 13. Select the list of accounts used on your smartphone *
> - [ ] Mail
> - [ ] Calendar
> - [ ] Slack
> - [ ] Intuit
> - [ ] Github
> - [ ] Bitwarden
> - [ ] Discord
> - [ ] Notion
> - [ ] Trello
> - [ ] Jira
> - [ ] Youtube
> - [ ] AWS
> - [ ] Zoom
> - [ ] Other:

<br> 

> ##### Services Inventory

<br> 

> 14. Check all services you have organizational account access for: *
> <i>Accounts include official accounts created with an organizational email address, and also any personal accounts that have access to organizational resources (e.g. Github, reddit, etc).</i>
> - [ ] Mail
> - [ ] Calendar
> - [ ] Slack
> - [ ] Intuit
> - [ ] Github
> - [ ] Bitwarden
> - [ ] Discord
> - [ ] Notion
> - [ ] Trello
> - [ ] Jira
> - [ ] Youtube
> - [ ] AWS
> - [ ] Zoom
> - [ ] Other:

<br>

> 15. Check all services you have admin access to: *
> - [ ] None
> - [ ] Mail
> - [ ] Calendar
> - [ ] Slack
> - [ ] Intuit
> - [ ] Github
> - [ ] Bitwarden
> - [ ] Discord
> - [ ] Notion
> - [ ] Trello
> - [ ] Jira
> - [ ] Youtube
> - [ ] AWS
> - [ ] Zoom
> - [ ] Other:

<br>

> 16. Any suggestion on how we could improve security at our organization?
> 
> ┌──────────────────────────────────────────────────┐<br>
> │&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
> └──────────────────────────────────────────────────┘<br>


<br>

> 17. Would you be interested in attending short bi-yearly <i>(twice a year)</i> educational sessions for improving your security and keeping up to date on the latest threats? *
> - [ ] Yes
> - [ ] No

<br>

# 2. Identify potential threats

<br>

# 3. Evaluate current security

Based on the responses to your initial assessment and questionnaire you should now have enough information to evaluate your current security.

Common issues that present themselves include:

* Indidivuals having the wrong permissions or access to resources they don't need to have
* Security habits that make it easy to hack the organization <i>(e.g. not using password managers, using personal devices and installing malware alongside organizational applications)</i>
* Organizational members who travel a lot having no encrytion on their devices and drives they bring with them on trips
* Not using 2FA on critical services
* Not using secure passwords
* Not updating an OS, browser, or application regularly when security patches are available
* False sense of security <i>(e.g. thinking a pattern lock is safe, thinking a password manager isn't necessary because "my password is both my name and birthdate together!")</i>

Depending on the services and systems used, complexity of operations of your organization, and on the severity of the risks, issues you need to resolve in your organization can vary. Consult relevant leadership in your organization for additional issues you may have missed. If you don't work in payroll, you may not understand the intracacies and vulnerabilities of the payroll system so it would make sense to consult with the individual handling accounting.

> [!IMPORTANT]
> It's critical to think of the auditing process as educational for you as an auditor as well. Don't hesitate to ask for feedback from others and to make changes to your process and questionnaire whenever you find an issue, something that needs clarifying, or to make changes to assets, threats, risks, etc at any time. When it comes to security, it's better to be late than to become a victim.

<br>

# 4. Assign risk scores

<br>

# 5. Build a plan

<br>

## 5.1 Plan checklist

<br>

Now that you have a good idea of what assets need protecting, who and what the weak links are, and the likelihood of anything bad coming from it, you can make your own plan of what needs to be changed, removed, and otherwise secured.

Below is an example plan constructed as a to-do list you can use for your audit that includes common actionables for securing your organization.

> [!NOTE]
> This is not an exhaustive list. Your needs will depend on results of previous steps. Discuss with the relevant organizational leadership on what actions will be most relevant for your organization and <b>the rammifications of each action</b> <i>(e.g. costs, liabilities, setbacks)</i>, and what support you will need <i>(e.g. 2FA, removing admins, etc)</i>.

<br>

> **General:**
> 
> - [ ] Set up an email address for security matters (example: security@.). Forward it to the developers' group.
> - [ ] Regularly check for vulnerabilities in organization systems
> - [ ] Create security rules for systems and access and keep them documented in a specific digital place> 

<br>

> **Incident Response Plan:**
> 
> - [ ] Be ready for a ransomware attack <i>(form a team, have emergency contacts, have a plan based on backups that can be restored, think about insurance, worst case decide how much money you'd pay for ransom if needed, etc)<i>.
> - [ ] Make a plan that explains what to do if there are breaches and leaks, like who does what and how to report and respond to issues.

<br>

> **Pentesting:**
> 
> - [ ] Begin a program where people can find and report bugs (like Hacker One or Bugcrowd).
> - [ ] Use a tool from another company to help with testing (like Cobalt or Securisea).

<br>

> **Intrusion Detection:**
> 
> - [ ] Keep an eye on the dark web for signs of a data breach (for example, using PhishLabs).
> - [ ] Use software to watch for any unusual activity on computers (like OSSEC, Wuzah, Tripwire, or rkhunter).
> - [ ] Also, use software to look for strange things happening on the network (like Suricata, Snort, or Bro).

<br>

> **Risk and Vulnerability Management:**
> 
> - [ ] Do a big review of the risks inside the company and do it again every year.
> - [ ] Regularly check for weaknesses and fix them.

<br>

> **Configuring for Least Functionality:**
> 
> - [ ] Adjust the rules for the firewall.
> - [ ] Shut down things that aren't needed and block things that shouldn't be used.
> - [ ] Separate different functions, like admin work and APIs.

<br>

> **Personnel:**
> 
> - [ ] When people start working at the organization (including contractors), check their background.
> - [ ] Make sure they get the right permissions to access things and keep track of this.
> - [ ] Get them to sign agreements to keep information safe if needed.

<br>

> **Device Security:**
> 
> - [ ] Make sure all devices, like laptops and hard drives, have a lock on them and drives/storage are encrypted.
> - [ ] Stop backups to personal online storage.
> - [ ] Think about giving employees special phones for work, which you can control remotely.
> - [ ] Stop people from installing apps or software on their devices.
> - [ ] Make sure you can check that devices are secure.

<br>

> **Software Security:**
> 
> - [ ] List all the security software used (like firewalls and antivirus).
> - [ ] Think about using software that stops data from leaking out.
> - [ ] Make sure everyone has to use two or more ways to log in for outside services (like Slack or GitHub).
> - [ ] Make sure all the important settings for admins are on.
> - [ ] Get a password manager for passwords.
> - [ ] Keep all the software up to date and use a tool to help with this.
> - [ ] For domain names, make sure they stay active and keep them safe.

<br>

> **Application Security:**
> 
> - [ ] Check the website to see if it's secure (using something like Mozilla Observatory).
> - [ ] Make sure no private information is written in the software.
> - [ ] Check to see if any of the software components have known vulnerabilities.
> - [ ] Inspectsoftware without running it to find issues.
> - [ ] Keep passwords safe.
> - [ ] Slow down any repeated attempts to log in.
> - [ ] Tell users when their email or password changes.
> - [ ] Keep track of login attempts and protect against someone taking over accounts.

<br>

> **Email Security:**
> 
> - [ ] Make sure the system that sends emails follows the rules.
> - [ ] Make sure emails sent from the organization have a special signature and rules.
> - [ ] Check if incoming emails follow those rules too.
> - [ ] For email addresses that aren't used anymore, remove them.

<br>

> **Data Storage & Processing Security:**
> 
> - [ ] Make a list to turn off all accounts when employees leave (or make it happen automatically).
> - [ ] Make sure data sent between computers is kept secret.

<br>

> **Data Storage:**
> 
> - [ ] Make a list of personal data and where it's kept.
> - [ ] Make sure data is secret when it's saved.
> - [ ] Keep data safe when it's used.
> - [ ] Use encryption.

<br>

> **Data Access and Processing:**
> 
> - [ ] Keep data secret when it's sent between computers.
> - [ ] Make sure people have strong passwords.
> - [ ] Use different roles for different jobs.
> - [ ] Keep an eye on how data is used.
> - [ ] Check to see if data is getting out in places it shouldn't.

<br>

> **End-user Security:**

<br>

> **User Management:**
> 
> - [ ] Every three months, check who has special permissions on the computer systems.
> - [ ] Also, check who is using the computer systems.
> - [ ] Remove accounts that aren't used anymore.

<br>

> **Internal Threats:**
> 
> - [ ] Keep a record of what employees do on the computer.
> - [ ] Make sure not too many people have special permissions on systems.

<br>

> **Physical and Environmental Security:**
> 
> - [ ] Lock rooms with computers and make sure only authorized people can get in.
> - [ ] Keep an eye on who goes into these rooms with a book or camera.
> - [ ] Decide who gets to use the computer systems and check this often.
> - [ ] Keep track of who has keys and badges and remove access when someone leaves.
> - [ ] Don't let people plug in strange devices.
> - [ ] Watch the temperature and humidity and set limits for warnings.
> - [ ] Look for water that shouldn't be there.
> - [ ] Have extra power, lights, and ways to stop fires in case of problems.
> - [ ] Plan for big problems like earthquakes and floods.

<br>

## 5.2 Supplemental checklists

Additional (application / service / situation specific) checklists to consider:

* Github security checklist (https://github.com/kristovatlas/github-security-checklist) - A list of important security checks for GitHub individual and organization accounts.
* Devops security checklist (https://github.com/vikrum/SecurityChecklists/blob/main/devops-security-checklist.md)
* Organization member security checklist (https://github.com/vikrum/SecurityChecklists/blob/main/personal-infosec-security-checklist.md)
* SaaS CTO checklist (https://github.com/vikrum/SecurityChecklists/blob/main/saas-cto-security-checklist.md)


  


