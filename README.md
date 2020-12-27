# Stratergies-To-Crack-CKA
## Certified Kubernetes Administrator [Updated in Sept 2020] 
It includes a set of notes and practice test references to prepare for Certified Kubernetes Administrator  exam by Cloud Native Computing Foundation.

I started my preparation in first week of Dec 2020 and cleared the exam in third week of Dec 2020.

**Content is based on new updated CKA Curriculum.** 

## Update of September 2020

Here is the official curriculum of CKA which got updated in last sept [2020].
[Official Curriculum](https://github.com/cncf/curriculum/blob/master/CKA_Curriculum_v1.19.pdf)

**Section Weightage Marks :**

1. Cluster Architecture, Installation & Configuration – 25%
2. Services & Networking – 20%
3. Troubleshooting – 30%
4. Workloads & Scheduling – 15%
5. Storage – 10%


**Details :**
***1. Cluster Architecture, Installation & Configuration – 25%***

-   Manage role based access control (RBAC)
-   Use Kube-adm to install a basic cluster
-   Manage a highly-available Kubernetes cluster
-   Provision underlying infrastructure to deploy a Kubernetes cluster
-   Perform a version upgrade on a Kubernetes cluster using Kubeadm
-   Implement etcd backup and restore

***2. Services & Networking – 20%***

-   Understand host networking configuration on the cluster nodes
-   Understand connectivity between Pods
-   Understand ClusterIP, NodePort, LoadBalancer service types and endpoints
-   Know how to use Ingress controllers and Ingress resources
-   Know how to configure and use CoreDNS
-   Choose an appropriate container network interface plugin


***3. Troubleshooting – 30%***

-   Evaluate cluster and node logging
-   Understand how to monitor applications
-   Manage container stdout & stderr logs
-   Troubleshoot application failure
-   Troubleshoot cluster component failure
-   Troubleshoot networking

***4. Workloads & Scheduling – 15%***

-   Understand deployments and how to perform rolling update and rollbacks
-   Use ConfigMaps and Secrets to configure applications
-   Know how to scale applications
-   Understand the primitives used to create robust, self-healing, application deployments
-   Understand how resource limits can affect Pod scheduling
-   Awareness of manifest management and common templating tools

***5. Storage – 10%***

-   Understand storage classes, persistent volumes
-   Understand volume mode, access modes and reclaim policies for volumes
-   Understand persistent volume claims primitive
-   Know how to configure applications with persistent storage


### **Information About the Test:**

Once you schedule the test, you can’t reschedule or cancel it before 24hr of the scheduled test. You will get 1 free retake incase you didn’t qualify in first attempt.

_Here is the following details about the test._

-   2 hours : 17 questions
-   Remotely proctored in Chrome browser plus an extension
-   Government-issued Non-expired ID Card
-   Webcam and microphone
-   Completely practical, no theory. All on the command line
-   Questions are weighted with a percentage. Harder question, more points

####  **Bookmarks :**  
This file contains all `kubernetes.io/docs` links only.   [CKA bookmarks ](https://github.com/nikhilagrawal577/CKA-Notes/blob/main/cka_bookmarks.html) 
 Just import in your browser and use it.  

Here i have kept the sequence as per my requirement. you can change, add, remove as per your comfort.
    

#### **Use Imperative Commands**

I have noted down few imperative commands. It saves alot of time during the test. Practice these command as many times as you can. :D
```
1.  kubectl create service nodeport <myservicename>
2.  kubectl expose Pod / Deployment — port=123 — name= Service_Name — namespace= Namespace_Name
3.  kubectl label / annotate / set / scale
4.  kubectl run nginx — image=nginx — restart=Never — replicas=3
5.  kubectl create secret generic abcd — from-literal=id=1
6.  kubectl create congimap cm1 — from-literal=id=1
7.  kubectl create role pod-reader --verb=get --verb=list --verb=watch --resource=pods
8.  kubectl create clusterrole pod-reader --verb=get,list,watch --resource=pods
9.  kubectl create rolebinding bob-admin-binding --clusterrole=admin --user=bob --namespace=acme
10. kubectl create clusterrolebinding root-cluster-admin-binding --clusterrole=cluster-admin --user=root
```

#### **Generating Yamls**

_Don’t try to write your own yamls at the exam._  
**_1. Pods , Deployments, Secrets, Configmaps, Jobs, Cron jobs_**  
These yamls can be generated using — dry-run , — export , -o yaml flags

    eg: k create deployment — image=nginx —- dry-run=client -o yaml > dp.yaml

**_2. Persistent Volume, Persistent Volume Claim, Node Affinity, Node Selector, Service Account, Volumes_**  
These yamls can easily fetched from k8s.io documentations.

#### Editor

Be familiar with the editor you want to use. In my case , I have used Vi.  

**Things you should know better and fast in doing**
1.  Find and replace
2.  Going to exact line
3.  Deleting the word and line
4.  Checking the alignment
5.  Save & exit

### **Tips for the Exam**

1.  **Kubectl cheatsheet** : [https://kubernetes.io/docs/reference/kubectl/cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
3.  **Context :** Always pay attention to which context are you working ? It is correct or not. Make sure, you set the context before answering the actual question. Context will be given in the top of each question.
4.  If you are unsure of the spec or parameters of a yaml, always use `**kubectl explain <resource>.<key>**` Eg : `kubectl explain pod.spec`
5.  Time is extremely crucial. Try to read the question carefully and understand in a single go. **Don’t waste time in reading the question multiple times.**
6.  As weightage is already given for each question, if some less weightage question is taking more time to solve , you can skip and come back to that question later part of the test.
7.  Make sure, you are executing the commands in the **provided namespace**.
8.  **Be familiar with mouse or trackpad** as you need them to copy paste few names of the objects from the questions and to copy yaml from Kubernete.io page.
9.  Be an expert in terms of **Imperative commands** . It saves quite a lot of time.
10.  Don’t waste time in typing yaml codes. Generate Yamls

# Articles : 

1.   [https://github.com/kodekloudhub/certified-kubernetes-administrator-course](https://github.com/kodekloudhub/certified-kubernetes-administrator-course)
2.  [https://github.com/walidshaari/Kubernetes-Certified-Administrator](https://github.com/walidshaari/Kubernetes-Certified-Administrator)
	



# Courses :
1. https://training.linuxfoundation.org/training/kubernetes-fundamentals-lfs258-cka-exam-bundle/

2. https://www.katacoda.com/courses/kubernetes 

3. https://www.udemy.com/course/certified-kubernetes-administrator-with-practice-tests/ 
	


# Practice Tests : 
1. https://kubernetes.io/docs/tasks/

2.  https://kodekloud.com/courses/675080/lectures/12038819




## References 
1. How to crack CKAD in 1st attempt

https://medium.com/@nikhilagrawal577/how-to-pass-ckad-exam-in-1st-attempt-tips-tricks-in-k8s-9e14477699ca
