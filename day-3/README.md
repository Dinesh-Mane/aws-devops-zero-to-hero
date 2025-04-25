## Introduction to EC2:

### What is EC2, and why is it important?

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



## EC2 Instance Types (Trick - GA CMS | Balanced speed performance memory and storage | GTaM, A-PiG, CC, MRX1Z1, SId2h1)

Recommended to follow [this](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) page for very detailed and updated information.

**1) General Purpose** : General Purpose instances हे compute, memory, आणि network resources यांचा balance देण्यासाठी design केले गेले आहेत. हे विविध types च्या applications साठी suitable आहेत, जसे की web servers, small databases, development and test environments, आणि अजून काही.  

**2) Compute Optimized** : Compute Optimized instances हे memory च्या तुलनेत जास्त compute power देतात. हे workloads साठी perfect आहेत ज्यांना high-performance processing ची आवश्यकता आहे, जसे की batch processing, scientific modeling, gaming servers, आणि high-performance web servers.  

**3) Memory Optimized** : Memory Optimized instances हे memory-intensive workloads handle करण्यासाठी design केलेले आहेत. हे applications साठी उपयुक्त आहेत ज्यांना खूप जास्त memory लागते, जसे की in-memory databases, real-time big data analytics, आणि high-performance computing.  

**4) Storage Optimized** : Storage Optimized instances हे applications साठी optimize केलेले आहेत ज्यांना high, sequential read आणि write access लागते. हे tasks साठी perfect आहेत जसे की data warehousing, log processing, आणि distributed file systems.  

**5) Accelerated Computing** : Accelerated Computing instances हे accelerators पासून equipped असतात, जसे की Graphics Processing Units (GPUs), Field Programmable Gate Arrays (FPGAs), किंवा Application Specific Integrated Circuits (ASICs). हे accelerators main CPU वरून computationally intensive tasks offload करतात, ज्यामुळे specific workloads साठी faster आणि efficient processing मिळते.  


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
## Access Key vs Key Pair
### 1. Access Key (for AWS Console/CLI access)
हे कोणासाठी?  
→ User साठी — जर तुझं IAM user आहे आणि तुला AWS CLI किंवा SDK वापरून AWS account access करायचं असेल.  
काय असतं access key मध्ये?
- Access Key ID (उदाहरण: AKIA...)
- Secret Access Key (एक गुप्त पासवर्डसारखा key)

📌 Use Case:
- AWS CLI वापरून EC2 instance launch करायचं, S3 मधून फाईल download करायची etc.
- Programmatically AWS services access करायला वापरतो.

### 2. Key Pair (for EC2 login)
हे कोणासाठी?  
→ EC2 instance साठी — जर तु EC2 instance launch केलं, तर त्यावर SSH ने login करायला लागतो key pair.
काय असतं key pair मध्ये?
- Public Key → EC2 instance वर store होतं.
- Private Key (.pem file) → तुझ्या machine वर ठेवतोस. SSH करताना ही लागते.

📌 Use Case:
- EC2 instance SSH करून access करायचं असेल तर हाच private key वापरतो.
- जर key file हरवली, तर instance ला access नाही करता येत (unless alternate method वापरली).

### In-short 
**- Access key** : AWS CLI किंवा SDK वापरून AWS account access करायचं असेल.   
**- Key Pair** : EC2 instance वर SSH ने login करायचं असेल.

### Scenario: Tula ek web app deploy karaycha ahe on AWS EC2
**Step 1: AWS Console madhe login**
तु AWS ला browser मधून access करतोस → यासाठी IAM user लागतो.  
जर तु programmatically (CLI/SDK) वापरून EC2 create करणार असशील, तर तुला Access Key लागेल.  

उदा: `aws ec2 run-instances --image-id ami-xxxx --instance-type t2.micro`
ह्या command ला Access Key ID + Secret Access Key लागतील authentication साठी.

**Step 2: EC2 instance launch करताना – Key Pair निवडतोस**
EC2 instance तयार करताना AWS विचारतो:
- "Which key pair to use?" - इथे आपण .pem file generate करतो (Key Pair).

**Step 3: Login to EC2 instance**
आता EC2 तयार झाल्यावर त्यात SSH login करायचंय:  
`ssh -i "my-key.pem" ec2-user@<Public-IP>`
इथे my-key.pem म्हणजे तुझा private key (Key Pair).

