## What is MISP? 
<p>
  MISP, also know as <b> Malware Information Sharing Platform </b> is an open source threat intelligence platform. It lets you store information such as malware, threats, and vulnerabilities in an organized manner. We can think of MISP like <b> Tableau </b> or <b>  PowerBI </b> which these platforms store and display information about business intelligence. In the case of MISP, it stores and displays information about cyber threat intelligence. 
</p>

<hr>

## What is Docker? 
<img src="/picturesv2/docker1.1.jpg" alt="docker-explanation" width="800px">
<p>
  In this, imagine you have created a Python application on your Windows computer that does data processing using specific libraries such as <b> Panda </b> and <b> NumPy </b>. You want to send this application to your co-worker who is working on a Linux machine so they can run it.         
</p>
<img src="/picturesv2/docker1.2.jpg" alt="docker-explanation" width="800px">
<p>
  When we send the application, a problem occurred? When our co-working installed those libraries on their OS, it was different from ours. The dependencies and configurations were different causing a failure in running the Python application. 
</p>
<img src="/picturesv2/docker1.3.jpg" alt="docker-explanation" width="800px">
<p>
  We are going to send the application in a docker container. Supposedly, by sending this application in a container, your co-worker does not need to manually install Python, Pandas, and NumPy on their Linux system. This container has everything included. Since this container uses a Linux-based Python image, it should behave the same on Windows and Linux. Also, Docker will isolate the environment, ensuring the Python script runs with the correct versian of Pandas and NumPy, regardless of what is installed on the host (application can run independently of the underlying OS). 
</p>
