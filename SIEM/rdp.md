<img src="/picturesv2/step17.JPG" width="600px" alt="no-incidents-yet">
<p>
  Under the Threat management tab, click on <b> Incidents </b>. You should see that there are 0 incidents that have been logged. This is because we have not logged in via RDP 3389 yet. Since we specified to filter out System accounts, there are no incidents. If we did not specifiy it, we would get ton of alerts as background processes keep running. 
</p>

<hr>

<img src="/picturesv2/step18.JPG" width="600px" alt="download-rdp-file">
<p>
  In the search bar, we are going to head to <b> Virtual Machine </b> page and then click on <b> Connect </b>. Once you are there, click on <b> Download RDP file </b> which will be downloaded to your computer. 
</p>

<hr>

<img src="/picturesv2/step19.JPG" width="600px" alt="double-click-on-file">
<p>
  The file should look like this in your file manager. Double click on the file to open it. 
</p>

<hr>

<img src="/picturesv2/step20.JPG" width="600px" alt="click-on-connect">
<p>
  You will be prompted a RDP page, please click on <b> Connect </b>
</p>

<hr>

<img src="/picturesv2/step21.JPG" width="600px" alt="your-password">
<p>
  Remember earlier when we made a password for the VM? We are going to need that to be able to access it.
</p>

<hr>

<img src="/picturesv2/step22.JPG" width="600px" alt="attempts">
<p>
  Once you are logged in, you will see a windows display just like how you normally log into a computer. This would be your virtual environment. Play around with it; try searching up something familiar. Once you're done, exit at the top and head to <b> Incidents </b> and wait 5 minutes until an message pops up. In this case, we can see <b> Verifed sign ins </b>. This message displayed because we logged in VIA RDP 3389 and it logged it. Right underneath, it says <b> Successful Sign ins </b>. As mentioned earlier we did not want to see system accounts as they would pop up regularily. Those <b> Successful Sign in </b> incidents are those processes which are different from RDP 3389. 
</p>
