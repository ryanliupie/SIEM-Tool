## What is Docker? 
<img src="/picturesv2/docker1.1.jpg" alt="docker-explanation" width="800px">
<p>
    Imagine you’ve created a Python application on your Windows computer that processes data using specific libraries like Pandas and NumPy. Now, you want to send this application to a co-worker who is working on a Linux machine so they can run it.        
</p>
<img src="/picturesv2/docker1.2.jpg" alt="docker-explanation" width="800px">
<p>
    However, when you send the application, a problem occurs. When your co-worker installs those libraries on their operating system, the dependencies and configurations differ from yours. This discrepancy causes the Python application to fail to run. 
</p>
<img src="/picturesv2/docker1.3.jpg" alt="docker-explanation" width="800px">
<p>
    To solve this issue, we send the application inside a <b> Docker container </b>. By using a container, your co-worker doesn’t need to manually install Python, Pandas, or NumPy on their Linux system. The container includes everything required to run the application. Since the container uses a Linux-based Python image, it behaves consistently on both Windows and Linux systems. Docker also isolates the environment, ensuring the Python script runs with the correct version of Pandas and NumPy, regardless of the host system’s setup. This means the application can run independently of the underlying operating system.
</p>
<img src="/picturesv2/docker1.4.jpg" alt="docker-explanation" width="800px">
<p>
    This time, when the application is sent, the Linux user can successfully run it! Keep in mind that a Docker container is not the same as a virtual machine. A virtual machine includes a full operating system for each application, which requires significant resources and costs. Docker containers, however, share the host OS kernel and only package what is necessary to run the application. This makes them lightweight and efficient. It’s a way to package software that can run on any supported hardware.
</p>

<hr>

<img src="/picturesv2/step23.JPG" alt="docker-explanation" width="800px">
<p>
    We are going to create a new virtual machine, but this time, the OS we want to use is Linux-based, specifically <b>Ubuntu</b>. This will allow us to connect via Secure Shell (SSH) on port 22. 
</p>
<img src="/picturesv2/step24.JPG" alt="docker-explanation" width="800px">
<p>
    Once the virtual machine is created, we are going to click on <b> Connect </b>, then select <b> SSH using Azure CLI </b>.  
</p>
<img src="/picturesv2/step25.JPG" alt="docker-explanation" width="800px">
<p>
    A terminal will pop up, and it will ask if we want to continue connecting. We will type <b> yes </b> to proceed.
</p>
<img src="/picturesv2/step26.JPG" alt="docker-explanation" width="800px">
<p>
    We will keep the terminal open and install Docker by following the steps provided on this website: <a href="https://docs.docker.com/engine/install/ubuntu/"> dockerdocs </a>. We need to set up a Docker apt repository because Docker has dependencies that apt can install and resolve. This ensures that we are installing the official version of Docker and allows for automatic updates. Run the commands individually—when I tried running them all at once, it caused issues with the system.
</p>
<img src="/picturesv2/step27.JPG" alt="docker-explanation" width="800px">
<p>
    Next, we will install the Docker packages. These packages are the core of Docker, enabling us to create, manage, and execute Docker containers.
</p>
<img src="/picturesv2/step29.JPG" alt="docker-explanation" width="800px">
<p>
    After installation, you should see that the Docker service is up and running. If there are any issues, try repeating the entire process.
</p>