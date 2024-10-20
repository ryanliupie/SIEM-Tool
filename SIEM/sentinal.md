## What is Microsoft Sentinal? 
<p>
  After creating the VM, you can simply log into it by downloading the RDP file and logging in with the password you created. However, since we want to monitor when we log in with RDP 3389 and sent an alert back to us, we need to add a tool. The tool in question is <b> Microsoft Sentinal </b>, where it is a cloud-native Security and Event Management (SIEM) solution. This helps users or organizations monitor, detect, and respond to cyber threats.
  
<hr>

</p>
<img src="/picturesv2/step7.JPG" width="800px" alt="search-sentinal">
<p>
  Once the VM loads in, search up <b> Microsoft Sentinal </b> and click on it in the drop down below.  
</p>

<hr>

<img src="/picturesv2/step8.JPG" width="650px" alt="instance-details">
<p>
  Before, we made a resource group that houses all of our resources. We want to create log analytics based off that group which is why we must select that option. Right after, we can name the information that will have those analytics stored in them, like a container mentioned previously. For the region, select the same region from before as you want resources in the same region to avoid delay. 
</p>

<hr>

<img src="/picturesv2/step9.1.JPG" width="650px" alt="creation of log analysis">
<p>
  Just like last time, go to <b> Review + create </b> and hit the blue <b> Create </b> button on the bottom left. After a couple seconds, you should be prompted with this page shown. At the bottom left, click on <b> Add </b>. This will add Microsoft Sentinal to our log analytics workspace. 
</p>

<hr>

<img src="/picturesv2/step10.JPG" width="650px" alt="data connectors">

