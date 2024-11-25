<img src="/picturesv2/step48.JPG" alt="misp-to-docker" width="800px"> 
<p>
  Just like how we installed the <b> Windows Security Events </b> data connector, we also have to install the <b> MISP2Sentinal </b> data connector. This lets us push threat indicators from MISP to Microsoft Azure, where Azure would be able to automatically process threat indicators and block them for an organization. By pushing on Azure, we do not need to access MISP through web browser as we can centralize security monitoring all in one place. 
</p>
<img src="/picturesv2/step49.JPG" alt="misp-to-docker" width="800px"> 
<p>
  Refresh the data connector page and click into the data connector we installed. There is additional setup required where we can follow a Github that helps us out with that using the <b> Upload Indicators API </b>
</p>
<img src="/picturesv2/step50.JPG" alt="misp-to-docker" width="800px"> 
<p>
  We need to register an application in our Azure tenant. Provide a name for the application in relation, leave everything in default and click <b> Register </b>. 
</p>
<img src="/picturesv2/step50.JPG" alt="misp-to-docker" width="800px"> 
<p>
  Go to certificates and secrets and create a new client secret. Rename it to something similar and click <b> Add </b>. You will get a value with the secret key which is extremely important later on. Keep a copy of it somewhere such as your online notes.  
</p>





<b>  </b>

<p>

</p>