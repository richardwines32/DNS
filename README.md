<h1>DNS</h1>
In this tutorial, we will be working with DNS. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server

<h2>Actions and Observations</h2>
<p>
1.  A-Record Exercise.  Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin).  Connect/log into Client-1 as an admin (mydomain\jane_admin).  From Client-1 try to ping “mainframe” notice that it fails.  

</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 25 17 PM" src="https://github.com/richardwines32/DNS/assets/162821778/b9834df5-0199-44c9-899a-5d69ddbd6d27">
 
</p>
<br />
<p>
 1A.  Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address. 
</p> 
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 32 54 PM" src="https://github.com/richardwines32/DNS/assets/162821778/ce944376-2469-4a6f-9465-6b47107ca165">
 
</p>

<br />
<p>
1B.  Go back to Client-1 and try to ping it. Observe that it works. 
</p>
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 36 54 PM" src="https://github.com/richardwines32/DNS/assets/162821778/48ff7798-4c89-43f6-b9da-5d872b54d4c3">
</p>

<br />
<p>
2.  Local DNS Cache Exercise.  Go back to DC-1 and change mainframe’s record address to 8.8.8.8.  

</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 44 15 PM" src="https://github.com/richardwines32/DNS/assets/162821778/12d51939-2004-4714-bc18-7632b227d1ad">

</p>

<br />
<p>
2A.  Go back to Client-1 and ping “mainframe” again.  Observe that it still pings the old address.  
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 47 23 PM" src="https://github.com/richardwines32/DNS/assets/162821778/cd41320b-6a15-424b-9233-4848f7334d9d">

</p>

<br />
<p>
2B.  Observe the local dns cache (ipconfig /displaydns).  Flush the DNS cache (ipconfig /flushdns).  Observe that the cache is empty.  Attempt to ping “mainframe” again. Observe the address of the new record is showing up.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
