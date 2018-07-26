#### 0 what is devops?  https://aws.amazon.com/devops/what-is-devops/  
  * DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops).  
  The main characteristic of the DevOps movement is to strongly advocate automation and monitoring at all steps of software construction    
  ||  
  * DevOps is the combination of cultural philosophies, practices, and tools that increases an organization’s ability to deliver applications and services at high velocity: evolving and improving products at a faster pace than organizations using traditional software development and infrastructure management processes. This speed enables organizations to better serve their customers and compete more effectively in the market.  

#### 0.2 What is SRE? - https://cloudplatform.googleblog.com/2018/05/SRE-vs-DevOps-competing-standards-or-close-friends.html
SRE and DevOps share the same foundational principles.SRE ensures that everyone agrees on how to measure availability, and what to do when availability falls out of specification. This process includes individual contributors at every level, all the way up to VPs and executives, and it creates a shared responsibility for availability across the organization. SREs work with stakeholders to decide on Service Level Indicators (SLIs) and Service Level Objectives (SLOs).

#### 0.3 Agile vs Devops
  * Agile software development methodology focuses on the development of software but DevOps on the other hand is responsible for development as well as deployment of the software in the safest and most reliable way
  
#### 0.4 DevOps Best Practices  
  * Continuous Integration (Jenkins,TeamCity,Travis CI,Go CD,Bamboo,Gitlab CI,CircleCI)
  * Continuous Delivery  
  * Microservices  
  * Infrastructure as Code  
  * Monitoring and Logging  
  * Communication and Collaboration  

#### 0.5 SLA/SLO/SLI
  * SLA - A service-level agreement (SLA) is a commitment between a service provider and a client. Particular aspects of the service – quality, availability, responsibilities – are agreed between the service provider and the service user  
  * SLO - are specific measurable characteristics of the SLA such as availability, throughput, frequency, response time, or quality. These SLOs together are meant to define the expected service between the provider and the customer and vary depending on the service's urgency, resources, and budget. SLOs provide a quantitative means to define the level of service a customer can expect from a provider.    
  * SLI - is a Service Level Indicator (SLI). When we evaluate whether our system has been running within SLO for the past week, we look at the SLI to get the service availability percentage.
  
#### 0.6  
  * BDD – Behavior-Driven Development -  BDD is a set of best practices for writing great tests. BDD can, and should be, used together with TDD and unit testing methods.  
  * TDD - Test-Driven Development is a process for when you write and run your tests. Following it makes it possible to have a very high test-coverage. Test-coverage refers to the percentage of your code that is tested automatically, so a higher number is better
  * TDD VS BDD - Unit Testing gives you the what. Test-Driven Development gives you the when. Behavior Driven-Development gives you the how  

#### 0.7 What is Docker? - https://www.edureka.co/blog/interview-questions/docker-interview-questions/
  * Docker -  is a containerization platform which packages your application and all its dependencies together in the form of containers so as to ensure that your application works seamlessly in any environment be it development or test or production.

#### 0.8 - What is Docker container?
  * Docker containers include the application and all of its dependencies, but share the kernel with other containers, running as isolated processes in user space on the host operating system. Docker containers are not tied to any specific infrastructure: they run on any computer, on any infrastructure, and in any cloud.  

#### 0.8 What is Docker image?  
  * Docker image is the source of Docker container. In other words, Docker images are used to create containers. Images are created with the build command, and they’ll produce a container when started with run. Images are stored in a Docker registry such as registry.hub.docker.com because they can become quite large, images are designed to be composed of layers of other images, allowing a minimal amount of data to be sent when transferring images over the network.  
  
#### 0.9 - Docker layers ; https://medium.com/@jessgreb01/digging-into-docker-layers-c22f948ed612 
  * Layers of a Docker image are essentially just files generated from running some command. You can view the contents of each layer on the Docker host at /var/lib/docker/aufs/diff. Layers are neat because they can be re-used by multiple images saving disk space and reducing time to build images while maintaining their integrity.


