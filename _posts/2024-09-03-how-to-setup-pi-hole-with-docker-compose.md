---
layout: posts
title: "Set Up Pi-hole with Docker Compose for Ad Blocking & Security"
excerpt: "Learn how to set up Pi-hole using Docker Compose to block ads and secure your network across various hardware platforms."
seo_title: "Pi-hole Setup Guide Using Docker Compose | Block Ads & Secure Your Network"
seo_description: "Step-by-step guide on setting up Pi-hole with Docker Compose to block ads and enhance network security. Ideal for various hardware platforms including Raspberry Pi and servers."
image: "/assets/images/pi-logo-400ish.png"
header:
  tags: ["Pi-hole", "Docker", "Network Security", "Ad Blocking", "Tech Guide", "Cybersecurity", "Home Network Security", "IT Management", "Data Protection", "DNS Sinkhole", "Ad Blocker", "Open Source", "Docker Container", "Network Tools", "Raspberry Pi", "Small Business Security"]
---

Are you looking for a reliable way to block annoying ads and improve your network security? Pi-hole, combined with Docker Compose, offers a flexible solution that works on a wide range of hardware. This guide will take you through the basic steps to set up Pi-hole using Docker Compose, making it easy to deploy on any system that supports Docker.

## What is Pi-hole?
{% include figure popup=true image_path="/assets/images/pihole-dashboard-1250x1000.png" alt="Pi-hole Dashboard" caption="Pi-hole Dashboard" %}

Pi-hole is a powerful network-wide ad blocker that prevents unwanted ads from reaching your devices. By blocking access to malicious domains, it also adds an extra layer of security to your network, making your browsing experience faster and safer.

## Why Use Docker Compose?

Using Docker Compose to set up Pi-hole allows for easier management and deployment across different hardware platforms. Whether you're running a Raspberry Pi or a high-performance server, Docker Compose simplifies the installation process, keeps your system organized, and makes future updates more manageable.

## Step-by-Step Setup Guide

### 1. Install Docker and Docker Compose
{% include figure popup=true image_path="/assets/images/docker-logo-960x540.png" alt="Docker Logo" caption="Docker Logo" %}

- **Linux Users:**
  ```bash
  sudo apt-get update
  sudo apt-get install docker.io docker-compose
  ```

- **Windows or macOS Users:**
  Download and install Docker Desktop, which includes Docker Compose.

### 2. Create a Docker Compose File

- Create a directory for your Pi-hole setup:
  ```bash
  mkdir pihole
  cd pihole
  ```

- Create a `docker-compose.yml` file with the following content:
  ```yaml
  version: "3"

  services:
    pihole:
      container_name: pihole
      image: pihole/pihole:latest
      environment:
        TZ: 'America/New_York' # Set your timezone
        WEBPASSWORD: 'yourpassword' # Set a password for the admin interface
      volumes:
        - './etc-pihole:/etc/pihole'
        - './etc-dnsmasq.d:/etc/dnsmasq.d'
      networks:
        - pihole_network
      ports:
        - "53:53/tcp"
        - "53:53/udp"
        - "80:80"
        - "443:443"
      restart: unless-stopped

  networks:
    pihole_network:
  ```

### 3. Start the Pi-hole Container
{% include figure popup=true image_path="/assets/images/pi-logo.png" alt="Pi-hole Logo" caption="Pi-hole Logo" %}

- Run Docker Compose to set up and start Pi-hole:
  ```bash
  sudo docker-compose up -d
  ```
  The `-d` flag runs Pi-hole in detached mode, allowing it to continue running in the background.

### 4. Configure Your Router

- Set your router’s DNS server to the IP address of your Pi-hole container. This will direct all network traffic through Pi-hole, effectively blocking ads on all connected devices.

### 5. Access the Admin Interface
{% include figure popup=true image_path="/assets/images/dark-pihole-dashboard-1920x966.png" alt="Dark Mode Pi-hole Dashboard" caption="Dark Mode Pi-hole Dashboard" %}

- Open a web browser and go to `http://<your-server-ip>/admin`.
- Log in with the password you set in the `docker-compose.yml` file.

### 6. Verify the Setup

- Visit a website known for displaying ads to confirm they are being blocked.
- Use the Pi-hole admin interface to monitor your network activity and see how many ads are being blocked in real-time.

## Advanced Pi-hole Configuration

Now that you have Pi-hole up and running, you've made a significant leap toward a more secure, ad-free network. But this is just the beginning! [Check out the advanced configuration article](/advanced-pi-hole-configuration)

Stay tuned for more in-depth guides on how to enhance your network’s security!

---

**Need Help?**

If you need assistance with the setup or prefer a professional touch, Subvertec is here to help. Contact us today to secure your network and enjoy an ad-free browsing experience.

---