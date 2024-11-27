<img src="/picturesv2/step48.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Just like how we installed the <b> Windows Security Events </b> data connector, we also have to install the <b> MISP2Sentinal </b> data connector. This lets us push threat indicators from MISP to Microsoft Azure, where Azure would be able to automatically process threat indicators and block them for an organization. By pushing on Azure, we do not need to access MISP through web browser as we can centralize security monitoring all in one place. 
</p>
<img src="/picturesv2/step49.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Refresh the data connector page and click into the data connector you installed. There is additional setup required where we can follow a Github that helps us out with that using the <b> Upload Indicators API </b>
</p>
<img src="/picturesv2/step50.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    You need to register an application in our Azure tenant. Provide a name for the application in relation, leave everything in default and click <b> Register </b>. 
<img src="/picturesv2/step50.5.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    There will be 3 values that will have to be copied down somewhere either in google docs or simply your notes on macOS. Copy down the <b> client ID </b> <b> Object ID </b>, and the <b> Tenant ID </b>. 
</p>
<img src="/picturesv2/step51.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Go to certificates and secrets and create a new client secret. Rename it to something similar and click <b> Add </b>. You will get a value with the secret key which is extremely important later on. Keep a copy of it somewhere just as last time. 
</p>
<img src="/picturesv2/step52.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    You will get a value with the secret key which is extremely important later on. Keep a copy of it somewhere such as in google docs or notes if you are using macOS. 
</p>
<img src="/picturesv2/step53.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Go to the LogAnalytics you created, click on <b> Add role assignment </b>
</p>
<img src="/picturesv2/step54.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Scroll down to <b> Microsoft Sentinal Contributer </b> then hit <b> next </b>. 
</p>
<img src="/picturesv2/step55.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Where it says Members, click on <b> +select members </b>. Previously, a registered app was created, search for it, hit <b> Select </b> then <b> Review + assign </b>. 
</p>
<img src="/picturesv2/step56.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Now, it has been added to the Sentinal Contributor role. This is important because this will let MISP to interact with Microsoft Sentinal. As mentioned before, Sentinal will collect, analyze, and respond to the security data that MISP has. 
</p>
<img src="/picturesv2/step57.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    Go back to the MISP instance on your web browser, click on <b> Administration </b>, then <b> auth keys </b>. From here you want to create a new authentication key, click on hit <b> +Add Authentication Key </b>, then <b> Submit </b>. 
</p>
<img src="/picturesv2/step58.JPG" alt="misp-to-sentinal" width="800px"> 
<p>
    The authentication key will be generated, and make sure to note it down in your google docs or notes app. 
</p>