---
## EBS Volume आणि Instance Store यातला फरक 

### 🔄 **Storage Type**  
- **EBS Volume**: ही *persistent block storage* आहे — म्हणजे instance बंद/terminate केल्यावर सुद्धा data टिकतो.  
- **Instance Store**: ही *temporary storage* आहे — म्हणजे instance बंद किंवा crash झालं की सगळा data उडतो.

### 🛡 **Durability (टिकाऊपणा)**  
- **EBS Volume**: खूपच *high durability* असते कारण data हे same Availability Zone मधील multiple hardware वर replicate केलं जातं.  
- **Instance Store**: कोणतीही durability guarantee नाही. Instance बंद झाला किंवा hardware fail झाला की सगळा data गेलाच म्हणून समजा.

### 💼 **Use Cases (वापर कशासाठी?)**  
- **EBS Volume**: जर तुला *important data* store करायचा असेल जसे की databases, OS files, application data – तर हाच option बेस्ट आहे.  
- **Instance Store**: जर तुला फक्त temporary data हवं असेल (जसे की cache, temp files, scratch data) तर हे उपयोगी आहे.

### 🔗 **Attach/Detach**  
- **EBS Volume**: तू एक instance वरून दुसऱ्या instance ला attach आणि detach करू शकतोस.  
- **Instance Store**: हे specific त्या instance ला जोडलेलं असतं, detach किंवा दुसऱ्या ठिकाणी वापरता येत नाही.

### 🧾 **Snapshot/Backup**  
- **EBS Volume**: यात तू *snapshot* घेवू शकतोस – म्हणजे backup तयार करून नंतर restore सुद्धा करू शकतोस.  
- **Instance Store**: यात कोणताही snapshot किंवा backup support नसतो.

### ⚡ **Performance**  
- **EBS Volume**: performance हि volume च्या type वर अवलंबून असते (जसे SSD, HDD) — तुला आवडीनुसार निवडता येतं.  
- **Instance Store**: कारण हि storage host machine ला directly जोडलेली असते, त्यामुळे I/O (read-write) फारच fast असतो — short term processing साठी heavy performance.

### 💰 **Cost (खर्च)**  
- **EBS Volume**: तुला जितकी storage लागते तितक्याच GB/month नुसार पैसे भरावे लागतात.  
- **Instance Store**: काही instance types मध्ये ही free मध्ये येते — पण ही long-term साठी योग्य नाही.

### ☁️ **Availability (उपलब्धता)**  
- **EBS Volume**: instance बंद झाला तरी volume independent आहे — पुन्हा वापरता येतो.  
- **Instance Store**: जर instance बंद झाला किंवा crash झाला तर हि storage गेलीच.
---

### 🆚 **S3 vs EBS – मुख्य फरक**

### 🧱 1. **Storage Type (कसली storage आहे?)**

- **S3**: ही *object storage* आहे – म्हणजे आपण data objects (images, videos, backups, documents) फाइल्स म्हणून store करतो.  
- **EBS**: ही *block storage* आहे – म्हणजे एक hard disk सारखं, ज्यावर operating system, databases, applications चालवू शकतो.

### 🖥 2. **Usage (कशासाठी वापरतात?)**

- **S3**: media files, website backups, logs, documents – *long-term and scalable* data storage साठी.  
- **EBS**: *EC2 instance च्या operating system किंवा software applications* साठी use होतो.

### 🔄 3. **Attach/Detach**

- **S3**: EC2 ला direct attach होत नाही. API किंवा SDK द्वारे access करावा लागतो.  
- **EBS**: EC2 instance ला *attach* करता येतो — अगदी जसं physical hard drive ला जोडतो.

### 📂 4. **Data Access Method (कशा प्रकारे data access करतो?)**

- **S3**: *HTTP/HTTPS* द्वारे access करतो. Web browser, SDK, CLI मधून सहज.  
- **EBS**: EC2 instance वर *mount* करतो आणि normal file system सारखं वापरतो.

### 💾 5. **Persistence (data टिकतो का?)**

- दोन्हीही persistent storage आहेत – म्हणजे instance stop केल्यावरसुद्धा data टिकतो.  
  पण:
  - **S3** मध्ये डेटा खूप secure आणि globally available असतो.
  - **EBS** मध्ये डेटा एका Availability Zone मध्येच accessible असतो.

