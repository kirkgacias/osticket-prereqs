
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites, Setup, and Installation</h1>
This guide details the necessary requirements and steps for installing osTicket, an open-source help desk ticketing system.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> 

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
</p>
<p>
<b>1.Create a Virtual Machine on Azure</b>
<p>The first step is to create a virtual machine on Azure. 
Choose the image or base operating machine as Windows 10 Pro, version 22H2.</p>
<p>
<img width="758" alt="VM setup-windows 10" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/a22b387c-d396-4fe5-8db9-7c2677941a30">

<p>
</p>
<p>
<strong> NOTE: Make sure to set the size to at least 2 vcpus and 16 GiB memory. 
And confirm that RDP (3389) is allowed in "Select inbound ports" in order to allow Remote Desktop access to the VM.</strong> </p>
<p>
<img width="757" alt="VM inbound ports" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/3eb204b9-a099-4656-a4ec-9d8badb1f56b">



</p>
<br />

<p>
</p>
<p>
<b>2. Review and Create</b> </p>
<p>Click on the last check box to confirm an eligible Windows 10 license then proceed to "Review + create". A validation process will occur then once it has passed simply continue to create.</p>

</p>
<br>
<p><strong>3.Find your VM's public IP address</strong></p>
<p></p>Allow some time for your deployment to complete then find your VM's public IP address and copy it.</p>
<p>
<img width="1009" alt="VM IP ADDRESS" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/f7720ced-3abc-49ad-8292-c7969da636f1">

</p>
<p>
4. Open your Remote Desktop Connection app and paste the VM's IP and login with the same login credentials used to create the VM.
<p>
<img width="302" alt="Remote desktop app" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/f331b259-db5b-447d-a05c-0367ef4297a0">


</p>
<br />
