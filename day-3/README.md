## Introduction to EC2:

### What is EC2, and why is it important?**

EC2 म्हणजे **Amazon Elastic Compute Cloud** — ही एक AWS ची service आहे, ज्याचा use करून आपण cloud मध्ये secure आणि resizable compute power setup करू शकतो. म्हणजे जर आपल्याला कोणत्याही application साठी server ची गरज असेल, तर आपण EC2 वर quick setup करून application run करू शकतो.  
त्याचा main benefit म्हणजे on-demand scalable infrastructure — जसं traffic वाढलं की आपण लगेच capacity वाढवू शकतो, आणि कमी traffic असेल तर कमी करू शकतो. म्हणूनच EC2 मुळे 99.99% uptime ठेवता येतं, त्यामुळे आपलं app नेहमी available राहतं.  
Security चं पण खूप मजबूत setup आहे — AWS Nitro System मुळे तुझा data आणि environment safe असतो.  
आणि सगळ्यात महत्त्वाचं म्हणजे: तू cost आणि performance optimize करू शकतो. त्यासाठी options आहेत जसं की Graviton instances (जे cheap + fast आहेत), Spot instances (unused capacity साठी low price मध्ये मिळतात), आणि Savings Plans (जे आपल्याला long term मध्ये cost कमी करायला मदत करतात).

Amazon **Elastic Compute Cloud** (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.  
Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.  
Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.  
Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.


## EC2 usecases

Secure, reliable, high-performance, आणि cost-effective compute infrastructure देण्यासाठी वापरला जातो, जो demanding business needs पूर्ण करण्यासाठी ideal आहे.  
On-demand infrastructure आणि capacity मिळवण्यासाठी वापरता येतो, ज्यामुळे तुम्ही HPC applications (High-Performance Computing) जलद आणि cost-effective रितीने चालवू शकता.   
Environments मिनिटांत मिळवता येतात, आणि त्यानुसार capacity dynamically scale करू शकता. AWS च्या pay-as-you-go pricing चा फायदा घेऊन cost कमी करू शकता.  
Compute, networking (जास्तीत जास्त 400 Gbps), आणि storage services याचा व्यापक पर्याय मिळतो, जो ML projects (Machine Learning projects) साठी price performance optimize करण्यासाठी purpose-built आहे.  

Deliver secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.  
Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively.  
Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing.  
Deliver the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects.  



## EC2 Instance Types

Recommended to follow [this](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) page for very detailed and updated information.

**1) General Purpose**
General Purpose instances हे compute, memory, आणि network resources यांचा balance देण्यासाठी design केले गेले आहेत. हे विविध types च्या applications साठी suitable आहेत, जसे की web servers, small databases, development and test environments, आणि अजून काही.  

**2) Compute Optimized**
Compute Optimized instances हे memory च्या तुलनेत जास्त compute power देतात. हे workloads साठी perfect आहेत ज्यांना high-performance processing ची आवश्यकता आहे, जसे की batch processing, scientific modeling, gaming servers, आणि high-performance web servers.  

**3) Memory Optimized**
Memory Optimized instances हे memory-intensive workloads handle करण्यासाठी design केलेले आहेत. हे applications साठी उपयुक्त आहेत ज्यांना खूप जास्त memory लागते, जसे की in-memory databases, real-time big data analytics, आणि high-performance computing.  

**4) Storage Optimized**
Storage Optimized instances हे applications साठी optimize केलेले आहेत ज्यांना high, sequential read आणि write access लागते. हे tasks साठी perfect आहेत जसे की data warehousing, log processing, आणि distributed file systems.  

**5) Accelerated Computing**
Accelerated Computing instances हे accelerators पासून equipped असतात, जसे की Graphics Processing Units (GPUs), Field Programmable Gate Arrays (FPGAs), किंवा Application Specific Integrated Circuits (ASICs). हे accelerators main CPU वरून computationally intensive tasks offload करतात, ज्यामुळे specific workloads साठी faster आणि efficient processing मिळते.  


General purpose  
General Purpose instances are designed to deliver a balance of compute, memory, and network resources. They are suitable for a wide range of applications, including web servers, small databases, development and test environments, and more.

Compute optimized  
Compute Optimized instances provide a higher ratio of compute power to memory. They excel in workloads that require high-performance processing such as batch processing, scientific modeling, gaming servers, and high-performance web servers.

Memory optimized  
Memory Optimized instances are designed to handle memory-intensive workloads. They are suitable for applications that require large amounts of memory, such as in-memory databases, real-time big data analytics, and high-performance computing.

Storage optimized  
Storage Optimized instances are optimized for applications that require high, sequential read and write access to large datasets. 
They are ideal for tasks like data warehousing, log processing, and distributed file systems.