### ⚡ 6. **Performance**

- **S3**: High throughput साठी optimized आहे – especially *large files* serve करण्यासाठी.  
- **EBS**: Low latency आणि fast I/O operations साठी optimized – म्हणजे *databases* आणि OS साठी बेस्ट.

### 💸 7. **Cost (खर्च)**

- **S3**: तुला फक्त storage आणि access operations साठी पैसे द्यावे लागतात – *खूपच कमी खर्च*.  
- **EBS**: तुला provision केलेल्या GB/month नुसार पैसे लागतात – किंचित महाग पण fast आणि flexible.

### ✅ 8. **Best For?**

- **S3**: Backup, archives, media content, static website hosting.  
- **EBS**: Boot volumes, running databases, app-level storage.

### 🎯 एक सोपा Trick लक्षात ठेवायचा:
> **S3** = Simple Storage (for files)  
> **EBS** = Block Storage (for OS/Data disk)
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
## Interview Q&A
### Q: What options are available for backing up EC2 instances?
A: You can back up your EC2 instance using the following methods:
- Amazon Machine Images (AMI): Create an AMI of your instance to capture its configuration and data, which can later be used to launch new instances.
- Snapshots: Take snapshots of the EBS volumes attached to your EC2 instance. Snapshots are incremental backups that capture only the changes made to the volume since the last snapshot.
- AWS Backup: A fully managed backup service that can automate and centralize backups for EC2 instances and other AWS resources.

### Q: EBS (Elastic Block Store) volume kay ahe?
A: **EBS volume** he ek **persistent block storage** device ahe, jyala apn **EC2 instance** la attach karu shakto. Hya volume cha use data store karayla hota. **Instance storage** (je ephemeral ahe) cha fark asha ki, **EBS volumes** stop kelele ki terminate kelele instance war pan **data** persist (rakhta) rahate. Mhanje, instance stop kelela asla tari, EBS volume warch data suru rahato.  

#### **Key Features**:
1. **Persistent Storage**: EBS volumes **data** **instance stop** kelya war pan **retain** kartat. Instance **terminate** kelay tari EBS volume war data rakhta rahato.  
2. **Block Storage**: EBS volume block-level storage ahe, je **fixed-size blocks** madhe data store karto. Tya data la **file system** (ext4, NTFS) war mount karke access karu shakto.  
3. **Attachable and Detachable**: EBS volume aplya EC2 instances la attach and detach karu shakto, tya mule data easily move karu shakto.  
4. **Durability and Availability**: EBS volumes **99.999% durability** sathi design kelele ahet. AWS **multiple replicas** store kartat, jya mule instance failure nantar pan data safe rahato.  
5. **Scalability**: EBS volumes resize (capacity increase) karu shakto as per your needs. Tya mule aplya performance requirements pramane storage change karu shakto.

#### **Use Cases**:  
- **Databases**: Database files store karayla (example: MySQL, PostgreSQL).  
- **Application Data**: Application files, logs, config files store karayla.  
- **File Systems**: File systems create karayla (ext4, NTFS) and mount karayla EC2 instance var.  
- **Backup and Recovery**: EBS snapshot ghenyacha use karu data backup kela jato.  

#### **Types of EBS Volumes**:  
1. **General Purpose SSD (gp3/gp2)**: Basic SSD storage for general applications.  
2. **Provisioned IOPS SSD (io2/io1)**: High performance storage for critical workloads like databases.  
3. **Throughput Optimized HDD (st1)**: Cost-effective storage for large datasets.  
4. **Cold HDD (sc1)**: Low-cost storage for infrequent data access.  

#### **How to Attach EBS Volume**:
1. EC2 **Dashboard** madhe **Volumes** menu var jaa.  
2. **Create Volume** option select karun, volume size, type choose kara.  
3. **Attach Volume** option select karun, instance choose kara, ani device name (e.g., `/dev/sdf`) specify kara.  
4. Instance la SSH karke volume mount kara.  

#### **Snapshot**:
EBS snapshots backup sathi use karayche, jya mule data safe rakha jaata.  
1. **Create Snapshot**: Volume select karun snapshot create kara.  
2. **Restore from Snapshot**: Snapshot la volume create karun, instance la attach kara.  

