## Microsoft Sentinal? 
<p>
    After creating the VM, you can log into it by downloading the RDP file and using the password you created. However, to monitor logins via RDP (port 3389) and send alerts back to us, we need to add a tool. The tool in question is <b> Microsoft Sentinel </b>, a cloud-native Security Information and Event Management (SIEM) solution. This tool helps users and organizations monitor, detect, and respond to cyber threats.
</p>

<hr>

<img src="/picturesv2/step7.JPG" width="800px" alt="search-sentinal">
<p>
    Once the VM loads, search up <b> Microsoft Sentinal </b> and select it from the dropdown menu. 
</p>

<hr>

<img src="/picturesv2/step8.JPG" width="650px" alt="instance-details">
<p>
    Previously, we created a resource group to house all our resources. Now, we’ll create log analytics based on that group. Choose the resource group and name the container where analytics data will be stored. For the region, select the same one as before to ensure resources remain in the same region and avoid delays.
</p>

<hr>

<img src="/picturesv2/step9.1.JPG" width="650px" alt="creation of log analysis">
<p>
    Just like before, navigate to <b> Review + create </b> and click the blue <b> Create </b> button at the bottom left. After a few seconds, you should be redirected to a new page. Click <b >Add </b> at the bottom left to integrate Microsoft Sentinel with our log analytics workspace.
</p>

<hr>

<img src="/picturesv2/step10.JPG" width="650px" alt="data connectors">
<p>
    Once Sentinel is added, you’ll be directed to its dashboard. Select <b> Data connectors </b> and then click <b> More content at Content Hub </b>. This allows you to integrate data from various resources for security monitoring and analysis. For example, you can connect third-party firewalls, VPNs, or Azure Active Directory for advanced security analysis. 
</p>

<hr>

<img src="/picturesv2/step11.JPG" width="650px" alt="data connectors">
<p>
    Search for <b> Windows security events </b> and download this specific data connector. It collects security logs from the Windows computer and sends them to Microsoft Sentinel for monitoring and analysis. This helps detect unusual activity, such as failed login attempts, allowing you to respond appropriately.
</p>

<hr>

<img src="/picturesv2/step12.JPG" width="800px" alt="data-connectors-refresh">
<p>
    Go back to <b> Data connectors </b> and click the <b> Refresh </b> button. You’ll notice several data connectors installed, including the legacy version for collecting security events. However, the legacy version lacks performance and configuration capabilities. Microsoft is transitioning to the newer <b> AMA </b> (Analytical Monitoring Agent), which is more efficient in data collection and better suited for cloud-native environments. Click on the newer version and select <b> Open connector page </b>. The other data connectors displayed integrate seamlessly with the one we manually installed. 
</p>

<hr>

<img src="/picturesv2/step13.2.JPG" width="800px" alt="creation-of-data-collection-rule">
<p>
    Scroll up until you see <b> Logs </b> and copy the code written in the Query. 
</p>
<p>
    <b> SecurityEvent </b> refers to our table in Log Analytics. <b> where Activity contains "success" </b> refers to successful actions. In this case, we are looking for successful logons. <b> and Accounts !contains "system" </b> refers to not looking for accounts with the word "system" in it. This is because you would be alerted these incidents with system accounts as processes work in the background. 
</p>
<p>
    Once the query is written, click <b> New alert rule </b>
</p>

<hr>

<img src="/picturesv2/step14.JPG" width="600px" alt="rule-details">
<p>
    Name the rule something relevant to logging into the system, such as “RDP Login Monitoring.” Set the MITRE ATT&CK tactic to <b> Initial Access </b>, as we’re tracking verified sign-ins to detect unusual or unauthorized access attempts.
</p>

<hr>

<img src="/picturesv2/step15.1.JPG" width="600px" alt="rule-logic">
<p>
    Since we pre-wrote the rule, it will appear automatically. Change the query time to every <b> 5 minutes </b> to test if the rule works as expected.
</p>

<hr>

<img src="/picturesv2/step16.JPG" width="800px" alt="validate-rule">
<p>
    Navigate to the final step, <b> Review + create </b>, and wait for the validation process to complete. Once validated, click <b> Save </b> and head to the <b> Analytics </b> page to view the newly created rule. If the rule doesn’t appear immediately, click the <b> Refresh </b> button.  
</p>