Accelerated computing  
Accelerated Computing Instances typically come with one or more types of accelerators, such as Graphics Processing Units (GPUs),
Field Programmable Gate Arrays (FPGAs), or custom Application Specific Integrated Circuits (ASICs). These accelerators offload computationally intensive tasks from the main CPU, enabling faster and more efficient processing for specific workloads.  

![image](https://github.com/iam-veeramalla/aws-devops-zero-to-hero/assets/43399466/fc8e083c-dba5-41a6-94b9-14ebef0255c1)

![image](https://sudoconsultants.com/wp-content/uploads/2023/03/EC2-Instance-Types-1-1536x1011.png)  

## Instance families  

- **C** – **Compute**: **Compute-intensive tasks** साठी instances, जिथे processing power जास्त आवश्यक आहे.
- **D** – **Dense storage**: या instances मध्ये **high storage capacity** असते, जी मोठ्या डेटा सेटसाठी उपयुक्त असते.
- **F** – **FPGA**: **Field Programmable Gate Arrays** असलेले instances, ज्यात hardware-based acceleration ची क्षमता असते.
- **G** – **GPU**: **Graphics Processing Units** असलेले instances, जे **machine learning**, **gaming**, आणि **graphical workloads** साठी उपयुक्त असतात.
- **Hpc** – **High Performance Computing**: **High-performance computing** साठी असलेले instances, ज्यात complex simulations आणि scientific computations करता येतात.
- **I** – **I/O**: **Input/output optimized instances**, ज्यांचा मुख्य वापर **high-speed data transfer** आणि **high throughput** साठी होतो.
- **Inf** – **AWS Inferentia**: **Machine learning inference** साठी असलेले instances, जे **AWS Inferentia chips** वापरून fast and scalable inference workloads चालवतात.
- **M** – **Most scenarios**: **General purpose instances** ज्यांचा वापर विविध सादरीकरणांसाठी होऊ शकतो.
- **P** – **GPU**: **Graphics Processing Units** असलेले instances, जे **AI**, **ML**, आणि **high-performance graphics rendering** साठी वापरले जातात.
- **R** – **Random access memory**: **Memory-optimized instances** ज्यामध्ये मोठ्या प्रमाणावर **RAM** असते.
- **T** – **Turbo**: **Burstable performance** instances, ज्यांना **temporary high-performance needs** ची आवश्यकता असते.
- **Trn** – **AWS Tranium**: **AWS Tranium processors** वापरणारे instances, जे **AI training** साठी optimized आहेत.
- **U** – **Ultra-high memory**: **Ultra-high memory instances** ज्यामध्ये खूप मोठ्या प्रमाणावर **memory** असते, ज्याचा वापर **large in-memory databases** साठी होतो.
- **VT** – **Video transcoding**: **Video transcoding** साठी optimized instances, जे video processing आणि conversion कार्यांसाठी वापरले जातात.
- **X** – **Extra-large memory**: **Extra-large memory** instances, जे **memory-intensive applications** साठी ideal असतात.

## Additional Capabilities

- **a** – **AMD processors**: **AMD processors** असलेले instances.
- **g** – **AWS Graviton processors**: **AWS Graviton processors** असलेले instances, जे **ARM-based** आहेत आणि cost-efficient processing offer करतात.
- **i** – **Intel processors**: **Intel processors** असलेले instances.
- **d** – **Instance store volumes**: **Instance store volumes** असलेले instances, ज्यात **local storage** दिले जाते.
- **n** – **Network and EBS optimized**: **Network** आणि **EBS** साठी optimized instances, जे **high network throughput** आणि **fast EBS performance** देतात.
- **e** – **Extra storage or memory**: **Extra storage** किंवा **memory** असलेले instances.
- **z** – **High performance**: **High performance instances**, जे अत्यधिक computational power आणि speed offer करतात.

## EC2 Instance Basics:

**Virtual Server** : A virtual server is a software-based computer that runs on a real physical server. It works like a normal computer but is created using software.   
Example: Imagine you have one powerful computer at your office. Using special software, you divide it into 3 small virtual computers, each running its own app — like one for email, one for website, and one for storage.  
In short: One big PC → Many small virtual computers.  

**Instance (EC2 Instance)** : An instance is a virtual server in the cloud (like AWS EC2) that you can use when you need it, and pay only for the time you use.  
Example: You want to launch a website but don’t want to buy your own server. So, you go to AWS EC2, start a virtual server (instance) in the cloud, upload your code, and your website is live. When traffic is high, you can start more instances easily.  

### Key Components of an EC2 Instance

**1) Instance Type** : Defines the hardware power (CPU, RAM, etc.). Example: t2.micro for small apps, m5.large for general use.

**2) Amazon Machine Image (AMI)** : Like the starter kit for your server. It includes the operating system (like Linux/Windows) and pre-installed software. Example: Ubuntu AMI, Windows Server AMI, etc.

