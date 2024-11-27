## What is MISP? 
<p>
  MISP, also know as <b> Malware Information Sharing Platform </b> is an open source threat intelligence platform. It lets you store information such as malware, threats, and vulnerabilities in an organized manner. We can think of MISP like <b> Tableau </b> or <b>  PowerBI </b> which these platforms store and display information about business intelligence. In the case of MISP, it stores and displays information about cyber threat intelligence. Many companies around the world come together by providing feeds to detect any instances of an attack. 
</p>

<img src="/picturesv2/step30.JPG" alt="misp-to-docker" width="800px">
<p>
  Before anything, double check to see if the installation of Docker was successful with the command <b> sudo docker run hello-world </b>. Docker should say Hello to you and if not, redo the installation. Since we are configuring MISP on Docker, we have to clone a repository that contains the image to do so. Clone this <a href="https://github.com/MISP/misp-docker"> to the terminal <a/>
</p>
<img src="/picturesv2/step31.JPG" alt="misp-to-docker" width="800px">
<p>
  We want to <b> cd misp-docker </b> where cd means change directory and since we to get into the repo we cloned, we cd into that one. Once inside, we're going to follow the next instruction and run <b> template.env .env </b> This template.env will create a .env file where we can customize it. 
</p>
<img src="/picturesv2/step32.JPG" alt="misp-to-docker" width="800px">
<p>
  Edit the file with <b> nano.env </b> where nano lets you edit any file you create. 
</p>
<img src="/picturesv2/step33.JPG" alt="misp-to-docker" width="800px">
<p>
  Scroll down where you see <b> BASE_URL </b> and we are going to type of public IP address of the virtual machine that we initially created. This lets us access the MISP instance externally outside the localhost (Ubuntu virtual machine) such as opening it on the web browser. Save this change and exit the file. 
</p>
<img src="/picturesv2/step34.JPG" alt="misp-to-docker" width="800px">
<p>
  Run <b> sudo docker compose pull </b> to download the latest version of the Docker images defined by the docker-compose.yml file. 
</p>
<img src="/picturesv2/step35.JPG" alt="misp-to-docker" width="800px">
<p>
  Now we want to spin up the docker container using <b> sudo docker compose up </b>. This will hang on for awhile kind of like a glitch. To see if process worked, run <b> sudo docker ps </b> where you would see all the images. 
</p>
<img src="/picturesv2/step37.JPG" alt="misp-to-docker" width="800px">
<p>
  If we take a look here SSH port 22 is open on the inbound rules. On a production VM, having this open is a security risk as anyone can try and gain access. You'd have to add security measures on that, but because we want quick access to it, we will leave it open for now. Besides this, we have to add a new inbound rule. Click on <b> Network settings </b> and then <b> Inbound port rule <b/>
</p>
<img src="/picturesv2/step38.JPG" alt="misp-to-docker" width="800px">
<p>
  The inbound port we have to add is is port 443 also known as HTTPS. This will let us connect to the MISP instance from anywhere including a local computer, or the many virtual machines you create. From that the BASE_URL we specified in the .env file. By applying this inbound port we can simply do <b> https://4.206.218.123 </b>. 
</p>
<img src="/picturesv2/step39.JPG" alt="misp-to-docker" width="800px">
<p>
  Once we put that URL into our browser, it will first take you to 
<b> connection not secure </b> which is okay because there is no certificate on the website signed by the CA. Since we know where the connection leads, simply click on ok and it will take you to the username and login. 
</p>
<img src="/picturesv2/step40.JPG" alt="misp-to-docker" width="800px">
<p>
  Just like if you were to set up a new router, there are default credentials in place since we do not know what they are. Use these credentials to login. 
</p>
<img src="/picturesv2/step41.JPG" alt="misp-to-docker" width="800px">
<p>
  As we can interpret, if somebody were to get ahold of this, they can easily access the system which is a major security risk. We have to change our password to something we know and challenging enough to avoid password attacks.
</p>
<img src="/picturesv2/step42.JPG" alt="misp-to-docker" width="800px">
<p>
  Click on this link <a href="https://www.misp-project.org/feeds"/> MISP feeds </a> to import into MISP where this information contains various types of threat intelligence data. Mind you this data are not specific websites, rather tools designed to detect, analyze, and respond to potential threats. Click on <b> simple JSON format </b>
  </p>
<img src="/picturesv2/step43.JPG" alt="misp-to-docker" width="800px"> 
<p> 
  It will take you to a repository that holds the JSON data. We will copy all of this data. 
</p>
<img src="/picturesv2/step44.JPG" alt="misp-to-docker" width="800px"> 
<p> 
  Go back to MISP, click on <b> Sync Actions </b>, <b> Import Feeds from JSON </b>, paste the copied code and click <b> Add </b>
</p>
<img src="/picturesv2/step45.JPG" alt="misp-to-docker" width="800px"> 
<p>
  The feeds should load in and you want to enable each feed. There will be 5 pages of feeds. I made the mistake of checking off each box, but if you look closely, there is an <b> empty box beside ID where if you check it off, it will check off each feed in the row </b>. 
</p>
<img src="/picturesv2/step46.JPG" alt="misp-to-docker" width="800px"> 
<p> 
Once the feeds are enabled, you want to fetch and store all the feed data. This will take some time so wait around 5 - 10 minutes. 
</p>
<img src="/picturesv2/step47.JPG" alt="misp-to-docker" width="800px"> 
<p>
  A couple of minutes later, go th <b> List feeds </b> and you can see all the threat intelligence data that companies supply. For instance, Turla group was observed in 2018 as a threat. After some research, it is a russian based threat actor that attacks governments and large enterprises. 
</p>

