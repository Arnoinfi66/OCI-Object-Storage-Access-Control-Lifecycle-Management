# Product Usage Summary

## Product Used

Oracle Cloud Infrastructure Object Storage

---

## Purpose

This repository documents my product usage and understanding of OCI Object Storage access control and lifecycle management.
The focus is to explain how buckets, objects, IAM access, pre-authenticated requests, lifecycle rules, versioning, retention, and replication work together.

---

## What I Created

I created a structured documentation repository covering:

- Bucket and object overview
- Object Storage access flow
- IAM access control
- Pre-authenticated requests
- Lifecycle management
- Versioning
- Retention rules
- Replication policy
- Product usage summary

---

## What I Reviewed

I reviewed the following OCI Object Storage areas:

- Bucket creation or bucket details screen
- Object upload and object naming
- Object prefixes
- IAM policy requirement for bucket and object access
- Pre-authenticated request options
- Lifecycle rule options
- Versioning, retention, and replication options

---

## What I Understood

My main understanding is that Object Storage needs both storage design and access control.
A bucket stores objects, but IAM policies decide who can access or manage those objects. Pre-authenticated requests can provide temporary URL-based access, but the URL must be handled carefully. Lifecycle rules help manage objects after they are uploaded by moving or deleting them based on defined conditions.
Versioning, retention, and replication provide additional controls, but they should be enabled based on requirement and reviewed carefully.
