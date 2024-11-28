<img src="/picturesv2/step74.JPG" alt="environmental_variables" width="800px">
<p> 
    Go into your app registrations, and click the function app. 
</p>
<img src="/picturesv2/step75.JPG" alt="environmental_variables" width="800px">
<p> 
    On the left panel, click on <b> Functions </b> and then select <b> Environmental Variables </b>. In the __init__.py file, it references IDs such as <b> tenant </b>, <b> client </b>, <b> client secret </b>, and <b> workspace </b>. This file pulls these values from config.py, which expects them to be set in the environmental variables. To start adding these items, click on <b> Add </b> and name each variable exactly as it is defined. Begin with <b> Workspace_ID </b>. 
</p>
<img src="/picturesv2/step76.JPG" alt="environmental_variables" width="800px">
<p> 
    To find the <b> Workspace ID </b>, navigate to your Log Analytics page and select <b> Properties </b>. Add the name in lowercase as defined in config.py, and copy the value to paste into the environmental variable.
</p>
<img src="/picturesv2/step77.JPG" alt="environmental_variables" width="800px">
<p> 
    It should look something like this. Repeat this process for the other required items. Remember the values you saved in your Google Docs or Notes? Use those values here. 
</p>
<img src="/picturesv2/step78.JPG" alt="environmental_variables" width="800px">
<p> 
    A <b> MISP key </b> will also be required. Go back to the MISP instance in your web browser, navigate to the page where authentication keys are managed, and create a new key. However, if you already copied the previously generated key to your notes, you can use that same value.
</p>
<img src="/picturesv2/step79.JPG" alt="environmental_variables" width="800px">
<p> 
    The final item the function needs is the <b> mispurl </b>. Copy and paste the URL used to access your MISP instance into the environmental variables. 
</p>
<img src="/picturesv2/step80.JPG" alt="environmental_variables" width="800px">
<p> 
    The Python script will also require a time trigger schedule. Follow the expression provided in the GitHub repository to implement this. 
</p>
<img src="/picturesv2/step81.JPG" alt="environmental_variables" width="800px">
<p> 
    Afterward, navigate to <b> Invocations and more </b>, where you can view the previously deployed code. 
</p>
<img src="/picturesv2/step84.JPG" alt="environmental_variables" width="800px">
<p> 
    In the <b> Code + Test </b> tab, you want to run the code to see if it works. 
</p>
<img src="/picturesv2/step85.JPG" alt="environmental_variables" width="800px">
<p> 
    As you can see, the function is pulling the environmental variables that we set earlier. Approximately around an hour or two, you can go back to Sentinal and open <b> Threat indicators </b> to confirm that everything is working correctly. 
</p>


