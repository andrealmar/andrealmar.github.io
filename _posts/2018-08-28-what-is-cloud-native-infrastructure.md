---
title: Cloud Native Infrastructure and why You should keep an eye on it
description: What is Cloud Native Infrastructure
header: Cloud Native and why You should keep an eye on it
---

Unless you've been hidden in some cave I'm sure you have heard about Cloud Native Applications or Cloud Native Infrastructure. It has been one of the hottest topics on software nowadays. But what exactly is a Cloud Native Application? It's just a hype? It's something worth it to have a look at? Stay with me, take my hand and I will guide you through this journey.

Let's take a closer look at what CNCF (Cloud Native Computing Foundation) says about the definiton of "Cloud Native":

> Cloud native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

> These techniques enable loosely coupled systems that are resilient, manageable, and observable. Combined with robust automation, they allow engineers to make high-impact changes frequently and predictably with minimal toil. <br />

Font: [https://github.com/cncf/toc/blob/master/DEFINITION.md](https://github.com/cncf/toc/blob/master/DEFINITION.md){:target="_blank"}

Now things are more clear, right? Hmmm...I'm not sure....

If we pick some words out of the definition above we start to have an idea on what Cloud Native means. *Containers, microservices, immutable infrastructure, loosely coupled services, automation, frequently and predictable changes* and *minimal toil.*

### Containers

I'm not going to introducte you to the container world here. I'm going to say that each part of your application, in an ideal Cloud Native world, is packaged in its own container. This will give us some advantages like: resource isolation, reproducibility, portability. No more dependency hell, "works on my machine" and other problems like that. But this doesn't mean that if you package your application in some container(s) you are doing it right. You also need an orchestrator for your containers. Containers are ephemeral by its nature. They born and die frequently. They need to be actively scheduled and managed to optimize resource utilization and free you from managing containers by hand. Believe me, I've saw some companies managing their containers in a "manual way" and its a terrible thing to do.

The orchestrator will take care of tasks like: starting and shutting down of containers, load balancing between application instances, make sure the application is behaving the way you told it to behave (declarative) and so on.

### Microservices

### Immutable Infrastructure

### Loosely Coupled Services

### Automation

### Frequently and Predictable Changes

### Minimal Toil

What is toil? The Google SRE book define toil as:

> blalalblablalbalblalbalblbablalbalbalblablabla

So you goal here is to have a MINIMUM of TOIL blablablablabbal

https://www.redhat.com/en/explore/cloud-native-apps

Infrastructure is now represented by software. Software is opinionated. Cloud Native Infrastructure is an opinionated way to manage virtual hardware. A software is now capable to manage it's own infrastructure. Keep that in mind:

> Infrastructure is now software

Before Infrastructure was separated from the Software layer. Not anymore. Infrastructure and Software are running on the same layer. This is Cloud Native.

Infrastructure can be represented as software, we are watching the pattern of mapping the complex ideas of infrastructure into elegant software pattern. Perhaps the most notable pattern is the reconciliation and control loops found in Kubernetes core components. This pattern has its origin in advanced robotics, and has been battle tested over time to demonstrate stability.

> In applications of robotics and automation, a control loop is a non-terminating loop that regulates the state of the system. In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the API server and makes changes attempting to move the current state towards the desired state. Examples of controllers that ship with Kubernetes today are the replication controller, endpoints controller, namespace controller, and serviceaccounts controller.

https://kubernetes.io/docs/reference/command-line-tools-reference/kube-controller-manager/

To quote Kris Nova: We desperately need to free ourselves mentally from the old paradigms of developing software ON infrastructure. We need to begin developing our software WITH infrastructure.

So what is Cloud Native infrastructure? It's the ability for software to manage it's own infrastructure.

In a Cloud Native environment, traditional infrastructure operators need to be infrastructure software engineers. You ARE NOW a SOFTWARE ENGINEER !!!

Infrastructure as Software - Infrastructure exposes an API for defining desired state.

Cloud Native Patters: Reconcile, BLA BLA BLA
