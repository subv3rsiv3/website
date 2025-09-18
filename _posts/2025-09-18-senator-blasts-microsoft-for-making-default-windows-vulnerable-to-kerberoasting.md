---
layout: posts
title: Senator blasts Microsoft for making default Windows vulnerable to “Kerberoasting”
date: '2025-09-18 06:26:19 '
excerpt: '### Subvertec Rewind: Microsoft’s Kerberoasting Mess – A Wake-Up Call for SMBs Senator Ron Wyden is calling out Microsoft for its sloppy defaults in Windows, specifically how the outdated RC4 encryption in Kerberos authentication leaves sys'
seo_title: Senator blasts Microsoft for making default Windows vulnerable to “Kerberoasting”
seo_description: '### Subvertec Rewind: Microsoft’s Kerberoasting Mess – A Wake-Up Call for SMBs Senator Ron Wyden is calling out Microsoft for its sloppy defaults in Window'
categories:
- Security
- Azure
- Backup_DR
tags:
- Security
- Azure
- Backup_DR
permalink: /blog/senator-blasts-microsoft-for-making-default-windows-vulnerable-to-kerberoasting/
---

### Subvertec Rewind: Microsoft’s Kerberoasting Mess – A Wake-Up Call for SMBs Senator Ron Wyden is calling out Microsoft for its sloppy defaults in Windows, specifically how the outdated RC4 encryption in Kerberos authentication leaves systems wide open to "Kerberoasting" attacks, as seen in the Ascension health breach. In that case, hackers slipped in via a contractor's laptop using Microsoft Edge and Bing, then escalated privileges in Active Directory to spread ransomware across thousands of machines—exploiting weak password hashing that makes cracking admin creds a breeze for anyone with basic GPU power. Microsoft's response? Suggest using super-long passwords (at least 14 chars) without actually enforcing it, while dragging their feet on ditching RC4 despite announcing it over a year ago in a buried blog post. For SMBs and MSPs, this highlights a real risk: if your network relies on default Microsoft setups, you're one compromised endpoint away from a costly breach, emphasizing the need to audit and harden AD configs ASAP to avoid playing catch-up with hackers. And let's be real—Microsoft acting like an "arsonist" here means you can't just trust the defaults; get proactive with multi-factor auth, salted hashes, and better encryption to keep your small biz secure without breaking the bank. **Key Takeaways for SMBs and MSPs:** - **Audit Your AD Now:** Don't rely on Microsoft's weak defaults—check for RC4/Kerberos vulnerabilities and switch to stronger encryption like AES to prevent easy offline password cracking.

**Key takeaways**
- ### Subvertec Rewind: Microsoft’s Kerberoasting Mess – A Wake-Up Call for SMBs Senator Ron Wyden is calling out Microsoft for its sloppy defaults in Windows, specifically how the outdated RC4 encryption in Kerberos authentication leaves systems wide open to "Kerberoasting" attacks, as seen in the Ascension health breach. In that case, hackers slipped in via a contractor's laptop using Microsoft Edge and Bing, then escalated privileges in Active Directory to spread ransomware across thousands of machines—exploiting weak password hashing that makes cracking admin creds a breeze for anyone with basic GPU power. Microsoft's response? Suggest using super-long passwords (at least 14 chars) without actually enforcing it, while dragging their feet on ditching RC4 despite announcing it over a year ago in a buried blog post. For SMBs and MSPs, this highlights a real risk: if your network relies on default Microsoft setups, you're one compromised endpoint away from a costly breach, emphasizing the need to audit and harden AD configs ASAP to avoid playing catch-up with hackers. And let's be real—Microsoft acting like an "arsonist" here means you can't just trust the defaults; get proactive with multi-factor auth, salted hashes, and better encryption to keep your small biz secure without breaking the bank. **Key Takeaways for SMBs and MSPs:** - **Audit Your AD Now:** Don't rely on Microsoft's weak defaults—check for RC4/Kerberos vulnerabilities and switch to stronger encryption like AES to prevent easy offline password cracking.

**Source:** [https://arstechnica.com/security/2025/09/senator-blasts-microsoft-for-making-default-windows-vulnerable-to-kerberoasting/](https://arstechnica.com/security/2025/09/senator-blasts-microsoft-for-making-default-windows-vulnerable-to-kerberoasting/)
