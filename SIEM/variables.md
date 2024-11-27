<img src="/picturesv2/step74.JPG" alt="environmental_variables" width="800px">
<p> 
    Go into your app registrations, and click the function app. 
</p>
<img src="/picturesv2/step75.JPG" alt="environmental_variables" width="800px">
<p> 
    On the left panel, click on <b> Functions </b> and hit <b> Environmental Variables </b>. In the __init__.py file, it looks for IDs refering to <b> tenant </b>, <b> client </b>, <b>  client secret </b>, and <b> workspace </b>. This file pulls from the config.py and it looks for these items in the environmental variables that must be set. Therefore to start adding these items, click on <b> Add </b> and the name the item exactly. We will start with the Workplace_ID. 
</p>
<img src="/picturesv2/step76.JPG" alt="environmental_variables" width="800px">
<p> 
    To get the <b> Workspace ID </b>, go back to your log analytics page, and then select <b> Properties </b>. Add the name is lowercase just as in the config.py is, and copy the value after. 
</p>
<img src="/picturesv2/step77.JPG" alt="environmental_variables" width="800px">
<p> 
    It should look something like this, and we are going to do this for the other items as well. Remember the values you copied to your google docs or notes? Those values will be pasted here. 
</p>
<img src="/picturesv2/step78.JPG" alt="environmental_variables" width="800px">
<p> 
    A misp key will also be needed; go back to the MISP instance on the web browser; go to page where the the authentication is located and create a new key. However, remember that very important value that was copied to your google docs or notes? Use that same one. 
</p>
<img src="/picturesv2/step79.JPG" alt="environmental_variables" width="800px">
<p> 
    The last item that the function wants to know is the <b> mispurl </b>. Copy and paste the url where you access the misp instance from into the environmental variables. 
</p>
<img src="/picturesv2/step80.JPG" alt="environmental_variables" width="800px">
<p> 
    The python script will also look for a time trigger schedule and by following the expression given in the repository, that can be implemented easily. 
</p>
<img src="/picturesv2/step81.JPG" alt="environmental_variables" width="800px">
<p> 
    After, go to <b> Invocations and more </b> where you will be able see the code previously. 
</p>
<img src="/picturesv2/step82.JPG" alt="environmental_variables" width="800px">
<p> 
    You want to create two separate tabs. The first tab will contain <b> Code + Test </b>. This is where we will run the code to test if it works. 
</p>
<img src="/picturesv2/step83.JPG" alt="environmental_variables" width="800px">
<p> 
    The second tab will be <b> Logs </b>. This would allow us to see cleary what happens when the code runs. 
</p>
<img src="/picturesv2/step84.JPG" alt="environmental_variables" width="800px">
<p> 
    Run the code. 
</p>
<img src="/picturesv2/step84.JPG" alt="environmental_variables" width="800px">
<p> 
    As you can see, the logs appear at the bottom, which means you do not neccesarily have to open both tabs, but just for clarity we can. Aside of this, you can see that the function is pulling the environmental variables that we set earlier. Approximately around an hour or two, you can go back to Sentinal and open <b> Threat indicators </b>.
</p>


