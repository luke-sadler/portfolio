---
layout: project
title: "MOT Checker"
appstore: "https://apps.apple.com/gb/app/mot-checker/id1478314114"
icon: mot.png
images: 
  - /mot/image1.png
  - /mot/image2.png
  - /mot/image3.png
  - /mot/image4.png
  - /mot/image5.png
tag: "A free UK MOT history checker with custom ML plate detection, DVSA data integration, and smart reminders."
stack:
  - Swift
  - UIKit
  - CoreML
  - Typescript
  - Firebase Functions
  - Google Vision
---

The MOT Checker app was designed to give drivers and car buyers quick, reliable access to MOT history and vehicle data in a clean, user-friendly interface. At its core, the app integrates directly with the **DVSA API**, enabling users to fetch accurate, up-to-date historical records for any UK-registered vehicle.  

In addition to vehicle lookups, the app also helps drivers stay on top of their MOT schedule. Users can set custom reminders on their phone, with the option to be notified two or four weeks before their MOT is due. This ensures they have plenty of time to book an appointment and avoid the risk of their certificate expiring.  

To make this data more meaningful, I developed a custom scoring algorithm that evaluates cars based on their MOT history and presents results in an easy-to-understand breakdown. This allows users not just to see raw MOT entries, but also to quickly assess the overall condition and reliability of a vehicle.  

A key feature of the project was the ability to identify vehicle registration plates directly from images. To achieve this, I built a bespoke machine learning model using **TensorFlow**, trained on **more than 2,500 manually annotated images**. These included UK number plates in a variety of conditions — front, rear, and square formats, captured from different angles. After three days of training, the resulting model could accurately detect and localise plates in real-world scenarios.  

Once a plate is detected, the app automatically crops the relevant portion of the image and sends it to the backend, built with **Firebase Functions (TypeScript)**. There, **Google Vision OCR** extracts the registration number, which is then sanitised before being passed to the DVSA API. The result is a seamless, end-to-end workflow: point the device at a car, capture the plate, and instantly retrieve its MOT history.  

This combination of computer vision, cloud functions, and government data integration not only showcases the technical depth of the project but also highlights how advanced technologies can be used to solve a very practical, everyday problem for drivers.  

This project was very much a passion endeavour, requiring me to step outside of my existing skill set and learn entirely new technologies. I taught myself key machine learning concepts, worked extensively with **TensorFlow**, and TypeScript to build the backend. Every one of the 2,500+ training images was captured and annotated manually, a time-intensive but crucial step to ensure accuracy. From initial research to deployment, the project spanned well over a year of dedicated effort, reflecting both my technical growth and commitment to delivering a high-quality product.