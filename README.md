# Meeting Manager

## Project Description

The Meeting Manager is a comprehensive web-based application that revolutionizes meeting management for organizations, especially client service departments. It replaces inefficient spreadsheet-based systems with a centralized platform for scheduling, tracking, and analyzing meetings. Developed using Angular (with NG-ZORRO) for the front end, ASP.NET Core (C#) for the back end, and SQL Server for data storage, it integrates Quartz Scheduler for automated real-time status updates.

## Tech Stack

- **Frontend**: Angular 19 + NG-ZORRO Ant Design  
- **Backend**: ASP.NET Core (C#), Dapper ORM  
- **Database**: Microsoft SQL Server  
- **Scheduler**: Quartz.NET for automated job execution  
- **Security**: Multi-Factor Authentication (MFA), Role-Based Access Control (RBAC), AES-256 File Encryption  

## Key Features

- Create and edit meetings (with recurrence, agenda, type, and location)  
- Participant management with conflict detection  
- Visual calendar view (daily, weekly, monthly)  
- Automated meeting status updates via Quartz Scheduler  
- File upload (up to 5 files per meeting, 10MB each - configurable)  
- Real-time in-app notifications via WebSocket  
- Reports and analytics (by date, type, user, frequency)  
- Advanced search and filtering (by date range, participants, title, and status)  

## Unique Implementations

- Quartz Scheduler automatically updates statuses such as Scheduled, In Progress, Completed, and Cancelled  
- AES-256 encryption ensures secure file storage and transmission  
- Analytics dashboard displays meeting trends by type, topic, and user activity  
- Conflict detection prevents overlapping meetings for users  
- Role-based access ensures only authorized users can create or edit meetings  

## Role-Based Access Control

- **Admin/Organizer**:
  - Can create, edit, and cancel meetings
- **Participant**:
  - Can only view meeting details (read-only access)

All actions are secured by Role-Based Access Control (RBAC) and Multi-Factor Authentication (MFA).

## Sample Use Cases

- **Create Meeting** – Organizer sets topic, recurrence, participants, uploads files  
- **Edit Meeting** – Allowed only for Admin/Organizer before meeting starts  
- **Cancel Meeting** – Only Admin/Organizer can cancel meetings  
- **View Meeting** – Participants have read-only access  
- **Calendar View** – Everyone sees the calendar; only authorized users can manage events  

## Visual Calendar Color Codes

The calendar uses color indicators to show the current status of each meeting:

- **Green**: In Progress  
- **Blue**: Scheduled  
- **Yellow**: Completed  
- **Red**: Cancelled  

This helps users quickly identify the state of each meeting at a glance.

## System Design Overview

- **Architecture**: Multi-tiered (Frontend → API → Database)  
- **Scheduling**: Background status automation using Quartz.NET  
- **Frontend**: Angular 19 with NG-ZORRO components  
- **Backend**: ASP.NET Core REST API
- **Data**: Meetings, recurrence rules, files, notifications, and participants stored in SQL Server  

## Future Enhancements

- Email notifications for invitations and updates  
- AI-based smart meeting scheduling recommendations  
- Acceptance and rescheduling workflows for participants  
- Integration with external calendars like Outlook and Google  
- Editable calendar view with daily meeting list  

## Deployment and Usage

- **Frontend** served at: `http://localhost:4200`  
- **Backend** hosted at: `https://localhost:5001`  
- **Database**: SQL Server configured locally or on cloud  
- **Authentication**: Handled via session storage and MFA  

## Project Outcome

- Enhanced collaboration and scheduling transparency  
- Secure file handling and controlled access  
- Real-time tracking of meeting statuses  
- Exportable reports for performance and decision-making  

## Visual Demo

To see a walkthrough of the Meeting Manager interface and features:  
👉 [Click here to view the Demo](./demo)

