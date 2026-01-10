# 📑 Data Labeling Support System

We'll cover the following
+ [🎯 Project Overview & Goals](#🎯-project-overview-goals)
+ [🧑‍💻 Team Roles & Responsibilities](#🧑‍💻-team-roles-responsibilities)
+ [ 🛠️Technology Stack](#🛠️-technology-stack)
+ [🏗️ System Architecture](#🏗️-system-architecture)
+ [🌊 Warranty Workflow](#🌊-warranty-workflow)
+ [🎨 Database Design](#🎨-database-design)
+ [📚 Document References](#📚-document-references)

## 🎯 Project Overview & Goals
ELV Warranty Management System helps local service staff handle warranty requests efficiently and transparently. It allows them to record customer issues, verify warranty eligibility, and submit claims directly to the manufacturer. The system tracks the status of each request—from submission and inspection to approval and replacement—ensuring quick resolution and accurate documentation. By digitizing the entire process, local staff can reduce paperwork, improve communication with the manufacturer, and deliver faster, more reliable service to customers.

Goal:
+ Digitize the warranty workflow to reduce manual paperwork.
+ Improve response time for warranty approvals.
+ Provide transparency for both service centers and the manufacturer.

<img src="./Resources/logo.png" alt="logo">

## 🧑‍💻 Team Roles & Responsibilities
### Team Structure
| Role              | Name / Placeholder |
| ------------------|:------------------:|
| Front-End Dev     | Quốc Thái          |
| Front-End Dev     | Thế Anh            |
| Back-End Dev      | Huy Vũ             |
| Back-End Dev      | Kim Ngân           |
| Back-End Dev      | Trương Minh Nhật   |

### Github Workflow
<img src="./Resources/Github_Workflow.png" alt="Github workflow">

## 🛠️ Technology Stack
### Front-End
**Technologies**
+ React 19 - UI library
+ Vite - Build tool
+ React Router DOM - URL Mangement
+ Axios - Http Client for API calls
+ Shadcn - Components UI
+ Phosphoricons - Icons library

**Tools**
+ Visual Studio Code

### Back-End
**Technologies**
+ Spring Boot - Main Framework
+ BCrypt.NET - Securely hashing and Verifying passwords
+ JWT Authentication - Security
+ MicrosoftSQL - Database

**Tools**
+ IntelliJ
+ Microsoft SQL Management

### API Testing
**Tools**
+ Postman - API documentation

### DevOps
**Technologies**
+ Docker - Containerization
+ Kubernetes - Container Orchestration
+ Traefik - Reverse proxy
+ NGINX - Load Balancer 
+ SonarQube - Code quality & Security reviews
+ Trivy - Vulnerability scanner for containers
+ Jenkins - Continuous Integration
+ ArgoCD - Continuous Delivery

## 🏗️ System Architecture
```
[ Frontend (React) ]
   ↓ REST API calls
[ Backend (Spring Boot) ]
   ↓
[ Database (MSSQL) ]
   ↓
[ File Storage (Local / S3 / MinIO) ]
```

## 🌊 Warranty Workflow
1. Local Staff logs a new warranty claim → fills in customer, vehicle, and defect details.
2. Backend validates claim, assigns claim ID, stores data, and uploads related files.
3. Manufacturer Reviewer checks eligibility and approves/rejects the request.
4. System updates claim status and notifies the local staff.
Service Center receives replacement parts or reimbursement.

## 🎨 Database Design
Our system will have total 15 Entities:

+ Users: User management and authorization
+ Customer: Customer information
+ CustomerVehicle: Customer vehicle information
+ Campaign: A voluntary, non-safety-related action, often for a technical update or a less serious issue. 
+ CampaignType: Recall/Service
+ ServiceCenter: A service center have many users
+ WarrantyPolicy: Warranty policy for each part
+ WarrantyClaim: Received claim vehicles
+ Report: A Claim/Campaign report
+ ReportType: Type of warranty report
+ WorkOrder: Tasks information for SC Technician
+ VehicleParts: Parts from customer vehicle
+ PartItem: Parts detail information
+ Parts: Parts information
+ Inventory: Parts management

## 📚 Document References
### DevOps & Deployment
+ [🚀 CI/CD Pipeline](CICD.md)
### Project Documentation
+ [⚙️ Project Main Flow](MAIN_FLOW.md)
+ [📰 Features](FEATURE.MD)
+ [🗄️ Database Overview](DATABASE.md)