#### 1. Three main cloud computing models: IaaS,SaaS,PaaS  
  * Infrastructure as a Service (IaaS) - Contains the basic building blocks for cloud IT and typically provide access to networking features, computers (virtual or on dedicated hardware), and data storage space. Infrastructure as a Service provides you with the highest level of flexibility and management control over your IT resources and is most similar to existing IT resources that many IT departments and developers are familiar with today.

  * Software as a Service (SaaS)  - is the simplest form of cloud computing. There is no third-party development or resource for the user, rather SaaS applications offer powerful tools right from your web browser that, in most cases, give users the ability to collaborate with others cheaply and from any location.( google docs, gmail ) 

  * Platforms as a service -  remove the need for organizations to manage the underlying infrastructure (usually hardware and operating systems) and allow you to focus on the deployment and management of your applications. This helps you be more efficient as you don’t need to worry about resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting involved in running your application.

#### 2. Cloud Computing Deployment Models
  * Cloud  
  * Hybrid  
  * On-premises  
 
#### 3. Deployment strategies https://thenewstack.io/deployment-strategies/ 

  * Recreate: Version A is terminated then version B is rolled out. 
  * Ramped (also known as rolling-update or incremental): Version B is slowly rolled out and replacing version A.
  * Blue/Green: Version B is released alongside version A, then the traffic is switched to version B.
  * Canary: Version B is released to a subset of users, then proceed to a full rollout.
  * A/B testing: Version B is released to a subset of users under specific condition.
  * Shadow: Version B receives real-world traffic alongside version A and doesn’t impact the response.

#### 4. Branch Strategy
https://www.atlassian.com/agile/software-development/branching   
   
  * Branching ( feature development[Feature branching,Task Branching,Release branching])   
 -- allow parallel development of distinct features   
 -- isolate changed without destabilitinz the codebase   
 -- integrate changes according to development process  

  * TRUNK(mainline) - A source-control branching model, where developers collaborate on code in a single branch called ‘trunk’   
  * Gitflow Workflow  - The Gitflow Workflow defines a strict branching model designed around the project release. https://datasift.github.io/gitflow/IntroducingGitFlow.html   

  * GitHub flow - https://www.freshconsulting.com/git-development-workflows-git-flow-vs-github-flow/
  * GitLab Flow - https://docs.gitlab.com/ee/workflow/gitlab_flow.html 
  https://about.gitlab.com/2016/07/27/the-11-rules-of-gitlab-flow/
  
  
#### 5. Containerization vs virtualization ( Containers vs virtual machines )  https://blog.netapp.com/blogs/containers-vs-vms/
  * Containers and virtual machines have similar resource isolation and allocation benefits, but function differently because containers virtualize the operating system instead of hardware. Containers are more portable and efficient.


#### 6. Devops KPI (metrics) 
https://puppet.com/blog/5-kpis-make-case-for-devops  
https://dzone.com/articles/devops-kpi-in-practicechapter-1deployment-speed-fr  
https://stackify.com/15-metrics-for-devops-success/

  * Deployment frequency    
  * Speed of deployment   
  * Deployment success rate / Failure rate   
  * Time to recovery / How quickly service can be restored after a failed deployment  
  * Change lead time  
  * Service availability
  
The business benefits of DevOps practices are clear. Companies that can deploy changes quickly and reliably are able to introduce new features and improvements in response to the market, and ahead of competitors. Their revenue streams are more dependable, and they can plan better for the future. 

#### 7. Continuous Integration (CI):   
  * Continuous Integration (CI) is a development practice that requires developers to integrate code into a shared repository several times a day. Each check-in is then verified by an automated build, allowing teams to detect problems early. By integrating regularly, you can detect errors quickly, and locate them more easily.Continuous Integration brings multiple benefits to your organization:
  
> Say goodbye to long and tense integrations  
> Increase visibility enabling greater communication  
> Catch issues early and nip them in the bud  
> Spend less time debugging and more time adding features  
> Build a solid foundation  
> Stop waiting to find out if your code’s going to work  
> Reduce integration problems allowing you to deliver software more rapidly  


#### 8. Continuous Delivery (CD): 
  * Continuous delivery is an extension of continuous integration to make sure that you can release new changes to your customers quickly in a sustainable way. This means that on top of having automated your testing, you also have automated your release process and you can deploy your application at any point of time by clicking on a button.

#### 9. Continuous Deployment (CI+CD): -  https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd
  * CI + CD + fully automated deployment to production.