### **Summary**:
- **EBS volumes** hi **persistent block storage** device ahe je EC2 instances la attach karu shakto.  
- He volumes data **store** karayla use hote jya mule **stop** and **terminate** kelelya instances madhe pan data safe rahato.  
- EBS volumes resize karu shakto, backup gheu shakto, ani easily move karu shakto.  

### Q. What Are Key-Pairs In AWS?
A: A key pair consists of two types of keys - a public key and a private key. The public key is used to encrypt data and stored on the AWS EC2 instance while a private key is used to decrypt data and is kept by the user. Whenever you want to connect to an AWS EC2 instance a key-pair works as a security credential to prove your secure authentication identity and access to EC2 instance via SSH.  

### Q. What Is Elastic Load Balancing (ELB) And How Does It Function?
A: Elastic Load balancer ( ELB ) is a service provided by AWS that helps in distribution of incoming traffic of the applications across multi targets such as EC2 instances, containers etc.. in one or more Availability zones.  

### Q. What Are The Various Load Balancers Provided By AWS?
The following are the types of load balancers provided by AWS:
- **Application Load Balancer:** ALB works on layer 7(application layer) of OSI Model. It supports  HTTP, HTTPS, and gRPC protocols. and works on Round Robin algorithm.
- **Network Load Balancer:** NLB works on layer 4(Transport layer) of OSI Model. It Supports TCP, UDP, and TLS protocols and works on Flow hash algorithm.
- **Gateway Load Balancer:** GLB works on network layer (3 and 7).It supports IP-based routing and works on routing table lookup algorithm.

### 1. What is AWS EC2, and how does it fit into the DevOps workflow?
Answer: AWS EC2 is a web service that provides resizable compute capacity in the cloud. It plays a pivotal role in DevOps workflows by allowing DevOps engineers to provision and manage virtual machines (instances) for running applications, microservices, and infrastructure as code.

### 2. Explain the different instance types in EC2 and when you would choose one over the other.
Answer: EC2 offers various instance types optimized for different use cases, such as compute-optimized, memory-optimized, and storage-optimized instances. The choice depends on your application’s requirements, with factors like CPU, memory, storage, and network performance influencing the decision.

### 3. What are Amazon Machine Images (AMIs) in EC2, and how do you create custom AMIs for your applications?
Answer: An AMI is a pre-configured virtual machine image that you can use to launch EC2 instances. To create a custom AMI, you typically start with an existing instance, customize it to your needs, and then create an image from that instance. Custom AMIs are useful for replicating application environments and configurations.

### 4. How can you secure your EC2 instances, and what are some best practices for enhancing EC2 security?
Answer: EC2 security best practices include:
- Restricting network access using Security Groups and Network ACLs.
- Applying IAM roles and policies for fine-grained access control.
- Using key pairs for secure SSH/RDP access.
- Regularly patching and updating your instances and applications.
- Implementing monitoring and logging, such as CloudWatch and AWS Config, to track security events.

### 5. Explain Auto Scaling in EC2 and how it helps ensure application availability.
Answer: Auto Scaling is a service that allows you to automatically adjust the number of EC2 instances in response to changing application demands. It helps maintain application availability, improves fault tolerance, and optimizes resource usage by scaling out during periods of high demand and scaling in during lower demand.

### 6. What is Elastic Load Balancing (ELB) in AWS, and how does it integrate with EC2 instances to improve application scalability and availability?
Answer: ELB is a service that automatically distributes incoming application traffic across multiple EC2 instances. It improves application availability and scalability by distributing traffic evenly, detecting and routing around unhealthy instances, and providing a single entry point for users.

### 7. How do you automate the provisioning and configuration of EC2 instances in a DevOps environment?
Answer: In a DevOps environment, you can automate EC2 provisioning and configuration using Infrastructure as Code (IaC) tools like AWS CloudFormation, Terraform, or Ansible. These tools allow you to define and manage your infrastructure as code, making it reproducible, version-controlled, and easily integrated into your CI/CD pipeline.

### 8. Explain the concept of EC2 instance metadata and user data.
Answer:
- EC2 Instance Metadata: EC2 instances have metadata that provides information about the instance, such as instance ID, public IP address, and IAM role. This metadata can be accessed from within the instance.
- User Data: User data is a script or data that can be passed to an EC2 instance during launch. It is often used to perform instance-specific configuration and customization.

