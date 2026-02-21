

# Cloud Computing Course — Winter Semester

Notes for My Cloud Computing Course — Winter Semester 

If you find the notes useful, please consider giving it a star! I will try to keep this updated during the semester.

---

## Table of Contents

### Session 1 — Introduction to Cloud Computing
- 1.1 [What is "The Cloud"?](#11-what-is-the-cloud)
- 1.2 [Cloud Storage](#12-cloud-storage)
- 1.3 [Cloud Computing](#13-cloud-computing)
- 1.4 [Cloud Service Models (IaaS, PaaS, SaaS)](#14-cloud-service-models-iaas-paas-saas)
- 1.5 [Pros and Cons of Cloud](#15-pros-and-cons-of-cloud)
- 1.6 [Computing Paradigms Overview: Cloud, Fog, MEC, Edge](#16-computing-paradigms-overview-cloud-fog-mec-edge)

---

## Session 1 — Introduction to Cloud Computing

---

### 1.1 What is "The Cloud"?

At its core, **the cloud** simply means **using someone else's computers/servers over the internet** instead of your own local hardware.

---

### 1.2 Cloud Storage

Storing your data on **remote servers** rather than on your local device.

- **Examples:** iCloud, Google Drive, Dropbox, OneDrive
- You upload files → they live on a data center somewhere → you access them from any device

---

### 1.3 Cloud Computing

Using remote servers not just for storage, but for **processing power and computation**.

- **Examples:**
  - Training an AI/ML model on **AWS, Google Cloud Platform (GCP), or Microsoft Azure**
  - Running a website on a virtual server
  - Netflix streaming (processing and delivery happens in the cloud)
- Instead of buying a $10,000 GPU, you **rent** computing power by the hour

---

### 1.4 Cloud Service Models (IaaS, PaaS, SaaS)

| Model | Meaning | What You Manage | Example |
|-------|---------|-----------------|---------|
| **IaaS** | Infrastructure as a Service — raw computing resources | OS, apps, data | AWS EC2, Google Compute Engine |
| **PaaS** | Platform as a Service — platform to build/deploy apps | Apps and data only | Google App Engine, Heroku |
| **SaaS** | Software as a Service — ready-to-use software | Nothing (just use it) | Gmail, Zoom, Microsoft 365 |

Think of it as a **pizza analogy**:

```
IaaS  → You get an oven and ingredients          → You cook everything yourself
PaaS  → You get dough, sauce, and a kitchen      → You just assemble and bake
SaaS  → You get a fully made pizza delivered      → You just eat
```

---

### 1.5 Pros and Cons of Cloud

#### ✅ Pros

| Advantage | Explanation |
|-----------|-------------|
| **Scalability** | Scale resources up/down based on demand (pay for what you use) |
| **Cost Efficiency** | No need to buy/maintain expensive hardware upfront (CapEx → OpEx) |
| **Accessibility** | Access your data/apps from anywhere with internet |
| **Reliability & Redundancy** | Data is backed up across multiple data centers |
| **Automatic Updates & Maintenance** | The provider handles patches, upgrades, hardware failures |
| **Collaboration** | Multiple users can work on shared resources in real-time |

#### ❌ Cons

| Disadvantage | Explanation |
|-------------|-------------|
| **Latency / Delay / Lag** | Data must travel to a remote server and back; critical for real-time apps like **cloud gaming** (Google Stadia failed partly due to this) |
| **Security & Privacy of Data** | Your data lives on someone else's servers; risk of breaches, unauthorized access, or surveillance |
| **Internet Dependency** | No internet = no access to anything |
| **Downtime** | If the cloud provider goes down, you go down (e.g., AWS outages affect thousands of sites) |
| **Vendor Lock-in** | Migrating between providers can be difficult and costly |
| **Limited Control** | You don't fully control the underlying infrastructure |

---

### 1.6 Computing Paradigms Overview: Cloud, Fog, MEC, Edge

> ⚠️ **Note:** This is a high-level introduction. We will deep dive into each paradigm in later sessions.

#### The Core Problem

Cloud computing is powerful but **centralized and far from the user**. As billions of IoT devices came online, sending all data to the cloud became impractical due to **latency, bandwidth, and privacy** concerns.

**The solution:** Process data **closer to where it's generated**. This gave rise to multiple computing paradigms that sit between the cloud and the user.

#### The Spectrum

```
☁️ CLOUD ──────→ 🌫️ FOG ──────→ 📡 MEC ──────→ 📱 EDGE
  (far)                                           (near user)
```

#### Quick Definitions

| Paradigm | Where It Runs | One-Liner |
|----------|--------------|-----------|
| **Cloud** | Centralized data centers (far away) | Massive power, high latency |
| **Fog** | Local network devices (gateways, routers) | Filters & pre-processes data before sending to cloud |
| **MEC** (Mobile-Edge) | Cell towers / base stations | Cloud-like compute at the telecom network edge, great for 5G |
| **Edge** | On or right next to the device itself | Process data where it's created, minimal latency |

#### Summary Comparison

| Aspect | Cloud | Fog | MEC | Edge |
|--------|-------|-----|-----|------|
| **Distance from user** | Far | Medium | Near | Immediate |
| **Latency** | ~100ms+ | ~20ms | ~5-10ms | ~1ms |
| **Compute Power** | Virtually unlimited | Moderate | Moderate | Very limited |
| **Internet Required** | Yes | Partially | Yes (mobile) | No |
| **Example** | Training an AI model | Smart factory gateway | AR app on 5G | Self-driving car braking |

#### Key Takeaway

> 💡 It's **not** about choosing one over the other. Modern systems use **all layers together**, placing each task at the layer that makes the most sense based on **latency, compute needs, bandwidth, and privacy**.

*More detail on each paradigm in upcoming sessions.*