https://www.quora.com/What-is-the-difference-between-continuous-integration-and-continuous-deployment


#### 10. What is a difference between "git rebase" and "git merge" 
  * https://www.atlassian.com/git/tutorials/merging-vs-rebasing  
  > Merge takes all the changes in one branch and merges them into another branch in one commit.   
  > Rebase says I want the point at which I branched to move to a new starting point  
  
  * Merge - Let's say you have created a branch for the purpose of developing a single feature. When you want to bring those changes back to master, you probably want merge (you don't care about maintaining all of the interim commits).  
  * Rebase - A second scenario would be if you started doing some development and then another developer made an unrelated change. You probably want to pull and then rebase to base your changes from the current version from the repo.  

#### 10.1 git pull vs git fetch
  *  In the simplest terms, git pull does a git fetch followed by a git merge  
  * You can do a git fetch at any time to update your remote-tracking branches under refs/remotes/<remote>/.  
This operation never changes any of your own local branches under refs/heads, and is safe to do without changing your working copy. I have even heard of people running git fetch periodically in a cron job in the background (although I wouldn't recommend doing this).  
A git pull is what you would do to bring a local branch up-to-date with its remote version, while also updating your other remote-tracking branches.  
 
#### 11. Chef Best Practicies 
> https://github.com/pulseenergy/chef-style-guide 
> https://docs.chef.io/ruby.html#patterns-to-follow
  * use the chef-client cookbook.
  * Use berkshelf to manage dependencies
  * Use ChefSpec to simulate the convergence of resources on a node ( Unit testing)( ChefSpec::SoloRunner.new(pla,); expect(chef_run).to create_templ...; ChefSpec is a framework that tests resources and recipes as part of a simulated chef-client run
  * Integration Testing ( test kitchen )
  * foodcritic
  * rubocop
  * Fauxhai - Fauxhai is a tool for mocking out ohai data to provide node attributes for testing. Fauxhai is used within ChefSpec.

#### 11.0 Monolithic vs single cookbook
  https://github.com/anniehedgpeth/chef-certification-study-guides/blob/master/local-cookbook-development/local-cookbook-development-study-guide.md  
  
#### 11.1 Chef Development Phases https://blog.chef.io/2015/04/21/overview-of-test-driven-infrastructure-with-chef/
  * Pre-convergence -  is the phase before a node is converged by Chef, and is the phase when testing that doesn’t require a node to run Chef happens. Syntax checking, lint checking, or unit tests are performed during pre-convergence. Automated testing in CI usually does pre-convergence tests, such as GitHub repositories configured with Travis CI.  
  * Convergence - is the phase when Chef runs and makes changes to the system to “converge” it to be in the desired state. This is where resources are tested for current state, and repaired (action taken by providers) if they’re not correct.
  * Post-convergence - is the phase after a node finishes running Chef. Testing in this phase verifies that the node is in the desired state. This can include checks that a particular port is listening, that a configuration file contains the correct content, or that a service is running with the proper configuration.  
>Load -> Compile -> Converge --> Cleanup  

  * ruby_block Use the ruby_block resource to execute Ruby code during a chef-client run. Ruby code in the ruby_block resource is evaluated with other resources during convergence, whereas Ruby code outside of a ruby_block resource is evaluated before other resources, as the recipe is compiled.  
  
#### 11.2 Chef Types of Testing
  * Unit Testing - Unit tests are meant to execute fast, and happen without converging the node, so they are done in the pre-convergence phase. Unit testing Chef cookbooks is done with ChefSpec. It is very important that one does not fall into the trap of testing that Chef itself works.  
  * Integration Testing(inspec) - The intent of integration testing is to verify that the end state of the system is in fact what we wanted after Chef converges the node so we can have a higher degree of confidence that our code is doing what we need.

#### 11.3 Chef Vs Ansible
  * Ansible’s agentless push-mode using a ZeroMQ implementation at the transport layer means quick deployment and low performance overhead when triggering ad-hoc jobs from a developer workstation or a central resource like the Ansible tower.
  * Chef can work like pull-base client-agent however, Chef also provides a ZeroMQ-based push agent via its “push-jobs” add-on package.
   
#### 12. Network: Load Balancing methods  
  * Round Robin - A simple method of load balancing servers or for providing simple fault tolerance.  
  * Weighted Round Robin - This builds on the simple Round Robin load balancing method. In the weighted version each server in the pool is given a static numerical weighting. Servers with higher ratings get more requests sent to them.  
  * Least Connection - Neither Round Robin or Weighted Round Robin take the current server load into consideration when distributing requests. The Least Connection method does take current server load into consideration. The current request goes to the server that is servicing the least number of active sessions at the current time.  
  * Weighted Least Connection - Builds on the Least Connection method. Like in the Weighted Round Robin method each server is given a numerical value. The load balancer uses this when allocating requests to servers. If two servers have the same number of active connections then the server with the higher weighting will be allocated the new request.   
  * Agent Based Adaptive Load Balancing - Each server in the pool has an agent that reports on its current load to the load balancer. This real time information is used when deciding which server is best placed to handle a request. This is used in conjunction with other techniques such as Weighted Round Robin and Weighted Least Connection.
  * Chained Failover (Fixed Weighted) - In this method a predetermined order of servers is configured in a chain. All requests are sent to the first server in the chain. If it can’t accept any more requests the next server in the chain is sent all requests, then the third server. And so on.   
  * Weighted Response Time - This method uses the response information from a server health check to determine the server that is responding fastest at a particular time. The next server access request is then sent to that server. This ensures that any servers that are under heavy load, and which will respond more slowly, are not sent new requests. This allows the load to even out on the available server pool over time.   
  * Source IP Hash - Source IP Hash load balancing uses an algorithm that takes the source and destination IP address of the client and server and combines them to generate a unique hash key. This key is used to allocate the client to a particular server. As the key can be regenerated if the session is broken this method of load balancing can ensure that the client request is directed to the same server that it was using previously. This is useful if it’s important that a client should connect to a session that is still active after a disconnection. For example, to retain items in a shopping cart between sessions.     
   
#### 13. Linux Load average(LA) - https://www.tecmint.com/understand-linux-load-averages-and-monitor-performance/
  * Load average(LA) – is the average system load calculated over a given period of time of 1, 5 and 15 minutes. In Linux, the load-average is technically believed to be a running average of processes in it’s (kernel) execution queue tagged as running or uninterruptible.  

#### 13.1 Filedescriptor (FD)  
  * Filedescriptor - In simple words, when you open a file, the operating system creates an entry to represent that file and store the information about that opened file. So if there are 100 files opened in your OS then there will be 100 entries in OS (somewhere in kernel). These entries are represented by integers like (...100, 101, 102....). This entry number is the file descriptor. So it is just an integer number that uniquely represents an opened file in operating system. If your process opens 10 files then your Process table will have 10 entries for file descriptors. Similarly when you open a network socket, it is also represented by an integer and it is called Socket Descriptor.
  * inode (inode)   - is a data structure in a Unix-style file system that describes a filesystem object such as a file or a directory. Each inode stores the attributes and disk block location(s) of the object's data.[1] Filesystem object attributes may include metadata (times of last change,[2] access, modification), as well as owner and permission data. https://www.cyberciti.biz/tips/understanding-unixlinux-filesystem-inodes.html  

#### 13.2 What-really-happens-when-you-type-ls - https://medium.com/meatandmachines/what-really-happens-when-you-type-ls-l-in-the-shell-a8914950fd73  
  * Alias file(s) are checked to see if a shortcut for the command has been previously set.  
  * Shell searches its own built-in functions to see if the token command’s program exists.  
  * shell will continue it’s search in the PATH, a list of directories whose content programs can be executed no matter where in the directory tree it is run. You can view which directory paths are in the PATH environmental variable by typing env  
  * To execute ls, three system calls are made:fork / execve / wait  

#### 13.3 How SSL works - https://www.digicert.com/ssl/  
  * Browser connects to a web server (website) secured with SSL (https). Browser requests that the server identify itself.  
  * Server sends a copy of its SSL Certificate, including the server’s public key.  
  * Browser checks the certificate root against a list of trusted CAs and that the certificate is unexpired, unrevoked, and that its common name is valid for the website that it is connecting to. If the browser trusts the certificate, it creates, encrypts, and sends back a symmetric session key using the server’s public key.  
  * Server decrypts the symmetric session key using its private key and sends back an acknowledgement encrypted with the session key to start the encrypted session.   
  * Server and Browser now encrypt all transmitted data with the session key.   

#### 14. SSO/SAML
  * SAML - Security Assertion Markup Language. is an open standard for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider. As its name implies,SAML is an XML-based markup language for security assertions (statements that service providers use to make access-control decisions).requests a service from the service provider. The service provider requests and obtains an authentication assertion from the identity provider.
  
  * SSO Single sign-on (SSO) is a session and user authentication service that permits a user to use one set of login credentials (e.g., name and password) to access multiple applications.  

#### 15. HighAvailability(HA) vs FaultToulerance  - https://blog.interfaceware.com/disaster-recovery-vs-high-availability-vs-fault-tolerance-what-are-the-differences/

### soft 


#### Agile/Scrum/Kanban https://www.atlassian.com/agile/kanban/kanban-vs-scrum

#### 1. Agile
 * Agile is a structured and iterative approach to project management and product development. It recognizes the volatility of product development, and provides a methodology for self-organizing teams to respond to change without going off the rails. Agile principles are all about being collaborative, flexible and adaptive.  Agile Methodologies Scrum and Kanban .

#### 2. Kanban – Incremental Improvements
 * Kanban is all about continuous development and delivery, tackling a small number of tasks fluidly and concurrently. Kanban teams use a visual planning tool—the kanban board—that displays each project (user story) on a card and moves cards through columns that represent progressive stages of completion. If your team has a continuous stream of work requests, kanban may be right for you.
 
#### 2.1 - What is an aim of KANBAN methodology, and why it works better in DevOps?
  * The Kanban Method follows a set of principles and practices for managing and improving the flow of work.Kanban has come to the software development world from the automotive industry (Toyota Production System). The aim is to achieve higher throughput with lower delivery lead times. The Main Core Practices of the Kanban Method:    
> 1) Visualize the flow of work  
> 2) Limit WIP (Work in Progress):   
> 3) Manage Flow:   
> 4) Make Process Policies Explicit   
> 5) Implement Feedback Loops   

  * "why it works better in DevOps" -    
