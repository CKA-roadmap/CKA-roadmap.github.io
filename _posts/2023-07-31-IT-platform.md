---
layout: page
title: IT platform
permalink: /it-platform/
categories: main
tags: main
nav_order: 4
---
# IT Industry Challenges
Dissertation on IT Industry Challenges.

Goals:
- How a systems department works and different models that I have found so far and vision of the possible roles that systems specialists play in companies.
- What are the possible futures of systems specialists (DevOps, SRE, Kubernetes, etc.), and how is the world of infrastructure evolving to face different challenges. (A booming industry indeed). This direction that the market is taking is in order to overcome different challenges and adapt to new needs.
- During the talk I will try to emphasize that OpenSource has revolutionized and is revolutionizing this entire world.
- The importance of the GSX subject since it provides a good base knowledge to start a career in the world of infrastructure. For example, it is impossible to be an SRE or Kubernetes specialist without a strong knowledge of systems and networks, since this is the basis.

The speech begins introducing how the IT industry works and what are tha current challenges and solutions. Afterwards, it gets a bit techy and introduces concepts to address the challenges in the IT industry. This doc is meant to provide a brief introduction, so none of the topics are covered in depth. It is meant for students or people getting started in the IT industry.

Only two main problems will be addressed. Other challenges have been left aside due to the scope of the dissertation.

