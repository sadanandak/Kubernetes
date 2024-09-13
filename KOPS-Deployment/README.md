![image](https://github.com/user-attachments/assets/9e7db6e9-9d88-4316-8c2a-0a6806514220)


Generate SSH Keys: These keys will be used by KOPS and applied to all servers.

ssh-keygen 


Smoke Testing:

Get Nodes:

kubectl get nodes

Get Nodes (No Headers):

kubectl get nodes --no-headers

Cluster Info:

kubectl cluster-info

Get Namespaces:

kubectl get ns

Example namespaces: Alpha, Bravo, Charlie.

Note: If three teams are working on three different projects but using the same cluster, we can isolate with Namespaces. To allow communication between them, use Network Policies.


Pods Information:

Get Pods (Default Namespace):

kubectl get pods

Output: "Nothing is there" (if no pods are running)

Get Pods (Kube-System Namespace):

kubectl get pods -n kube-system

Get Pods (Kube-System Namespace, Detailed):

kubectl get pods -n kube-system -o wide | grep -i <component-name>

Replace <component-name> with the specific component you're looking for.


Deploy Resources in Kubernetes:

Imperative Approach:

kubectl run testpod1 --image=nginx:latest --dry-run=client -o yaml

Note: This generates the YAML manifest without creating the pod.

Declarative Approach (Using YAML or JSON): Create a file pod.yaml with the following content:

apiVersion: v1

kind: Pod

metadata:

  name: testpod1
  
spec:

  containers:
  
  - name: nginx
    
    image: nginx:latest
    
Apply the manifest:

kubectl apply -f pod.yaml

Run Pod Directly:

kubectl run testpod1 --image=nginx:latest

Get Pods:

kubectl get pods
