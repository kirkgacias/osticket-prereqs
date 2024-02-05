
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
<img width="1009" alt="VM IP ADDRESS" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/9b3ffb24-60c9-421d-a22e-c4035c1b9fe4">


</p>
<p>
<strong> 4.Connect to your VM using the Remote Desktop Connection app </strong> </p>
<p>Open your Remote Desktop Connection app and paste the VM's IP and login with the same login credentials used to create the VM.</p>
<p>
<img width="302" alt="Remote desktop app" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/f331b259-db5b-447d-a05c-0367ef4297a0">


</p>
<br />
<p><strong> 5. Enable IIS </strong></p>
<p> Once the VM is open, we will have to install / enable IIS. Go to the Control Panel and open the programs applet. Under programs, select "Turn Windows features on or off".</p>
<p> <img width="552" alt="CONTROL PANEL PROGRAMS" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/52defb88-4165-4b34-bbea-8292bc2890c8">

  
</p>
<p>Then you will have to enable and expand the following features:</p>
<p><img width="295" alt="Checklist 2" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/0b7b096f-43e7-47a8-a3ef-5500a360453d">
</p>
<p> [X] Internet Information Services</p>
<p>[X] Web Management Tools </p>
<p>[X] IIS Management Console </p>
<p>[X] World Wide Web Services  </p>
<p>[X] Application Development Features </p>
<p>[X] CGI</p>
<p>[X] Common HTTP Features</p>
<br>
<p> Click okay and the features should be enabled.</p>
<br>
<p> <strong> NOTE: To quickly test if the changes were applied succesfully, simply type 127.0.0.1 on your browser and the page below should appear. </strong></p>
<img width="1094" alt="WINDOWS IIS" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/4836fb28-6fcf-403d-853b-f412c707295c">
<br> <br>
<p> <strong> 6. Download and Install PHP Manager</strong></p> <p> Simply download and install PHP manager from the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>(PHPManagerForIIS_V1.5.0.msi) 
</p> <br>
<p><img width="386" alt="PHP Manager" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/566a1c1c-3731-4ff7-a74c-10a21b84a851">
</p> 
<br>
<p> <strong> 7. Download and Install the Rewrite Module</strong></p>
<p> Download and install the rewrite module (rewrite_amd64_en-US.msi) from the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> </p>
<p><img width="386" alt="rewrite module" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/177cc396-71e3-4658-9084-3e6fae94c1a5"></p>
<p> <strong> 8.Create a new directory</strong></p>
<p>Proceed to File Explorer and create the directory C:\PHP </p>
<img width="647" alt="PHP" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/683aa120-d73c-4bce-bf6d-f58309fdac5c">
<br>
<br>
<p><strong> 9.Download and install php-7.3.8-nts-Win32-VC15-x86.zip </strong></p>
<p> Download and install php-7.3.8-nts-Win32-VC15-x86.zip from the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> and unzip the contents into the newly created C:\PHP </p>
<img width="631" alt="PHP zip" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/b43949f3-78a7-4ab8-a526-dfd4f159d2d6">
<br>
<p><strong> 10.Download and install VC_redist.x86.exe </strong></p>
<br>
<p><strong> 11.Download and install MySQL 5.5.62 </strong></p>
<p> Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>  and select the following configurations; </p>
<p> [X] Typical Setup</p>
<p>[X] Launch Configuration Wizard after install </p>
<p>[X]Standard Configuration 
</p>
<br>
<img width="383" alt="mysql" src="https://github.com/kirkgacias/osticket-prereqs/assets/158519921/964a5ada-7d58-4efd-a0f2-6744610d999d">












