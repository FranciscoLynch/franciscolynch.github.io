---
title: "Systems Administrator"
date: 2026-08-09
draft: false
tags: ["sysadmin", "devops", "sre", "linux"]
summary: "An introduction to systems administration as I wish someone had explained it to me."
---

##### *My idea is to present an introduction so that anyone —including my mother (no offense, mom!)— can understand what a **SysAdmin** essentially does.*

--- 

## Part 1 - What is a systems administrator?

That's the usual question when people ask what I do for a living.

I usually get by answering that I manage computer systems, which involves configuring various tools to make sure a service or program works correctly.

It's pretty vague and general. What does that mean for someone outside this world?

To explain it better, I usually say it's like managing a home computer shared by several people with different goals:
- One person wants to open the browser to check emails and everything gets slow and annoying.
- At another point, the screen freezes in the middle of a game and nobody knows why, forcing a restart.
- Or they run out of space to save photos and don't know how to expand storage.

Put simply, a systems administrator is in charge of solving those kinds of problems.

From a more formal definition, a person in this role is responsible for **ensuring that an organization's software generates business value continuously, securely, predictably, and efficiently**.

Let's break down these key words:

### Software

Software is the **logical** part of a device — what allows us to interact with the **physical** part (hardware).

The physical device is a tool for storing, transforming, and exchanging information. To achieve this, we need a component that controls said hardware: that's where software comes in. It's a set of instructions that dictates system behavior (physically represented by electrical charges, transistor states, and memory signals; it's not magic, though it sometimes seems like it).

An operating system like **Windows** or **Linux** is software. In turn, it includes applications that are also software: from a calculator or a web browser, to a game like Pac-Man.

Everything around you today uses software.

**In summary:** it's what allows us to leverage the physical resources of a device (like your phone or computer) to manage information.

### Generating business value

A company doesn't create software solely for the love of art — it does so to solve a problem or make people's lives easier.

**Business value** is the tangible benefit that software generates. For example:
- **In a bank:** allowing you to transfer money from your phone in 10 seconds.
- **In an e-commerce site:** making it possible for you to buy sneakers without the site crashing from too many users.
- **In a hospital:** letting the doctor check your medical history on screen without waiting 20 minutes for it to load.

If the software doesn't work, the company can't operate, loses money, and disappoints its users. Generating value means the program actually fulfills its function with real utility.

### What does it mean to generate value continuously, securely, predictably, and efficiently?
    
- **Continuously:** Working to ensure the service never crashes or, if it fails, recovers so quickly that nobody notices. If you try to use your banking app daily and read "An error occurred, please try again later," you'll end up switching banks.
- **Securely:** Protecting data so that only authorized people access their information and no third party can steal it. It's the equivalent of putting up bars, locks, and alarms on your house.
- **Predictably:** Maintaining stable and consistent behavior. If the system responds in 1 second with 10 users but takes 10 seconds with 10,000, the user experience degrades drastically.
- **Efficiently:** Making everything work fast and secure **without wasting resources**. If to fix a failure you constantly need to add computing power (more CPU or RAM), it means the architecture isn't efficient and you're covering up a design problem with hardware.

### In short

The systems administrator is the person behind the scenes who ensures that the technological infrastructure on which a company's services operate works correctly and allows the organization to keep operating.

--- 

## Part 2 - Behind the scenes: How does one become a systems administrator?

With the role clarified, I'd like to dive deeper into what's most interesting, at least for me: **how do you manage software so that it generates value?**

First, it's necessary to understand **what software needs to "live"** and be available. After all, it's what we're going to maintain in our infrastructure and must take care of.

A program is a sequence of digital instructions that requires a physical environment to run. Just as a fish needs water, software requires four **basic conditions**:

1. **Solid ground (The Operating System):** The base layer (usually Linux or Windows) that organizes and manages everything.
2. **Communication pathways (Networks):** Cables, ports, and virtual routes that allow information to travel between the user and the server.
3. **Storage space (Disks):** The digital shelf where information is stored long-term (databases, files, images).
4. **Computing power (CPU and RAM):** They process the program's orders instant by instant (the analytical "brain" and short-term memory).

If any of these four elements fails or is misconfigured, the software stops.

### The two fundamental pillars of learning

Although storage and computing are vital, in practice they're managed through two major disciplines that every SysAdmin should try to master from day one: **the computer from the inside (the Operating System)** and **connections to the outside (Networks).**

Why should a SysAdmin's fundamental base aim at this? Because it's normally the first thing you face when starting out: **managing software directly installed on the operating system**.

###### *There are more abstraction layers that allow managing software in a better way depending on the case (Proxmox, Docker, Kubernetes, etc.), rather than installing it directly on an OS, but that's a topic for another day.*

#### 1. Operating Systems
Regardless of whether we use Linux or Windows, every operating system fulfills the same function: managing hardware and providing a framework for programs to run correctly. This involves understanding six aspects:

**1.** Measuring and allocating the resources needed for the system to function correctly. We don't want to over-provision extremely because we'll overspend, but we need to ensure nothing is lacking because otherwise the system will saturate, and that's where it "freezes" and software stops working as we want (**Resource Management**).

**2.** Managing programs that run in the background all the time (like the clock or antivirus), understanding what a process is (*daemon/service*), how to start it, how to configure its automatic restart, or how to stop it if it consumes excessive resources **(Process and Service Lifecycle)**.

**3.** Defining which people have "the key" to a certain drawer to protect important information, which means determining who can execute what (*authentication*), what resources they access (*authorization*), and how to isolate processes and users **(Security and Permissions)**.

**4.** Structuring disk space *(partitions/volumes)* so that information is stored in an orderly manner and persists even if the power goes out **(Storage and File Systems)**.

**5.** Controlling which programs have permission to send data externally and which must be isolated, exposing ports, routing tables, and filtering rules or *firewalls* to manage traffic **(Local Connectivity, Ports, and Interfaces)**.

**6.** Reading the "diary" where the computer writes everything that happens (*logs*) to discover the root cause of something failing and inspecting system state **(State Records and Logging)**.

*(At this point, my mom has probably stopped reading from how dizzy she got — I hope I'm underestimating you!)*

#### 2. Networks
There's no point having a perfectly configured server if nobody can communicate with it. To master the networking area, you need to understand:

**1.** Uniquely identifying each device on a network and organizing them to avoid traffic chaos **(Addressing and Identity, IPs and Subnets)**.

**2.** Translating human-readable addresses (like `google.com`) into numbers that computers understand (IP addresses). If DNS fails, for the user "the internet went down" **(Name Resolution, DNS)**.

**3.** Understanding the path that data travels from the user's device to our server, passing through routers and switches **(Routing)**.

**4.** Defining traffic rules to allow only legitimate traffic and isolate sensitive networks from potential attacks **(Security and Filtering, Firewalls and Segmentation)**.

**5.** Understanding the "virtual doors" of entry to each service (like port 80/443 for websites) and the communication rules between applications **(Ports and Protocols)**.

**6.** Knowing how to trace at what exact point communication was interrupted when a service doesn't respond **(Connectivity Diagnostics, Troubleshooting)**.

### Architecture complexities

To further dimension the daily challenge of a SysAdmin, you also need to understand that not all software is hosted or managed the same way. The strategy varies depending on:

- **The application's architecture:** Is it a classic all-in-one monolith or independent microservices communicating via API?
- **Demand and scaling tolerance:** Will it handle constant traffic or massive spikes that require multiplying instances in seconds?
- **Isolation level and regulation:** Does it require dedicated physical hardware (*Bare Metal*) or can it be deployed on virtualized cloud infrastructure?
- **Operational complexity and costs:** Do we use our own servers (IaaS), package applications in containers with Kubernetes (CaaS), or delegate the complete infrastructure (PaaS / Serverless)?

All these variables require designing different strategies to respond to demand and guarantee that software works continuously, securely, predictably, and efficiently. This deserves its own post, where I'll dive deeper into these concepts.

---

## Part 3 - What does it take to do it well?

At this point, the complexity can seem overwhelming: different operating systems, network configurations, and changing architectures just to begin...

So how do you guarantee that software works correctly?

Well, you don't achieve it by working 24 hours straight or putting out fires in desperation. You achieve it by applying four practical operational pillars:

1. **Know what's happening before it fails:**
   You can't protect or fix what you can't see. To achieve predictable behavior, a systems administrator installs **monitoring tools** that alert if a disk is filling up or the network is saturating before the end user perceives a failure. It's the equivalent of an airplane's instrument panel.

2. **Automation:**
   Configuring a server by hand once is fine; doing it fifty times generates inevitable errors. That's why it becomes essential to learn to write programs or instructions (*scripts*) so that repetitive tasks (deployments, updates, backups) execute identically, guaranteeing consistency and time savings.

3. **Design assuming everything will fail:**
   In infrastructure there's a maxim: if something can fail, it will fail. To operate continuously, architecture is designed without "single points of failure" (if one server shuts down, another takes its place automatically). And to guarantee security, it's mandatory to apply *Redundancy and Backup*, meaning: having tested backups ready to restore in any eventuality.

4. **Operational efficiency:**
   Applying the principle of *"least privilege"* (giving each user or process only the strictly necessary permissions) and keeping infrastructure documented. Efficiency isn't just about using less RAM — it's also about *standardizing and organizing* to avoid wasting days trying to guess how something was configured in the past.

---

## Conclusion: it's not magic

Systems administration isn't a discipline of wizards typing weird commands on a black screen, nor of blindly putting out fires at 3 AM. It's a discipline of preventive engineering, order, and strategy.

True success lies in **being invisible**: when a systems administrator does impeccable work, nobody notices they're there. The banking app opens in a second, online purchases complete without errors, and data is safe.

I hope this walkthrough helped you understand a bit better what's behind every click you make daily on your devices. And if I managed to explain it to you... then to my mother too!