**3) Instance Storage** : Hard drive space for your instance.
Two types:  
- **EBS (Elastic Block Store)** – Persistent storage (data stays even after stop).
- **Instance store** – Temporary storage (data gone after stop/terminate).

**4) Security Groups** : Acts like a firewall to control what traffic can come in or go out of your instance. You can allow/block specific IPs, ports, etc.  

**5) Key Pair** : Used to securely log in to your instance. Public key stays with EC2, private key stays with you.

**6) Elastic IP (optional)** : A static IP address you can assign to your instance. Helpful when your server needs a fixed address for users.  

**7) VPC (Virtual Private Cloud)** : A private network for your EC2 instances. You can control how your instance connects to the internet or other services.  

**8) IAM Role (optional)** : A set of permissions that allows your instance to access other AWS services (like S3, DynamoDB) securely.  

## EC2 Instance Types  

**1. On-Demand Instance** : Pay-as-you-go, no long-term commitment.  
Use case: Testing, dev work, temporary apps.  
Real-life Example: Tu ek website develop kartoy ani tula fakt 2-3 divas instance lagel test sathi.➡️ Use On-Demand — start kar, kaam zala ki stop kar.  
AWS Example: Start kar EC2 instance for 2 days → shut down → pay only for those 2 days.  

**2. Reserved Instance** : Commit for 1 or 3 years in exchange for huge discount.  
Use case: Long-term apps like business website or backend system.  
Real-life Example: Tujha company la ek e-commerce website 24x7 live thevaychiye for next 3 years. ➡️ Use Reserved Instance — cost kami, guaranteed capacity.  
AWS Example: Book one t3.medium instance for 3 years → get ~70% discount compared to On-Demand.  

**3. Spot Instance** : Buy unused EC2 capacity at up to 90% lower price. Super cheap, but AWS can take it back anytime.  
Use case: Background jobs, data analysis, ML training.  
Real-life Example: Tu ML model train kartoy ani tula compute power pahije at low cost. Instance jara band jhala tari chalel. ➡️ Use Spot Instance — it’s cheap and fast.  
AWS Example: Train a deep learning model on a Spot instance for 5 hours → pay 10% of On-Demand price.  

### EC2 Instance States
**🟢 Running**  
Your instance is active and working.  
You're being charged for compute time.  
You can log in, run applications, etc.

**🟡 Stopped**  
Instance is turned off, like shutting down a computer.  
You're not charged for compute, but EBS storage costs still apply.  
You can start it again anytime — AWS new public IP assign karto automatically. ani jr Elastic IP (fixed/static IP) use kelela asel, tr IP address same rahto, even after stop/start.

**🔴 Terminated**  
Instance is permanently deleted.  
Cannot be restarted.  
All data (except EBS if saved separately) is lost. Zar tu EBS volume separately banavla hota (ani detach kela hota), tr to data safe rahu shakto.

**🔄 Pending**   
Instance is in the process of starting.  
Temporary state before it becomes running.  

**🔁 Stopping**  
Instance is in the process of shutting down.  
Temporary state before it becomes stopped.  

**❌ Shutting-down**  
Instance is in the process of termination.  
Temporary state before it becomes terminated.   

## 🚀 Launching an EC2 Instance: Step-by-Step  
### **1. Login to AWS Console**
- Go to [https://aws.amazon.com/](https://aws.amazon.com/)
- Sign in with your AWS account.  

### **2. Go to EC2 Dashboard**
- Search for **EC2** in the search bar.
- Click on **"Launch Instance"** button.

### **3. Choose an Amazon Machine Image (AMI)**
- Select your **Operating System** (Linux, Ubuntu, Windows, etc.)
- This is your instance's **OS base setup**.
- *Marathi Touch:* He ek **starter setup** ahe — jashi tu Windows install karto navin laptop madhye.

### **4. Choose Instance Type**
- Example: `t2.micro` (Free Tier eligible)
- It defines the **CPU + RAM power**.
- *Marathi Touch:* Ekda OS zala, ata **kiti strong machine pahije te select karto**.

### **5. Configure Instance Details**
- Set number of instances
- Set VPC, subnet, IAM roles (optional)
- Keep defaults if not sure

### **6. Add Storage**
- Default is 8 GB (for most AMIs)
- Increase if you expect more data
- Type: **EBS (persistent)** or **Instance Store (temporary)**

### **7. Add Tags (optional)**
- Key-Value tags like `Name = MyAppServer`
- Helps in managing instances

### **8. Configure Security Group**
- Acts like a **firewall**
- Allow necessary ports:
  - `22` for SSH (Linux)
  - `3389` for RDP (Windows)
  - `80` for HTTP, `443` for HTTPS
- *Marathi Touch:* Security Group mhanje **kon connect hou shakto te control karaycha zariya**.

### **9. Create / Select Key Pair**
- Key pair = for **secure login**
- If creating new: download `.pem` file and **keep it safe**.
- *Marathi Tip:* He **password sarkha ahe**, jar file haravli tar tu instance access karu shakat nahi.

### **10. Launch the Instance**
- Review everything and click **“Launch Instance”**
- Wait for a few seconds… it’s ready!

---

## Managing EC2 Instances:

### 1) Monitoring Performance & Utilization 

#### **Monitoring mhanje naktay kay?**
"Monitoring" mhanje tuza EC2 instance kasa kaam karat aahe, kay chukatay, kay overload hotay, he sagla continuously baghne.
Yamule tu:  
- Lag yene adhich pakad shakto
- Resource kami-zast usage samjun gheu shakto
- Future madhe server size adjust karu shakto (optimize cost)

**CloudWatch Monitoring** : Amazon CloudWatch is AWS’s built-in monitoring service. It helps you track and visualize metrics in real time.  
- Real-time madhe data capture karto
- Graphs ani alerts provide karto
- Tula instance cha health check karayla help karto

#### **Important CloudWatch Metrics (Term-by-term)**  
**1) CPUUtilization**  
- Tumcha processor kiti busy aahe te dakhavto (in percentage)
- 100% = full busy, 0% = idle
- E.g. CPUUtilization = 85% mhanje server khup kaam karat aahe

