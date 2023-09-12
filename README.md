# Internal Organizational Security Audit Guide

This guide will help you from step one to completion of an internal organizational security audit. This guide is written to be friendly towards those with little to no background in security and audits so that you can share it with your CEO, manager, or others inside your organizational easily. 

> [!NOTE]
> If you already understand the importance and process of an internal organizational security audit, skip to <a href="#get-started">get started</a>. 

<br>

## Is an organizational audit important?

<p>An internal organizational security audit is akin to a regular checkup; it's crucial for every organization <i>(especially technology focused ones)</i> to do because it helps ensure that your software, network, systems, sensitive data, and customer information are safe from bad actors and mistakes. By doing these checkups, you find and fix any weak spots or potential entry points that could be used to exploit and cause havoc.</p>

<p>This not only protects your organization's reputation but also ensures that your customers can trust your software and services to keep their information secure and keep providing services reliably. If you're doing an audit audit on your code but haven't done an internal organizational security audit, it's like installing a lock on your door but giving everyone the key.</p>


> [!IMPORTANT]
> Each and every audit should help further the goal of building a strong culture of security across your organization.

<br>

## The process

An internal organizational security audit consists of a few steps that should be done in order:

1. <a href="#assess-assets">Assess assets</a>
2. <a href="#identify-potential-threats">Identify potential threats</a>
3. <a href="#evaluate-current-security">Evaluate current security</a>
4. <a href="#assign-risk-scores">Assign risk scores</a>
5. <a href="#build-a-plan">Build a plan</a>

> [!NOTE]
> Don't worry about remembering every detail of every step. After learning about the process itself, you'll be directed to the step-by-step guide that will help you keep track and follow clear actionables.

<br>

## 1. Assess assets

Determine what the audit will cover by making a list of all the important things to check. For instance:

- Computers, devices, and other equipment
- Sensitive organizational and customer data
- Important internal records and documents
- Access to services used by the organizational (payroll, social media, continuous integration of software, etc)

> [!NOTE]
> It’s unlikely to be able to audit all assets. The final part of this step is determining which assets to audit, and which not to.

<br>

## 2. Identify potential threats

> [!NOTE]
> What counts as a threat? Any activity, occasion, behavior, or thing that can cost your business its reputation, a significant amount of money, or rob your users of their freedom and security.

Some example threats that might apply to your organizational are:

- How careful employees are <i>(e.g. diligence)</i>
- Physical break-ins or natural disasters <i>(e.g. breach, force majeure)</i>
- Using your own devices for work <i>(e.g. BYOD)</i>
- Trickery emails to steal information <i>(e.g. phishing)</i>
- Employees with bad intentions <i>(e.g. insiders)</i>
- Harmful software <i>(e.g. malware, ransomware)</i>
- Not-so-great password practices <i>(e.g. password hygiene, habits)</i>
- Online attacks <i>(e.g. DDoS, service zero days)</i>
- Supply chain attack <i>(e.g. access to CI, backdoored dependencies, service zero days)</i>

<br>

## 3. Evaluate current security

> [!NOTE]
> “You can't improve what you don't measure.”<br><sub>-Peter Drucker</sub>

<p>Now that you know what threats might exist, it's time to be honest about your ability to defend against them. It's important to assess the organization and departments honestly, not trying to hide deficiencies.</p>

<p>Everyone in your organization will have different strengths and weaknesses. Some teams may be good at monitoring network and detecting threats but haven’t updated their training in a while. Others may be good at network security but too trusting about internal requests for actions including financial requests they believe are from a trusted individual. Other teams may not be technically minded for security and easily phished.</p>

<p>When conducting an assessment, it can be helpful to let individuals know this and to not worry too much about what their weaknesses might be, as you're just there to help provide education, training, and build a stronger culture of security in the organization.</p>

> [!IMPORTANT]
> When assessing the security of others in your organization and team, depending on technical literacy and understanding of the importance of security, it may be tempting for them to be dismissive, defensive, or fluff their responses to seem less severe <i>(e.g. "I'm fine, don't worry about me")</i>. It's important to incentivize them to be honest so that your software and organizational can be safer for everyone.

<br>

## 4. Assign risk scores

To keep things simple and prioritized, we assign scores based on how potentially harmful they are. For that you can use a simple formula that considers three  factors, and for each factor, you assign a score from 1 to 10. Have relevant individuals in the organization weight the scores accordingly.


