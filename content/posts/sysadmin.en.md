---
title: "Systems Administrator"
date: 2026-08-09
draft: false
tags: ["sysadmin", "devops", "sre", "linux"]
summary: "An introduction to systems administration, explained simply."
---

<u>My idea:</u> present an introduction so that someone like my mom (no offense, mom) can understand what a SysAdmin (systems administrator) essentially does.

--- 
## Part 1 - What is a systems administrator?

This is the question I get when people ask what I do for a living: "**So what is a systems administrator, what do you do?**"

At 23 years old (of age, not experience) I barely navigate the moment by saying I manage computer systems — that involves configuring various things to make sure a service or program works correctly.

Pretty vague and generic.

To help people understand a bit better, I sometimes explain that it's like managing a home computer (which is used by maybe 4 or 5 people) and that, for example:
- At certain times you want to use the browser to check emails and everything gets really slow, which is super annoying.
- Or maybe at some point it freezes and you don't know why, having to restart it every few hours.
- Or maybe there comes a time when you run out of space to save photos and don't know how to add more.

Well, that's what a systems administrator handles at a very basic level — fixing those kinds of problems.

Getting to a more specific definition, a person in this role is responsible for **ensuring that the organization's software generates business value continuously, securely, predictably, and efficiently**.

- Software.
- Generating business value.
- Continuously, securely, predictably, and efficiently.

Let's pause on each of these words for a moment so I can clarify them and make things easier to understand.

### Software

What is it? Well, software is the "**logical**" part of a device — it's what allows us to use the **physical** part of the device.

The physical device itself is **a tool** in which we can store, transform, and exchange information of all kinds. Software is an operating system like **Windows**, which has tools that are also software, like a calculator, text files, or web browsers.

In short, software is what allows us to use physical resources (memory, chips, cables, etc.) to create, store, modify, transform, delete, and exchange information.

### Generating business value

It's as simple as: **a company doesn't create software for the love of art (or maybe it does), but rather to solve a problem or make life easier for its users** (and obviously benefit in the process — it's a win on both sides).

"Business value" is the benefit that software generates. For example:

- For a bank, the value is that you can transfer money from your phone in 10 seconds.
- For an e-commerce site, it's that you can buy sneakers without the page crashing.
- For a hospital, it's that the doctor can see the medical history on screen without waiting 20 minutes for it to load.

If the software doesn't work, the company can't operate, loses money, and/or disappoints people. Generating value means **the program actually fulfills its function and is useful.**

### What does it mean to generate value **continuously, securely, predictably, and efficiently**?

- **Continuously:** means working to ensure the service never goes down, or that if something fails, it recovers so quickly that nobody notices. Imagine trying to make a bank transfer and not being able to because it says: "Closed for maintenance, come back later."
- **Securely:** means protecting data so that only those with permission can access their information and no external party can steal it. It would be the equivalent of putting up fences, locks, and alarms.
- **Predictably:** means the system behaves in a stable and expected manner as consistently as possible, because if it takes 1 second with 10 users but takes 10 seconds or more with 10,000, it hurts the user experience and therefore the service and the company.
- **Efficiently:** means making everything work fast and secure **without wasting extra resources**. If you need more computing power (more CPUs and/or RAM) to make it work better, it means the system isn't as efficient as it could be, and you're throwing hardware at the problem to compensate.

### In conclusion

Basically, the systems administrator is the person behind the scenes making sure the infrastructure that supports the company's services works correctly.

--- 

## Part 2 - Behind the scenes — How is it done and what's the real complexity?

Having explained what a SysAdmin is, I'd now like to dive into the interesting part: **how do they do it?, what do they need to ensure software generates value?, what's the complexity behind this role?**

First and foremost, I think you need to understand something fundamental: **what does software need to "live"?** After all, that's what someone in this role must host and care for, right?

Well, a program or application is a sequence of digital instructions that needs a physical place to exist and run. Just as a fish needs water, or a car needs a road, fuel, and an engine to move, software needs **basic conditions to function**:

1. **Computing power:** The CPU and RAM, which process the program's orders instant by instant (think of it as the brain that processes and temporarily stores tasks).
2. **Space to store things:** we're talking about storage space on disks. It's the digital shelf where the program keeps its information (databases, files, images).
3. **Paths to communicate:** These are computer networks that enable connectivity (cables, ports, and virtual routes), which allow information to travel from the user's phone to the company's server and back.
4. **A solid floor:** The operating system. This is the base layer (usually Linux, though Windows exists too) that organizes and manages everything above.

If any of these four elements is missing, or if just one is misconfigured, the software freezes or simply ceases to exist for users.

With that in mind, I'd like to go deeper into **Operating Systems** since they're the fundamental foundation for a systems administrator and generally where you start.

Regardless of whether it's Linux, Windows, or another, I wonder **what do you need to know to properly manage a system?**

At an abstract level, every operating system fulfills the same role (managing hardware and providing an environment for programs). Therefore, on any OS you need to master **six pillars**:

1. **Resource Management:** How CPU (Central Processing Unit), RAM, disk I/O, and network I/O are measured, allocated, and limited, and what the system does when they run out.
2. **Process and Service Lifecycle:** What a process is, how it starts, how it runs in the background (_daemon/service_), how its automatic restart is configured, and how it's stopped.
3. **Security and Permissions:** Who can execute what (_authentication_), what files or resources they can access (_authorization_), and how users/processes are isolated.
4. **Storage and Files:** How information persists on disk, how partitions/volumes are structured, and how reads/writes are managed.
5. **Networking and Interfaces:** How the system exposes ports, manages the routing table, and applies filtering/firewall rules to receive or send traffic.
6. **Logs and State (Logging):** Where the system writes when something fails and how to check internal health through logs and state inspection.

After this, my mom has probably stopped reading from how dizzy she got — I hope I'm underestimating you, mom :)

To wrap up, those are the pillars you need to understand and master if you want to manage operating systems the best way possible.

Now, to further understand the complexity a SysAdmin faces in general, you need to understand that not all software is hosted the same way. How you manage it varies depending on:

- **The application's architecture:** Is it a classic all-in-one monolith, or independent microservices communicating via API?
- **Demand and scaling tolerance:** Does it handle constant, predictable traffic, or does it suffer massive spikes where it needs to multiply its instances in seconds?
- **Isolation level and regulations:** Does it need to run on dedicated physical hardware due to security requirements (_Bare Metal_), or can it share virtualized infrastructure in the cloud?
- **Operational complexity and costs:** Do you have the capacity to maintain your own servers (IaaS), do you prefer to package everything in containers using modern tools like Kubernetes (CaaS), or do you simply delegate all infrastructure to not worry about servers (PaaS / Serverless)? (Fancy English names we'll leave for another post).

### In develop...