**2) NetworkIn / NetworkOut**
- Instance la kiti data yetoy (In) ani jato (Out)
- E.g. Tumcha web app war user jast visit kartoy tar traffic vadhnar

**3) DiskReadOps / DiskWriteOps**
- Kiti files read/write zhale
- E.g. database access zasta asel tar he vadhnar

**4) Status Checks**  
Two Types :
- System Status Check → AWS hardware/machine barobar aahe ka te baghtay
- Instance Status Check → Tumcha OS boot zala ka, error aahet ka

**Alarm kase set karayche?**  
- CloudWatch → Alarms → Create alarm
- Metric select kara (e.g. CPUUtilization)
- Threshold set kara (e.g. > 80%)
- Notification setup kara (e.g. Email or SNS)

### **CloudWatch Agent (optional pan useful)**
- Default CloudWatch metrics madhe memory ani disk usage (in %) disat nahi. Tya sathi CloudWatch Agent install karava lagto.
- Tip: He ek software ahe je tumcha instance var chalun adhik information AWS la pathavto.

**What Metrics You’ll Get After Setup?**
- **mem_used_percent** - RAM madhla kiti % usage aahe
- **disk_used_percent** - Disk madhla usage (per mount point)
- **swap_used_percent** - Swap space usage
- **cpu_usage_idle** - Idle CPU % (lower mhanje busy CPU)

**Alarm Setup Example (Memory Usage Alert)**
- Go to CloudWatch → Alarms → Create Alarm
- Choose metric:
    - Namespace: CWAgent
    - Metric: mem_used_percent
- Threshold: "Greater than 80% for 5 minutes"
- Notification: SNS/email alert setup

---

## EC2 Troubleshooting & SSH
- Troubleshooting mhanje problem samjun ghyun te solve karaychi process

### SSH Access 

**Key Pair (.pem file)** : 
- He ek private key ahe je tu SSH connection sathi vaparto.
- Jar ha file haravla, tar login karata yet nahi. (login karta yeto pn te key pair navin generate karav lagitil. tyat khup sare steps ahet ajun)
- File la 400 permission dene garjeche ahe (secure thevaycha). `chmod 400 my-key.pem`

**SSH Connection Command (Linux OS sathi):** `ssh -i my-key.pem ec2-user@<Public-IP>`  
- `-i my-key.pem` = key file
- `ec2-user` = login username (Ubuntu asel tar ubuntu)
- `@<Public-IP>` = instance cha IP address

### Common Troubleshooting Scenarios:

**1) Instance SSH ne access nahi hotay:**
Check kara:
- Security group madhe port 22 open aahe ka?
- Public IP barobar aahe ka?
- `.pem` file barobar aahe ka? Correct permission aahet ka?

**2) Instance band zala (unexpectedly)**
Possible causes:
- High CPU load
- Billing issue
- AWS maintenance  
CloudWatch madhe graphs check kara — sudden CPU spike disel

**3) Disk full zala mhanun boot hot nahi**
- AWS dashboard → Get System Log
- Bagha error ka disatoy (`no space left on device` etc.)
- Solution: EBS volume increase kara / temp files delete kara

System Log Access (`Console madhun system logs kashe baghayche?`)
- EC2 → Select instance
- Actions → Monitor and Troubleshoot → Get System Log
- Output madhe check kara:
    - Boot issues
    - Application errors
    - User logs

---


