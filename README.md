# Certified-Kubernetes-Cloud-Native-Associate-KCNA

[Kubernetes Cloud Native Associate KCNA Certification Course](https://www.udemy.com/course/dive-into-cloud-native-containers-kubernetes-and-the-kcna/)

👉 All additional files are stored on Google Disc in the folder Certification `Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)`


[Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/)
[CNCF Landscape](https://landscape.cncf.io/) - list of CNCF applications.

## Cloud Native Architecture Fundamentals
Characteristics of Cloud Native Applications
Cloud Native Applications harness the power of the cloud to provide increased resilience, agility, operability, and observability. Let's dive a bit deeper into these characteristics.

### Resiliency
Resilient applications are designed to withstand failures and continue to function or recover quickly. They typically make use of patterns such as redundancy, failover, and graceful degradation. Self-healing, where systems automatically detect and recover from failure, is a key aspect of resilient cloud-native applications. Kubernetes, for instance, has a built-in self-healing mechanism where it maintains a desired number of pod replicas and replaces failed instances.

### Agility
Agility in the context of cloud-native applications refers to the ability to quickly build, modify, and deploy applications. Agile practices such as microservices and continuous delivery pipelines, backed by automation, promote rapid iteration and responsiveness to change.

### Operability
Operability encompasses the ease of deploying, running, and managing applications. Cloud-native applications are designed to be easily monitored, configured, and maintained. They typically leverage automation and Infrastructure as Code (IaC) tools like Terraform to streamline operations and minimise toil.

### Observability
Observability is the ability to understand the internal state of your system based on the outputs it generates. It's a critical component in diagnosing issues and understanding how an application behaves in the wild. Logging, monitoring, and tracing (collectively known as the 'three pillars of observability') are vital practices to understand the state and performance of cloud-native applications.

It is important as part of your studies especially if you’re planning on taking the KCNA exam to remember these characteristics! A friendly anagram for this is “RAOO: Racoons are Often Observant” -

Racoons Are Often Observant = Resiliency, Agility, Operability, Observability



## Key Pillars of Cloud Native Architecture
Building upon the characteristics and practices discussed, cloud-native architecture is sometimes referenced as being founded on four key pillars:

### Microservices Architecture

Microservices architecture involves breaking down the application into loosely coupled, independently deployable components, each focusing on a single responsibility. This design enables agility, scalability, and resilience as each microservice can be developed, scaled, and managed independently.

### Containerisation

Containerisation involves encapsulating an application with its dependencies into a container, which can run uniformly across different environments. It facilitates isolation, consistency, and efficiency, making applications easier to build, deploy, and manage.

### DevOps

DevOps is a collaborative approach that combines software development (Dev) and IT operations (Ops) to enhance the efficiency, reliability, and speed of software delivery. By fostering a culture of excellence, DevOps emphasises automation, monitoring, and collaboration across development and operations teams.

### Continuous Delivery (CD)

Continuous Delivery is a practice where code changes are automatically built, tested, and prepared for a release to production. CD accelerates the release cycle, enhances productivity, and reduces the risk, complexity, and downtime of application deployment.

In essence, building cloud-native applications is a strategy that promotes agility, resilience, operability, and observability by leveraging modern technological practices.

With a clear understanding of these characteristics and key pillars, organisations can fully exploit the advantages of cloud-native architectures.

This is also an important area for your studies especially with reference to the KCNA exam. A friendly acronym for this is Morning Coffee Delivers Caffeine Delight = Microservices, Containerisation, DevOps, Continuous Delivery.



## Autoscaling
For the upcoming video, as you prepare for the KCNA Certification, please give special attention to these key topics:

- The concepts of Horizontal and Vertical Scaling and their respective significances
- The functionality and role of the Kubernetes Cluster Autoscaler
- An understanding of Keda, the utilization of ScaledObjects, and its capability for Scaling to Zero
- The distinctions between Vertical Pod Autoscaler (VPA) and Horizontal Pod Autoscaler (HPA)


[Cluster Autoscaler and Karpenter](https://kubernetes.io/docs/concepts/cluster-administration/node-autoscaling/) are the two Node autoscalers currently sponsored by SIG Autoscaling. 

[HPA vs VPA (Horizontal Pod Scaling vs Vertical Pod Scaling](https://kubernetes.io/docs/concepts/workloads/autoscaling/)

[Keda](https://github.com/kedacore/keda) allows for fine-grained autoscaling (including to/from zero) for event driven Kubernetes workloads. KEDA serves as a Kubernetes Metrics Server and allows users to define autoscaling rules using a dedicated Kubernetes custom resource definition.
KEDA can run on both the cloud and the edge, integrates natively with Kubernetes components such as the Horizontal Pod Autoscaler, and has no external dependencies.


## Serverless
- KNative
- OpenFaaS


## Cloud Native Personas
From a KCNA examination viewpoint, please pay attention to the following areas in the next video and further study guide which relate to common exam topics -

- Understand and recognise the acronyms commonly associated with the role of SRE, i.e. SLA, SLO and SLI
- Understand the role of SRE and how this differs to DevOps
- The role of FinOps for financial accountability

### 📝 SLA (Service Level Agreement)
Definition: A formal, contractual agreement between a service provider and a customer.

Purpose: Defines what level of service is expected, and what happens (e.g., penalties or credits) if the provider fails to meet that level.

Audience: External (legal/customers).

Example: “Our API will have 99.9% uptime per month. If uptime drops below that, we’ll issue a 10% credit.”

### 🎯 SLO (Service Level Objective)
Definition: A specific measurable goal for a particular aspect of service performance (like availability or latency).

Purpose: Internally used to track and manage reliability.

Audience: Internal (engineers, product teams).

Example: “We aim for 99.95% availability over a rolling 30-day window.”

### SLI (Service Level Indicator)
SLI = the actual measurement.

For example: “This month’s uptime was 99.96%” → that's your SLI.

| Term    | Meaning                 | Scope            | Audience             | Legal? | Example                       |
| ------- | ----------------------- | ---------------- | -------------------- | ------ | ----------------------------- |
| **SLA** | Service Level Agreement | Contractual      | External (Customers) | ✅ Yes  | "99.9% uptime, or credit"     |
| **SLO** | Service Level Objective | Operational goal | Internal             | ❌ No   | "99.95% uptime target"        |
| **SLI** | Service Level Indicator | Measurement      | Internal             | ❌ No   | "Uptime last 30 days: 99.96%" |



## Open Standards
For the KCNA examination, please pay attention to the following areas in the next video -

- Role of the Open Container Initiative (OCI)
- The reference implementation of the OCI runtime specification
- Different types of Open Standards, i.e. CNI, CRI, CSI

### 📦 Key Open Standards in Cloud-Native Systems

| **Acronym**        | **Full Name**                | **What It Standardizes**                | **Used By**                  |
| ------------------ | ---------------------------- | --------------------------------------- | ---------------------------- |
| **CNI**            | Container Network Interface  | **Networking** (IP assignment, routing) | Kubernetes, Nomad, OpenShift |
| **CRI**            | Container Runtime Interface  | **Container runtime abstraction**       | Kubernetes                   |
| **CSI**            | Container Storage Interface  | **Storage provisioning and mounting**   | Kubernetes, OpenShift, etc.  |
| **OCI**            | Open Container Initiative    | **Image format & runtime**              | Docker, Podman, containerd   |
| **SDS**            | Software-Defined Storage     | **Storage abstraction via software**    | Ceph, Rook                   |
| **SCS**            | Secure Compute Specification | **Confidential computing standards**    | Intel TDX, AMD SEV, etc.     |
| **SMI**            | Service Mesh Interface       | **standard API specification on kubernetes**    |     |
| **OPA/Gatekeeper** | Open Policy Agent            | **Policy as Code / Authorization**      | Kubernetes admission control |


