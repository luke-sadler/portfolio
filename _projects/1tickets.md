---
layout: project
title: "TicketMeister"
icon: tickets.png
github: "https://github.com/luke-sadler/TicketMeisterVapor"
tag: "A Swift Vapor application for booking event tickets"
stack:
  - Swift
  - Vapor
  - FluentSQL
  - SPM
---

I created this Vapor application (with accompanying [client app](https://github.com/luke-sadler/TicketMeisterClient)) for the purpose of learning about server side events. 

This application, essentially, is a 'toy' ticket booking API. With events, venues, and seating plans injected into a db, it will handle seat booking. Seats can be reserved during a checkout phases, purchased, and released. The client can register for updates to seating status changes so they can see seats becoming available/ unavailable in real time.  