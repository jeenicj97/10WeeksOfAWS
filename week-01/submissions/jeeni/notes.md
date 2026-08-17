# Day 1 — Cloud Foundations

**Goal:** Understand how AWS is organized and what AWS manages vs. what you manage.

---

## Before You Start — Quick Recall Questions

1. **What is a Region?** → Region is a geographical area where AWS has multiple Datacentre
2. **What is an Availability Zone?** → Each region has multiple AZ
3. **What is one thing AWS secures?** → Security of the cloud
4. **What is one thing you must secure?** → Security in the cloud

---

## 1. AWS Global Infrastructure

AWS infrastructure is built using three core building blocks:

| Term | Definition |
|---|---|
| **Region** | A geographic area where AWS has multiple data centers (e.g., `us-east-1`, `ap-south-1`). |
| **Availability Zone (AZ)** | An isolated data center location *inside* a Region. Each Region has multiple AZs. |
| **Edge Location** | A location used by services like CloudFront to serve users faster (closer to end users). |

### Exam Pointers
- Use **multiple Availability Zones** → for **high availability**.
- Use **CloudFront + Edge Locations** → for **low-latency content delivery**.

---

## 2. Shared Responsibility Model

AWS security is **shared** between AWS and the customer.

- **AWS is responsible for:** security **of** the cloud.
- **You are responsible for:** security **in** the cloud.

### What AWS Manages
- Data centers
- Hardware
- Networking infrastructure
- Managed service infrastructure

### What You Manage
- IAM & permissions
- Your data
- Applications
- Network rules (e.g., security groups, NACLs)
- EC2 guest OS patching

### Simple Line to Remember
> **AWS secures the cloud. You secure what you build in the cloud.**

---

## 3. Root User

The **root user** owns the AWS account and has **full access to everything**.

### Best Practices
- ✅ Enable **MFA** on the root user.
- ❌ Do **not** use the root user for daily work.
- ✅ Create **IAM users or roles** for regular tasks.
- ✅ Monitor **billing** from the beginning.

### Rule of Thumb
> Use the root user **only** for account-level setup (MFA, billing). After that, avoid using it for daily practice.

---

## Quick Revision Summary

- **Region** = geographic area with multiple data centers
- **AZ** = isolated data center inside a Region → use multiple for HA
- **Edge Location** = CloudFront caching point → for low latency
- **Shared Responsibility** = AWS secures *of* the cloud, you secure *in* the cloud
- **Root user** = full access, MFA it, don't use daily, create IAM users instead
