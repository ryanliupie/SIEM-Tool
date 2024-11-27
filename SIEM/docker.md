## What is Docker? 
<img src="/picturesv2/docker1.1.jpg" alt="docker-explanation" width="800px">
<p>
    In this, imagine you have created a Python application on your Windows computer that does data processing using specific libraries such as <b> Panda </b> and <b> NumPy </b>. You want to send this application to your co-worker who is working on a Linux machine so they can run it.         
</p>
<img src="/picturesv2/docker1.2.jpg" alt="docker-explanation" width="800px">
<p>
    When we send the application, a problem occurred? When your co-worker installed those libraries on their OS, it was different from ours. The dependencies and configurations were different causing a failure in running the Python application. 
</p>
<img src="/picturesv2/docker1.3.jpg" alt="docker-explanation" width="800px">
<p>
    We are going to send the application in a <b> docker container </b>. Supposedly, by sending this application in a container, your co-worker does not need to manually install Python, Pandas, and NumPy on their Linux system. This container has everything included. Since this container uses a Linux-based Python image, it should behave the same on Windows and Linux. Also, Docker will isolate the environment, ensuring the Python script runs with the correct version of Pandas and NumPy, regardless of what is installed on the host (application can run independently of the underlying OS). 
</p>
<img src="/picturesv2/docker1.4.jpg" alt="docker-explanation" width="800px">
<p>
    This time, the application was sent, and the Linux user was able to use it! Remember that a docker container is not a separate VM. That would be a separate OS for each application, where it would require an intense amount of money and resources. Instead, docker containers share the host OS kernel, meaning they do not need their own full operating system. This makes the container lightweight by only packaging what is neccesary to run the application. <b> It is a way to package software that can run on any hardware supported. </b>
</p>

<hr>

<img src="/picturesv2/step23.JPG" alt="docker-explanation" width="800px">
<p>
    We are going to create new virtual machine, but this time, the OS we will want to make is Linux based, specifically <b> Ubuntu </b>. This would let us connect via Secure Shell (SSH) port 22. 
</p>
<img src="/picturesv2/step24.JPG" alt="docker-explanation" width="800px">
<p>
    Once the  virtual machine is created, we are going to click on <b> Connect </b> then <b> SSH using Azure CLI </b>.  
</p>
<img src="/picturesv2/step25.JPG" alt="docker-explanation" width="800px">
<p>
    A terminal will pop up and it will ask if we want to continue connecting, so we are going to write <b> yes </b>
</p>
<img src="/picturesv2/step26.JPG" alt="docker-explanation" width="800px">
<p>
    We are going to keep the terminal open and install docker using this website <a href="https://docs.docker.com/engine/install/ubuntu/"> dockerdocs <a/>. We have to set up a Docker apt respository because Docker has dependencies that that apt can install and resolve. It lets us know that we are installing the actual version of docker and allows for automatic updates. Go back and run these commands individually. When I did this all together, it confused the system. 
</p>
<img src="/picturesv2/step27.JPG" alt="docker-explanation" width="800px">
<p>
    Then, we have to install the Docker packages. This is the heart of Docker which creates, manages, and executes Docker containers.
</p>
<img src="/picturesv2/step29.JPG" alt="docker-explanation" width="800px">
<p>
    After installation, you should see that the Docker service is up and running. If there are any issues, try the entire process again. 
</p>