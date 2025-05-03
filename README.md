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
## Final Outcomes
- Empty State UI when no events are found in events.json from S3:
<img width="1464" alt="Screenshot 2025-04-30 at 6 43 38 PM" src="https://github.com/user-attachments/assets/e787a583-1e27-4af3-aa93-ba5ea1d437fa" />

- Create Event form UI to submit new event details to AWS Lambda via API Gateway:
<img width="1463" alt="Screenshot 2025-04-30 at 6 44 03 PM" src="https://github.com/user-attachments/assets/cb3b6dde-3a13-4333-a8fa-dcfe83920a83" />

- Subscribe form interface to capture user emails and forward them to AWS SNS via Lambda:
<img width="1464" alt="Screenshot 2025-04-30 at 6 44 24 PM" src="https://github.com/user-attachments/assets/dd4585d1-736c-4a64-8ce1-8c4ed334d887" />

- Form filled with sample event data:
<img width="1468" alt="Screenshot 2025-05-01 at 12 05 39 AM" src="https://github.com/user-attachments/assets/e05a7caf-c4ed-4251-9fb5-5b0372295e20" />

- Confirmation message after successfully creating an event:
<img width="1469" alt="Screenshot 2025-05-01 at 12 31 55 AM" src="https://github.com/user-attachments/assets/7f37b740-9382-4f6b-95fd-5e9486c934c6" />




















