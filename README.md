# Windows System Configuration Guide

This repository contains step-by-step guides for configuring and managing Windows systems. Whether you're looking to block specific domains using the firewall or disable Windows updates permanently, and installing essential software, this guide has you covered.

## Blocking Domain using Firewall

To block a domain using the Windows Firewall, follow these steps:

1. Open the Control Panel.
2. Click on "Large Icon".
3. Select "Windows Defender Firewall".
4. Go to "Advanced Settings".
5. Click on "Outbound Rules".
6. Create a New Rule.
7. Choose "Custom Rule".
8. Select "All programs" and click "Next".
9. Choose "Any" and click "Next".
10. IMPORTANT! Obtain the remote IP addresses:
    - Open Command Prompt and type: `nslookup www.website.com`
    - Copy and paste the IP addresses.

## Disabling Windows Update Permanently

To disable Windows Update permanently, follow these steps:

1. Open `services.msc`.
2. Find "Windows Update" and open its properties.
3. Set the startup type to "Disabled".
4. Open the Registry Editor (`regedit`).
5. Navigate to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows`.
6. Inside the "Windows" folder, create a new folder named "WindowsUpdate".
7. Inside "WindowsUpdate", create a new folder named "AU".
8. Create a DWORD (32-bit) value named "NoAutoUpdate".
9. Set the value of "NoAutoUpdate" to 1.


## HOW TO ACTIVATE WINDOWS

1. Search for KMS client Activation
2. Copy the Product key for your OS
3. cmd run as admin
4. slmgr /ipk (paste product key)
5. slmgr /skms kms9.MSGuides.com
6. slmgr /ato
7. exit


## HOW TO INSTALL MS OFFICE

1. Search for `Office Deployment Tool`
2. Search for `Office Customization Tool`
3. Office Suites -> Office Professional Plus 2019 - Volume License
4. Languages -> English (United States)
5. After that, keep everything as Default. then Export
6. cd c:\office 2019
7. setup.exe /configure configuration.xml

## HOW TO SETUP FIREWALL FOR LOCAL ACCESS

Select 'Inbound Rules':
In the left pane, click on "Inbound Rules."

Create a New Rule:
In the right pane, click on "New Rule."

Choose Rule Type:
Select "Port" and click "Next."

Specify Ports:
Choose "TCP" and enter 80, 443 in the "Specific local ports" field.
Click "Next."

Allow the Connection:
Select "Allow the connection" and click "Next."

Profile Selection:
Choose when this rule applies (Domain, Private, Public). Usually, you can select all three, depending on your network settings.
Click "Next."

Name the Rule:
Give your rule a name, like "Allow HTTP and HTTPS."
Optionally, provide a description.
Click "Finish."

Step 4: Verify the Rules
Check Inbound Rules:
In the "Inbound Rules" list, locate your newly created rule to ensure it’s enabled.

Step 5: Test the Configuration

## Change IP Address name

notepad C:\Windows\System32\drivers\etc\hosts

## Speed up your slow laptop

### List to disable: 
- Cortana

