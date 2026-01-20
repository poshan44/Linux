# Creating Ubuntu VM on Aure and SSH connection
This is my all documentation what I did during creating ubuntu virtual machine in azure and connection with SSH

## Step 1: Azure Account + Free Credits
First I logged into portal.azure.com with my HAMK email id.
Then I activated Azure for students with free credits.

## Step 2: Created Resources Group
I made a new resource group called SOS-HAMK in France Central

## Step 3: Created a virtual machine

.Image: Ubuntu server 24.04 LTS

.Size: Standard D2s v3

.Name: oli-linuxmanagement

.Authentication: SSH key

.Allowed SSH from my ip

After that I face a region issue and I fix it after a bit time , the Vm was ready

This is the VM overview 
![Virtual machine](Image/Virtual.png)

## step 4: Connected with SSH using PuTTY

I downloaded PuTTY from the site.
Took the public IP from Azure ->opened PuTTY -> entered Ip + username + loaded my SSH key.

login worked perfectly! I got Ubuntu welcome message
![Disk](Image/Disk.png)

## step 5: Connected with terminal

After completing all the steps I had run it with terminal as professor guidance. We also created shortcut key so that we can open it easily