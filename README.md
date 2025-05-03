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

- View Events page displaying a successfully created event from S3 data:
<img width="1470" alt="Screenshot 2025-05-01 at 12 50 29 AM" src="https://github.com/user-attachments/assets/14bd3610-add8-42bd-8abf-ab1c07a0f636" />

- events.json updated in S3 with new event after successful Lambda trigger:
<img width="637" alt="Screenshot 2025-05-01 at 12 37 35 AM" src="https://github.com/user-attachments/assets/f98f20a5-091a-43fa-96bd-81e639aad45d" />

- Entering email for event updates via AWS SNS subscription:
<img width="1467" alt="Screenshot 2025-05-01 at 12 51 02 AM" src="https://github.com/user-attachments/assets/db06f73c-4f81-40d8-976a-348d37751549" />

- Successful subscription message:
<img width="1469" alt="Screenshot 2025-05-01 at 12 51 45 AM" src="https://github.com/user-attachments/assets/16a68567-f41a-4e68-b237-0beebc42e815" />

- AWS SNS email received for confirming event notification subscription on my email:
<img width="670" alt="Screenshot 2025-05-01 at 12 52 23 AM" src="https://github.com/user-attachments/assets/dafd75fa-b905-4d2e-81dc-2752f8e8b3ee" />

- AWS SNS subscription successfully confirmed for event notifications via my email:
<img width="589" alt="Screenshot 2025-05-01 at 12 54 21 AM" src="https://github.com/user-attachments/assets/86cf1a59-4406-4ddc-a9aa-907ac1ac96c4" />

- SNS subscription confirmed and visible in AWS console for email-based event notifications:
<img width="1470" alt="Screenshot 2025-05-01 at 12 57 19 AM" src="https://github.com/user-attachments/assets/073e1119-db66-41c5-bb8b-35ff8f92181c" />

- Creating another new event with form inputs named Perplexity Hackathon:
<img width="1466" alt="Screenshot 2025-05-01 at 1 03 19 AM" src="https://github.com/user-attachments/assets/1a1f276a-e810-4fc9-90b9-871db4b41a3f" />

- New event created sucessfully:
<img width="1462" alt="Screenshot 2025-05-01 at 1 03 55 AM" src="https://github.com/user-attachments/assets/ce9347ee-e6bb-4061-9b70-37667e02974f" />

- Email notification received from AWS SNS confirming new event creation and broadcasted to all the subscribers:
<img width="664" alt="Screenshot 2025-05-01 at 1 04 22 AM copy" src="https://github.com/user-attachments/assets/7960bee6-2149-44fe-b96d-09eea649fab5" />

- Updated events.json file in S3 reflecting newly created events via Lambda integration:
<img width="637" alt="Screenshot 2025-05-01 at 1 05 53 AM" src="https://github.com/user-attachments/assets/1c1080bd-252f-4d3a-a823-249df5779039" />

- View of upcoming events dynamically rendered from S3-hosted events.json data.
<img width="1467" alt="Screenshot 2025-05-03 at 12 41 56 AM" src="https://github.com/user-attachments/assets/6571346f-24f1-426e-b686-154563b7961f" />



































