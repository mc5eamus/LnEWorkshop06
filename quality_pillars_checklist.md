# Quality Dimensions - Checklist

## Resiliency

### Which business metrics have you defined for your application? 
* Set your workload availability targets. 
* Identified how long the workload can be down for, and how much data it's acceptable to lose in a disaster. 
* Identified your redundancy requirements and SLAs. 
* Have an understanding of Azure Service Level Agreements (SLAs) and how they interact with your workload.

### How are you managing your data? 
* Segregated read operations from update operations on your data stores. 
* Architected databases for resiliency. 
* Implemented geographic replication for your databases. 
* Architected storage for resiliency.

### How are you managing errors and failures? 
* Implemented Throttling. 
* Have a strategy to handle transient failures. 
* Configured request timeouts. 
* Have a method of preventing cascading failures. 
* Split the application components with separate health probes.

### How are you handling disaster recovery (backup and restore) for this workload? 
* Planned for dependency failures. 
* Have a response plan in place for network outages. 
* Defined manual responses where automation doesn't exist. 
* Understand what to do when data is corrupted or deleted. 
* Have a disaster recovery plan. 
* Defined a backup strategy. 
* Protected virtual machines from corruption and accidental deletion. 
* Have a resource management strategy. 
* Automatically schedule and test backup and restore operations. 
* Document regional failure plans. 
* Archive application configuration and installation information.

### How have you ensured that your application is resilient to failures? 
* Identified your subscription and service requirements. 
* Planned the expected usage patterns. 
* Identified distinct workloads. 
* Have SLAs and support information for third-party services. 
* Implemented health probes/checks for load balancers (LB) and application gateways (AGW). 
* Replicated storage locally utilizing RAID or equivialnt technologies to protect against disk failure. 
* Implemented load balancing. 
* Implemented queuing between application tiers. 
* Run multiple instances of the app and database. 
* Performed a failure-mode analysis of the workload. 
* Deployed the application across multiple regions.

### How are you ensuring failures are resolved quickly? 
* Have an early warning system for workloads where that makes sense. 
* Monitor any long-running workflows for failures. 
* Have visualization and alerts so that the monitoring is actionable. 
* Validated that the monitoring system is functional. 
* Azure subscription/service limits are documented and known. 
* Implemented the necessary instrumentation to monitor my workload. 
* Monitoring tools are used to collect and view historical statistics. 
* Health probes are implemented to validate application functionality. 
* Collect log information and correlate across all tiers.

### How do you test your applications to ensure they are fault tolerant? 
* Perform testing in small, real-life situations. 
* Test my workload by injecting faults. 
* Perform load testing on my workload.


## Cost

### What actions are you taking to optimize cloud costs? 
* Identify opportunities to reduce overall cost. 
* Use cost management tools to plan and track costs. 
* Tag my resources and track that back to costs.

### How do you ensure that cloud resources are appropriately provisioned? 
* Automate based on the application lifespan. 
* Use DevOps and deployment automation. 
* Perform capacity planning iteratively. 
* Configure auto-scale policies for my workload (both in and out). 
* Select the right resource offering size (VM, disk, database). 
* Choose appropriate services that match my business requirements.

### How is your organization modeling cloud costs? 
* Estimate and track my costs. 
* Educate the employees about the cloud and various pricing models. 
* Have appropriate governance about expenditure. 
* Treat resources as a utility

### How do you manage the storage footprint of your digital assets? 
* Track how data flows in and out of Azure. 
* Defined and enforce data retention and archival requirements. 
* Spec-ed out the data storage and partitioned it correctly.

### How are you monitoring your costs? 
* Watch my cloud costs. 
* Create and respond to cost alerts. 
* Perform cost reviews on a regular cadence. 
* Defined budgets for my workload.

### What trade-offs have you made to optimize for cost? 
* Analyze ROI regularly. 
* Use different Azure datacenter locations to optimize cost. 
* Use Azure Marketplace. 
* Track the resource tier and optimize appropriately. 
* Take advantage of appropriate subscription offer types.

## Scalability 

### How are you designing your applications to scale? 
* Have the right data store to match usage. 
* Use dynamic service discovery for microservices applications. 
* Utilize connection pooling. 
* Compress data when appropriate. 
* Use locking to ensure consistency. 
* Use async calls and waits to prevent locks. 
* Use microservices when you can. 
* Use queues. 
* Avoid sticky sessions and client affinity. 
* Automatically scale when load increases. 
* Use background jobs.

### How are you thinking about performance? 
* Have well-defined performance goals. 
* Use horizontal scaling when possible. 
* Have policies to scale in and scale down when my load decreases. 
* Understand the performance bottlenecks. 
* Use idempotent operations.

### How are you handling user load? 
* Run tests at peak load. 
* Have awareness about the time taken to scale in response to events.

### How are you ensuring you have sufficient Capacity? 
* Use a Content Delivery Networks (CDN) if applicable. 
* Have a strategy in place to manage events that may cause a spike in load. 
* Optimized resource choices (vm, database sizing, etc) to match the needs of my application. 
* Configured scaling policies by using the appropriate metrics. 
* Automatically schedule autoscaling to add resources based on time of day trends.