>  1) Kanban combines multiple streams into one  
> 2) Gives leverage to say NO ( If your plate is full already, Kanban will tell you. You hit the WIP limits)  
> 3) Improves flow team communication    

  ###### Release Methodology    
> In kanban, updates are released whenever they are ready, without a regular schedule or predetermined due dates.       
> In theory, kanban does not prescribe a fixed time to deliver a task. If the task gets completed earlier (or later), it can be released as needed without having to wait for a preset release milestone, as in the case of scrum.    
#### 3. Scrum  
  * Scrum also splits out complex tasks into user stories and visualizes them on a workflow. Scrum teams commit to ship working software at the end of set intervals, called sprints. If you need to ship value to customers on a regular basis, scrum is the way.  
   ###### Scrum Roles:  
> The Product Owner owns and manages the product backlog, understands business requirements, and prioritizes the work to be done by the development team.     
> The Scrum Master manages the scrum board and workflow, and helps the team stay grounded in the scrum framework.   
> The development team completes the work and demonstrates collective accountability.    

#### 4. Kanban vs Scrum 
  * Looking at both agile software development methodologies it should be more clear what to introduce when: If your organization is really stuck and needs a fundamental shift towards a more efficient process, Scrum seems to be more appropiate. If you already have working processes, which you want to improve over time without shaking up the whole system, Kanban should be your tool of choice.
  
