<img src="/picturesv2/step17.JPG" width="600px" alt="no-incidents-yet">
<p>
    Under the <b> Threat management </b> tab, click on <b> Incidents </b>. You should see that there are <b> 0 incidents </b> logged. This is because we haven’t logged in via <b> RDP 3389 </b> yet. Since we specified filtering out <b> System accounts </b>, there are no incidents. If we hadn’t specified this, we would see a lot of alerts as background processes run regularly.
</p>

<hr>

<img src="/picturesv2/step18.JPG" width="600px" alt="download-rdp-file">
<p>
    In the search bar, navigate to the <b> Virtual Machine </b> page and click on <b> Connect </b>. Then, select <b> Download RDP file </b>. This file will be saved to your computer. 
</p>

<hr>

<img src="/picturesv2/step19.JPG" width="600px" alt="double-click-on-file">
<p>
    Locate the downloaded file in your file manager. It should appear like this. Double-click on the file to open it. 
</p>

<hr>

<img src="/picturesv2/step20.JPG" width="600px" alt="click-on-connect">
<p>
    You will see an <b>RDP connection</b> prompt. Click on <b>Connect</b> to proceed.
</p>

<hr>

<img src="/picturesv2/step21.JPG" width="600px" alt="your-password">
<p>
    Remember the <b> password </b> we created for the VM earlier? You’ll need it now to access the virtual machine.
</p>

<hr>

<img src="/picturesv2/step22.JPG" width="600px" alt="attempts">
<p>
    Once logged in, you’ll see a <b> Windows interface </b>, similar to logging into a regular computer. This is your <b> virtual environment </b>. Feel free to explore—try searching for something familiar. When you’re done, exit the environment and return to the <b> Incidents </b> tab. Wait approximately <b> 5 minutes </b> for a message to appear.
</p>
<p>
    In this case, you’ll see <b> Verified sign-ins </b>, which indicate successful logins via <b> RDP 3389 </b>. Below that, you’ll also see <b> Successful sign-ins </b>, which are related to non-RDP processes. These were filtered to exclude <b> System accounts </b>, preventing unnecessary noise from regular background processes. 
</p>
