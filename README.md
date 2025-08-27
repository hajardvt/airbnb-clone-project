# 🏡 StayEase – Airbnb Clone Project  

## 📌 Project Overview  
StayEase is a **full-stack Airbnb clone** that allows users to:  
- Browse and filter property listings  
- View detailed property information  
- Make secure bookings and payments  
- Manage bookings, reviews, and favorites  
- Admins can manage users, properties, and transactions  

### Project Goals  
- Build real-world experience in frontend & backend development  
- Learn collaborative workflows using Git & GitHub  
- Apply best practices in API security and DevOps  
- Deliver a scalable and responsive application  

---

## 🛠 Technology Stack  

### Frontend  
- **HTML, CSS, JavaScript** – Base structure, styling, and interactivity  
- **React** – Component-based architecture, responsive UI/UX  
- **Figma** – Wireframes and UI design  

### Backend  
- **Django (Python)** – Business logic and API development  
- **PostgreSQL / MySQL** – Relational database to store users, properties, and bookings  
- **RESTful API / GraphQL** – Communication between frontend and backend  
- **JWT Authentication** – Secure login and role-based access  

### DevOps  
- **Git + GitHub** – Version control and collaboration  
- **Docker** – Containerization  
- **GitHub Actions** – CI/CD automation  
- **NGINX + Gunicorn** – Deployment on cloud platforms (AWS/GCP/DigitalOcean)  

---

## 🎨 UI/UX Design Planning  

### Design Goals  
- Create an intuitive booking flow with minimal steps  
- Maintain visual consistency across all pages  
- Ensure fast loading times with optimized assets  
- Prioritize mobile-first responsiveness  

### Key Features  
- Property search and filtering  
- Detailed property viewing (photos, description, pricing, reviews)  
- Secure checkout process  
- User authentication and account management  

### Primary Pages  

| Page                  | Description                                                   |  
|-----------------------|---------------------------------------------------------------|  
| **Property Listing**  | Grid display of available properties with filtering options   |  
| **Listing Detail**    | Full property details with photo gallery and booking form     |  
| **Checkout**          | Streamlined payment and booking confirmation flow             |  

### Importance of User-Friendly Design  
A user-friendly design improves the booking experience, reduces friction, increases conversions, and ensures customer satisfaction.  

### Figma Design Specifications  

**Color Styles:**  
- Primary: `#FF5A5F`  
- Secondary: `#008489`  
- Background: `#FFFFFF`  
- Text: `#222222`  
- Secondary Text: `#717171`  

**Typography:**  
- Primary Font: Circular  
- Body: Medium (500), 16px  
- Headings: Bold (700), 24–32px  
- Secondary Text: Book (400), 14px  

**Why important?**  
Defining colors and typography ensures UI consistency, makes collaboration easier, and improves developer handoff.  

---

## 👥 Project Roles and Responsibilities / Team Roles  

| Role                 | Responsibilities |  
|----------------------|------------------|  
| **Project Manager**  | Oversees planning, deliverables, and deadlines |  
| **Frontend Developers** | Build reusable React components, implement responsive UI |  
| **Backend Developers** | Build APIs, manage business logic, and connect database |  
| **Designers**        | Create Figma mockups, maintain design system |  
| **QA/Testers**       | Write and run test cases, report issues |  
| **DevOps Engineers** | Manage CI/CD pipeline, containerization, and deployment |  
| **Database Administrator** | Ensure schema design, optimization, and data integrity |  
| **Product Owner**    | Defines requirements, prioritizes backlog |  
| **Scrum Master**     | Facilitates Agile process, resolves blockers |  

---

## 🧩 UI Component Patterns  

### Planned Components  

**Navbar**  
- Logo  
- Search bar  
- User navigation  
- Responsive menu  

**Property Card**  
- Property image  
- Price, location, and rating  
- Favorite button  
- Responsive layout  

**Footer**  
- Site links  
- Company information  
- Social media links  
- Copyright  

Each component is designed for **reusability and consistency** across the application.  

---

## 🗄 Database Design  

### Entities & Fields  

**User**  
- user_id  
- name  
- email  
- password_hash  
- role  

**Property**  
- property_id  
- title  
- description  
- location  
- price_per_night  
- owner_id (FK)  

**Booking**  
- booking_id  
- user_id (FK)  
- property_id (FK)  
- start_date  
- end_date  
- total_price  

**Review**  
- review_id  
- user_id (FK)  
- property_id (FK)  
- rating  
- comment  

**Payment**  
- payment_id  
- booking_id (FK)  
- amount  
- status  
- method  

### Relationships  
- A **User** can own multiple **Properties**  
- A **Property** can have multiple **Bookings**  
- A **Booking** links one **User** and one **Property**  
- A **Review** links a **User** to a **Property**  
- A **Payment** is tied to one **Booking**  

---

## 🔒 API Security  
- **Authentication:** JWT tokens for user sessions  
- **Authorization:** Role-based (guest, host, admin)  
- **Input Validation:** Protect against SQL injection & XSS  
- **Rate Limiting:** Prevent abuse of API endpoints  
- **Encryption:** Secure storage of passwords & payment details  

---

## ⚙️ CI/CD Pipeline  

### What is CI/CD?  
Continuous Integration (CI) and Continuous Deployment (CD) automate testing, building, and deployment, ensuring faster and more reliable releases.  

### Benefits  
- Faster deployment cycles  
- Automated testing reduces human error  
- Consistent and reliable releases  
- Improved collaboration across teams  

### Tools Used  
- **GitHub Actions:** Automates build and testing pipelines  
- **Docker:** Containerizes app for consistency  
- **AWS/DigitalOcean/GCP:** Deployment environments  

### Pipeline Flow  
1. Developer pushes code to GitHub  
2. GitHub Actions triggers automated tests  
3. Docker builds container images  
4. Staging deployment for QA  
5. Production deployment with NGINX + Gunicorn  

---
