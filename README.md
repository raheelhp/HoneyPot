# HoneyPot
STEPS:
To install and use a program called Pentbox on a Kali Linux device to create a basic honeypot system and test it using a standard web browser to detect an intrusion.
A honeypot is a decoy, or a trap, created by organizations to attract hackers into a computer system. One of the main objectives of using a honeypot is to monitor the hacker’s exploit of the system’s vulnerabilities. Subsequently, learn the system’s weaknesses and apply the necessary security measures to strengthen it from future attacks. Another objective is to study the hacker’s methodology. The final objective is to divert the hacker’s attention from the main network to the decoy system.

Download and Install Pentbox on Kali Linux.

Use the following commands in the Kali Linux terminal:
git clone https://github.com/technicaldada/pentbox
cd pentbox
tar -zxvf pentbox.tar.gz
cd pentbox-1.8
./pentbox.rb


Set up a Honeypot with Pentbox.
Run the following command to start Pentbox in Kali Linux:
./pentbox.rb
Select the Network tools section from the Pentbox menu by typing: 2
You will get a notification that the HONEYPOT ACTIVATED ON PORT 80.
Test Honeypot Fast Auto Configuration Functionality with Windows.
IP Address of Windows 10 machine: 10.60.0.10
IP Address of Pentbox Honeypot host (Kali): 10.60.0.7.
Open Microsoft Edge on the Windows machine, click on the address bar, and type: 10.60.0.7
An “Access denied” message appears on the web page.
The Kali terminal window displays INTRUSION ATTEMPT DETECTED from 10.60.0.10:50061.
Note that the port numbers may vary.
In a real scenario, the system administrator where the honeypot is deployed can take the appropriate measures to strengthen a computer system’s defenses.
Test Honeypot Manual Configuration Functionality with Parrot.
IP Address of Parrot machine: 10.60.0.22
Run Pentbox in Kali Linux: ./pentbox.rb
Select the network tools section: 2
Open a new terminal in Parrot and run the telnet command followed by the Honeypot host IP address and the port number:

telnet 10.60.0.7 23
Test Honeypot Manual Configuration False message to show Functionality.
Apply the following manual configuration settings.

Port number: 80
Insert false message to show:
You are not allowed to access my system, so get the hell out of here now!
Save a log with intrusion? y
Press Enter for Default: */pentbox/other/log_honeypot.txt.
Activate beep sound? n
You will be notified that the HONEYPOT ACTIVATED ON PORT 80.
On the Parrot machine, on the browser, click on the address bar and type: 10.60.0.7
