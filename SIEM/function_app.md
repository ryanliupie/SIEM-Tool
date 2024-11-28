<p>
    We will continue following the outlined steps in the Github. 
</p>

<hr>

<img src="/picturesv2/step59.JPG" alt="function_app" width="800px">
<p>
    In the search bar in Azure, find <b> Function App </b> and click <b> Create </b>.
</p> 
<img src="/picturesv2/step60.JPG" alt="function_app" width="800px">
<p>
    The hosting option for this use case will be <b> App Service </b>, as it provides sufficient resources to pull data directly from the MISP instance into Sentinel. 
</p>
<img src="/picturesv2/step61.JPG" alt="function_app" width="800px">
<p>
    Choose the same resource group you’ve been using, and name the function app accordingly. It’s important to deploy the function app using code written in <b> Python </b>. Once done, click <b> Review + Create </b>.
</p>
<img src="/picturesv2/step62.JPG" alt="function_app" width="800px">
<p>
    After the deployment completes, note that the actual function will not be created in Azure directly; instead, it will be done using a different method 
</p>
<img src="/picturesv2/step63.JPG" alt="function_app" width="800px">
<p>
    Following the instructions in the GitHub guide, download the <b> misp2sentinel </b> repository as a ZIP file. 
</p>
<img src="/picturesv2/step64.JPG" alt="function_app" width="800px">
<p>
    Locate the ZIP file on your computer and unzip it to access all the contents. 
</p>

<img src="/picturesv2/step65.JPG" alt="function_app" width="800px">
<p> 
    If you haven’t already, download and install an IDE called VS Code. Then, install the <b> Azure Functions </b> extension.
</p>
<img src="/picturesv2/step66.JPG" alt="function_app" width="800px">
<p>
    Open the unzipped folder in the IDE. You should see all the files. If the files are not visible, try downloading, zipping, and unzipping again. 
</p>
<img src="/picturesv2/step67.JPG" alt="function_app" width="800px">
<p>
    In the left panel of VS Code, click on <b> Azure Functions </b>. Then, sign in to your Azure account by clicking <b> Sign in to Azure </b>. This step allows deployment to your Azure tenant. 
</p>
<img src="/picturesv2/step68.JPG" alt="function_app" width="800px">
<p>
     After signing in, the files should appear as shown in the example. If the structure looks different, ensure that the files are correctly unzipped and recheck.
</p>
<img src="/picturesv2/step69.JPG" alt="function_app" width="800px">
<p>
    Within the files, there is a specific script that pulls security events from the MISP instance using the API key and sends them to the Sentinel data connector. Since there is no multi-tenant support, you need to delete the snippet of code related to multi-tenancy. Failing to remove it will result in an error. 
</p>
<img src="/picturesv2/step70.JPG" alt="function_app" width="800px">
<p>
    Once the snippet is deleted, right-click on the main folder, <b> Azure Function </b>, and select <b> Deploy to Function App </b>. 
</p>
<img src="/picturesv2/step71.JPG" alt="function_app" width="800px">
<p>
    A pop-up message will appear. Click <b> Deploy </b> to proceed.
</p>
<img src="/picturesv2/step72.JPG" alt="function_app" width="800px">
<p>
    After deployment, the Azure Function App should display the deployed function.
</p>
<img src="/picturesv2/step73.JPG" alt="function_app" width="800px">
<p>
    Click into the function, then select <b> Code + Test </b>. Verify that the code matches what you had in the IDE and scroll down to ensure the snippet related to multi-tenancy has been deleted. If it hasn’t, delete it and redeploy.
</p>
<p>
     Note that the deployment process can take up to 10 minutes. If the function does not display in Azure after this time, there is likely an error that needs troubleshooting. 
</p>


