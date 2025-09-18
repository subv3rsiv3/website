---
layout: posts
title: Mis-issued certificates for 1.1.1.1 DNS service pose a threat to the Internet
date: '2025-09-18 06:26:57 '
excerpt: '### Subvertec''s Take: Dodgy Certs for Cloudflare''s 1.1.1.1 DNS – A Wake-Up Call for Web Trust Look, folks, someone snagged mis-issued TLS certificates for Cloudflare''s super-popular 1.1.1.1 DNS service, potentially letting bad actors pull o'
seo_title: Mis-issued certificates for 1.1.1.1 DNS service pose a threat to the Internet
seo_description: '### Subvertec''s Take: Dodgy Certs for Cloudflare''s 1.1.1.1 DNS – A Wake-Up Call for Web Trust Look, folks, someone snagged mis-issued TLS certificates for '
categories:
- Security
- Microsoft365
- Networking
tags:
- Security
- Microsoft365
- Networking
permalink: /blog/mis-issued-certificates-for-1111-dns-service-pose-a-threat-to-the-internet/
---

### Subvertec's Take: Dodgy Certs for Cloudflare's 1.1.1.1 DNS – A Wake-Up Call for Web Trust Look, folks, someone snagged mis-issued TLS certificates for Cloudflare's super-popular 1.1.1.1 DNS service, potentially letting bad actors pull off man-in-the-middle attacks to spy on, decrypt, or mess with your traffic—yeah, that's as sketchy as it sounds in our fragile web of trust. These certificates, which are supposed to securely tie a domain to its public key via the Public Key Infrastructure (PKI), got handed out by a certificate authority (CA) without proper checks, exposing a classic single-point-of-failure in the system that could tank security for sites like your bank's or email provider. For SMBs and MSPs, this is a stark reminder that if attackers exploit this, your business could face data breaches, downtime, or supply chain hacks, especially since you're often juggling lean IT teams without the big-budget defenses. Certificate Transparency logs eventually caught this mess (after a embarrassing four-month delay), highlighting how even tools meant to spot these issues can slip through the cracks—blame poor monitoring or, hey, maybe Microsoft for not blocking them sooner. Bottom line, SMBs and MSPs need to amp up their vigilance on certificate validation and PKI hygiene to avoid becoming collateral damage in these internet castle collapses. **Key Takeaways for SMBs and MSPs:** - **Monitor Certificates Religiously:** Use tools like Certificate Transparency logs to scan for mis-issued certs in real-time—don't wait for the pros to flag them, or you might be four months too late.

**Key takeaways**
- ### Subvertec's Take: Dodgy Certs for Cloudflare's 1.1.1.1 DNS – A Wake-Up Call for Web Trust Look, folks, someone snagged mis-issued TLS certificates for Cloudflare's super-popular 1.1.1.1 DNS service, potentially letting bad actors pull off man-in-the-middle attacks to spy on, decrypt, or mess with your traffic—yeah, that's as sketchy as it sounds in our fragile web of trust. These certificates, which are supposed to securely tie a domain to its public key via the Public Key Infrastructure (PKI), got handed out by a certificate authority (CA) without proper checks, exposing a classic single-point-of-failure in the system that could tank security for sites like your bank's or email provider. For SMBs and MSPs, this is a stark reminder that if attackers exploit this, your business could face data breaches, downtime, or supply chain hacks, especially since you're often juggling lean IT teams without the big-budget defenses. Certificate Transparency logs eventually caught this mess (after a embarrassing four-month delay), highlighting how even tools meant to spot these issues can slip through the cracks—blame poor monitoring or, hey, maybe Microsoft for not blocking them sooner. Bottom line, SMBs and MSPs need to amp up their vigilance on certificate validation and PKI hygiene to avoid becoming collateral damage in these internet castle collapses. **Key Takeaways for SMBs and MSPs:** - **Monitor Certificates Religiously:** Use tools like Certificate Transparency logs to scan for mis-issued certs in real-time—don't wait for the pros to flag them, or you might be four months too late.

**Source:** [https://arstechnica.com/security/2025/09/mis-issued-certificates-for-1-1-1-1-dns-service-pose-a-threat-to-the-internet/](https://arstechnica.com/security/2025/09/mis-issued-certificates-for-1-1-1-1-dns-service-pose-a-threat-to-the-internet/)