<table>
  <tr>
    <th>Potential damage</th>
    <th>+</th>
    <th>Likelihood</th>
    <th>+</th>
    <th>Ability to mitigate</th>
    <th>/3=</th>
    <th>Risk score</th>
  </tr>
  <tr>
    <td colspan=7>
      Example risk score: Supply chain compromised via malicious dependency 
    </td>
  </tr>
  <tr>
    <td>The open source libraries we depend on get backdoored or malware inserted</td>
    <td></td>
    <td>We check all dependencies before merging PRs and update them with ever security alert from github's dependabot</td>
    <td></td>
    <td>We don't currently have a plan in place to contact users or quickly update the affected pre-compiled versions of the software</td>
    <td></td>
    <td>Risk score</td>
  </tr>
    <tr>
    <td>10</td>
    <td>+</td>
    <td>3</td>
    <td>+</td>
    <td>8</td>
    <td>/3=</td>
    <td>7</td>
  </tr>

</table>


#### Other example factors you may want to consider:

- What are the most common hacks and tricks hackers use today?
- What kinds of security issues do other organizations in the same industry commonly face?
- Are there rules or laws about the data we deal with? Do we handle important financial or personal info? Who can get into our systems?
- How does political climate affect our safety and access? Think about things like power outages during protests or government actions that might impact our servers and access.

<br>

> [!NOTE]
> This is not an exhaustive list. Factors may differ depending on the industry, complexity, reputation, and experience of your organization and its participants. Brainstorm with trusted others in and outside your organization on what other factors you may need to consider.

<br>

## 5. Build a plan

For every threat assessed, let's decide what should be done about it. If it's possible to completely eliminate it, that should be the goal. Otherwise, work on reducing its impact and making it less harmful.

Here are some typical ways to do that:

#### Supply chain attacks / dependency risks

Developers often use extra pieces of code, called dependencies, to make developing software easier and faster. While this is often critical for modern development, this can also introduce vulnerabilities in the software you're developing. Developers should be careful both when adding new code or introducing older code. They should also check new code changes carefully. You can learn more about <a href="https://github.com/readme/guides/dependency-risk">this type of risk here</a>.

#### Employee education and awareness

Over 80% of hacking incidents happen because bad actors get their hands on credentials <i>(e.g. keys, usernames and passwords, access to emails that control access and credentials)</i>. People working on the inside of organizations can make it easier for these hackers too. To prevent this, it's important for all individuals in an organization to learn how to secure their credentials. This includes learning how to recognize suspicious emails, not hesitating to ask for extra security checks, and speaking up if something seems off. Training for everyone is a must to keep any organization safe.

#### Email protection

Phishing attacks and social engineering are on the rise and getting trickier to spot. When you click a link in a phishing email, it can open the door for attackers to do sneaky stuff like installing harmful software or giving them access to information they shouldn't have. They can also trick individuals in organizations to perform actions <i>(e.g. social engineering)</i> such as sending funds, adding access, or providing otherwise priviledged information. Consider applying strict spam filters and clearly marking emails as either from within or outside your network. <i>Some email providers now do this by default.</i>

#### Password safety and access management

Make it a rule for everyone in the organization to use a password manager. This helps stop people from using the same password over and over, makes passwords more complicated and harder to guess or crack, and provides a secure way for individuals to share them inside the organization. Additionally, using a single sign-on (SSO) integrated into the password manager for important accounts, you can make a single secure solution for all organizational accounts.

#### Network monitoring

Think about using network monitoring software to get warnings about any suspicious activity or attempts to access your network that you don't recognize. Some of these tools and services can provide round-the-clock protection and even use artificial intelligence to spot potential cybercrimes before they happen. Costs vary from free to expensive, depending on organizational needs and services or tools chosen.

#### Data backup

Regularly backup data of the organization in a secure and encrypted way to make sure there is redundancy of data in case of malware, physical theft, destruction of servers and connected systems and platforms <i>(e.g. Notion, Google, Github, etc)</i> and to nullify the threat of ransomware.

#### Software updates

To keep access points safe, it's critical that all individuals in the organization using the network have the most recent updated software and security updates. You can make sure software updates happen either by doing them manually or by using a tool that restricts access to sensitive accounts for employees whose software isn't up to date.

<br>

## Get started

Ready to start your audit? <a href="./audit-template">Use this guide</a> that provides you a step-by-step template you can modify as needed.

<br>

