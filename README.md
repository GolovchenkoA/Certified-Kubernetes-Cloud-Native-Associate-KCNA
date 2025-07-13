# Certified Kubernetes Cloud Native Associate (KCNA)

[Kubernetes Cloud Native Associate KCNA Certification Course](https://www.udemy.com/course/dive-into-cloud-native-containers-kubernetes-and-the-kcna/)
[Course GitHub link](https://github.com/spurin/diveintokcna)
👉 All additional files are stored on Google Disc in the folder `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)`


### Links
- [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/)

- [CNCF Landscape](https://landscape.cncf.io/) - list of CNCF applications.

- [Kubectl quick reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)

- [Kubectl All Commands](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands)

- !!!!!!!Kubernetes Playgrounds ([source](https://kubernetes.io/docs/tasks/administer-cluster/change-default-storage-class/)) : [Play with K8s](https://labs.play-with-k8s.com/), [CodeCloud](https://kodekloud.com/public-playgrounds),[Killercoda](https://killercoda.com/playgrounds/scenario/kubernetes)

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


### Deployment
Deployment (with dry-run)
```
$ sudo kubectl create deployment nginx --image=nginx --dry-run=client -o yaml
[sudo] password for defaultuser:
apiVersion: apps/v1
kind: Deployment
metadata:
  creationTimestamp: null
  labels:
    app: nginx
  name: nginx
spec:
  replicas: 1
  selector:
    matchLabels:
      app: nginx
  strategy: {}
  template:
    metadata:
      creationTimestamp: null
      labels:
        app: nginx
    spec:
      containers:
      - image: nginx
        name: nginx
        resources: {}
status: {}
```

It  can be applied by
```
$ sudo kubectl create deployment nginx --image=nginx --dry-run=client -o yaml | tee nginx-deployment.yaml | kubectl apply -f -

$ kubectl get deployment
$ kubectl get replicaset
```

### Rollout history
This command shows the revision history of a Kubernetes Deployment named nginx.
```
$ kubectl rollout history deployment/nginx

REVISION  CHANGE-CAUSE
1         <none>
2         kubectl apply --record ...
```


🔍 Breakdown:
kubectl: Command-line tool to interact with Kubernetes.

- rollout: Subcommand for managing the rollout of a resource (like a deployment).
- history: Shows past rollout revisions.
- deployment/nginx: Specifies the type (deployment) and name (nginx) of the resource.

🚀 Related Commands
Check current rollout status `kubectl rollout status deployment/nginx`
Undo to a previous revision `kubectl rollout undo deployment/nginx`
Add or update a deployment annotation `kubectl annotate deployment my-deployment description="Production deployment"`
Scale a Deployment to 5 Pods `kubectl scale deployment/nginx-deployment --replicas=5`
Get deployment details in YAML format `kubectl get deployment/nginx -o yaml | more`
Monitor deployment in real-time after applying changes `kubectl apply -f deployment-nginx.yaml && kubectl rollout status deployment/nginx`
Replace image in deployment and monitor rollout `kubectl set image deployment/nginx nginx=nginx:alpine && kubectl rollout status deployment/nginx`
Describe a deployment in detail `kubectl describe deployment/nginxollout undo deployment/nginx `
Expose a resource as a new Kubernetes service. see [cubectl expose](https://kubernetes.io/docs/reference/kubectl/generated/kubectl_expose/)

🚀 For additional information see: [Kubectl quick reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/) and [Kubectl All Commands](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands)


### [Services](https://kubernetes.io/docs/concepts/services-networking/service/#publishing-services-service-types)
As Kubernetes (K8s), I define five types of Services (⚠️ 4 main and 1 as an extention), each designed to expose your applications in different ways:

1.[ClusterIP](https://kubernetes.io/docs/concepts/services-networking/service/#type-clusterip) (default)
Exposes the Service internally within the cluster.
🔹 Use case: Internal microservice communication.
spec.type: ClusterIP

2. NodePort
Exposes the Service on a static port (30000–32767) on each node’s IP.
🔹 Use case: Basic external access for development or testing.
spec.type: NodePort

3. [LoadBalancer](https://kubernetes.io/docs/concepts/services-networking/service/#loadbalancer)
Provisions an external load balancer (cloud provider specific) to expose the Service.
🔹 Use case: Public-facing services in cloud environments.
spec.type: LoadBalancer

4. ExternalName
Maps the Service to an external DNS name without proxying traffic.
🔹 Use case: Integrating with external services via DNS.
spec.type: ExternalName

5. Headless Service (ClusterIP: None)
⚠️ It's a special type of ClusterIP
Creates a Service without a stable cluster IP, allowing direct access to individual Pods.
🔹 Use case: Stateful apps needing DNS-based Pod discovery.
spec.clusterIP: None


### DNS in Kubernetes
Kubernetes clusters run a built-in DNS service (usually CoreDNS) that provides automatic DNS resolution for Services and Pods.

📘 Why `ping xxx.default.svc.cluster.local` works.
So this fully qualified domain name (FQDN) maps to the ClusterIP of the Kubernetes Service named xxx in the default namespace.
Also `/etc/resolv.conf` should contain `search default.svc.cluster.local`  suffix.

Let’s break down xxx.default.svc.cluster.local:
| Part            | Meaning                                             |
| --------------- | --------------------------------------------------- |
| `xxx`           | Name of the **Service**                             |
| `default`       | Kubernetes **Namespace** (default if not specified) |
| `svc`           | Indicates it's a **Service**, not a Pod             |
| `cluster.local` | The cluster’s **DNS domain**                        |



### Kubernetes Jobs
For the KCNA examination it is important to have an understanding of both Jobs and CronJobs, please pay particular attention to the following in the next video -

- A [Job](https://kubernetes.io/docs/concepts/workloads/controllers/job/) vs a CronJob
- Completions and Parallelism

  ` kubectl explain job.spec` - Provides detailed information of the structure and fields of this resource

### Kubernetes ConfigMaps
[ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)

[Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)


### Kubernetes Secrets
For the KCNA examination it is important to understand that ⚠️ **secrets are not encrypted*!!!!*, they are encoded with base64.
Also please pay attention to the type of secret, for example, Opaque (the default type used if a type is not specified).


### Lables
[Lables](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/)


## Kubernetes Deep Dive

### Kubernetes API - Study Tips

The KCNA Examination focusses on the theory of the API and particular attention should be made for the following areas -
- How CRD's ([Custom Resource Definition](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/)) can be used to extend the Kubernetes API
- How to list resource types in a cluster
- The use of --authorization-mode
- The main three stages a request will pass through on its journey via the API server

[Kubernetes Authorization](https://kubernetes.io/docs/reference/access-authn-authz/authorization/) . See --authorization-mode

Command line authorization mode configuration 
You can use the following modes:
- --authorization-mode=ABAC (Attribute-based access control mode)
- --authorization-mode=RBAC (Role-based access control mode)
- --authorization-mode=Node (Node authorizer)
- --authorization-mode=Webhook (Webhook authorization mode)
- --authorization-mode=AlwaysAllow (always allows requests; carries security risks)
- --authorization-mode=AlwaysDeny (always denies requests)

List API resources 
```
kubectl api-resources | more
```

### Kubernetes API

[Kubernetes API](https://kubernetes.io/docs/concepts/overview/kubernetes-api/), also has links to its OpenAPI specs


We can get additional information how the API is called by providing verbosity levels `-v=XXX`, where XXX is a number
```
kubectl run ngingx --image=nginx -v=9
```

So we are allowed to use, for example CURL, to call the API directly. The API requires authentication. See `/root/.kube/config` config file in Linux.

### Admission Control
[A Guide to Kubernetes Admission Controllers](https://kubernetes.io/blog/2019/03/21/a-guide-to-kubernetes-admission-controllers/) . Also shows how API call workflow.
[Admission Control in Kubernetes](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/)

⚠️In the video we touched on this briefly but given, that this is an area that typically arises in the KCNA exam, please pay particular attention to the following resource and how long a feature or behaviour functions for after deprecation is announced. https://kubernetes.io/docs/reference/using-api/deprecation-policy/#deprecating-a-feature-or-behavior
”Rule #7: Deprecated behaviors must function for no less than 1 year after their announced deprecation.”


### Kubernetes RBAC
From a KCNA examination viewpoint, only a high level knowledge of RBAC is required, for example what is the role and purpose of RBAC and how would you implement granular control. You should also be aware of Service Accounts which are covered in the Further Study section.

RBAC is typically deemed as one of the most challenging topics to learn in Kubernetes and it is a favourite with interviewees in most Kubernetes job interviews.

A lot of content on RBAC is fragmented and doesn't cover the specifics or mechanics of how RBAC is actually working on a newly installed Cluster.

This 3 part video series is an extensive look at RBAC from the ground up and by the end of it, you'll be able confidently use and support RBAC. You'll also gain knowledge of advanced usage with Service Accounts in the Further Study section.

If your focus in the KCNA examination then use these videos and further study sections accordingly and where required, treat them as available resources for consumption later.

[RBAC Authorization](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)

```
kubectl config view (--raw optional)
```

⚠️ Kubernetes does not manage user groups and accounts it expect certificates that are created and authorized by cerificate authority !!!!!!!

An issued certificate contains a group (`O=xxxx`) and user (`CN=xxx`) and it`s considered as user name and group.

The output of the command has "USERS", "GROUPS" and "SERVICEACCOUNTS" columns

⚠️In k8s users and groups are managed externaly and within k8s they are represented as strings.
⚠️ServiceAccounts are k8s objects tied to a specific namespace. It's used to give an application that's running on a Pod required permissions to interact with k8s API
```
kubectl get clusterrolebinding --sort-by name -o wide | more

```
```
kubectl create clusterrolebinding ...
```


### [Role and ClusterRole] (https://kubernetes.io/docs/reference/access-authn-authz/rbac/#role-and-clusterrole)
An RBAC Role or ClusterRole contains rules that represent a set of permissions. Permissions are purely additive (⚠️there are no "deny" rules). ⚠️Kubernetes object always has to be either namespaced or not namespaced
- A Role always sets permissions within a particular namespace; when you create a Role, you have to specify the namespace it belongs in.
- ClusterRole, by contrast, ⚠️is a ***non-namespaced*** resource. The resources have different names (Role and ClusterRole) because a Kubernetes object always has to be either namespaced or not namespaced; it can't be both.

+----------------------+

|   ClusterRole        |

|   Name: pod-reader   |

|   Verbs: get, list,  |

|   watch              |

|   Resources: pods    |

+----------+-----------+

           |
           
           | referenced by
           
           v
           
+------------------------------+

|     ClusterRoleBinding       |

|  Name: read-pods-for-dev-team|

|  ClusterRole: pod-reader     |

|  Subject: Group: dev-team    |

+-----------+------------------+

            |
            
            | grants access to
            
            v
            
+--------------------------+

|      Group: dev-team     |

| (from auth provider like |

|   OIDC, LDAP, etc.)      |

+-----------+--------------+

            |
            
            v
            
+---------------------------+

| Access to:                |

| - All Pods                |

| - Across all namespaces   |

| - With: get, list, watch  |

+---------------------------+






describe ClusterRole
  ```
  $ kubectl describe ClusterRole/cluster-admin
  
  Name:         cluster-admin
    Labels:       kubernetes.io/bootstrapping=rbac-defaults
    Annotations:  rbac.authorization.kubernetes.io/autoupdate: true
    PolicyRule:
  Resources  Non-Resource URLs  Resource Names  Verbs
  ---------  -----------------  --------------  -----
  *.*        []                 []              [*]
             [*]                []              [*]
  ```

🔹 1. Create the ClusterRole
```
kubectl create clusterrole pod-reader \
  --verb=get,list,watch \
  --resource=pods
```
📝 This creates a ClusterRole named pod-reader that allows:  get, list, watch on pods Across all namespaces

🔸 2. Bind it to a group using ClusterRoleBinding
```
kubectl create clusterrolebinding read-pods-for-dev-team \
  --clusterrole=pod-reader \
  --group=dev-team
```

How to check your permissions
```
cubectl auth can-i '*' '*'
yes
cubectl auth can-i '*' '*' --as-group="pod-reader" --as="batman"
yes
```


### Certificates and Certificate Signing Requests
[How to create and sign a certificate for a user (CertificateSigningRequest)](https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/)
[Approve\Reject certificate request](https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/#approval-rejection)

list certificate requests and their statuses
```
kubectl get certificatessigningrequest
or
kubectl get csr your_user_name
```

[KUBECONFIG Variable](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/#set-the-kubeconfig-environment-variable)

Use specific config to call kubectl command:
```
KUBECONFG=youruser-configfile.config kubectl ........
```

[Gitlab kubeconfig creator wrapper](https://github.com/spurin/kubeconfig-creator). A handy tool to generate a config file.

```
./kubeconfig_creator.sh -u bob -g cluster-viewonly
⚙️ Stage 1 - User - Configuring user keys and certificate signing requests

✨ Creating key for user bob-clusterviewonly as bob-clusterviewonly.key - openssl genrsa -out bob-clusterviewonly.key 4096
✨ Creating certificate signing request, configuration file for bob-clusterviewonly as bob-clusterviewonly.cnf, embedding CN=bob and O=cluster-viewonly
✨ Creating certificate signing request as bob-clusterviewonly.csr - openssl req -config ./bob-clusterviewonly.cnf -new -key bob-clusterviewonly.key -nodes -out bob-clusterviewonly.csr
✨ Creating certificate signing request, kubernetes yaml declaration as bob-clusterviewonly-csr.yaml

⚙️ Stage 2 - Kubernetes - Applying Certificate Signing Requests

✨ Applying kubernetes yaml declaration - kubectl apply -f bob-clusterviewonly-csr.yaml
✨ Approving kubernetes csr request - kubectl certificate approve mycsr

⚙️ Stage 3 - Information Capture - Capturing information from Kubernetes

✨ Capturing variable CLUSTER_NAME - kubectl config view --minify -o jsonpath={.current-context}
✨ Capturing variable CLIENT_CERTIFICATE_DATA - kubectl get csr mycsr -o jsonpath='{.status.certificate}'
✨ Capturing variable CLIENT_KEY_DATA - cat bob-clusterviewonly.key | base64 | tr -d '\n'
✨ Capturing variable CLUSTER_CA - kubectl config view --raw -o json | jq -r '.clusters[] | select(.name == "'default'") | .cluster."certificate-authority-data"'
✨ Capturing variable CLUSTER_ENDPOINT - kubectl config view --raw -o json | jq -r '.clusters[] | select(.name == "'default'") | .cluster."server"'

⚙️ Stage 4 - Kubeconfig - Creating a Kubeconfig file with captured information

✨ Creating Kubeconfig as bob-clusterviewonly.config - Test with - KUBECONFIG=./bob-clusterviewonly.config kubectl

⚙️ Stage 5 - Cleanup - Moving temporary files from current directory, cleanup Kubernetes CSR

🗑️  Creating temporary files store - mkdir tmp-bob-clusterviewonly-20230613101447
🗑️  Cleanup bob-clusterviewonly.key - mv bob-clusterviewonly.key tmp-bob-clusterviewonly-20230613101447
🗑️  Cleanup bob-clusterviewonly.cnf - mv bob-clusterviewonly.cnf tmp-bob-clusterviewonly-20230613101447
🗑️  Cleanup bob-clusterviewonly.csr - mv bob-clusterviewonly.csr tmp-bob-clusterviewonly-20230613101447
🗑️  Cleanup bob-clusterviewonly-csr.yaml - mv bob-clusterviewonly-csr.yaml tmp-bob-clusterviewonly-20230613101447
🗑️  Cleanup csr/mycsr - kubectl delete csr/mycsr
```

### RoleBinding vs ClusterRoleBinding
⚠️ RoleBinding - namespace specific, ClusterRoleBinding is cluster-wide



## Kubernetes RBAC (Service Accounts)
In our video lesson we covered extensively, role based access control through the use of ClusterRoles, ClusterRoleBindings and the equivalent with Roles and RoleBindings.

It is also worth being aware of ServiceAccounts and their relation to Pods and how these operate behind the scenes.

Each Pod in Kubernetes is automatically associated with a Service Account. This association is key to determining the permissions and resources that the processes inside the Pod will have access to.

⚠️If you don’t specify a Service Account for a Pod, it defaults to using the 'default' Service Account in the same namespace and the Pod will have limited access to the Kubernetes API from within the Pod. This adheres to the Kubernetes best practice principle of least privilege.

From a KCNA examination viewpoint, it is important to be aware that by default, a Pod will be assigned the ‘default’ Service Account in that Namespace.

In everyday operations, you would not need to make use of a custom Service Account unless you wished for the Pod in Kubernetes to be able to perform specific operations against the Kubernetes cluster from within the Pod. For example, a Pod being permitted to create another Pod/Deployment/Secret etc.

To show a simple example of how this may function you can perform the following exercise that will demonstrate the use of Service Accounts.

#### Kubernetes RBAC (Service Accounts) Trainings
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\92. Kubernetes RBAC - Further Study (Service Accounts)`


## Kubernetes Scheduling and NodeName
For the KCNA qualification, a basic knowledge and understanding of the role of the scheduler is required. Particular attention should be applied to the use of nodeName as well as nodeSelector and the mechanism of labels that the nodeSelector makes us of (nodeSelector is an addition covered in the Further Study addendum).

[Kube-Scheduler Docs](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)

There are 3 stages when the scheduler decide on what node a pod should be created:
1. Filtering
2. Scoring
3. Binding

There is a posibility to build your own custom scheduler if it's needed 

⚠️ Full example of creating custom schedulers can be found on Google Disk 


pod.spec has schedulerName option:
```
kubectl explain pod.spec | more
```

### nodeSelector
```
kubectl describe node/worker-1 | more

Name:               worker-1
Roles:              <none>
Labels:             beta.kubernetes.io/arch=arm64
                    beta.kubernetes.io/instance-type=k3s
                    beta.kubernetes.io/os=linux
                    kubernetes.io/arch=arm64
                    kubernetes.io/hostname=worker-1
                    kubernetes.io/os=linux
                    node.kubernetes.io/instance-type=k3s
```
And then, you can use the nodeSelector option to select specific nodes through the use of labels -
```
apiVersion: v1
kind: Pod
metadata:
  creationTimestamp: null
  labels:
    run: nginx
  name: nginx
spec:
  nodeSelector:
    kubernetes.io/hostname: worker-1
  containers:
  - image: nginx
    name: nginx
    resources: {}
  dnsPolicy: ClusterFirst
  restartPolic
```


## Kubernetes Storage
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\99. Kubernetes Storage)`
🔎 [Kubernetes Storage Docs](https://kubernetes.io/docs/concepts/storage/)
[Storag Classes](https://kubernetes.io/docs/concepts/storage/storage-classes/)
⚠️ Storage and Volume are not the same thing!!!!
For the KCNA Examination, as well as having top level knowledge there is a heavy emphasis on the internals and specifics of the Kubernetes Storage subsystem. Please pay attention to the following areas -

- What is Ephemeral Storage
- What is [Persistent Storage](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)
- What is [Dynamic Volume Provisioning](https://kubernetes.io/docs/concepts/storage/dynamic-provisioning/)
- Examples of CNCF Graduated Storage Solution(s)
- Retain Policies

  Special [emptyDir](https://kubernetes.io/docs/concepts/storage/volumes/#emptydir) ephemeral folder. For a Pod that defines an emptyDir volume, the volume is created when the Pod is assigned to a node. As the name says, the emptyDir volume is initially empty. All containers in the Pod can read and write the same files in the emptyDir volume, though that volume can be mounted at the same or different paths in each container

[Pods and persistent volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#using). ⚠️Persistent volume climes is namespace specific
[Climes as Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#claims-as-volumes)
[Reclaim policies](https://kubernetes.io/docs/concepts/storage/storage-classes/#reclaim-policy)

### Ceph Storage
You should also be aware of Ceph, an offering from RedHat that provides object, block and file storage in one solution.

Given the commercial nature of Ceph's relationship with RedHat, it is sometimes used as a storage solution in the OpenShift distribution of Kubernetes. From a KCNA viewpoint you should be aware of the project and it being a unified object/block and file solution.

If this project is of interest, see the following resources -

https://www.redhat.com/en/technologies/storage/ceph

https://docs.openshift.com/container-platform/3.11/install_config/storage_examples/ceph_example.html



### Kubernetes StatefulSets - Study Tips
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\103. Kubernetes StatefulSets)`
For the KCNA examination, please focus on the following areas -

- The purpose of StatefulSets
- The difference/similarities between StatefulSets and Deployments
- The StatefulSet relation/dependency on Services for naming

### StatefulState, Update Strategy and partition
[Update Strategies](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#update-strategies) and [Partitioned Rolling Updates](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/#partitions)

📌 What is partition?
The partition setting delays updates to lower-numbered Pods.

You can think of it like this:

A StatefulSet with replicas: 5 has Pods:
myapp-0, myapp-1, myapp-2, myapp-3, myapp-4

If partition: 3, then:

myapp-4 and myapp-3 get updated

myapp-2, myapp-1, and myapp-0 will NOT be updated

✔️ This gives you fine-grained control over which Pods are updated during a rollout.


## Kubernetes NetworkPolicies
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\105. Kubernetes NetworkPolicies)`
For the KCNA Examination, you need to be aware of the role of Network Policies and that policies are cumulative. If you apply multiple NetworkPolicies to a set of pods, the policies are added together.

The effective policy is the union of all the individual policies. This approach ensures that if any policy allows a particular type of traffic, that traffic is allowed.

[Ingress and Egress Network Policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/#the-two-sorts-of-pod-isolation)

[Network policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/) are implemented by the network plugin. To use network policies, you must be using a networking solution which supports NetworkPolicy. Creating a NetworkPolicy resource without a controller that implements it will have no effect
⚠️ [Container Network Interface (CNI) plugin](https://kubernetes.io/docs/concepts/extend-kubernetes/compute-storage-net/network-plugins/)  is essential for the enforcement of NetworkPolicies in Kubernetes


### Kubernetes Pod Disruption Budgets
For the KCNA examination, a general understanding of Pod Disruption Budgets is required, specific on the implementation and use-cases should be considered as informational only in the following video.
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\Kubernetes Pod Disruption Budgets`


⚠️Familiarise yourself with the kubectl drain command -
```
kubectl drain --help | more
```

Introduce a more disruptive scenario by draining worker-2 using the kubectl drain command. This simulates a scenario like node maintenance, where the node is taken offline, and observe the impact on pod availability -
```
kubectl drain worker-2 --delete-emptydir-data=true --ignore-daemonsets=true
```

Create a Pod Disruption Budget for the nginx deployment, ensuring that a minimum of 2 pods are always available
```
kubectl create pdb nginx --selector=app=nginx --min-available=2
```


### kubectl cordon vs drain
The difference between kubectl drain and kubectl cordon, which are often used together but serve different purposes.

🔹 kubectl cordon  What it does:
- Marks a node as unschedulable.
- Does NOT remove or evict existing Pods.
- New Pods will NOT be scheduled on this node.

```
kubectl cordon <node-name>
```
🧠 Use when:
- You want to prevent new Pods from being scheduled to the node (e.g., before maintenance).
- But you are not yet ready to evict existing Pods.

🔸 kubectl drain What it does:
- Cordon the node (same as above), AND
- Evicts (gracefully deletes) all non-daemonset, non-static Pods.
- Respects PodDisruptionBudgets (PDBs).
- Intended to safely prepare the node for shutdown or maintenance.

```
kubectl drain <node-name> --ignore-daemonsets
```
🧠 Use when:
You want to empty a node in preparation for:

- Node reboot
- OS upgrade
- Hardware maintenance
- Scaling down

You want to migrate workloads off the node

| Feature                  | `kubectl cordon` | `kubectl drain`                           |
| ------------------------ | ---------------- | ----------------------------------------- |
| Makes node unschedulable | ✅ Yes            | ✅ Yes                                     |
| Evicts existing Pods     | ❌ No             | ✅ Yes (except DaemonSets and static Pods) |
| Honors PDBs              | ❌ Not needed     | ✅ Yes — may block if PDB violated         |
| Use case                 | Pause scheduling | Maintenance, reboot, upgrade              |


## Kubernetes Security
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\114. Kubernetes Security)`

For the KCNA exam, the following considerations -

- Awareness of Security Tools and their function including `Falco` and `Open Policy Agent`
- Knowledge that `Kubescape` can be used for hardening to NSA and CISA standards
- OpenID Connect and it's purpose, be aware that the exam may shorten this to OIDC
- Legacy: Although Pod Security Policies are deprecated, this was previously a common question in the exam and you should be aware that Pod Security Policies manage Clusters and Namespaces at runtime
- The 4C's of Cloud Native Security

[Configure a Security Context for a Pod or Container](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)

```
apiVersion: v1
kind: Pod
metadata:
  name: security-context-demo
spec:
  securityContext:        <----------------------
    runAsUser: 1000
    runAsGroup: 3000
    fsGroup: 2000
    supplementalGroups: [4000]
  volumes:
  - name: sec-ctx-vol
    emptyDir: {}
  containers:
  - name: sec-ctx-demo
    image: busybox:1.28
    command: [ "sh", "-c", "sleep 1h" ]
    volumeMounts:
    - name: sec-ctx-vol
      mountPath: /data/demo
    securityContext:
      allowPrivilegeEscalation: false  <----------------------
```

### Pod Security Policies 

[Pod Security Policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/) ⚠️ deprecated from k8s v1.21 and removed from v1.25 and repalced by [Admission Controllers ](https://kubernetes.io/blog/2019/03/21/a-guide-to-kubernetes-admission-controllers/). Now k8s is following the module approach and tools like `Kyverno` and `Open Policy Agent` (see also https://kubescape.io/) can be used.

[Kubernetes Authentication with OIDC (OpenID): Simplifying Identity](https://medium.com/@extio/kubernetes-authentication-with-oidc-simplifying-identity-management-c56ede8f2dec)

#### Kyverno and Open Policy Agent (OPA) Gatekeeper
Pod Admission Controllers is used to enforce policies on incomming pods, by updating and mutating configurations before they are created. Kyverno and Open Policy Agent (OPA) Gatekeeper provides the same 

#### What Kubescape does:
It is designed for vulnerability and misconfiguration scanning in Kubernetes clusters

 #### What Falco Does:
 
Falco monitors the behavior of containers, Pods, and nodes at runtime, and detects:

- Abnormal activity (e.g., shell inside a container, unexpected file access)
- Suspicious system calls
- Policy violations
- Potential attacks like:
- Crypto mining
- Privilege escalation
- Sensitive file reads

📦 How It Works with Kubernetes: Falco:

- Integrates with the Linux kernel using eBPF or a kernel module
- Watches system calls made by containers and processes
- Has built-in Kubernetes-aware rules
- Can send alerts to Slack, webhooks, Prometheus, or even trigger automated responses


### 4C's of Cloud Native Security
⚠️For awareness and also for the purposes of the KCNA exam, you should be aware of the 4C’s of Cloud Native Security, namely Cloud, Cluster, Container, Code.

Each endpoint acts as a layer from the outside-in and is a security best practice in Cloud Native Computing.

Each subsequent layer acts as a reinforcement for the layer within. For example, Code would benefit from the security implementations of Container, Cluster and Cloud respectively.


### Helm and Helm Charts
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\117. Helm and Helm Charts)`

[Helm quick start](https://helm.sh/docs/intro/quickstart/)


### Service Meshes 
- The purpose of Service Meshes
- The main components, Proxy and Data Plane
- Common open source offerings for Service Meshes
- The role of the [SMI (Service Mesh Interface)](https://smi-spec.io/)

[SMI (Service Mesh Interface)](https://smi-spec.io/) is a specification that covers the most common service mesh capabilities:

- Traffic policy – apply policies like identity and transport encryption across services
- Traffic telemetry – capture key metrics like error rate and latency between services
- Traffic management – shift traffic between different services

[Service Mesh Architecture](https://www.tigera.io/learn/guides/service-mesh/service-mesh-architecture/). 2 main components:
- Data Plane
- Control Plane


## Telemetry and Observability

🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section5\128. Prometheus and Grafana)`

### Cloud Native Observability 

- The 3 pillars of Cloud Native Observability
- Where and why you would use each Pillar, i.e. `Logs`, `Metrics`, `Traces`
- The different types of Metrics, i.e. Gauges, Counters, Meters, Histograms
- The relation between `Alerting` and the `3 pillars` of Cloud Native Observability
- ```kubectl top```
- understanding of options such as OpenTracing/OpenTelemetry and that these operate at the Application layer

**Cloud native observability** is the ability to understand what’s happening inside a complex, distributed cloud native environment — in real time — using:
- data like logs
- metrics
- traces, and events.


### Logging agents
| Tool           | Primary Focus               | Data Types | Footprint   | Kubernetes Native       | Written In |
| -------------- | --------------------------- | ---------- | ----------- | ----------------------- | ---------- |
| **Fluentd**    | Log collection & processing | Logs       | Heavy       | Yes (via DaemonSet)     | Ruby       |
| **Fluent Bit** | Lightweight log forwarder   | Logs       | Lightweight | Yes (DaemonSet/sidecar) | C          |


#### Metric Types
| Metric Type   | Can Decrease? | Stores Rate?       | Buckets? | Use Case                              |
| ------------- | ------------- | ------------------ | -------- | ------------------------------------- |
| **Counter**   | ❌ No          | ✅ Yes (via rate()) | ❌ No     | Requests, errors, job runs            |
| **Gauge**     | ✅ Yes         | ❌ No               | ❌ No     | Memory, CPU, queue size               |
| **Histogram** | ❌ No (sum)    | ✅ Yes              | ✅ Yes    | Latency, size, duration distributions |
| **Summary**   | ❌ No          | ✅ Yes              | ❌ No     | Percentiles (client-side calc)        |

📦 What Are Buckets and Bins (Histogram)?

In data analysis and monitoring, buckets (or bins) are intervals that group values into ranges for aggregation or visualization.


There is "Meters" metric type (as I uderstand it's the same as Histogram), but ChatGPT says it has different meaning in different systems and usually it's confusing :
| Context               | What "Meter" Means                        | Real Metric Types          |
| --------------------- | ----------------------------------------- | -------------------------- |
| **OpenTelemetry**     | API to create instruments                 | Counter, Histogram, Gauge  |
| **Micrometer (Java)** | Base class for all metric types           | Counter, Gauge, Timer      |
| **Dropwizard**        | A specific metric that tracks event rates | Meter (rate), Timer, Gauge |
| **Prometheus**        | Not used as a type                        | Counter, Gauge, Histogram  |


### OpenTracing/OpenTelemetry
[OpenTracing]( https://opentracing.io/) and [OpenTelemetry](https://opentelemetry.io/docs/migration/opentracing/)
is an open-source project under the Cloud Native Computing Foundation (CNCF) that provides APIs and instrumentation for distributed tracing. It offers a consistent, expressive, vendor-neutral API  (like Jaeger or Zipkin). for distributed tracing, which is critical for understanding and monitoring the performance of microservices-based applications.


### Grafana and metric storages
Grafana supports integration with Prometheus\InfluxDB\Elasticsearch

🔁 Comparing InfluxDB and Prometheus
| Feature                  | **Prometheus**                            | **InfluxDB**                           |
| ------------------------ | ----------------------------------------- | -------------------------------------- |
| Type                     | Pull-based monitoring system              | General-purpose time-series database   |
| Data collection          | Pull (scrapes targets)                    | Push or pull (via Telegraf, API, etc.) |
| Query language           | PromQL                                    | InfluxQL or Flux                       |
| Data retention           | Local retention, no long-term storage     | Configurable, supports long retention  |
| Use case focus           | Monitoring & alerting (Kubernetes, infra) | Metrics, IoT, real-time analytics      |
| Integration with Grafana | ✅ Yes                                     | ✅ Yes                                  |


🎯 When is InfluxDB Used in This Stack?
While Prometheus + Grafana is the standard for Kubernetes monitoring, InfluxDB is often used when:

🔹 1. You need high-frequency or custom time series data
- IoT data (sensors, weather, logs)
- Financial market data
- Industrial systems

🔹 2. You already use Telegraf

Telegraf is an agent from InfluxData that collects, processes, and pushes metrics to InfluxDB. It's super flexible and supports plugins for:

- Docker
- Kubernetes
- System metrics
- Databases (MySQL, Redis, etc.)

🔹 3. You want push-based metric collection
Prometheus is pull-based by design.
InfluxDB supports push-based via API or Telegraf, which is better for edge cases or restricted networks.

🧪 Use Case Example: Side-by-side
| Use Case                               | Use Tool                                  |
| -------------------------------------- | ----------------------------------------- |
| Kubernetes pod metrics                 | Prometheus                                |
| System metrics (host uptime, disk I/O) | Telegraf → InfluxDB                       |
| IoT sensor data from edge devices      | InfluxDB                                  |
| Long-term or hybrid retention          | InfluxDB (or Prometheus + remote storage) |
| Alerting                               | Prometheus + Alertmanager                 |
| Visualization                          | Grafana (for both)                        |


### SLI (Service Level Indicators) vs Fitness Functions

| Aspect      | SLI                                     | Fitness Function                                      |
| ----------- | --------------------------------------- | ----------------------------------------------------- |
| **Purpose** | Measure user-experience quality         | Evaluate overall system or configuration fitness      |
| **Scope**   | Specific metric (latency, errors, etc.) | Composite or custom metric combining multiple factors |
| **Context** | SRE, SLAs, SLOs                         | Optimization, automated decision-making               |
| **Usage**   | Track and alert on service health       | Guide deployment, autoscaling, or experiments         |
| **Nature**  | Direct measurable indicator             | Derived/evaluative score                              |


### SLA
Top 10 SLA metric names:
- Availability / Uptime
- Response Time / Latency
- Error Rate
- Throughput
- Mean Time to Recovery (MTTR)
- Data Durability
- Support Response Time
- Request Success Rate
- Capacity / Scalability
- Security Compliance


### Cost Management 

- Cloud Anomaly Detection
- `KubeCost` as a tool for Cost Observability

✅ Tools like FinOps platforms, cloud-native cost dashboards, or third-party aggregators (e.g., CloudHealth, Spot.io) help track and optimize costs across clouds.

🌐 Why Use Multiple Cloud Providers?
- Avoid Vendor Lock-In
- Reduces dependency on a single provider’s ecosystem or pricing.
- High Availability & Resilience
- Improves fault tolerance by distributing workloads across clouds.
- Best-of-Breed Services
- Different providers offer strengths in AI, storage, networking, etc.
- Regulatory or Geographic Requirements
- Some workloads must run in specific regions or clouds due to compliance.
- Cost Optimization
-  Organizations can shift workloads to the most cost-effective cloud.



### KubeCost

💡 Top Features of Kubecost
1. Real-Time Cost Monitoring Tracks cost of workloads by:

- Namespace

- Deployment

- Pod

- Label

- Service

- Helps teams understand where money is being spent in a cluster.

2. Cost Allocation & Chargeback Enables accurate cost allocation across:

- Teams

- Projects

- Environments (dev/test/prod)

- Supports multi-tenant Kubernetes clusters.

- Helps with internal chargeback/showback models.

3. Savings Recommendations Identifies underused resources (CPU, memory, etc.)

Suggests:

- Rightsizing pods

- Spot instance usage

- Node scaling options

- Helps reduce overprovisioning and lower cloud bills.

4. Budget Alerts
- Allows teams to set cost budgets and thresholds.

- Sends alerts (Slack, email, etc.) when limits are approached or exceeded.

5. Multi-Cluster Support
- Supports aggregation of cost data across multiple clusters.

- Centralized cost monitoring for large environments.

6. Integrates with Cloud Billing APIs
-  Connects to AWS, GCP, Azure billing APIs.

- Provides accurate cloud-native cost data for:

- EBS volumes

- Load balancers

- Network traffic

- Cloud provider discounts (e.g., AWS Savings Plans)

7. Custom Pricing Support
- Supports custom pricing models:

- Internal infrastructure (bare metal, on-prem K8s)

- Enterprise pricing agreements

- Useful for hybrid cloud or private cloud setups.

8. Open Source and Enterprise Editions
- Open Source: Core features for single-cluster cost visibility

- Enterprise: Enhanced UI, governance, multi-cluster views, and integrations (e.g., SSO, cost policies)

9. Integration with Prometheus & Grafana
- Uses Prometheus metrics for resource tracking.

- Easily integrates with Grafana dashboards and other monitoring tools.

10. Network Cost Allocation
- Breaks down egress and ingress traffic costs.

- Helps identify high-cost services and external communication.

  Summary Table
  | Feature                    | Open Source | Enterprise |
| -------------------------- | ----------- | ---------- |
| Real-time cost tracking    | ✅           | ✅          |
| Budget alerts              | ✅           | ✅          |
| Multi-cluster aggregation  | ❌           | ✅          |
| SSO / RBAC                 | ❌           | ✅          |
| Cloud provider billing API | Limited     | ✅          |
| Custom pricing             | ✅           | ✅          |



## Section 7 Cloud Native Application Delivery and GitOps

### Cloud Native Application Delivery and GitOps 
Main points of consideration for the Cloud Native Application Delivery and GitOps section -

- Be aware of Argo and how this software integrates with the GitOps lifecycle
- Knowledge that Argo can be further utilised through the use of Argo Workflows
- Have an understanding and awareness of Flux, an Argo alternative
- Have an understanding of the GitOps toolkit which Flux utilises

Cloud Native Application Delivery: 
- Scalable (microservices)
- Resilient (orchestration)
- Fast Paced (containerization)

**GitOps** - is about using Git to manage your infrastrucutre and application

### ArgoCD
🔍⚠️  Traininsg with all the commands can be found on Google disk in `Certification Courses\Kubernetes\Certified Kubernetes Cloud Native Associate (KCNA)\Section7\ArgoCD`


It is also important from an exam perspective to have an awareness of Flux, an ArgoCD alternative and in particular, be aware that Flux may be a more appropriate solution for synchronised cluster changes. This is explained and detailed below. From an examination viewpoint please pay particular attention to Configuration Sync:

**Argo CD Workflows**

For more information, visit the [Argo Workflows documentation](https://argoproj.github.io/workflows/)

Argo CD workflows are central to managing complex deployment processes. These workflows allow for the orchestration of multi-step deployment processes, integrating with the Argo Workflows project for advanced automation capabilities.

Key aspects include:

- Sequential and Parallel Execution: Workflows can be configured to run tasks either in sequence or parallel, providing control over the deployment process.
- Integration with Argo Workflows: This integration allows for the creation of complex pipelines combining CI (Continuous Integration) and CD (Continuous Deployment) tasks in a unified workflow.
- Customisable Pipelines: Users can create custom pipelines to match their specific deployment requirements, such as incorporating testing stages, approval processes, or integration with external tools.

### Flux
 [Flux](https://fluxcd.io/) is an open-source project maintained by the CNCF

Comparison Between Argo CD and Flux

Both Argo CD and Flux are powerful tools for GitOps, but they have distinct features and architectural approaches.

- Architecture and Operation: Argo CD follows a more centralised approach, with a single point of control for deployment. In contrast, Flux adopts a more decentralised stance, where each Flux instance operates independently, making it potentially more scalable in large systems.

- Configuration Sync: Both Argo CD and Flux can continuously monitor a Git repository and can automatically apply [changes.In](http://changes.in/) the video demonstration for Argo CD you’ll note that we optionally selected the synchronise option when setting up our app. It would have been possible if we wished to toggle this and to then synchronise manually later if we wished.

Flux however has always traditionally used a **pull-based approach** and was one of the first tools in the Kubernetes ecosystem to introduce this capability as one of it’s core features. It will automatically synchronise changes.

Flux’s original design was strongly centered around it’s synchronisation process and this approach has made Flux synonymous with the GitOps approach of continous synchronisation between the repository and cluster. For this reason, many would consider Flux the “textbook” choice for continous synchronisation, **even though both Flux and ArgoCD share this capability**.

- **Customisation and Extensibility**: Flux is built on the GitOps Toolkit, a set of composable APIs and specialised tools, allowing for more customisation and extensibility. This modular approach lets you tailor Flux to fit more complex scenarios.

- **Ecosystem and Community**: Both tools have strong communities and are part of the CNCF landscape. However, their ecosystems differ slightly, with 🚀 **Flux being more aligned with the broader CNCF ecosystem, potentially offering better integration with other CNCF projects**.

### **Flux and the GitOps Toolkit**

Flux's use of the GitOps Toolkit is a significant aspect that sets it apart from other similar tools. The GitOps Toolkit is a collection of APIs and controllers that can be combined to create a complete GitOps workflow. These components include:

- Source Controller: Manages the acquisition of source code from repositories like Git.
- Kustomize Controller: Applies Kubernetes manifests using Kustomize, a tool for customising Kubernetes configurations.
- Helm Controller: Allows for the declarative management of Helm chart releases.
- Notification Controller: Handles alerts and notifications for the GitOps workflow.

These components provide a flexible and powerful way to implement GitOps, allowing for more granular control and customisation of the continuous delivery process.

While Argo CD is an excellent GitOps tool that we've explored in our lesson, 🚀 understanding Flux and its use of the GitOps Toolkit can provide you with a more comprehensive view of the GitOps landscape. Both tools have their strengths, and knowing when to use one over the other can be crucial in certain deployment scenarios. For those interested in delving deeper into Flux, its documentation is a great starting point.
