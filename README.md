# Certified Kubernetes Cloud Native Associate (KCNA)

[Kubernetes Cloud Native Associate KCNA Certification Course](https://www.udemy.com/course/dive-into-cloud-native-containers-kubernetes-and-the-kcna/)
[Course GitHub link](https://github.com/spurin/diveintokcna)
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



## Introduction to Containers
- namespaces
- [cgroups](https://www.kernel.org/doc/html/latest/admin-guide/cgroup-v1/cgroups.html)



### Container Networking Services and Volumes
Challenge:

Create and run 3 Nginx containers with different content using volumes. Each container should serve its own custom HTML page. Each container should be accessible on the localhost with it’s own unique port

Solution:
```
% cd /tmp
% mkdir website1 website2 website3

% echo 1 > website1/index.html
% echo 2 > website2/index.html


% docker run -d --rm -p 12301:80 -v /tmp/website1:/usr/share/nginx/html nginx
844b0ddbccd795d16d2bc78368c23114e095dfffe46c1ced97e5b10ef0ae69b8

% docker run -d --rm -p 12302:80 -v /tmp/website2:/usr/share/nginx/html nginx
ad7892ac554ae3b2a1f385f3e2a2f20e107832ab7235b7485a9552e04aac9ae0


% curl http://localhost:12301
% curl http://localhost:12302
```

## Kubernetes Fundamentals

### Kubernetes Architecture
For the KCNA Examination it is important to have a thorough understanding of the Kubernetes Architecture and the roles of specific components:

- The role of the kubelet and how it interacts with the CRI (Container Runtime Interface)
- The role of the kube-scheduler
- The role of the kube-proxy
- The role of the kubeapi-server
- The role of etcd
- Container Runtimes and the differences between high level and low level runtimes
- The hierarchy of Kubernetes components - From Cluster to Node to Pod to Container
- What is the CCM (Cloud Controller Manager) and where this would reside in a Kubernetes cluster

### Install docker extensions
The extension below can be opened in Docker Desktop on the `Extensions` tab. Login\password: root
```
docker extension install spurin/diveintokcna-lab-extension
```

### Google Cloud Shell
https://github.com/spurin/diveintokcna/tree/cloudshell

### k3s Kubernetes Cluster
k3s, a streamlined Kubernetes distribution, to minimise the system resource requirements. The implementation of k3s enables us to comprehensively address the entire curriculum necessary for the KCNA examination.


### kubectl port forward
`kubectl port-forward` is a command used to forward one or more local ports to a port on a pod in your Kubernetes cluster. It’s especially useful for debugging services or accessing internal pods without exposing them via LoadBalancer or Ingress.

```
kubectl port-forward pod/my-pod 8080:80 8443:443
```

### Dry run
The `--dry-run` flag simulates a command. It validates your YAML or CLI input and shows the result, but does not apply any changes to the cluster.

Examples
✅ Validate a Deployment manifest:

Checks if deployment.yaml is valid — but doesn’t apply it.
```
kubectl apply -f deployment.yaml --dry-run=client
```
✅ Generate YAML from command (preview):

Outputs the YAML that would be created, but does not create anything.
```
kubectl create deployment myapp --image=nginx --dry-run=client -o yaml
```

### kubectl Explain 

```
kubectl explain pod.spec.restartPolicy

[sudo] password for defaultuser:
KIND:       Pod
VERSION:    v1

FIELD: restartPolicy <string>
ENUM:
    Always
    Never
    OnFailure

DESCRIPTION:
    Restart policy for all containers within the pod. One of Always, OnFailure,
    Never. In some contexts, only a subset of those values may be permitted.
    Default to Always. More info:
    https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy

    Possible enum values:
     - `"Always"`
     - `"Never"`
     - `"OnFailure"`
```

### Imperative and Declarative commands

Imperative commands like `kubectl create`, `kubectl update` provide explicit instructions to the cluster.

Declarative commands like `kubectl apply` provides desired state of a resource\resources. Can be executed multiple times without errors.


### Group Commands with {} — Execute Sequentially in the Same Shell
All commands are executed sequentially. `{ command1; command2; command3; }`

They run in the same shell (they can share variables).
The entire group must be followed by a semicolon (;) or a newline before the closing }.

🔸 Example:

```
{ echo "Starting..."; ls -l; echo "Done."; }
```


### Init containers vs Sidecar containers
[Init containers vs Sidecar containers](https://kubernetes.io/docs/concepts/workloads/pods/init-containers/)

### Get logs for a crashed container
The `-p` flag in kubectl logs stands for "previous". It allows you to view the logs of a container from its previous instance, before it was restarted.

🧠 Full Command:
```
kubectl logs -p <pod-name> [-c <container-name>]
```


## Kubernetes Namespaces (NS)
Key areas to concentrate on include:

- Default Namespaces in Kubernetes: Understand the predefined namespaces that come with a Kubernetes cluster and their specific purposes
- Kubernetes API Objects and Namespaces: Kubernetes API objects that can operate within namespaces. Specific focus should be given to ResourceQuotas and LimitRanges
- Role-Based Access Control (RBAC) in Relation to Namespaces: The purpose of RBAC and the relationship with namespaces
- Namespaced vs Non-Namespaced Kubernetes Components: The distinction between namespaced and non-namespaced components in Kubernetes, such as the difference between pods (namespaced) and nodes (non-namespaced)
- Kubernetes resources: How to list resources and how to check if a resource is namespaced or non-namespaced

Purposes:
- isoltion
- resource management - resource quatas (for a whole namespace)
- resource management - resource limits (for each pod)
- security (RBAC) - only allowed users have access to resources within the namespace
- security (RBAC) - for the whole k8s cluster

Different namespaces can have resources with the same names. It should be unique in scope of one namespace

Namesapces (ns) explanation:
`K8s cluster -> namespace -> pods -> resources`

it's like

`Town -> house -> room -> an object in the room`

### Contexts
🧩 A context is made up of 3 parts:
| **Component** | **What it means**                         |
| ------------- | ----------------------------------------- |
| **Cluster**   | The Kubernetes API server to connect to   |
| **User**      | The credentials (e.g. token, cert) to use |
| **Namespace** | The default namespace for commands        |


🛠 Example Context Configuration (~/.kube/config):
```
contexts:
- name: dev-cluster
  context:
    cluster: dev
    user: dev-user
    namespace: development
```
In this context:

- kubectl talks to the cluster named dev
- Uses credentials from dev-user
- Defaults to the development namespace

✅ Common kubectl Context Commands
| **Command**                                 | **What It Does**                    |
| ------------------------------------------- | ----------------------------------- |
| `kubectl config get-contexts`               | Lists all available contexts        |
| `kubectl config current-context`            | Shows the current active context    |
| `kubectl config use-context <context-name>` | Switches to a different context     |
| `kubectl config set-context ...`            | Create or modify a context manually |
| `kubectl config delete-context <name>`      | Deletes a context from config       |


### 🛠  List cubectl commands and abreviations
Includes if a resource is specific to a namespace or not.
```
kubectl get-resources | more
```

### Config View

```
kubectl config view
kubectl config set-context --current --namespace={your default namespace}
kubectl config view
```

### How to get all resoures in all namespaces
```
kubectl get all -A
```


## Kubernetes Deployments and ReplicaSets 
- The relationship between Deployments and ReplicaSets
- Default Deployment strategies
- RollingUpdates and parameters
- How to monitor the progress of a deployment rollout
