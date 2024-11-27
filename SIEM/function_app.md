<p>
    We will continue following those steps listed from that GitHub.
</p>

<hr>

<img src="/picturesv2/step59.JPG" alt="function_app" width="800px">
<p>
    In the search in Azure, find Function App and hit <b> Create </b>
</p> 
<img src="/picturesv2/step60.JPG" alt="function_app" width="800px">
<p>
    The hosting option in this use case would be <p> App Service </p> which would provide enough resources to pull from the MISP instance directly in sentinel. 
</p>
<img src="/picturesv2/step61.JPG" alt="function_app" width="800px">
<p>
    Choose the same exact resource group, and name the function app in relation. One important thing to do is deploy the function app in code in <b> Python </b>. After, simply hit <b> Review + Create </b>. 
</p>
<img src="/picturesv2/step62.JPG" alt="function_app" width="800px">
<p>
    Once it deploys, instead of creating the actual function in Azure, it will be done another way. 
</p>
<img src="/picturesv2/step63.JPG" alt="function_app" width="800px">
<p>
    Following the instructions, download the misp2sential repository via ZIP. 
</p>
<img src="/picturesv2/step64.JPG" alt="function_app" width="800px">
<p>
    Locate where the file is on your computer, and unzip the file to get access to all the contents. 
</p>

<img src="/picturesv2/step65.JPG" alt="function_app" width="800px">
<p> 
    If you haven't already done so, download an IDE called VS Code and install <b> Azure Functions </b>
</p>
<img src="/picturesv2/step66.JPG" alt="function_app" width="800px">
<p>
    Open the unzipped file into the IDE, and you should see all the files there. If not, try downloading, zipping, and unzipping again. 
</p>
<img src="/picturesv2/step67.JPG" alt="function_app" width="800px">
<p>
    On the left panel, Azure functions should be there, click on it, and sign in to your Azure account by clicking <b> Sign in to Azure </b>. This will let us deploy to the Azure tenant. 
</p>
<img src="/picturesv2/step68.JPG" alt="function_app" width="800px">
<p>
    As you can see, the files should look something like this. 
</p>
<img src="/picturesv2/step69.JPG" alt="function_app" width="800px">
<p>
    This file pulls the security events from the MISP instance using the API key, and sends it to the sentinel data connector. Since there is no multi tenant, that snippet of code needs to be deleted otherwise an error will occur. 
</p>
<img src="/picturesv2/step70.JPG" alt="function_app" width="800px">
<p>
    Once that snippet of code is deleted, you want to right click on the main folder <b> Azure Function </b> and select <b> Deploy to Function App </b>. 
</p>
<img src="/picturesv2/step71.JPG" alt="function_app" width="800px">
<p>
    It will show a pop up message; click <b> Deploy </b>
</p>
<img src="/picturesv2/step72.JPG" alt="function_app" width="800px">
<p>
    The function app in Azure should display the function that was deployed right before. 
</p>
<img src="/picturesv2/step73.JPG" alt="function_app" width="800px">
<p>
    Click into the function, the hit <b> Code + Test </b> and you should see the function that previously in the IDE. Scroll down and double check if the code associated with multi-mode has been deleted. If it has, move onto the next step, if it hasn't, redeploy. Mind you, when you deploy the function it will take up to 10 minutes, after that, if no function displays, there is an error. 
</p>

