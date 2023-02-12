# CKAD-training
Helpful tips to get your [CKAD, Certified Kubernetes Application Developer](https://training.linuxfoundation.org/certification/certified-kubernetes-application-developer-ckad/).

## First step, learn Kubernetes
Take a course, or do it on your own. [Kubernetes for Developers (LFD259)](https://training.linuxfoundation.org/training/kubernetes-for-developers/) by the Linux Foundation is great. If your are new to Kubernetes you perhaps want to start with [Introduction to Kubernetes (LFS158x)](https://training.linuxfoundation.org/training/introduction-to-kubernetes/), it's free and a great place to start.

## Continue on you own
After you have done LFD259 its time to dig into the details about K8s. The course works a lot with yaml files when creating pods, deployments and other K8s objects. That works perfectly fine in your everyday work, but if you want to pass the certification you must be fast, and that means to learn the `kubectl` command.

## Learn the docs
During the certification exam you will only have access to K8s and Helm documentation. Be familiar with the documentation and the search functionality. Learn where to find the K8s cheat sheet!

* https://kubernetes.io/docs/home/ 
* https://kubernetes.io/blog/ 
* https://helm.sh/docs 

## Train
Take a look at [CKAD-exercises](https://github.com/dgkanatsios/CKAD-exercises). This is a great place for kubectl training, do the exercises at least once.

## Tools
Learn a text editor, either Vim or Nano. You must know how to copy, cut and paste, indenting large chunks of text is also good to know. You will have access to both Vim and Nano during the certification.

[Nano basics can be found here.](https://medium.com/@pranay.shah/nano-text-editor-tricks-for-ckad-exam-3b07f80dfe77)

But, if you select Nano as your preferred editor as I did, you still need to know the absolute basics of Vim such as deleting and inserting text and exiting with and without save. Why? Because when you edit a Kubernetes object from command line it's Vim time.

Do you really need the aliases so many other CKAD blogs mention? Yes, you will type `--dry-run=client -o yaml` so many times...

```
export do="--dry-run=client -o yaml"
export now="--force --grace-period 0"
export tmp="kubectl run tmp --image=nginx:alpine -it --rm --"
```

You need to know either `wget` or `curl`, but best is to know both. I recommend to learn the timeout flag.

## Containers and Helm
You need to learn the basics of containers and Helm.

* Be confident in creating a container image with other tag than latest. Also you need to know how to run a container from that image.
* Use Helm to install, uninstall and upgrade packages.

## Certification
When you enlist for the certification, you get the possibility to train on a virtual machine that is similar to what you will use during the exam. Be sure to do the test exam. Learn how to navigate the questions, how copy paste works and all other things you may want to know before the real exam starts. 

Read the documents that you say that you have read, when registering for the exam! They contain information about the exam and what you need to do. Important is the part about a clutter free desk.

* When you delete objects, use the "--force" option (see above). You don't need the extra stress a slow deletion process generate.
* Be sure to validate what you do. If you shall create a service to expose a deployment, test that service.
* Be confident working with namespaces. When creating objects, be sure they are added to correct namespace.
* Know your weaknesses, this is not the time to carefully search and read the documentation. Skip to next question!

## Exam tips
* https://dev.to/akdevcraft/certified-kubernetes-application-developer-ckad-exam-tips-4a1b
* https://devopscube.com/ckad-exam-study-guide/