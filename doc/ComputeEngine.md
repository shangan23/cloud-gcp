# VM - Virtual Machine
  
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
