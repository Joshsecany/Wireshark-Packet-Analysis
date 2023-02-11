# Wireshark-Packet-Analysis
For this project I'm analyze network protocols traffic that flows to the VM. Wireshark is a free service that is already install in Kali Linux environment. 

Programs
1. Wireshark

Virtual Environments
1. Kali Linux
2. Windows 10 

                                                   Brief description on Wireshark
Wireshark is the most commonly used and world’s foremost network protocol analyzer. It enables one to observe the network on a microscopic level and let’s one analyze what is happening on thenetwork. It is a standard tool used by many non-profit, educational and commercial organizations alike.

                                                    Steps to install:
1. Install wireshark using this link: https://www.wireshark.org/download.html
2. Download the installer as per your file system configurations
3. Find the installer file of Wireshark you downloaded then open it.
4. As you go through the installtion you can agree to the settings. Once everythig is set you can click on finsih to complete the installtion of Wireshark.

![image](https://user-images.githubusercontent.com/89609767/218195508-ea372fc3-f6f2-4cfa-b3b1-96c78b31b6a6.png)

                                                    How to use display filters on Wireshark:
1. Filters are used to view packets to meet a specific criterion. 
2. When using analysis to help isolate a specific conversation to find malware.
3. The display filters has three colors. Red expressions for not accepted traffic, yellow is expression that is accpeted but is not working as expected, green expression is what has been accepted and will work.
![image](https://user-images.githubusercontent.com/89609767/218199011-617c0d05-5f66-4544-a421-3c539e54acaf.png)

                                                    How to use Boolean searches:
1. You can use Boolean expressions to display filter in specifying values and combining them.
2. And: && or and 
3. Equals: == or eq
4. Or: ||(double pipe) or or

                                                    Identify HTTP Traffic
1. To start I have creat a pcapng file that you can record by starting Wireshark as admin.
2. Once I started Wireshark, I went to internet explorer then click on www.google.com.
3. Once I get to google I stop the Wireshark services which recored pcapng file.
4. I turn on the display filters for HTTP traffic and boom here are the logs.
![image](https://user-images.githubusercontent.com/89609767/218206648-98ac4f56-6fba-4dcb-ad29-3b78a40479c4.png)

                                                   Identify a 3-way handshake
1. In this example you will see a 3-way handshake between two IP addresses.
2. The 3-way handshake is packets being sent to another host address. You can confirm this by [SYN] message in Wireshark. 
3. After the [SYN] message I look in the logs for a response back. The proper response from the second IP is [SYN, ACK] message.
4. To end the handshake first IP address send [ACK] message to the second IP address and it has your 3 way handshake. 
![image](https://user-images.githubusercontent.com/89609767/218211921-42cf21f4-60f1-4581-90f1-95a2c96c9df8.png)

                                                

