<img src="/picturesv2/step1.jpg" width="500px" alt="click on create and second option">
<p>
    As we explore the services at the top and click on Virtual machines, we will select <b> Create </b> and then choose <b> Azure virtual machine with preset configuration </b>.
</p>

<hr> 

<img src="/picturesv2/step2.JPG" width="600px" alt="picking size of VM">
<p> 
    For our use case, we will be deploying the VM in a production environment with the default workload. We don’t require large memory workloads for this scenario.
</p>

<hr>

<img src="/picturesv2/step3.JPG" width="800px" alt="selections">
<p>
    Create a new <b> resource group </b> and name it whatever you prefer. A <b> Resource Group </b> is a logical container that organizes resources such as storage accounts, virtual machines, databases, and more. Think of it like a lunchbox that holds different items such as a juice box, sandwich, crackers, or chocolate—each serving a specific purpose. After naming your VM, select your region and choose an <b> image </b>, which determines the operating system for your virtual machine.     
</p>

<hr> 

<img src="/picturesv2/step4.JPG" width="800px" alt="admin setup">
<p>
    We will configure the VM with 4 virtual central processing units (vCPUs) to ensure enough processing power for potential needs. Create a username and password for your administrator account to gain superuser access. Now, pay attention to the <b> Public inbound ports </b> setting. We have selected RDP (port 3389), which allows anyone on the internet to access this VM via Remote Desktop Protocol. Although a password is set, attackers could still use brute-force methods to attempt access. For testing purposes, we’ll keep this port open for now.
</p>

<hr>

<img src="/picturesv2/step5.JPG" width="800px" alt="VM container">
<p>
    Name your virtual network—this can be any name of your choice. The purpose of this network is to create a secure space for virtual machines to communicate with other resources.
</p>

<hr>

<img src="/picturesv2/step6.JPG" width="800px" alt="review + create last step">
<p>
    Once the previous steps are complete, navigate to the <b>Review + create</b> tab. Review the settings, and then click the blue <b>Create</b> button at the bottom to finalize the process.
</p>
