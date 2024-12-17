## What is MISP? 
<p>
    MISP, also known as <b> Malware Information Sharing Platform </b>, is an open-source threat intelligence platform. It lets you store information such as malware, threats, and vulnerabilities in an organized manner. We can think of MISP like <b> Tableau </b> or <b> PowerBI </b>, where these platforms store and display information about business intelligence. In the case of MISP, it stores and displays information about cyber threat intelligence. Many companies around the world collaborate by providing feeds to detect any instances of an attack. 
</p>

<img src="/picturesv2/step30.JPG" alt="misp-to-docker" width="800px">
<p>
    Before anything, double-check to see if the installation of Docker was successful with the command <b> sudo docker run hello-world </b>. Docker should say "Hello" to you. If it does not, redo the installation. Since we are configuring MISP on Docker, we need to clone a repository that contains the image to do so. Clone this <a href="https://github.com/MISP/misp-docker">repository </a> to the terminal.
</p>
<img src="/picturesv2/step31.JPG" alt="misp-to-docker" width="800px">
<p>
    We want to <b> cd misp-docker </b>, where "cd" means change directory. Since we need to get into the repo we cloned, we cd into that one. Once inside, follow the next instruction and run <b> cp template.env .env </b>. This command will copy the template.env file and create a .env file where we can customize configurations. 
</p>
<img src="/picturesv2/step32.JPG" alt="misp-to-docker" width="800px">
<p>
    Edit the file with <b> nano.env </b>, where "nano" lets you edit any file you create. 
</p>
<img src="/picturesv2/step33.JPG" alt="misp-to-docker" width="800px">
<p>
    Scroll down to where you see <b> BASE_URL </b>. Here, we are going to type the public IP address of the virtual machine that we initially created. This allows us to access the MISP instance externally (outside the localhost on the Ubuntu virtual machine), such as opening it in a web browser. Save the change and exit the file. 
</p>
<img src="/picturesv2/step34.JPG" alt="misp-to-docker" width="800px">
<p>
    Run <b> sudo docker compose pull </b> to download the latest version of the Docker images defined in the docker-compose.yml file. 
</p>
<img src="/picturesv2/step35.JPG" alt="misp-to-docker" width="800px">
<p>
    Now we want to spin up the Docker container using <b> sudo docker compose up </b>. This may seem to hang for a while, almost like a glitch. To verify if the process worked, run <b> sudo docker ps </b>, where you will see all the active containers.
</p>
<img src="/picturesv2/step37.JPG" alt="misp-to-docker" width="800px">
<p>
    If we take a look here, SSH port 22 is open in the inbound rules. On a production VM, having this open is a security risk as anyone can try to gain access. You would need to add security measures to mitigate this. However, because we want quick access, we will leave it open for now. Besides this, we need to add a new inbound rule. Click on <b> Network settings </b> and then <b> Inbound port rule </b>.
</p>
<img src="/picturesv2/step38.JPG" alt="misp-to-docker" width="800px">
<p>
    The inbound port we need to add is port 443, also known as HTTPS. This will allow us to connect to the MISP instance from anywhere, including a local computer or multiple virtual machines you create. This corresponds to the BASE_URL we specified in the .env file. By applying this inbound port, we can simply access <b> https://4.206.218.123 </b>. 
</p>
<img src="/picturesv2/step39.JPG" alt="misp-to-docker" width="800px">
<p>
    Once we enter that URL into our browser, it will first display a <b> connection not secure </b> warning. This is okay because there is no certificate signed by a CA on the website. Since we know where the connection leads, simply click "OK," and it will take you to the login page. 
</p>
<img src="/picturesv2/step40.JPG" alt="misp-to-docker" width="800px">
<p>
    Just like when setting up a new router, there are default credentials in place. Since we do not know what they are, use these credentials to log in. 
</p>
<img src="/picturesv2/step41.JPG" alt="misp-to-docker" width="800px">
<p>
    As we can interpret, if someone were to gain access to this, they could easily exploit the system, which poses a major security risk. We need to change the password to something strong and challenging enough to avoid password attacks.
</p>
<img src="/picturesv2/step42.JPG" alt="misp-to-docker" width="800px">
<p>
    Click on this link <a href="https://www.misp-project.org/feeds">MISP feeds </a> to import data into MISP. This feed contains various types of threat intelligence data. Keep in mind that this data does not refer to specific websites but rather tools designed to detect, analyze, and respond to potential threats. Click on <b> simple JSON format </b>.
  </p>
<img src="/picturesv2/step43.JPG" alt="misp-to-docker" width="800px"> 
<p> 
    It will take you to a repository that holds the JSON data. We will copy all of this data. 
</p>
<img src="/picturesv2/step44.JPG" alt="misp-to-docker" width="800px"> 
<p> 
    Go back to MISP, click on <b> Sync Actions </b>, then <b> Import Feeds from JSON </b>, paste the copied code, and click <b> Add </b>. 
</p>
<img src="/picturesv2/step45.JPG" alt="misp-to-docker" width="800px"> 
<p>
    The feeds should load in, and you will want to enable each feed. There are five pages of feeds. I made the mistake of checking off each box individually, but if you look closely, there is an <b>empty box beside ID</b>. Checking this will select all feeds in the row.
</p>
<img src="/picturesv2/step46.JPG" alt="misp-to-docker" width="800px"> 
<p> 
    Once the feeds are enabled, you will want to fetch and store all the feed data. This process will take some time, so wait about 5–10 minutes.
</p>
<img src="/picturesv2/step47.JPG" alt="misp-to-docker" width="800px"> 
<p>
    A few minutes later, go to <b>List feeds</b>, where you can see all the threat intelligence data provided by companies. For instance, the Turla group was observed as a threat in 2018. After some research, it was identified as a Russian-based threat actor that targets governments and large enterprises.
</p>

