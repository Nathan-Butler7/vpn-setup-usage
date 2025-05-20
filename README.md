<p align="center">
<img src="https://github.com/user-attachments/assets/9ca476c5-ce2c-4da4-a4c5-25e5fd9e098e" alt="VPN" width="700"
</p>



<h1> Virtual Private Network (VPNs) Setup and Usage (Proton VPN) </h1>
This tutorial provides a practical guide to setting up and using a VPN, and demonstrates how to test your VPN connection using a remote desktop from Microsoft Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Your PC

<h2>High-Level Steps</h2>

- What is my IP adress?
- Creating Resource Groups and Virtual Machines.
- Log into the VM with Remote Desktop.
- Sign up for ProtonVPN and test the VPN connection.
- Download the Proton VPN client.
- Changed IP address location.

<h2>Actions and Observations</h2>

1. What is my IP address?
Browse to https://whatismyipaddress.com/ FROM WITHIN YOUR OWN MACHINE and take note of this in a text file.

![image](https://github.com/user-attachments/assets/0100cd42-5f6e-42a3-ab57-4aa16c8c7be4)

2. Creating Resource Groups and Virtual Machines.
Resource Group:

- To create a Resource Group, go to the Azure Portal. In the middle of the homepage under 'Azure Services', click on 'Resource groups' and then select 'Create' to begin the process'.

![Screenshot 2025-05-02 161517](https://github.com/user-attachments/assets/f2711179-31d1-44eb-9409-53abcdce0d6d)

- All rescources in a subsciption are billed together so leave that as default.
- Resource group name can be named to your desire. I will call mine "vpn-test".
- When selecting a resource group region, it's recommended that you select a location close to where your control operations originate.
- Click 'Review + create' -> 'Create'.

![image](https://github.com/user-attachments/assets/5e9e1f16-b865-447c-a101-1bd5bd38ac7a)

Virtual Machines:

- In the Azure Portal, use the search bar at the top os search for 'Virtual Machines" and select it.
- In the display area, click 'Create' -> 'Azure virtual machine'.

![Screenshot 2025-05-02 225357](https://github.com/user-attachments/assets/8635eb0f-1ab8-4ed6-b59f-106d00c823af)

- Under 'Project details', assign your new resource group you just created (vpn-test).
- Give your Virtual Machine name "vpn-test-win-10".
- Select the resource region the same as the Resource groups ((Asia Pacific) Australia East).

![image](https://github.com/user-attachments/assets/ea4d5673-02be-4eb2-b460-33de41111564)

- For Image, select 'Windows 10 Pro version 22H2 - x64 Gen2'.
- Recommended for 'Size' you utilise "Standard_D2s_v5 - 2 vcpus, 8 GiB memory".
- For 'Administrator Account' create your Username "labuser" and password can be anything. e.g; "CyberLab123!".

![image](https://github.com/user-attachments/assets/0cb4f6c8-54c9-4875-8155-47e586a91ce2)

- Be sure to tick the box for eligibily of a windows liscence.
- Click 'Review + Create'.

![Screenshot 2025-05-11 175807](https://github.com/user-attachments/assets/c5e52f58-a5e3-4edf-b608-1ecf19dfd430)

- Wait for the VM to process till you see "Validation passed" on the top of the page.

![Screenshot 2025-05-06 141709](https://github.com/user-attachments/assets/94de286a-168e-4569-85c1-37a227c00835)

- Then click 'Create'.
- You have successfully created a Windows Virtual Machine.

![Screenshot 2025-05-06 141743](https://github.com/user-attachments/assets/fde070e8-0ded-4823-ad8d-bc0a4b8bb840)

- Search up "Virtual Machines" and click on it, there you will discover your Virtual Machine.

![image](https://github.com/user-attachments/assets/1d262933-4de4-443a-82fa-b6e6f42943bd)

3. Log into the VM with Remote Desktop.

- On your PC, click the Windows 'start' icon to open up the menu and search up "Remote Desktop Connection".
- If using Mac, install Microsoft Remote Desktop.
- Copy windows VM Public IP address and paste it into the Remote Desktop Connection.
- Click 'Show Options' and put in the user name for the windows VM (labuser).
- Click 'connect'.
- Insert the password then click 'ok'.
- Click 'Yes' to continue.

![Screenshot 2025-05-17 123635](https://github.com/user-attachments/assets/e82c2fe9-0147-4432-b4d3-63c3e58bf99b)

- Browse to https://whatismyipaddress.com/ and take note of this in a text file.

![image](https://github.com/user-attachments/assets/b455529b-22b2-4ecb-b253-34254c42702b)

4. Sign up for ProtonVPN and test the VPN connection.

- We're going to create a VPN tunnel from our VM to a VPN server.
- On your VM, sign up for the free version of Proton VPN https://account.protonvpn.com/signup?plan=free&language=en.

![image](https://github.com/user-attachments/assets/7a692631-eb78-4add-8df5-e522402c13a2)

5. Download the Proton VPN client.

- On the website, navigate to to the sidebar and click 'Downloads'.

![image](https://github.com/user-attachments/assets/12cf12be-cbd8-4f14-bb86-dab231bf707b)

- Click 'Download' for Windows.

![image](https://github.com/user-attachments/assets/db06bfec-dfdc-4109-8436-7d42171f66fa)

Click 'Download for Windows' and it will open a bar. Click 'Windows 11/10 (x64)' to download.

![image](https://github.com/user-attachments/assets/03d2335e-2275-4a69-b1e2-f83df82c6aa0)

- Open file when completed.

![image](https://github.com/user-attachments/assets/1a281c8c-4b43-4ee9-9edc-36d7f686d46a)

- Setup Language and click 'OK'.

![image](https://github.com/user-attachments/assets/b221a58f-bfce-48dc-bc83-6f21a443e181)

- Click Next -> Install.

![image](https://github.com/user-attachments/assets/6d469395-ffc9-48b2-bf88-7e180336f8f8)

![image](https://github.com/user-attachments/assets/c9df43eb-5c93-43da-896e-3b0b88e87c62)

- Sign into Proton VPN.

![image](https://github.com/user-attachments/assets/1edae9b9-eba3-43f8-b917-201871d6edcc)

- We're now logged into the Proton VPN client.

![image](https://github.com/user-attachments/assets/3490518f-c558-4b20-8dc3-ce4ef98e9693)

- Click 'Connect' to be protected by a new random VPN server from a different country (such as Japan).
- Now when we browse the internet it should look like our traffic is coming from our random VPN server.

![image](https://github.com/user-attachments/assets/07fc5adb-1379-4e53-842a-920f2010f517)

6. Changed IP address location.

- Go onto https://whatismyipaddress.com/ and observe how your IP addresses have changed.

![image](https://github.com/user-attachments/assets/02f15157-7fde-47a0-aa54-076261400793)

- Try browsing to Google, Disney, Netflix, and/or Amazon and see if there is anything different about the sites in relation to the location of your VPN server. For example, the language or URL may be different.

![image](https://github.com/user-attachments/assets/b8c8a39d-fe22-4565-8e8d-1445873a2082)



