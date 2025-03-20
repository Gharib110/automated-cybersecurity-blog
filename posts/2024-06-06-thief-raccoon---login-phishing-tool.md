---
title: "Thief Raccoon - Login Phishing Tool"
date: Thu, 6 Jun 2024 08:30:00 -0400
draft: false
type: posts
categories: 
- Flask,Python,Python3,Raccoon,Simulation,Thief_Raccoon,Windows,Windows 11
---
# Thief Raccoon - Login Phishing Tool

<br/>

<br/>
[![](https://blogger.googleusercontent.com/img/a/AVvXsEgN6oeE9rga5xXPKNgSN6e9139yGVGjUywMImmkW1kmJ2Wlvu8d-WoIxFJN1y1dG4ceskcL4L7D6eObjdx6LfcY4yOA1f7o8e3YJBcGFSzIbnmpw0UjiNIqoCSkHOWuNn86XnksK1E1a_o4XI23s0PvOq9W8KgIeQzWdt7ulNJhOIHiFgkYsmgbsWkTMcY=w640-h364)](https://blogger.googleusercontent.com/img/a/AVvXsEgN6oeE9rga5xXPKNgSN6e9139yGVGjUywMImmkW1kmJ2Wlvu8d-WoIxFJN1y1dG4ceskcL4L7D6eObjdx6LfcY4yOA1f7o8e3YJBcGFSzIbnmpw0UjiNIqoCSkHOWuNn86XnksK1E1a_o4XI23s0PvOq9W8KgIeQzWdt7ulNJhOIHiFgkYsmgbsWkTMcY)

  

Thief Raccoon is a tool designed for educational purposes to demonstrate how [phishing](https://www.kitploit.com/search/label/Phishing "phishing") attacks can be conducted on various operating systems. This tool is intended to raise awareness about [cybersecurity](https://www.kitploit.com/search/label/Cybersecurity "cybersecurity") threats and help users understand the importance of security measures like 2FA and password management.

  

Features
--------

-   Phishing simulation for Windows 10, Windows 11, Windows XP, Windows Server, Ubuntu, Ubuntu Server, and macOS.
-   Capture user credentials for educational demonstrations.
-   Customizable login screens that mimic real operating systems.
-   Full-screen mode to enhance the phishing simulation.

Installation
------------

### Prerequisites

-   Python 3.x
-   pip (Python package installer)
-   ngrok (for exposing the local server to the internet)

### Download and Install

1.  **Clone the repository:**

\`\`\`bash git clone https://github.com/davenisc/thief\_raccoon.git cd thief\_raccoon

1.  Install python venv

\`\`\`bash apt install [python](https://www.kitploit.com/search/label/Python "python")3.11-venv

1.  **Create venv:**

\`\`\`bash python -m venv raccoon\_venv source raccoon\_venv/bin/activate

1.  **Install the required libraries:**

\`\`\`bash pip install -r requirements.txt

**Usage**

1.  **Run the main script:**

\`\`\`bash python app.py

1.  **Select the operating system for the phishing simulation:**

After running the script, you will be presented with a menu to select the operating system. Enter the number corresponding to the OS you want to simulate.

1.  **Access the phishing page:**

If you are on the same local network (LAN), open your web browser and navigate to http://127.0.0.1:5000.

If you want to make the phishing page accessible over the internet, use ngrok.

Using ngrok

1.  **Download and install ngrok**

Download ngrok from ngrok.com and follow the installation instructions for your operating system.

1.  **Expose your local server to the internet:**
    
2.  **Get the public URL:**
    

After running the above command, ngrok will provide you with a public URL. Share this URL with your test subjects to access the phishing page over the internet.

**How to install Ngrok on Linux?**

1.  Install ngrok via Apt with the following command:

\`\`\`bash curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \\ | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \\ && echo "deb https://ngrok-agent.s3.amazonaws.com [buster](https://www.kitploit.com/search/label/Buster "buster") main" \\ | sudo tee /etc/apt/sources.list.d/ngrok.list \\ && sudo apt update \\ && sudo apt install ngrok

1.  Run the following command to add your authtoken to the default ngrok.yml

\`\`\`bash ngrok config add-authtoken xxxxxxxxx--your-token-xxxxxxxxxxxxxx

**Deploy your app online**

1.  Put your app online at ephemeral domain Forwarding to your upstream service. For example, if it is listening on port http://localhost:8080, run:
    
    \`\`\`bash ngrok http http://localhost:5000
    

**Example**

1.  **Run the main script:**

\`\`\`bash python app.py

1.  **Select Windows 11 from the menu:**

\`\`\`bash Select the operating system for phishing: 1. [Windows](https://www.kitploit.com/search/label/Windows "Windows") 10 2. [Windows](https://www.kitploit.com/search/label/Windows "Windows") 11 3. [Windows](https://www.kitploit.com/search/label/Windows "Windows") XP 4. [Windows](https://www.kitploit.com/search/label/Windows "Windows") Server 5. Ubuntu 6. Ubuntu Server 7. macOS Enter the number of your choice: 2

1.  **Access the phishing page:**

Open your browser and go to http://127.0.0.1:5000 or the ngrok public URL.

**Disclaimer**

**This tool is intended for educational purposes only. The author is not responsible for any misuse of this tool. Always obtain explicit permission from the owner of the system before conducting any phishing tests.**

**License**

This project is licensed under the MIT License. See the LICENSE file for details.

**ScreenShots**

[](https://ibb.co/mcNh32n "Thief Raccoon is a tool designed for educational purposes to demonstrate how phishing attacks can be conducted on various operating systems. This tool is intended to raise awareness about cybersecurity threats and help users understand the importance of security measures like 2FA and password (10)")[![](https://blogger.googleusercontent.com/img/a/AVvXsEjI1KhMtWE8kjSbr9MyFU2DPD9B7CxRL5pq6J_uQgDnc_o_7g2xsywiB8nJfaGF7WexEibu9vbf_MDtdUoi9ydc0EuYM54PYFtLBwWqfuIzVo4mUAZslVtY5cff9WlIRrTx9CPppp4Exy68Gz487bjU9Gx7K-0FDYGFYmi5LKF5084GysjtTp3gm60_ncM=w640-h322)](https://blogger.googleusercontent.com/img/a/AVvXsEjI1KhMtWE8kjSbr9MyFU2DPD9B7CxRL5pq6J_uQgDnc_o_7g2xsywiB8nJfaGF7WexEibu9vbf_MDtdUoi9ydc0EuYM54PYFtLBwWqfuIzVo4mUAZslVtY5cff9WlIRrTx9CPppp4Exy68Gz487bjU9Gx7K-0FDYGFYmi5LKF5084GysjtTp3gm60_ncM)

[](https://ibb.co/tcwRjPh "Thief Raccoon is a tool designed for educational purposes to demonstrate how phishing attacks can be conducted on various operating systems. This tool is intended to raise awareness about cybersecurity threats and help users understand the importance of security measures like 2FA and password (11)")[![](https://blogger.googleusercontent.com/img/a/AVvXsEjDqhSpNxPIGGs2DCi_h3Tx-ZxXkJVhZbDB1wUBNVHJfLV6ycOU5LNzSimIZ7ssyZhaPNzzYFmxH0biOoRXFnD-DxIGC3EK2Vfdj2dKKorHYudaLj_9X2TNI-Emw4L7SrWQatxk1fx_oBMD1jJFPRaqTbjs9b3eLqrvJEw16VuhM42sFbfKtdlfJaansWw=w640-h332)](https://blogger.googleusercontent.com/img/a/AVvXsEjDqhSpNxPIGGs2DCi_h3Tx-ZxXkJVhZbDB1wUBNVHJfLV6ycOU5LNzSimIZ7ssyZhaPNzzYFmxH0biOoRXFnD-DxIGC3EK2Vfdj2dKKorHYudaLj_9X2TNI-Emw4L7SrWQatxk1fx_oBMD1jJFPRaqTbjs9b3eLqrvJEw16VuhM42sFbfKtdlfJaansWw)

[](https://ibb.co/KjYk72D "Thief Raccoon is a tool designed for educational purposes to demonstrate how phishing attacks can be conducted on various operating systems. This tool is intended to raise awareness about cybersecurity threats and help users understand the importance of security measures like 2FA and password (12)")[![](https://blogger.googleusercontent.com/img/a/AVvXsEjkl9_lzt5i-eIbh8xxe3ee3u1XU3lctxkyo5qXQsr1oDRdBAsEDfbTO2K1hrfbLwbhYC6wPTQdG3JXVbHQ7rcUmHOLUnqXScDWOKuRvb5uU5KgEvZcVzmaYtN2uShyj6vJRAaozmLpiDZt2sQa3Jz-_kXwPItS3NQ2DvQdMH9WRl9kYNCL6Wgt8wGdJ2c=w640-h338)](https://blogger.googleusercontent.com/img/a/AVvXsEjkl9_lzt5i-eIbh8xxe3ee3u1XU3lctxkyo5qXQsr1oDRdBAsEDfbTO2K1hrfbLwbhYC6wPTQdG3JXVbHQ7rcUmHOLUnqXScDWOKuRvb5uU5KgEvZcVzmaYtN2uShyj6vJRAaozmLpiDZt2sQa3Jz-_kXwPItS3NQ2DvQdMH9WRl9kYNCL6Wgt8wGdJ2c)

[](https://ibb.co/Wy9MBtt "Thief Raccoon is a tool designed for educational purposes to demonstrate how phishing attacks can be conducted on various operating systems. This tool is intended to raise awareness about cybersecurity threats and help users understand the importance of security measures like 2FA and password (13)")[![](https://blogger.googleusercontent.com/img/a/AVvXsEjxemHXDxgpYoHb6zMwbI3XGFKaRrmmfETKRQbnSQHIqW4-JapAfM8yiykQf6U6IRB0fYkbJIm8vS3t4WRDlJWVpjf6XL9F0eOnsKB-Gx5JTK4XOySVZS7RapChhz7_jUI9TA6gC30m8Kt-HFO1fuzZvj-QiwnuRUr47WXwvpdJkSsR0iatmVpDxZDkY1o=w640-h416)](https://blogger.googleusercontent.com/img/a/AVvXsEjxemHXDxgpYoHb6zMwbI3XGFKaRrmmfETKRQbnSQHIqW4-JapAfM8yiykQf6U6IRB0fYkbJIm8vS3t4WRDlJWVpjf6XL9F0eOnsKB-Gx5JTK4XOySVZS7RapChhz7_jUI9TA6gC30m8Kt-HFO1fuzZvj-QiwnuRUr47WXwvpdJkSsR0iatmVpDxZDkY1o)

[](https://ibb.co/Qf7kKMJ "Thief Raccoon is a tool designed for educational purposes to demonstrate how phishing attacks can be conducted on various operating systems. This tool is intended to raise awareness about cybersecurity threats and help users understand the importance of security measures like 2FA and password (14)")[![](https://blogger.googleusercontent.com/img/a/AVvXsEi8eGMMAFwy5pcvYuvZE_KLoonHI8aQv8ocATUZba8gUsle--gpHw2LJeShXKT0EaeVKCOaY8-jf6-26xwOdMFK5jAzF_lKnNnitw3P-9ZmkfGdj2HLdhGVizWflQsDes2UdGFw4r-G9927DpU-G1ulVN1vZPRcArwa1ZBEFv1jZUUsWaSb6zXfx11oX-U=w640-h394)](https://blogger.googleusercontent.com/img/a/AVvXsEi8eGMMAFwy5pcvYuvZE_KLoonHI8aQv8ocATUZba8gUsle--gpHw2LJeShXKT0EaeVKCOaY8-jf6-26xwOdMFK5jAzF_lKnNnitw3P-9ZmkfGdj2HLdhGVizWflQsDes2UdGFw4r-G9927DpU-G1ulVN1vZPRcArwa1ZBEFv1jZUUsWaSb6zXfx11oX-U)

**Credits**

Developer: @davenisc Web: https://davenisc.com

  
  

**[Download Thief\_Raccoon](https://github.com/davenisc/thief_raccoon "Download Thief_Raccoon")**

<br/>
[Source](http://www.kitploit.com/2024/06/thief-raccoon-login-phishing-tool.html)
---
