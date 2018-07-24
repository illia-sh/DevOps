#### 0.what is devops?  https://aws.amazon.com/devops/what-is-devops/  
  * DevOps is a software engineering culture and practice that aims at unifying software development (Dev) and software operation (Ops).  
  The main characteristic of the DevOps movement is to strongly advocate automation and monitoring at all steps of software construction    
  ||  
  * DevOps is the combination of cultural philosophies, practices, and tools that increases an organization’s ability to deliver applications and services at high velocity: evolving and improving products at a faster pace than organizations using traditional software development and infrastructure management processes. This speed enables organizations to better serve their customers and compete more effectively in the market.  

#### 0.1 DevOps Best Practices  
  * Continuous Integration (Jenkins,TeamCity,Travis CI,Go CD,Bamboo,Gitlab CI,CircleCI)
  * Continuous Delivery  
  * Microservices  
  * Infrastructure as Code  
  * Monitoring and Logging  
  * Communication and Collaboration  

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
  * Gitflow Workflow  - is a Git workflow design that was first published and made popular by Vincent Driessen at nvie. The Gitflow Workflow defines a strict branching model designed around the project release.  

  * GitHub flow - https://www.freshconsulting.com/git-development-workflows-git-flow-vs-github-flow/
  
#### 5. Containerization vs virtualization ( Containers vs virtual machines )  https://blog.netapp.com/blogs/containers-vs-vms/
  * Containers and virtual machines have similar resource isolation and allocation benefits, but function differently because containers virtualize the operating system instead of hardware. Containers are more portable and efficient.


#### 6. Devops KPI 
https://puppet.com/blog/5-kpis-make-case-for-devops  
https://dzone.com/articles/devops-kpi-in-practicechapter-1deployment-speed-fr  

  * Deployment frequency    
  * Speed of deployment   
  * Deployment success rate / Failure rate   
  * Time to recovery / How quickly service can be restored after a failed deployment  
  * Change lead time  
  * Service availability
  
The business benefits of DevOps practices are clear. Companies that can deploy changes quickly and reliably are able to introduce new features and improvements in response to the market, and ahead of competitors. Their revenue streams are more dependable, and they can plan better for the future. 

#### 7. Continuous Integration (CI):   
  * short-lived feature branches, team is merging to master branch multiple times per day, fully automated build and test process which gives feedback within 10 minutes; deployment is manual.

#### 8. Continuous Delivery (CD): 
  * CI + the entire software release process is automated, it may be composed of multiple stages, and deployment to production is manual.

#### 9. Continuous Deployment (CI+CD):  
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
 
 #### 11.1 Chef Development Phases https://blog.chef.io/2015/04/21/overview-of-test-driven-infrastructure-with-chef/
  * Pre-convergence -  is the phase before a node is converged by Chef, and is the phase when testing that doesn’t require a node to run Chef happens. Syntax checking, lint checking, or unit tests are performed during pre-convergence. Automated testing in CI usually does pre-convergence tests, such as GitHub repositories configured with Travis CI.  
  * Convergence - is the phase when Chef runs and makes changes to the system to “converge” it to be in the desired state. This is where resources are tested for current state, and repaired (action taken by providers) if they’re not correct.
  * Post-convergence - is the phase after a node finishes running Chef. Testing in this phase verifies that the node is in the desired state. This can include checks that a particular port is listening, that a configuration file contains the correct content, or that a service is running with the proper configuration.

#### 11.2 Chef Types of Testing
  * Unit Testing - Unit tests are meant to execute fast, and happen without converging the node, so they are done in the pre-convergence phase. Unit testing Chef cookbooks is done with ChefSpec. It is very important that one does not fall into the trap of testing that Chef itself works.  
  * Integration Testing(inspec) - The intent of integration testing is to verify that the end state of the system is in fact what we wanted after Chef converges the node so we can have a higher degree of confidence that our code is doing what we need.

#### 11.3 Chef Vs Ansible
  * Ansible’s agentless push-mode using a ZeroMQ implementation at the transport layer means quick deployment and low performance overhead when triggering ad-hoc jobs from a developer workstation or a central resource like the Ansible tower.
  * Chef can work like pull-base client-agent however, Chef also provides a ZeroMQ-based push agent via its “push-jobs” add-on package.
   
#### 12.  Load Balancing methods  
  * Round Robin - A simple method of load balancing servers or for providing simple fault tolerance.  
  * Weighted Round Robin - This builds on the simple Round Robin load balancing method. In the weighted version each server in the pool is given a static numerical weighting. Servers with higher ratings get more requests sent to them.  
  * Least Connection - Neither Round Robin or Weighted Round Robin take the current server load into consideration when distributing requests. The Least Connection method does take current server load into consideration. The current request goes to the server that is servicing the least number of active sessions at the current time.  
  * Weighted Least Connection - Builds on the Least Connection method. Like in the Weighted Round Robin method each server is given a numerical value. The load balancer uses this when allocating requests to servers. If two servers have the same number of active connections then the server with the higher weighting will be allocated the new request.   
  * Agent Based Adaptive Load Balancing - Each server in the pool has an agent that reports on its current load to the load balancer. This real time information is used when deciding which server is best placed to handle a request. This is used in conjunction with other techniques such as Weighted Round Robin and Weighted Least Connection.
  * Chained Failover (Fixed Weighted) - In this method a predetermined order of servers is configured in a chain. All requests are sent to the first server in the chain. If it can’t accept any more requests the next server in the chain is sent all requests, then the third server. And so on.   
  * Weighted Response Time - This method uses the response information from a server health check to determine the server that is responding fastest at a particular time. The next server access request is then sent to that server. This ensures that any servers that are under heavy load, and which will respond more slowly, are not sent new requests. This allows the load to even out on the available server pool over time.   
  * Source IP Hash - Source IP Hash load balancing uses an algorithm that takes the source and destination IP address of the client and server and combines them to generate a unique hash key. This key is used to allocate the client to a particular server. As the key can be regenerated if the session is broken this method of load balancing can ensure that the client request is directed to the same server that it was using previously. This is useful if it’s important that a client should connect to a session that is still active after a disconnection. For example, to retain items in a shopping cart between sessions.     
   
  
  
### soft 

#### Agile/Scrum/Kanban https://www.atlassian.com/agile/kanban/kanban-vs-scrum

#### 1. Agile
 * Agile is a structured and iterative approach to project management and product development. It recognizes the volatility of product development, and provides a methodology for self-organizing teams to respond to change without going off the rails. Today, agile is hardly a competitive advantage. No one has the luxury to develop a product for years or even months in a black box. This means it’s more important than ever to get it right.

#### 2. Kanban – Incremental Improvements
 * Kanban is all about continuous development and delivery, tackling a small number of tasks fluidly and concurrently. Kanban teams use a visual planning tool—the kanban board—that displays each project (user story) on a card and moves cards through columns that represent progressive stages of completion. If your team has a continuous stream of work requests, kanban may be right for you.
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
 * It is how you manage the information systems that deliver value to your customers.ITSM could include activities like planning and managing changes so they don’t cause disruption to the business, fixing things when they go wrong

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
####  

  * RCA - root cause analysis 
  * ITSM - IT service management 
  * ITIL - Information Technology Infrastructure Library
  * CALMS - Culture / Automation /Lean practices /Measurement/ Sharing.  
