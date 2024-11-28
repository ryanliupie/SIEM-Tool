<img src="/picturesv2/step48.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Just like when we installed the <b> Windows Security Events </b> data connector, we also need to install the <b> MISP2Sentinel </b> data connector. This enables us to push threat indicators from MISP to Microsoft Azure, where Azure can automatically process and block these indicators for the organization. By integrating with Azure, we can centralize security monitoring in one place, eliminating the need to access MISP through a web browser.
</p>
<img src="/picturesv2/step49.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Refresh the data connector page and click into the data connector you installed. There is additional setup required where we can follow a Github that helps us out with that using the <b> Upload Indicators API </b>
</p>
<img src="/picturesv2/step50.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    ou need to register an application in your Azure tenant. Provide a relevant name for the application, leave all settings at their default values, and click <b> Register </b>.
</p>
<img src="/picturesv2/step50.5.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    You will be provided with three critical values that you need to save: the <b> Client ID </b>, <b> Object ID </b>, and <b> Tenant ID </b>. Ensure you store these securely, such as in Google Docs or Notes on macOS. 
</p>
<img src="/picturesv2/step51.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Navigate to the Certificates and Secrets section and create a new client secret. Assign it a descriptive name and click <b> Add </b>. You will receive a secret key, which is essential for later steps. Make sure to save it securely, just as before. 
</p>
<img src="/picturesv2/step52.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    The secret key should be a combination of letters and numbers.  
</p>
<img src="/picturesv2/step53.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Go to the LogAnalytics workspace you created and click on <b> Add role assignment </b>
</p>
<img src="/picturesv2/step54.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Scroll down to select <b> Microsoft Sentinel Contributor </b> and click <b> Next </b>.
</p>
<img src="/picturesv2/step55.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    In the Members section, click on <b> +Select members </b>. Search for the previously registered app, select it, and then click <b> Review + assign </b>. 
</p>
<img src="/picturesv2/step56.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    The app is now added to the <b> Sentinel Contributor </b> role. This is a crucial step, as it allows MISP to interact with Microsoft Sentinel. Sentinel will collect, analyze, and respond to the security data provided by MISP. 
</p>
<img src="/picturesv2/step57.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Go back to your MISP instance in the web browser, click on <b> Administration </b>, then <b> Auth Keys </b>. Create a new authentication key by clicking <b> +Add Authentication Key </b> and then <b> Submit </b>.
</p>
<img src="/picturesv2/step58.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    An authentication key will be generated. Be sure to note it down in a secure location, such as Google Docs or the Notes app. This key is important for later use. 
</p>
