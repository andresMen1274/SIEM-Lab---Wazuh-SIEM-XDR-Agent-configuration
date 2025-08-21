# SIEM-Lab---Wazuh-SIEM-XDR-Agent-configuration
In this project I will be configuring Wazuh &amp; XDR Agent in a virtual environment.

First we have to navigate to Wazuh website and download the Virtual Machine (OVA) edition.

<img width="1247" height="400" alt="image" src="https://github.com/user-attachments/assets/4735296e-c544-4b92-869c-caf559e312d3" />

Then we have to open Virtual Box and navigate to Tools/Import. Then we select the downloaded OVA file and let it install into Virtual Box.

<img width="617" height="602" alt="image" src="https://github.com/user-attachments/assets/ef97894c-0dcb-44f1-b078-132741444713" />

After successfully importing Wazuh onto Virtual Box we open the virtual machine. Then we let the machine boot up and login using the defalut wazuh username and password. Then we want to add this to our exisiting network. Therefore, we have to create a internal virtual network and a static IP address. To do this we have to have to find the name of the interface using ip a. In this case its eth0 and next we want to set a static IP and it is done as shown in the image below. 

<img width="657" height="572" alt="image" src="https://github.com/user-attachments/assets/98cd84fd-fd2e-4e66-b115-8493d90fc250" />

We go in and change the contents to match the given image below to configure an IP address and also make it point to the firewall that we have previously configured.

<img width="647" height="582" alt="image" src="https://github.com/user-attachments/assets/81bdd4f4-189d-4ede-970d-a9e8a365d7e0" />

Then we will restart the network and check that the IP address has been configured correctly. Which in this case it has been correclty configured to 192.168.1.6

<img width="651" height="570" alt="image" src="https://github.com/user-attachments/assets/4a12c46e-7629-4c15-8287-40678d0921ce" />

To check that it was correctly configured, we can ping the specific IP addresses and check if there is a response. Then we will type in the IP address into the browser of out Kali Linux machine. Then we will login to Wazuh using the defalut username and password.

<img width="794" height="518" alt="image" src="https://github.com/user-attachments/assets/22f38b3c-3c07-4294-b22d-dae4e5dc32ab" />

It should look like this after logging in.

<img width="978" height="650" alt="image" src="https://github.com/user-attachments/assets/ccfb19cd-7e90-45a4-9e35-579c89f662c0" />

Then we are going to add an agent. To do this we go to add agent then choose the operating system we want to add the agent to. Then enter in the server address (IP address that we previously configured). Then we will copy the command into the kali linux shell and run the script.

<img width="873" height="518" alt="image" src="https://github.com/user-attachments/assets/d45215b5-98e6-4dc7-b833-30f926501a95" />

The we will copy and paste the script that runs the service into the linux shell.

<img width="783" height="528" alt="image" src="https://github.com/user-attachments/assets/b12675d6-88f6-4074-b9dd-f41b55df096a" />

We can check that the agent is successfully running by going back to Wazuh and checking if the agents are running properly.

<img width="1171" height="693" alt="image" src="https://github.com/user-attachments/assets/59944756-7869-4be5-9bd0-74f62e8afc34" />

