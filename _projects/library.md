---
layout: project
title: "Library"
icon: book.png
images: 
  - /library/image1.png
  - /library/image2.png
  - /library/image3.png
tag: "A Swift + Vapor web app that helps a primary school track its library with barcodes, fast and lightweight."
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

This project was developed to solve a practical challenge faced by a local primary school my wife works for: books being borrowed without any system of tracking, leading to frequent losses and significant costs. The school lacked the budget for expensive commercial solutions, so I designed and built a lightweight, self-hosted library management system tailored to their needs.  

The system is built with **Swift and Vapor**, running as a web-based application to ensure compatibility with the school’s fleet of low-cost Chromebooks. The application is containerized with Docker and deployed off-site, backed by a **PostgreSQL** database. To ensure reliability, backups are taken hourly throughout working hours and stored securely in **Backblaze B2**.  

Every physical book in the library is given a unique 6-digit barcode, printed and affixed to the book. Each barcode is paired with the book’s metadata (fetched automatically from sources such as **Open Library and Google Books**) and stored in the database. Students are also managed within the system, with an annual script that automatically “ages up” their records and eventually removes them once they leave the school.  

The application uses server-side rendering with PicoCSS, making it extremely fast and lightweight, even on older hardware or low-bandwidth connections. Beyond performance, I placed a strong emphasis on security:
- Access is limited to authorised origin IPs (the school’s static IP), preventing off-site access to student data.
- The system is protected behind Cloudflare, adding further safeguards against malicious traffic.
- Repeated failed login attempts automatically lock staff accounts, helping defend against brute-force attacks.
- Authentication is token-based, ensuring access can be quickly revoked if a device is lost or stolen.  

By helping prevent book losses and eliminating the need for expensive licensing fees, the system is expected to save the school hundreds of pounds annually, while also streamlining the work of staff and student librarians.  

Introduced during the summer of 2025, the application will be rolled out in the 2025/26 academic year. Looking forward, the long-term plan is to open source the project, enabling other schools to adopt and self-host the system. The project is currently hosted in a private GitHub repository, with automated Docker image builds managed via **GitHub Actions**.