Topics:
- 1. [System administration in the real workd](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#1-sysadmin-in-the-real-world)
- 2. [Challenges faced by systems departments](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#2-challenges-faced-by-systems-departments)
- 3. [Current solutions](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#3-current-solutions)
- 4. [Containers, Kubernetes and Cloud](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#4-containers-kubernetes-and-cloud)
- 5. [Infrastructure as code, configuration as code, and GitOps](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#5-infrastructure-as-code-configuration-as-code-and-gitops)
- 6. [Work methodologies](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#6-work-methodologies)
- 7. [Conclusions](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#7-conclusions)
- 8. [Resources](https://github.com/jangel97/k8s-for-dummies/blob/main/docs/Others/0.IT-Industry-Challenges.md#8-resources)

# 1. Sysadmin in the real world
Systems administration is the field of work in which someone manages one or more systems, be they software, hardware, servers, or workstations. Its goal is to ensure that systems work efficiently and effectively.

There are different specialities (some examples):
- DBA
- Network sysadmin
- Security admin
- Technical support staff
- System admin
- Hardware (datacenter people)

The following lists illustrates an example of the tasks a system administrator can work:
- Daily system/software checks.
- Making data backups.
- Application of operating system updates and configuration changes.
- Installation and configuration of new hardware/software.
- Add/delete/create/modify user account information, reset passwords, etc.
- Answer technical queries.
- Responsibility for security.
- Responsibility for documenting the system configuration and architecture of the different solutions.
- Troubleshooting of any reported issues or reported issues.
- System performance tuning.
- Keep the network running. (corporate network, VPN, DNS, DHCP, etc.)

Without a resilient infrastructure, fault-tolerant, high availability, adjusted to the needs of consumers (developers), monitoring and alerts, developers' applications could not function.

The main goal of being a sysadmin is to be as lazy as possible. Not lazy in the sense that you don't work, but lazy in the sense that you make the computer do the hard, repetitive work, and you do the thinking work.

In this link you can find an example on some of the requirements to become a system administrator: https://www.linkedin.com/jobs/collections/recommended/?currentJobId=3047489497

Important technologies (traditionally):
- Linux.
- Network skills. (HTTP, TCP, udp, dns, dhcpd, sshd, IPAM, etc)
- Cloud.
- Databases.
- Containers.
- Observability.
- Continuous integration / Continuos Delivery.
- Windows (Windows AD, domain controller).

It's good to know a little about various runtimes for example the JVM, python, golang, php, etc.

Troubleshooting skill is extremely important.

We could possibly split the responsibilities of a system admin in three different groups:
1. **Operational work**. Attend customer requests, for example:
- Create DNS records
- System patching and reboot
- Remove or create resources in hypervisors or cloud providers
- Network ACL
- Troubleshooting
2. **Engineering work**. Deliver new infrastructure offerings, for example:
- Automate operational tasks.
- Deliver new DNS solution
- Implement a new technological solution.
3. **Training**. It is vital to keep up to date, there are many interesting sysadmin certs out there, for example:
- https://www.redhat.com/es/services/training-and-certification
- https://www.cncf.io/certification/training/
- https://www.elastic.co/es/training/
- https://www.cisco.com/c/en/us/training-events/training-certifications/certifications.html

  You have to be up to date and expand in different fields of knowledge. The more things you know, the more value it adds to you and the better you can define your path as a technician.
  Official certifications, from Red Hat, other manufacturers or CNCF.

# 2. Challenges faced by systems departments
## Problem 1: Systems department as bottleneck of an IT organisation

What happens, imagine there are 1000 developer teams with 10k+ VMs in an organization and systems team. The systems department  becomes a brutal bottleneck for the organization and the whole company loses agility, which is key against competitors. Also, how reliable are more than 10k systems managed by a single systems team?

Scaling up (adding technical resources) is not a scalable solution to the problem.
Scaling out horizontally and dividing the systems department is an interesting alternative. The concept of productization is interesting here. An SLA can be defined per product. In this case, a given product would be an infrastructure or automation offering.

Therefore, the market is evolving in a different direction, and as new problems appear, the sector has to adapt more and more. Agility is key for organizations, and business value depends on how reliable and compliant the systems are.

An interesting strategy to solve this problem consists in providing tooling and each team of developers being responsible for their own systems. The systems team now has a totally different role in this regard, and it is that now it does not manage teams but rather provides the tools to make possible the administration and access to the functionalities of each of the products. Documentation is very important here. Also automation, if you can give access to certain functionality of a product through a form is ideal.

The idea is that the more autonomous the teams are, the less operational work, the better offering and the greater agility for the organization. Of course, it is important to help the teams if necessary to use the tooling, consultation.

## Problem 2: Gap between systems and development departments
DevOps movement was born to narrow the gap between both departments.
This movement dates back to between 2007 and 2008, when the software development and IT operations communities came together to address a pressing concern in the industry. Both parties felt that there was a fatal level of dysfunction caused by the traditional model of software development. In the model, the people who develop the code and those who implement and support it work independently, organizationally, and functionally. Additionally, developers and IT professionals (Ops) worked in siled teams with different leadership, KPIs, goals, and physical locations.

Both communities stated that there was a better way of doing things than working in silos. They started online forums and local meetings to develop a way forward. In 2009, the first DevOps event was held in Belgium to achieve greater efficiency in software development. From its humble beginnings, DevOps is a hot topic in IT today.

Challenges addressed here:

1. Overcome the development versus operations mindset
2. Faster time to market
3. Speed up time to resolution of development issues
4. Optimize productivity

Personally I like to explain the conflict between Ops and Dev with the factory metaphor:
Imagine a factory where there are two teams:
- Team A dedicated to going to work to produce at the factory.
- Team B that goes into building plants and reactors and maintaining them. If needed provides new features in the factory tools and creates new plants and tooling for team A.

It turns out that these teams do not understand each other, because neither of them is capable of understanding the needs of the other, here is a major collaboration problem. In the end, this problem ends up generating unproductiveness and loss of business value, because of a considerable lack of agility.

Possible solutions? Check out the following topics.

# 3. Current solutions
## Solution to problem I. Site Reliability Engineering
Let us suppose an organisation of thousands of development teams. Imagine if systems team is required to manage resourcses, corporate network, Storage, accesses and so on for all developer teams. It is just unfeasible.

One solution to this problem is the Site Reliability Engineering. Let's split each responsability in a product offering managed by a virtual team behind IT.

Each team should be responsible of devlivering the tooling, documentation and automation to the development teams so they can, by themselves, manage their infrastructure.

SRE is what you get when you treat operations like a software problem.
The SRE mission is to protect, deliver, and advance the software and systems behind all different environments with an ever-vigilant eye on availability, latency, performance, and capacity. In order to achieve it, all infrastructure must be managed seemengly.

Standardization and automation are two important elements of the SRE model. Site reliability engineers must always look for ways to improve and automate operational tasks.

## Solution to problem II. DevOps engineering

In order to narrow the gap between Ops and Devs the DevOps movement was born (aforementioned in previous topic).
The idea of DevOps is that if you are a company with 100 developers and you compete against one that has 10,000. The only way you can make is by being agile. This implies important changes in organizations. Among these, one of the most important changes is the idea that the systems department and the development department have to begin to understand each other.

If you remember the factory metaphor, it is similar to the ongoing situation in the IT industry.

In the case of the IT Industry the idea of a hybrid profile is born. A profile that is capable of mediating between both teams.
In the case of software engineering, what this profile does is that the developer builds and deploys applications automatically and does not have to worry about the environment or the infrastructure. Concepts like CI/CD apply here. In the end, these new professionals build a platform where build and deploy is automatic. These new professionals know how the applications work (not at the level of a developer) as well as its requirements, and they also have the infrastructure knowledge to maintain this automatic construction and deployment platform.

Although DevOps is a cultural movement, some IT organisations call DevOps Engineer to this role, the main responsibility of which, is to narrow down the gap between Ops and Devs and speed up the delivery of applications, features and bugs.

Currently, in an organisation it is possible that system team has evolved into a SRE team and provide tooling, docs and consultation, so teams can manage infrastructure seemingly. As for DevOps engineers, it is possible that they exist either in the same Development teams or in a specific Delivery team. DevOps teams must be capable of using the SRE tooling to manage the required infrastructure for the applications to run.

These types of professionals are highly demanded because they significantly increase agility in organizations.

Currently, in some organizations the roles of devops and SRE can be a bit mixed. You may apply to a devops position and see that the requirements ask for a bit of SRE and DevOps.

You can find what are the responsabilities for a DevOps engineer or a Site Reliability Engineer in the following links:
- https://www.linkedin.com/jobs/search/?keywords=sre
- https://www.linkedin.com/jobs/search/?keywords=devops


# 4. Containers, Kubernetes and Cloud

The changes required in the IT organisations to tackle the aforementioned problems, require new technology. In this topic we will introduce new technologies vital to address both problematics.

## Containers

Linux containers are technologies that allow you to package and isolate your applications along with the entire runtime environment, that is, with all the files that they require to run. This allows you to move the application inside the container between environments (development, test, production, etc.), without losing any of its functionality.

![image](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/bltb6200bc085503718/5e1f209a63d1b6503160c6d5/containers-vs-virtual-machines.jpg)

You can easily build your own containers (or containerize existing ones). It's a nice consistent way to package your apps.
https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

**Pros**
- *Less overhead*

  Containers require less system resources than traditional or hardware virtual machine environments because they don’t include operating system images.
- *Increased portability*

  Applications running in containers can be deployed easily to multiple different operating systems and hardware platforms.
- *More consistent operation*

  DevOps teams know applications in containers will run the same, regardless of where they are deployed.
- *Greater efficiency*

  Containers allow applications to be more rapidly deployed, patched, or scaled.
- *Better application development*

  Containers support agile and DevOps efforts to accelerate development, test, and production cycles.

The pros make them specially suitable for microservices architectures. https://microservices.io/

**Use cases**
- *“Lift and shift” existing applications into modern cloud architectures*

  Some organizations use containers to migrate existing applications into more modern environments. While this practice delivers some of the basic benefits of operating system virtualization, it does not offer the full benefits of a modular, container-based application architecture.

  Lift and shift is a strategy for moving an application or operation from one environment to another without stopping to redesign the app or operations workflow.

- *Refactor existing applications for containers*
  Although refactoring is much more intensive than lift-and-shift migration, it enables the full benefits of a container environment.
- *Develop new container-native applications*
  Much like refactoring, this approach unlocks the full benefits of containers.
- *Provide better support for microservices architectures*
  Distributed applications and microservices can be more easily isolated, deployed, and scaled using individual container building blocks.
- *Provide DevOps support for continuous integration and deployment (CI/CD)*
  Container technology supports streamlined build, test, and deployment from the same container images.
- *Provide easier deployment of repetitive jobs and tasks*
  Containers are being deployed to support one or more similar processes, which often run in the background, such as ETL functions or batch jobs.

Containers in the end are Linux Processes. In order to provide isolation and control of resources they rely on following Kernel Linux features:
- Linux namespaces (isolation) https://en.wikipedia.org/wiki/Linux_namespaces
- cgroups v2 (control of resources) https://www.kernel.org/doc/html/latest/admin-guide/cgroup-v2.html
- chroot (file system isolation) https://btholt.github.io/complete-intro-to-containers/chroot

For now it's enough to provide a brief introducion into the container concept. If you wish to learn more about this, please, check out the following resources:
- https://podman.io/
- https://docs.podman.io/en/latest/Tutorials.html
- https://developers.redhat.com/blog/2018/08/29/intro-to-podman
- https://docs.docker.com/develop/develop-images/dockerfile_best-practices/
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#containerd
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#cri-o
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#docker
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#mcr
- https://www.aquasec.com/cloud-native-academy/container-security/container-runtime/

## Kubernetes
The name Kubernetes originates from Greek, meaning helmsman or pilot. K8s as an abbreviation results from counting the eight letters between the "K" and the "s". Google open-sourced the Kubernetes project in 2014. Kubernetes combines over 15 years of Google's experience running production workloads at scale with best-of-breed ideas and practices from the community.

What is Kubernetes and how does it work?
Kubernetes is an open source container orchestration platform designed to automate the use, scaling, and management of containerized applications. In fact, Kubernetes has established itself as the de facto standard for container orchestration.

Kubernetes makes it easy to use and operate applications in a microservices architecture. To do this, an abstraction layer is created on top of a group of hosts, so that development teams can deploy their applications and let this technology manage activities such as:
- Control resource consumption by application or system.
- Evenly spread application load across a host infrastructure.
- Automatically balance load requests between different instances of an application.
- Monitor resource consumption and resource limits to automatically prevent applications from consuming too many resources.
- Move an application instance from one host to another if there is a shortage of resources on a host, or if the host dies.
- Automatically take advantage of additional resources available when a new host is added to the cluster.
- Easily perform canary rollouts and rollbacks. These displays are named after the canaries that were used by miners in the past to detect gas leaks underground. In this context, the Canary deployment allows us to observe the impact of a deployment with a low impact on users.

**Pros:**
- Scalability and load balancing
- Isolation of processes and applications
- Ease of deployment
- Automatic resource optimization resources automatically
- High availability

**Cons:**
- Extremely difficult to administer.

**Use cases:**
- Manage and orchestrate thousands of containers.
- Use declarative style to deploy applications accross the cluster seemingly.

**Kubernetes architecture:**
![image](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg)
A Kubernetes cluster is a form of Kubernetes deployment architecture. Basic Kubernetes architecture exists in two parts: the control plane and the nodes or compute machines. Each node could be either a physical or virtual machine and is its own Linux environment. Every node also runs pods, which are composed of containers.

Kubernetes architecture components or K8s components include the Kubernetes control plane and the nodes in the cluster. The control plane machine components include the Kubernetes API server, Kubernetes scheduler, Kubernetes controller manager, and etcd. Kubernetes node components include a container runtime engine or docker, a Kubelet service, and a Kubernetes proxy service.

**Resources:**
- https://www.redhat.com/en/topics/containers/what-is-kubernetes
- https://www.redhat.com/topics/containers/kubernetes-architecture
- https://kubernetes.io/
- https://docs.okd.io/
- https://en.wikipedia.org/wiki/Kubernetes

## Cloud
Cloud Computing consists of offering computing services through the network using cloud storage. With this type of service, the user does not have to install anything on his computer, however, he will have access to different services (from the most everyday to the technical).

*Public Cloud:* virtual resources and computer services provided by third parties via the Internet for several mandates simultaneously.

*Private Cloud:* computing services and computing environments reserved for an organization such as intranets or data centers. In other words, your services are not provided or hosted for multiple clients.

*Hybrid Cloud:* Combines public and private cloud services. To do this, it uses local data centers and external public cloud services.

*Multicloud:* Simultaneous use of the same cloud model (either public or private cloud) from different cloud providers. Thus, companies use several private or public clouds in parallel.

**Pros:**
- Reduced IT costs (the cost of system upgrades, new hardware and software may be included in your contract, you no longer need to pay wages for expert staff, your energy consumption costs may be reduced, there are fewer time delays).
- Scalability
  Your business can scale up or scale down your operation and storage needs quickly to suit your situation, allowing flexibility as your needs change.
- Access to multiple integrations. Cloud providers usually offer multiple products which integrate with each other, creating awesome integrations.

**Cons:**
- Data protected environments.
  Depending on the data confidentiality it may not be possible to run workloads on cloud-providers.
- Loss of control of the underlying resources.
  The underlying resources are managed by the cloud provider.
- Vendor lock-in.
  The vendor lock-in problem in cloud computing occurs when clients become reliant (i.e., locked-in) on a single cloud provider's technological implementation and are unable to switch vendors in the future without incurring significant fees, legal restrictions, or technical incompatibilities.

** Main cloud providers **
- https://aws.amazon.com/
- https://azure.microsoft.com/
- https://cloud.google.com

# 5. Infrastructure as code, configuration as code, and GitOps
There are other approaches that also try to solve the challenges that we have seen in the previous points. They are not contrary ideas nor do they try to compete with what I have explained before, in fact they are complementary. It is worth commenting on these approaches, given that the market is going in this direction and they are part of the resolution of the challenges that we have discussed.

**Infrastructure as code
IaC is about describing the desired infrastructure in a file, written in a structured manner (code), so that an automation tool or engine can take that description and provision the infrastructure, or reconfigure an already-deployed infrastructure so it matches that description.

For example, I can have my virtual machines and my configurations in code. If I introduce a change in the code I can propagate the changes to all my infrastructure, I don't have to go machine by machine or do manual operations, everything is in the form of code. The code can be maintained by a team of few people, and it can manage a giant infrastructure in a “simple” way. However, a giant infrastructure requires many people to manage it.
Also the code can be tested, have pipelines, amongst many other stuff.
The idea is that if we have everything as code, it is much easier to maintain things, and automate all kind of operational tasks.
This approach is vital for SRE, if you need to manage thousands of resources, there is no way around it.

My favorites tools for IaaC:
- https://www.ansible.com/
- https://www.terraform.io/

## Configuration as code
CaC is the practice of managing configuration files in a repository. Config files establish the parameters and settings for applications, server processing, operating systems. By managing your config files alongside your code, you get all the benefits of version control for your entire product.
If I can map my config files, for example via Ansible, I can manage seemingly the configuration on thousands of systems.

My favorites tools for CaaC:
- https://www.ansible.com/
- https://github.com/ansible/awx

## GitOps
```
Gitps = IaC + MRs + CI/CD
```
```
Gitps = CaC + MRs + CI/CD
```

What is a Gitlab MR? https://docs.gitlab.com/ee/user/project/merge_requests/
What is CI/CD? https://www.redhat.com/topics/devops/what-is-ci-cd

My favourite tools for GitOps:
- https://docs.gitlab.com/ee/ci/
- https://argo-cd.readthedocs.io/en/stable/

In my opinion some of the benefits of the previous approaches are:
- Scalability
- Standardization
- Traceability
- Increased Productivity


# 6. Work methodologies

The way SRE and DevOps team deliver new features is key, project management plays a vital role in agility. The defacto model in the industry nowadays is Agile https://scrumguides.org/scrum-guide.html#daily-scrum

What is Agile?

Agile software development encompasses an approach to decision making in software projects, which refers to software engineering methods based on iterative and incremental development, where requirements and solutions evolve over time as needed. of the project

# 7. Conclusions
- The market adapts to new needs.
- New technological solutions are born to solve the needs.
- New needs and technologies also pose new challenges. The IT sector is transformed into a radically new paradigm.
- Open-source is vital in this transformation. Without community effort none of the tools that provide the transformation would possibly exist. Open-source shapes the world.
- Even though everything changes, the knowledge is ALWAYS the same. I personally believe that University is a great way to acquire this basic knowledge.
- No solution is perfect. It all depends on the use case or the problem we are trying to approximate.
- DevOps and Site Reliability Engineering have revolutionized providing solutions to both aforemetioned problems

# 8. Resources
https://en.wikiversity.org/wiki/System_administration

https://www.redhat.com/es/services/training-and-certification

https://www.cncf.io/certification/training/

https://www.elastic.co/es/training/

https://www.cisco.com/c/en/us/training-events/training-certifications/certifications.html

https://www.redhat.com/es/topics/devops

https://aws.amazon.com/es/devops/what-is-devops/

https://azure.microsoft.com/en-us/overview/what-is-devops/

https://www.redhat.com/es/topics/devops/what-is-sre

https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

https://docs.gitlab.com/ee/ci/

https://argo-cd.readthedocs.io/en/stable/

https://www.ansible.com/

https://www.terraform.io/

https://www.redhat.com/en/topics/containers/what-is-kubernetes

https://www.redhat.com/topics/containers/kubernetes-architecture

https://kubernetes.io/

https://docs.okd.io/

https://en.wikipedia.org/wiki/Kubernetes

https://podman.io/