#### 5. Agility 
 * Agility is something different all together. Agility is a clean, un-opinionated agile board that progressively adds more structure when you need it. If you can’t decide between scrum and kanban, go with an agility project. 
 
#### 6. ITSM https://en.wikipedia.org/wiki/IT_service_management
 * It is how you manage the information systems that deliver value to your customers.ITSM could include activities like planning and managing changes so they don’t cause disruption to the business, fixing things when they go wrong.The goal of IT Service Management is to ensure that the right processes, people, and technology are in place so that the organization can meet its business goals.

#### 7. ITIL https://en.wikipedia.org/wiki/ITIL
 * set of detailed practices for IT service management (ITSM) that focuses on aligning IT services with the needs of business. ITIL describes processes, procedures, tasks, and checklists which are not organization-specific or technology-specific, but can be applied by an organization for establishing integration with the organization's strategy, delivering value, and maintaining a minimum level of competency. It allows the organization to establish a baseline from which it can plan, implement, and measure. It is used to demonstrate compliance and to measure improvement.ITIL is divided into a series of five core volumes, each covering a different ITSM lifecycle stage. These stages are:   
> Service Strategy   
> Service Design    
> Service Transition   
> Service Operation   
> Continual Service Improvement    


#### 8. Top Leadership Skills  https://www.thebalancecareers.com/top-leadership-skills-2063782   
 * Communication - you need to be able to clearly and succinctly explain to your employees everything from organizational goals to specific tasks.
 * Motivation - need to inspire their workers to go the extra mile for their organizations.   
 * Delegating - identify the skills of each of your employees, and assign duties to each employee based on his or her skill set.    
 * Positivity   
 * Feedback ( Following up, coaching , Mentoring ...) 
 * Responsibility - A leader is responsible for both the successes and failures of his or her team. Therefore, you need to be willing to accept blame when something does not go correctly. ( Acknowledging mistakes, Project planning, Resolving problems) 

