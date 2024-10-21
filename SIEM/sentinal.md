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
<p>
  Once sentinal is added, you will take you to this page. Click on <b> Data connectors </b> and then click on <b> More content at Content Hub </b>. This lets you add data from many resources for security monitoring and analysis. For instance, you can bring in third party firewalls or VPNS. You could also add in Azure active directory. This will let you push the threshold for more in depth security analysis of incidents. 
</p>

<hr>

<img src="/picturesv2/step11.JPG" width="650px" alt="data connectors">
<p>
  Search <b> Windows security events </b> and download this specific data connector. This collects security logs from the Windows computer and sends them to Microsoft Sentinal for monitoring and analysis. It will help detect unusual activity such as failed login attempts in which you can respond to it. 
</p>

<hr>

<img src="/picturesv2/step12.JPG" width="800px" alt="data-connectors-refresh">
<p>
  Go back to data connectors and click the <b> refresh </b> button. You will see that there are two connectors installed. The legacy version collects those security events but it lacks performance and configuration. Microsoft has been trying to move away from it and replacing it with the <b> AMA </b> analytical agent. This is far more efficent in terms of data collection while integrating improved cloud-native environments. Click on the newer version and then clikc on <b> Open connector page </b>. 
</p>

<hr>

<img src="/picturesv2/step13.JPG" width="800px" alt="creation-of-data-collection-rule">
<p>
  Cick on <b> +Create data collection rule </b> and make up a name in relation to signing in via RDP and then select the same resource group. The purpose of this is to collect data based on the rule you provide to filter out unnecessary data. 
</p>