### How are you managing your data to handle scale? 
* Design for eventual consistency. 
* Use sharding for database storage when appropriate. 
* Minimize the load on the data store. 
* Normalize the data appropriately. 
* Optimize database queries and indexes. 
* Document plans for data growth and retention.

### How are you monitoring to ensure the workload is scaling appropriately? 
* Track when resources scale in and out. 
* Have an overall monitoring strategy for scalability.

## DevOps

### How are you designing your applications to take into account DevOps? 
* Leverage containers in your workload appropriately. 
* Treat your infrastructure as if it were code. 
* Track the dependencies of your workload. 
* Aware of your resource limits in Azure. 
* Tag and name your resources in a consistent fashion. 
* Isolate my workloads. 
* Have an orchestration system in place to deploy my application.

### How are you managing the configuration of your workload? 
* Automated manual tasks. 
* Monitor and update machine configurations. 
* Schedule deployments. 
* Deploy, manage, and monitor my workload as a group rather than handling its components individually.

### What considerations are you making around the deployment of your infrastructure? 
* Document the release process. 
* Use automation to deploy and update my workload. 
* Have a release process for my workload. 
* Track the release of new code as it progresses through different stages. 
* Audit and track changes in my code and infrastructure. 
* Have a rollback plan for each deployment. 
* Have knowledge of portions of my workload that need to be highly available and have an appropriate deployment strategy.

### How is development done on this workload? 
* Use environments for dev and test stages that simulate a production environment. 
* Instrumented my workload so view metrics in Azure Application Insights. 
* Manage and actively resolve the technical debt of the workload. 
* Have pipelines for continuous deployment/continuous integration. 
* Use feature flags to add new features.

### How are you monitoring your deployments? 
* Implement alerting and monitoring for the DevOps infrastructure of the workload. 
* Correlate events between the different application tiers. 
* Log for all deployments. 
* Track deployment metrics. 
* Report and set notifications for events. 
* Monitor underlying services.

### What processes and procedures have you adopted to optimize your workload for DevOps? 
* Have a branching strategy and adhere to its requirements. 
* Track and publish the roadmap. 
* Continuously improve the operational posture.

### How are you testing your DevOps infrastructure? 
* Perform business continuity drills. 
* Perform disaster recovery and fault injection. 
* Automate testing on deployments. 
* Use manual testing when required.

## Security

### What design considerations did you make in your workload in regards to security? 
* Identified and classified business critical applications. 
* Adopted a DevOps approach to building software. 
* Leverage DevOps security guidance. 
* Use cloud services instead of building custom security implementations. 
* Use native security capabilities built into cloud services. 
* Implement security practices and tools during the development lifecycle. 
* Follow best practices for container security. 
* Install a web application firewall in front of your workload. 
* Authenticate via identity services where you can.

### What considerations for compliance and governance do you need to take? 
* Evaluate your security posture using standard benchmarks. 
* Remove virtual machine direct internet connectivity. 
* Monitor identity risk. 
* Perform penetration testing. 
* Prioritize security best practices. 
* Manage connected tenants. 
* Lines of responsibility are established. 
* There is an enterprise segmentation strategy in place. 
* The security team has read only access into all environments. 
* Use the root management group carefully. 
* Have a policy in place to apply security updates to VMs and strong password requirements. 
* Assigned a security incident notification contact. 
* Regularly review access from critical accounts. 
* Discover and remediate common risks. 
* Use blueprints to consistently deploy environments that comply with organizational policies. 
* Discover and replace insecure protocols. 
* Considered whether or not you need elevated security capabilities. 
* Assigned appropriate privileges for managing the environment. 
* Audit and enforce policy compliance.

### How are you managing encryption for this workload? 
* Use identity based storage access controls. 
* Enabled platform encryption services. 
* Data at rest is encrypted. 
* Data in transit is encrypted. 
* Encrypt your virtual disk files.

### How are you managing identity for this workload? 
* Use a single enterprise directory. 
* Synchronize your identity systems. 
* Use cloud provider identity sources for third parties. 
* Block legacy authentication protocols. 
* Perform attack simulation on users. 
* Enforce conditional access for users. 
* Do not synchronize your on-premises admin accounts to cloud identity providers. 
* Use cross-platform identity management. 
* Have an identity strategy. 
* Use modern password protection offerings. 
* Have passwordless or multi-factor authentication enabled.

### How have you secured the network of your workload? 
* Have centralized network management and security. 
* Aligned network segmentation with the enterprise segmentation strategy. 
* Security extends past your network boundaries. 
* Deprecated the use of legacy security technologies. 
* Enabled enhanced network visibility. 
* DDoS mitigation plan is in place. 
* Have an intentional subnet security strategy. 
* Have a security containment strategy. 
* Have an internet ingress/egress policy defined. 
* Have implemented an internet edge strategy.

### What tradeoffs do you need to make to meet your security goals? 
* Build the appropriate level of resilience into your security infrastructure. 
* Balanced attacker cost versus your own. 
* Contained attacker access.

### How are you ensuring your critical accounts are protected? 
* Simulate attacks against critical impact accounts. 
* Don't assign users with granular or custom permissions. 
* Established a lifecycle management policy for critical impact accounts. 
* Appropriate emergency access accounts configured.