# 📢 Event Announcement – AWS Serverless Event Web App

A modern web application that allows users to create events, subscribe to notifications, and view upcoming events – all hosted and integrated using Amazon Web Services (AWS). This project combines serverless technologies, real-time interaction, and cloud-based scalability.

---

## 🔍 Project Overview

This is a **cloud-native serverless application** built with:
- A frontend hosted on **Amazon S3**
- A backend powered by **AWS API Gateway**, **Lambda**, and **SNS**
- Data persistence via **events.json** stored in S3

This app allows users to achieve the following functionality:

- Users can browse upcoming events  
- Organizers can publish new events  
- Attendees can subscribe for real-time email notifications

It’s a lightweight, fully serverless alternative to event platforms — no backend servers needed.

---

## Project Impact

In real-world community or campus settings, event management is often fragmented. This project solves that by enabling:

- Centralized event publishing and visibility
- Instant email notifications to interested users
- A lightweight, scalable alternative to complex CMS systems
- Fully serverless infrastructure that incurs **zero cost at low usage**

It’s perfect for:
- University clubs and hackathons
- Local meetups
- Volunteer groups
- Small-scale organizations needing real-time updates

---

## ⚙️ Tools & Technologies Used

| Tool/Service       | Purpose                                       |
|--------------------|-----------------------------------------------|
| **HTML/CSS/JS**    | Frontend interface (modern, responsive UI)    |
| **AWS S3**          | Static website hosting + JSON file storage   |
| **AWS Lambda**      | Serverless logic for POST operations         |
| **AWS API Gateway** | HTTP API layer to trigger Lambda functions   |
| **AWS SNS**         | Email-based notifications                    |
| **CORS Configuration** | Allow cross-origin requests                |

---

## 🚀 Project Functionality

### 1. View Events
- Loads `events.json` from S3
- Displays event name, date, and location in cards
- If no events, shows a helpful message

### 2. Create Event
- User submits a form with event details
- Data is sent to API Gateway → triggers Lambda
- Lambda appends event to `events.json` in S3

### 3. Subscribe for Notifications
- User enters an email
- API Gateway → Lambda → AWS SNS
- Email is added as a subscriber to the topic

---

## 🌟 Unique Advantages

Unlike many AWS projects focused purely on backend automation, this one:

- **Combines a visually appealing frontend with full backend logic**
- Uses a **flat-file (JSON)** data model to stay lightweight (no DB needed)
- Allows real-time event creation and subscription via **public-facing S3 frontend**
- Emphasizes **educational clarity** — great for learning or teaching AWS serverless
- Easy to deploy and extend with minimal AWS cost

---



