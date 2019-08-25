# Kubernetes in windows home

## Set up environment

To work on local environment we need to following software :

* minikube - it install virtual machine in Linux and provide kubernetes cluster with one node 
* virtual box - for installing OS.
* docker tool box - it is package of many software like docker and virutal box, it need to install for supporting virtualization, because hyper-v is missing in windows home. 

Start kubernetes cluster 

```shell
minikube start 
```

Create pod using yaml file

Next, we’re specifying that we want to create a Pod; we might specify instead a Deployment, Job, Service, and so on, depending on what we’re trying to achieve.

Next we specify the metadata. Here we’re specifying the name of the Pod, as well as the label we’ll use to identify the pod to Kubernetes.

Finally, we’ll specify the actual objects that make up the pod. The specproperty includes any containers, storage volumes, or other pieces that Kubernetes needs to know about, as well as properties such as whether to restart the container if it fails. You can find a [complete list of Kubernetes Pod properties](http://kubernetes.io/docs/api-reference/v1/definitions/#_v1_podspec) in the [Kubernetes API specification](http://kubernetes.io/docs/api/), but let’s take a closer look at a typical container definition:

https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.10/#_v1_podspec

https://kubernetes.io/docs/concepts/overview/kubernetes-api/

```yaml
apiVersion: v1  #api version is different based on resource
kind: Pod
metadata: 
 name: rss-site #name of pod
 labels:
   app: web #kubernates use is to identify the pod by label property
spec: #specify the actual object that make up the object, like container, storage valuce etc.
 containers:
   – name: store-pod
     image: dhananjay011/store:latest
     ports:
       – containerPort: 8080
   – name: rss-reader
     image: nickchase/rss-php-nginx:v1
     ports:
       – containerPort: 88
```







