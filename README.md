# 🎣 SecureTraining - A Phishing Simulation & Training Platform

[![Project Status: Showcase](https://img.shields.io/badge/status-showcase-blue.svg)](./)

---

> **Please Note:** This repository is a showcase for **SecureTraining**, a project developed by a team of three. The source code is private, but this README provides a comprehensive overview of the application's features, architecture, and the technologies we used to build it.

## 📖 About The Project

**SecureTraining** is a full-featured, web-based phishing simulation tool we developed to help organizations test and improve their employees' security awareness. In a world where human error is the weakest link in cybersecurity, this platform provides a safe and controlled environment to run realistic phishing campaigns and deliver instant, effective training.

Our goal was to build an end-to-end application that is both powerful for administrators and educational for employees, complete with multi-tenancy, campaign management, and a real-time analytics dashboard.

## ✨ Core Features

- **🏢 Multi-Tenant Architecture:** Securely serves multiple companies or departments from a single deployment, with isolated data and user management.
- **📚 Rich Template Library:** A well-organized library of pre-built, realistic email templates categorized by industry (Finance, Healthcare, IT, etc.) to allow for rapid campaign creation.
- **📁 Easy Employee Import:** Administrators can quickly upload target lists of employees from standard Excel or CSV files.
- **🎯 Dynamic Campaign Management:** Create, launch, and monitor targeted phishing campaigns with ease.
- **📊 Real-time Analytics Dashboard:** A visual dashboard provides immediate insights into campaign performance, including who clicked, click-through rates, and identification of high-risk individuals.
- **🎓 Instant User Education:** Employees who click a simulated phishing link are immediately redirected to a "You've Been Phished" landing page that explains the simulation and provides actionable tips for spotting real-world threats.
- **⚡ Asynchronous Task Processing:** Uses Celery and a message broker to handle the bulk sending of emails in the background, ensuring the UI remains fast and responsive.

## 📸 Visual Showcase

| Main Dashboard |
</br>
</br>
![1735966172482](https://github.com/user-attachments/assets/9fdab61d-10bb-4e19-80cf-11e6306e05aa)
</br>
</br>
| Phished Page  |
</br>
</br>
![1735966104384](https://github.com/user-attachments/assets/1bf96e9a-54e2-4014-90ff-4be4f8dd39e9)
</br>
</br>

| Example Email |
</br>
</br>
![1735965363756](https://github.com/user-attachments/assets/24a038a7-b53f-4ef1-82ee-46fbbedc726e)
</br>
</br>


## ⚙️ How It Works: User & System Flow

1.  **Administrator Login:** An admin logs into their dedicated company portal.
2.  **Campaign Creation:** The admin creates a new campaign, browsing the template library to select the most appropriate email for their target audience.
3.  **Targeting:** They upload a list of employees (name, email) via an Excel/CSV file.
4.  **Launch:** Upon launching, the campaign task is sent to a Celery worker. The worker processes the list and dispatches the customized emails via an SMTP server.
5.  **Employee Interaction:** An employee receives the email and clicks the unique tracking link.
6.  **Tracking & Education:** The system records the click event in the database and immediately redirects the employee to the educational landing page.
7.  **Analysis:** The administrator's dashboard updates in real-time, reflecting the new data and providing a clear overview of the campaign's effectiveness.

## 🛠️ Tech Stack & Architecture

We built this project using a modern and robust Python/Django stack, focusing on scalability and maintainability.

-   **Backend:** Python, Django, Django REST Framework
-   **Frontend:** Django Templates with HTML, CSS, and JavaScript (using Chart.js for data visualization).
-   **Database:** SQLite3
-   **Authentication:** `django-allauth`
-   **Email Delivery:** Integrated with an SMTP server.

## The Team

This project was a collaborative effort. We are proud of what we built together and would be happy to discuss our work.

- **Sohan Kanna** - [LinkedIn](https://www.linkedin.com/in/sohan-kanna/)
- **Sujan** - [LinkedIn](https://www.linkedin.com/in/sujan-h-u-80550a296/)
- **Vishwas Adhikari** - [LinkedIn](https://www.linkedin.com/in/vishwasadhikari/)
