+++
title = 'Containerization'
date = 2024-05-20T00:31:46+01:00
draft = false
+++

# Introduction 📢

* In this blog, we will explore why you should care about containerization and how it has become a crucial aspect of the tech industry today.

# Containerization : The best and simple definition 😍

Containerization, widely adopted in the Tech Industry as a development and deployment method, involves bundling an application’s source code along with its dependencies into a single, self-contained package that can be executed seamlessly across various computing environments.

Now, you might ask me : “ Bro, what do you mean by “Self-contained package 📦 that can be executed seamlessly across various computing environments”? “

Let me explain it.

1. Compatibility problems and Portability 💼

One of the major challenges faced by developers is “Environment Compatibility.” Imagine you’re working on a project with a classmate on your personal computer, and on the day of the presentation, you have to showcase the project on your friend’s machine. However, when you try to run a simple test of your application, errors start to appear, and you can’t find a solution in that situation. So you tell your professor, “Sir, I swear it worked on my machine 🥺”.

What’s happening here is that your project relies on specific libraries and files that exist on your personal machine. For example, you might be using Windows, while your friend’s machine has Linux as the operating system or you both have different python version. This is a common problem that containerization solves.

Containerization addresses this issue by bundling your project’s source code and all its dependencies into a single file. Regardless of your operating system version or distribution, you can run this single file containing all your project’s components without any compatibility problems.

> That `single file` we were talking about is called an image. An image can be defined as executable software package that contains everything needed to run a piece of software, including the code, runtime environment, system tools, libraries, and dependencies. 🤝 

> Running an `image` take us to what we called a container. In simple words, a `container` is like a running instance of image.Think of it as a classes and objects where an image is the class and containers are the objects created from that class.


2. Resource-efficient 👌

Before diving deeply into how containers are friendly to computing resources, let’s see how containerization is different than virtualization:

Containers share the host operating system’s kernel, utilize the host’s hardware resources and are managed by a container engine, such as Docker Engine or Containerd. Container images contain the necessary dependencies and runtime environment for the application.

Virtualization involves creating VMs that mimic the behavior of physical computers. A hypervisor abstracts the underlying hardware and allows multiple VMs to run on a single physical machine. Each VM has its own virtualized hardware resources, including CPU, memory, storage, and network interfaces.

Now the question you should ask yourself is: “Do I really need to set-up a whole VM to just deploy a simple web application with few MB of size and doesn’t consume more than 100MB of RAM? Do I need all these virtual network interfaces? 😵”. The answer is clearly NAAAAAAAAAAAH😐.

Containers are just like that : you don’t need to set up a bunch of things to just run one simple thing, instead you just need to get the container engine which is a lightweight software compared to OS size, then pack your source code with its dependencies using terminal commands and BOOM!!!! You can run multiple versions of your application without stressing 😫 about defining each container resources because it’s all managed by the docker engine, also those multiple apps are isolated from each other and you can use the same ìmage to run hundreds of applications.containers share the host operating system’s kernel, utilize the host’s hardware resources and are managed by a container engine, such as Docker Engine or Containerd. Container images contain the necessary dependencies and runtime environment for the application.

Virtualization involves creating VMs that mimic the behavior of physical computers. A hypervisor abstracts the underlying hardware and allows multiple VMs to run on a single physical machine. Each VM has its own virtualized hardware resources, including CPU, memory, storage, and network interfaces.

Now the question you should ask yourself is: “Do I really need to set-up a whole VM to just deploy a simple web application with few MB of size and doesn’t consume more than 100MB of RAM? Do I need all these virtual network interfaces? 😵”. The answer is clearly **NAAAAAAAAAAAH**😐.

Containers are just like that : you don’t need to set up a bunch of things to just run one simple thing, instead you just need to get the container engine which is a lightweight software compared to OS size, then pack your source code with its dependencies using terminal commands and BOOM!!!! You can run multiple versions of your application without stressing 😫 about defining each container resources because it’s all managed by the docker engine, also those multiple apps are isolated from each other and you can use the same ìmage to run hundreds of applications.

> **``Containers`` are lightweight and efficient, utilizing the host’s CPU, memory, disk space, and network resources.**`

> **They offer efficient ``resource management``, including `allocation` and ``scheduling``, allowing multiple applications to run on a single host while ``ensuring optimal utilization of resources``.**


3. Scalability ⏫

Now, let’s have another example.

You have a running application on your machine, and as it gains popularity, it requires more computing resources to handle all user requests simultaneously. If your application is hosted on a ``VM``, you would need to provision new VMs to accommodate the increased demand. This process of setting up new VMs can be time-consuming ⏳ and costly 💵, requiring hours of work and significant financial investment. You may ask “ 🤔 Why not scale on the same VM without creating new ones? 🤔 “ It’s generally considered a bad practice to host multiple apps on the same VM due to issues with isolation and dependency management.

On the other hand, containerization offers a different approach. Applications, along with their dependencies, are already packaged within containers. When your app needs to scale to handle increased user traffic, you can simply spin up (create) new containers within minutes. This allows you to dynamically scale the application to any desired number of instances, efficiently meeting the demand.

> ``Containerization`` enables quick and ``cost-effective scalability`` by spinning up new containers to handle increased user traffic

4. Isolation for Security 🚪 🔐

After successfully scaling up, one of your containers gets some security problems because one of those bad guys 👨‍💻 just gets unauthorized access to your app. Because of the way how containers are built and constructed, they are isolated from each other so each one has its own view of computing resources and none of them can access the others, and to make it simple you can say that each one of them has its own preocesses running independently. So you don’t need to worry about other running containers because they are isolated and far from any security problem because of the affected one. (Remember that there is no fully secured system on the planet)

For VMs, since running apps share the same computing resources and they are not fully isolated, once an unauthorized access happens to one of the app instance the others will be affected, even the whole system can be damaged.

> Containers are isolated from each other, with separate resources and independent processes. Unauthorized access to one container does not affect others.


**Summary** 🔚

In summary, ``containerization`` provides a solution to compatibility problems, ensures efficient utilization of computing resources, enables easy scalability, and offers isolation for enhanced security. Containers are lightweight, portable, and enable running multiple applications without conflicts. While ``virtualization`` remains a pillar of the internet, containers and VMs can work together to create an ideal environment for development and deployment, combining the benefits of both technologies 🤝🤝🤝.