### 9. What is an EC2 placement group, and in what scenarios would you use it?
Answer: An EC2 placement group is a logical grouping of instances that affects how they are placed in the underlying hardware. You might use placement groups for low-latency, high-throughput communication between instances, such as in a cluster or for high-performance computing workloads.

### 10. How can you resize an EC2 instance, and what are the considerations when doing so?
Answer: You can resize an EC2 instance by stopping it, changing its instance type, and then starting it again. However, it’s essential to ensure that the new instance type meets your application’s resource requirements and that any instance-specific settings and data are preserved during the process.

### 11. Explain the concept of EC2 instance types that are optimized for CPU, memory, and storage. Provide specific use cases for each.
Answer: EC2 offers instance types optimized for various resource requirements. For example, CPU-optimized instances (e.g., C5) are suitable for compute-intensive workloads, memory-optimized instances (e.g., R5) are ideal for memory-intensive applications, and storage-optimized instances (e.g., I3) are designed for data-intensive applications like databases.

### 12. What is an EC2 Spot Instance, and when would you use it in a DevOps environment?
Answer: Spot Instances allow you to use spare AWS capacity at a significantly lower cost. They are useful for non-critical, fault-tolerant workloads in a DevOps environment where you can handle interruptions and take advantage of cost savings by using Spot Instances.

### 13. How does EC2 handle instance failures, and what strategies can you implement to ensure high availability for your applications?
Answer: EC2 instances can fail, but you can enhance availability by:
- Using Auto Scaling to automatically replace failed instances.
- Distributing your application across multiple Availability Zones.
- Implementing load balancing with Elastic Load Balancing (ELB).
- Utilizing Elastic IP addresses and DNS solutions for failover.

### 14. Explain the process of attaching and managing EBS volumes to EC2 instances.
Answer: To attach an EBS volume to an EC2 instance, you:
- Create an EBS volume and specify its size and type.
- Attach the volume to the instance using the AWS Management Console, AWS CLI, or SDK.
- Mount and format the volume on the instance to make it usable.

### 15. What are the differences between instance store (ephemeral) and EBS-backed EC2 instances, and when would you choose one over the other?
Answer: Ephemeral instances use instance store volumes, which provide high-speed, temporary storage. EBS-backed instances use network-attached EBS volumes for durable storage. The choice depends on the need for data durability; EBS-backed instances are preferred for important data, while instance store is suitable for temporary, high-performance storage.

### 16. How can you monitor and manage the performance of EC2 instances and underlying resources?
Answer: You can use Amazon CloudWatch to monitor EC2 instances and the underlying resources. CloudWatch provides metrics and logs for CPU utilization, memory, network, and other performance-related data. You can set up alarms and use the AWS Management Console to analyze performance.

### 17. Explain the concept of EC2 instance metadata and user data and how they are accessed within EC2 instances.
Answer:
- Instance Metadata: EC2 instance metadata is accessible from within an instance and provides information about the instance itself, such as instance ID, public IP, IAM role, and more. It can be accessed using a specific URL, like http://169.254.169.254/latest/meta-data/.
- User Data: User data is user-provided information or scripts that can be passed to an EC2 instance during launch. It can be accessed from within the instance, typically as part of the instance initialization process.

### 18. How can you automate EC2 instance provisioning and scaling using AWS services like AWS Auto Scaling and AWS CloudFormation?
Answer: AWS Auto Scaling allows you to automatically adjust the number of EC2 instances based on specified conditions, such as CPU utilization or application load. AWS CloudFormation, on the other hand, allows you to define and provision infrastructure as code, including EC2 instances, making it repeatable and automatable as part of your DevOps pipeline.

### 19. What is an EC2 placement group, and what are the types of placement groups available in AWS?
Answer: An EC2 placement group is a logical grouping of instances to influence how they are physically placed within the data center. AWS offers three types of placement groups: Cluster Placement Group (low-latency clusters), Partition Placement Group (HPC workloads), and Spread Placement Group (fault-tolerant groups).

### 20. Explain how to implement an effective backup and disaster recovery strategy for EC2 instances and data.
Answer: To implement an effective backup and disaster recovery strategy for EC2, you can:
- Create regular EBS snapshots for data backup.
- Utilize automated backup solutions like AWS Backup.
- Replicate data across multiple Availability Zones.
- Implement standby instances and recovery procedures to minimize downtime during a disaster.
