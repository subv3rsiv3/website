---
layout: single
title: Images over DNS
date: '2025-09-20 13:52:01 '
excerpt: Ever thought DNS was just for resolving names? Think again—it's possible to smuggle hefty data like images through TXT records, bypassing the outdated 255-byte myth by chaining multiple strings and leveraging TCP for up to 64KB payloads, wh
seo_title: Images over DNS
seo_description: Ever thought DNS was just for resolving names? Think again—it's possible to smuggle hefty data like images through TXT records, bypassing the outdated 255-
categories:
- Networking
- AI_Automation
- Backup_DR
tags:
- Networking
- AI_Automation
- Backup_DR
permalink: /blog/images-over-dns/
header:
  image: /assets/images/images-over-dns-hero.webp
  overlay_color: '#000'
  overlay_filter: 0.3
image: /assets/images/images-over-dns-hero.webp
og_image: /assets/images/images-over-dns-hero.webp
twitter_image: /assets/images/images-over-dns-hero.webp
---

![Images over DNS](/assets/images/images-over-dns-hero.webp)
Ever thought DNS was just for resolving names? Think again—it's possible to smuggle hefty data like images through TXT records, bypassing the outdated 255-byte myth by chaining multiple strings and leveraging TCP for up to 64KB payloads, which is a nifty workaround for scenarios where traditional data transfer is blocked. A clever hack using Google's Public DNS and a custom Go server demonstrates this, serving binary data directly to browsers or tools like dig, though you'll need a quick Perl script to unscramble the escaped output into usable files. For SMBs and MSPs dealing with firewall restrictions, this could be a cheeky way to tunnel data without drawing attention, but watch out for security risks like evading DNS filters or overloading resolvers. Still, with a low TTL to keep caches light, it's a fun proof-of-concept that might inspire your own DIY data tricks, as long as you don't push it too far and annoy the big DNS providers.

**Source:** [https://dgl.cx/2025/09/images-over-dns](https://dgl.cx/2025/09/images-over-dns)
