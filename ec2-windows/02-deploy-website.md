Step 1: Create and open the file

Run:



powershell

Copy

Edit

notepad .\\ec2-windows\\02-deploy-website.md

Step 2: Paste this content into the file:

markdown

Copy

Edit

\# Deploying Static Website on EC2 Windows



\## Copy website files



\- Use RDP to connect to your Windows EC2 instance.

\- Place your static website files (HTML, CSS, JS) in the IIS default folder:



C:\\inetpub\\wwwroot



sql

Copy

Edit



\## Start IIS (if not running)



```powershell

Start-Service W3SVC

Test the website

Open your browser and navigate to the public IP or DNS of your EC2 instance, e.g.:



cpp

Copy

Edit

http://<your-ec2-public-ip>/

You should see your static website loaded.



Troubleshooting

Make sure the security group attached to your instance allows HTTP (port 80) inbound traffic.



Verify IIS is running:



powershell

Copy

Edit

Get-Service W3SVC

yaml

Copy

Edit



---



\### Step 3: Save and close the file.



---



\### Step 4: Add, commit, and push



```powershell

git add .\\ec2-windows\\02-deploy-website.md

git commit -m "Add website deployment guide"

git push origin main

