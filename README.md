# PleximusPrime

# 🤖 **PleximusPrime** – Transform Your Streaming Experience 🤖

Welcome to **PleximusPrime** – the **Optimus Prime** of Plex servers! Built for the ultimate media fan, this repository automates and powers your media collection with precision and reliability, like a true Autobot leading the charge.

**PleximusPrime** will organize, manage, and stream your entire media library effortlessly through Plex Media Server, all while being securely wrapped inside a VPN for privacy. Get ready to binge like never before!

![Stream like a pro](https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExNnM2c3BsbzRhZ295NXF1bjJyZWQ2NmE4dndnYmg4dHkzNDV2Mjh3aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/gpIEHMxj7JbXex2eQi/giphy.gif)


## 💡 **Features**:
- **Autonomous Media Management**: Automatically organizes your movies and TV shows like a true leader.
- **VPN-Integrated**: Supports Mullvad VPN out of the box but can be easily configured for other VPN providers.
- **Cross-Platform Streaming**: Access your media library from any device, anywhere.
- **Easy to Configure**: Simple to set up, making deployment as easy as transforming your home into an entertainment hub.

---

## 🔐 VPN Configuration:
The PleximusPrime setup works seamlessly with Mullvad VPN, but you can configure it for other VPN providers as well. Create an `.env` file and follow these steps to configure the VPN:

1. Get Your VPN Account: 
- For Mullvad, visit [Mullvad.net](https://mullvad.net/). For other VPNs, follow their respective account setup and configuration instructions.
- If using WireGuard, generate your private key and server location from your VPN provider. OpenVPN can also be configured but WireGuard offers better performance and speed due to its lightweight design and modern cryptography.

2. Download the VPN Configuration:
- For Mullvad, download the WireGuard or OpenVPN configuration.
- For other VPN providers, retrieve your configuration settings and connection details.

3. Set the Configuration details to the .env:

```bash
WIREGUARD_PRIVATE_KEY=your_vpn_private_key_here
WIREGUARD_ADDRESSES=your_vpn_addresses # Example: 10.x.x.x/32
SERVER_CITIES=city_name  # Example: Amsterdam
SERVER_COUNTRIES=country_name  # Example: Netherlands
```

4. Test the VPN Connection:

Run the container and check the logs to verify that your VPN is connected properly. If the VPN is configured correctly, your Plex server’s traffic will be routed securely through the VPN, ensuring a private and secure streaming experience:

```bash
docker logs gluetun
```

---

## 🔧 Other Environment Configurations

- *PUID* and *PGID* (User and Group IDs): You can get your current user ID and group ID by running the following commands on your host machine:

    ```bash
    id $(whoami)
    ```
- *TZ* - Ensures your server’s time zone is set correctly. Example: `America/Los_Angeles`
- *WEBUI_PORT* - Allows you to configure the port on which you can access Plex or other Web UIs. By default, Plex runs on port `32400` and qBittorrent on `8080`, but you can change this to suit your needs.

---

## 🚀 **Quick Start**:
Follow these steps to get **PleximusPrime** up and running in no time:

```bash
git clone https://github.com/harshil-darji/PleximusPrime.git
cd pleximusprime
docker-compose up -d
```

---

## 🛠 **Tech Stack**:
- **Plex Media Server**: For managing and streaming your media.
- **Docker & Docker Compose**: Ensures smooth deployment.
- **WireGuard VPN**: Keeps your streams secure, Autobots style!

---

## 🎬 **Ready to Transform and Roll Out?**
Launch **PleximusPrime** and let it take charge of your home theater! Whether you're marathoning your favorite series or hosting a movie night, PleximusPrime has your back.