#### 8.1 What key values should have a person who try to lead some project? 
  * 1) Recognising The Value Of Your Team Members  
  * 2) Involving The Team In Decisions That Affect Them  
  * 3) Being Prepared To Listen  
  * 4) Leading By Example ( One sure way to demonstrate your commitment to the role is to show what you can do. This means being a good role model for your team in terms of what you expect yourself in terms of behaviour.)  

#### 8.2 What are the ways to motivate a Team ? 
 * 1) insteseting tasks  
 * 2) Training  
 * 3) recognition  
 * 4) Listen  
 * 5) Use new technology  
 * 6) Flexible work hours  
 * 7) Respect  
 * 8) Opportunities for growth  
 
#### 9.RACI matrix (Responsible, Accountable, Consulted, and Informed) 
 * Responsible (also Recommender) Those who do the work to achieve the task
 * Accountable (also Approver or final approving authority), accountable must sign off (approve) work that responsible provides. There must be only one accountable specified for each task or deliverable
 * Consulted (sometimes Consultant )
 * Informed (also Informee)  Those who are kept up-to-date on progress, often only on completion of the task or deliverable;

#### 10. SDLC - Systems development life cycle 
  * SDLC is a process followed for a software project, within a software organization. It consists of a detailed plan describing how to develop, maintain, replace and alter or enhance specific software.
The life cycle defines a methodology for improving the quality of software and the overall development process.
>Planing --> Defining --> Designing --> Building --> Testing --> Deployment

#### 11.Task assignment VS Task delegation
  * An assignment is the process of transferring responsibility and accountability.
Delegation is the process by which responsibility and authority for performing a task or activity is transferred to another person.
#### 12. Incident Vs Problem (ITIL) - https://blog.samanage.com/it-service-management/whats-the-difference-between-problems-and-incidents/
  * An incident is an event that leads to an unplanned disruption of service. The important part to remember is ‘disruption of service,’ because if an issue does not disrupt service, even if it was unplanned and unexpected, it is not an incident. For example, if a piece of hardware fails after hours when nobody is using the system, it is not an incident, because it did not disrupt service. However, if the same equipment failed during the regular workday, it would be defined as an incident because service was, in fact, disrupted. The IT help desk is often the first ones to be made aware of an incident, as they are usually the first point of contact for users experiencing issues with the system.  
  * Problem - A problem is the underlying cause that leads to an incident. A problem may be something that could lead to the same incident occurring again, or lead to another incident entirely. The problem is essentially the root cause of an incident or incidents.

  * RCA - root cause analysis 
  * ITSM - IT service management 
  * ITIL - Information Technology Infrastructure Library
  * CALMS - Culture / Automation /Lean practices /Measurement/ Sharing. 
  * Atomic operations in concurrent programming are program operations that run completely independently of any other processes.
  * Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects", which may contain data, in the form of fields, often known as attributes; and code, in the form of procedures, often known as methods  
  * OAuth 2.0 is the industry-standard protocol for authorization( https://www.cubrid.org/blog/dancing-with-oauth-understanding-how-authorization-works ) 
