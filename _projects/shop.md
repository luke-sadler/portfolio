---
layout: project
title: "Shop Clients"
icon: sun.png
# images: 
#   - /library/image1.png
#   - /library/image2.png
#   - /library/image3.png
tag: "A lightweight credit-tracking system with secure backups, built to modernise a family member's shop workflow."
stack:
  - Swift
  - Vapor
  - HTMLKit
  - Docker
  - Postgres
  - PGBackWeb
  - Backblaze
  - GitHub Actions
---

This project is a **modern replacement** for a legacy .NET application I originally built over 10 years ago for a local sunbed and tanning shop run by my mother-in-law. The old system, which ran on a single Dell desktop PC, tracked customer accounts and managed credits for sunbed minutes. While it served its purpose for many years, the combination of aging hardware and limited reliability introduced serious risks of **data loss** — an outcome that would have been catastrophic for the business.  

The new solution is built using the same lightweight approach as my [School Library Application](/portfolio/projects/library.html), with a Swift + Vapor web front end and a PostgreSQL backend. Data is backed up securely and automatically via **pgBackWeb and Backblaze B2**, ensuring peace of mind and long-term reliability. By moving to a web-based, containerised deployment, the business is no longer tied to a single aging PC. Instead, the system can now be run on a simple laptop with vastly improved speed, reliability, and security.  

In addition to simplifying the customer check-in process, the new system also introduces better safeguards for sensitive data. **Authentication is token-based**, meaning if the shop’s machine is ever lost or stolen, access can be immediately revoked to keep client data safe.
This upgrade not only modernises their day-to-day workflow but also ensures critical business continuity through **secure backups**, reliable infrastructure, and a lightweight, easy-to-use front end.