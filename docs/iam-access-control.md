# IAM Access Control

## Overview

IAM policies control access to OCI Object Storage.
Access should be granted based on what the user or application needs to do.
For Object Storage, access can be managed at the bucket level, object level, or through the broader object-family resource type.

---

## Why IAM Matters

Without proper IAM control, users may get more access than required.
A better approach is to define access based on:

- Who needs access
- What action they need to perform
- Which compartment they need access to
- Which bucket or objects are involved

---

## Common Access Areas

Object Storage access can include:

- Listing buckets
- Creating buckets
- Uploading objects
- Reading objects
- Deleting objects
- Creating pre-authenticated requests
- Managing lifecycle policies
- Managing object versions

---

## Basic Policy Example

```text
Allow group DemoObjectAdmins to manage object-family in compartment Sandbox
```

This type of policy allows the group to manage Object Storage resources in the selected compartment.

---

## Read Access Example

```text
Allow group DemoObjectReaders to read buckets in compartment Sandbox
Allow group DemoObjectReaders to read objects in compartment Sandbox
```

This type of access is useful when users need to view buckets and read objects, but should not manage or delete them.

---

## Upload Access Example

```text
Allow group DemoObjectUploaders to read buckets in compartment Sandbox
Allow group DemoObjectUploaders to manage objects in compartment Sandbox
```

This can be used when a group needs to upload or manage objects, but bucket-level access still needs to be reviewed carefully.

---

## Pre-Authenticated Request Permission

To create or manage pre-authenticated requests, the user needs permission to manage pre-authenticated requests for the target bucket.
A user should also have the required object permissions based on the type of access being granted through the pre-authenticated request.

---

## What I Reviewed

I reviewed IAM access from a product usage perspective:

- Bucket access
- Object access
- Read and manage permissions
- Pre-authenticated request permission
- Compartment scope
- Why access should not be broader than required

---

## What I Understood

My main understanding is that Object Storage access should be controlled through IAM first.
A bucket may store the data, but IAM decides who can see it, upload to it, download from it, or manage it.
Pre-authenticated requests should not be used as a replacement for proper IAM design. They should be used only when temporary URL-based access is required.
