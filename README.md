# Cloud
- Why cloud?
  
  Servers were physically colacated. Minimal virtualized and automation. 
   
- What is Cloud Computing?

  The US national institute of standrards and technology created it. Cloud computing is way of using IT. It has 5 traits
  
      - On-demand self-service
      - Broad network access
      - Resource pooling
      - Rapid elasticity
      - Measured service
  
# GCP
- Services offered by GCP?
  
   GCP offers 4 main services - Compute, Storage, Big Data and Machine Learning.

- Computing Architecture

  Virtualization provides IAAS (Infrastructure As A Service) and PAAS (Platform As A Service). 

- How GCP is organized?

  Zones are grouped into Region. And regions are grouped by Multi Region
  
- How many regions does GCP supports?

  24 Regions. For latest information check https://cloud.google.com/
  
- GCP environmental responsibility

  Physical infrastrucure uses 2% of world's electricity. ISO 1401 certified. Finland has achieved 100% neutral and reusable energy from sea.
  
- How many ways to interact with GCP?

      - Mobile APP
      - Console
      - Rest API
      - SDK
  
## IAM - Identity and Access Management
   
  Who can be IAM?
   
    - Google Account or Cloud Identity user
    - Service Account
    - Google Group
    - Cloud Identiy or G Suite domain
  
  Types of Roles:
   
    - Primitive : Fixed coarse-grained level of access. Primitive roles includes Owner,Editor,Viewer and Billing
    - Predefined : Fine grained permission  
    - Custom : presise set of permission. Policies can be applied on Project and Organization

  Hierarchy: 
 
  - Resources > Projects > Folders > Organziation Nodes.
    
  Cloud Launcher/Marketplace:
   
  - Cloud Marketplace its tool to deploy functional software packages.Some cloud launchers are available on both free and paid versions(mostly third party).  Networking cost is based on the software used. 
  
  ## VM - Virtual Machine
  
  Compute engines lets you run VMs on Google global infrastructure. Can reconfigure CPU power, memory, storage..etc.
  
  - What is VPC?
  
    Virtual Private Cloud(VPC) networks are global; subnet are regional. A VPC in the region can have subnet ranges to be assigned to resources in different zones of the region. Can dynacmically expand the IP range. 
    
  - Compute Engine:
    
    Includes,
        - machine types - VCPUs, Memory. Can be custom machine types.
        - Storage - Standard, Local SSD (erased on VM termination) or Persistant SSD
        - Boot Image - Boot images
        - Startup script
        - Snapshots - for backup or migration
        - 
  - Preemptible VM
     
     Suitable for huge workload systems which runs continously for long hours without humman interaction. Which has benifit of per-second billing with sustained user discounts. Has high throughput to storage with zero cost. Custom machine type pay for only the hardware need.
     
  - Large VM: which has 224 vCPUs with 128 GB per vCPU.
  - AutoScaling: Add and take away VM from application based on load metrics
  - VPC has routing table to forward traffics networks even across subnets. 
  - VPC gives global Firewall to control network trafic by writting firewall rules.
  - VPC belongs to GCP projects. 
  - VPC peering allows to interconect differnt projects in GCP.
  - Shared VPC can be used with the help of IAM to share network between projects.
  
  - Cloud Load Balancer: Reacts quickly on traffic and users. 
  
    Types of Load balancers:
      - Global HTTP(s)
      - Global SSL proxy
      - Global TCP proxy
      - Regional
      - Regional Internal
  - Cloud DNS: A managed DNS server running on the same infrastructure as Google. 
  - Cloud CDN: Edge caching; using CDN interconnect to connect custom CDNs into GCP.
    
    Interconnect Options: 
    
    - VPN: No SLAs
    - Direct Peering : Without internet;No SLAs
    - Carrier Peering: No SLAs
    - Dedicated Interconnect: Recommended for 99.9% SLAs
  
 ## Cloud Storage
 
 - Cloud Storage is equivalent to AWS S3. All files are stored as Object and can be accessed by URLs. It's not a filesystem.
 - Cloud Storage can be stored and organized in a Bucket. Always encrypts the data at rest. Transfer is through HTTPs.
 - Roles are inherited to buckets and objects.
 - Cloud storage are immutable.
 - Bucket attributes,
 
    - Globally unique name
    - Storage class : 
        - Coldline for archive purpose(old data); accessed once a year
        - Newline for archive purpose(old data); accessed once a month
        - Regional: Accessed within the region
        - Multi-Region: Most frequently accessed.
    - Location
    - IAM policies or ACL
    - Object Versioning : if disabled new object overwrite old one
    - Object Lifecycle management rules - Delete object by date 
    - Upload data to Google Cloud
        - Online transfer : CMD or browser
        - Storage tranfer service :  Batch or scheduled 
        - Transfer Appliance: Leased from Google cloud
    - Cloud Bigtable
      
      NoSQL database service similar to AWS DynamoDB. It is self managed by Google for high availability with low latency, high i/o throughput.
      Hbase API enabled portability with Bigtable. Self managed Hbase is too risky considering availability, scalability. Bigtable handles upgrades, has IAM permission. Bigtable used by Gmail, Search and Analytics. It can be interacted with GCP services or 3rd party service. 
      
      Data can be imported through,
        
          - Applicatio API - Hbase API/ Java Hbase client.
          - Stream - Dataflow, Spark, Storm
          - Batch - Hadoop MapReduce, Dataflow or Spark
          
      Cloud Bigtable as a persistent hashtable - Each item in the database can be sparsely populated, and is looked up with a single key.
      
    - Cloud SQL 
    
      Relational DB service similar to AWS RDS. Supports vertical and horizondal scalabilty. Zonal replication services read and failover, backup with on demand on schedule. Data encryption is supported. 
      Each Cloud SQL database is configured at creation time for either MySQL or PostgreSQL. Cloud Spanner uses ANSI SQL 2011 with extensions.
      
    - Cloud Spanner
      
      Relational DB service similar to AWS RDS. Offers horizontal support, transactional support, replications with throught consistancy. Use case financial and inventory applicaions.
      Cloud Spanner can scale to petabyte database sizes, while Cloud SQL is limited by the size of the database instances you choose. At the time this quiz was created, the maximum was 10,230 GB.
      
     - Cloud Datastore
     
       Similar to Bigtable. Highly scalable. Automatically handles Sharding and Replication. SQL like queries. Free daily quota - Read, Write and Deletes.
       
    - Comparing Cloud Storage
      
      ![Comparing Cloud Storage](https://raw.githubusercontent.com/shangan23/cloud-gcp/main/comparing_storage_options.png)
      
 
