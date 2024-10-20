<img src="/picturesv2/step1.jpg" width="500px" alt="click on create and second option">
<p>
  As we have seen those services at the top and clicked on Virtual machines, we are going to choose <b> Create </b> and then choose <b> Azure virtual machine with preset configuration. </b>
</p>

<hr> 

<img src="/picturesv2/step2.JPG" width="600px" alt="picking size of VM">
<p> 
For our use case, we are going to deploying the VM in a production environment and the default workload. We are not going to be needing large memory workloads. 
</p>

<hr>

<img src="/picturesv2/step3.JPG" width="800px" alt="selections">
<p>
  Create a new <b> resource group </b> and call it whatever you want. The <b> Resource Group </b> is a logical container that will hold all these resources such as storage accounts, virtual machines, databases and more. For example, it is like a lunchbox that contains different foods inside. It could be a juice box, sandwhich, crackers, or even chocolate that all play a certain role. Select a name for the VM and select what region you are in. THe last thing is to choose an <b> image </b> which is the operating sytem you want your VM.     
</p>

<hr> 

<img src="/picturesv2/step4.JPG" width="800px" alt="admin setup">
<p>
  We will choose 4 virtual central processing units in case we need more power. Create a username and password for your administrator account to get that superuser access. Next, this is the important part. If you take a look at the <b> Public inbound ports </b>, we have selected RDP 3389. This means that anyone on the public internet can access this VM over RDP. Even though, we have set up a password, people on the outside can use brute-force attacks to try and gain access to it. However, to test this, we want to keep this opened in the meantime. 
</p>
