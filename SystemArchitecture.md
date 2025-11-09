Konnekt App System Architecture

1. Tech Stack Overview
Frontend: React.js 
Backend: Node.js with Express.js (REST API server)  
Database: MongoDB Atlas (cloud-hosted document database)  
Video Conferencing: WebRTC and Socket.io (embedded video call service)  
Calendar Integration: Google Calendar API  
Payment Processing:Paystack API  
Authentication: OAuth 2.0 (Google) + custom email/password

2. Component Breakdown
Frontend
Built with React.js, responsive for web browsers.  
Manages user interactions, dashboard UI, meeting scheduling, and file sharing.  
Communicates with the backend via REST API.
Backend
Node.js + Express.js handles:
User authentication and authorization  
Meeting creation, scheduling, and management  
File upload/download and privacy controls  
Payment verification with Paystack  
Post-meeting analytics computation
Database
MongoDB Atlas stores:
User accounts and profiles  
Meeting metadata (time, host, co-hosts, participants)  
File references and sharing permissions  
Attendance reports and analytics
Video Conferencing Flow
Frontend requests meeting creation from backend.  
Backend generates meeting room details via WebRTC and Socket.io
Users join the meeting using the unique room link.  
WebRTC and Socket.io handles live video/audio streams; backend manages permissions and access.
Calendar & Notifications
Backend syncs scheduled meetings with Google Calendar API.  
Automatic reminders are sent via email or in-app notifications.

Payment & Monetization
Premium features are unlocked after payment verification via Paystack API.  
Backend manages subscription status and feature access.
