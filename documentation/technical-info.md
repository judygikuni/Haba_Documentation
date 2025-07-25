# Technical Information

This section provides an overview of the Gorzo platform's technical architecture, key integrations, and other relevant technical details. It is intended for developers, system administrators, or anyone interested in the underlying technical aspects of the platform.


## 1. System Architecture Overview

The Gorzo platform utilizes a dual-application approach supported by a centralized backend.

-   **Customer Mobile App:** A native mobile application developed for both iOS and Android platforms.
-   **Mama Mboga Mobile App:** A mobile application accessible via the phone store, designed to provide a native-like experience for vendors.
-   **Backend System:** A robust and scalable server-side infrastructure that handles data storage, business logic, API management, and integration services. This system orchestrates interactions between the mobile app and third-party services such as location and M-Pesa.

*For a detailed visual representation of the system components and their interactions, please refer to the [System Architecture Link](https://lucid.app/lucidchart/6bd58d2a-b47f-4787-b17b-04b7e7fb3fe0/edit?invitationId=inv_1252e4ca-25ed-4e2d-84ac-37266019ae13&referringApp=slack&page=0_0#)

## 2. Key Integrations

### 2.1 Payment Integration: M-Pesa

The Gorzo platform leverages **M-Pesa STK Push** for seamless mobile money payment processing.

-   **Functionality:** This integration allows for direct payment requests to be sent to the customer's M-Pesa enabled device, enabling quick and secure transactions.
-   **Supported Transactions:** Supports both in-app purchases and payments during physical pick-ups.
-   **Security:** Adheres to M-Pesa's security protocols for secure transaction handling.

### 2.2 Geolocation Integration

The Gorzo platform incorporates geolocation services to support key functionality such as location-based group buying and vendor discovery.

- **Purpose:** To enable accurate location identification of vendors (Mama Mboga) and customers, facilitating nearby group order formation, efficient order fulfillment, and improved user experience.
- **Technology:** Utilizes device GPS data and network-based positioning (cell towers and WiFi access points) accessed via standard Geolocation APIs.
- **Features:**
  - Accurate vendor location capture during registration.
  - Location-based discovery for customers to find live group orders within approximately 300 meters.
  - Supports location accuracy validation to ensure orders are placed within feasible pickup zones.
- **Implementation:** Accessible via browser geolocation APIs in the PWA for vendors, and geolocation APIs in the mobile app for customers.
- **Data Handling:** Location data is processed in compliance with privacy standards and is used solely to enhance ordering logistics and market reach.

By integrating geolocation, Gorzo effectively connects the local community and optimizes the group buying system to be practical and convenient for both vendors and consumers.


## 3. Security and Data Handling

The platform is designed with security in mind, ensuring data privacy and integrity. Regular security audits and updates will be performed to maintain a secure environment. For more details on regulatory compliance, refer to the [Regulatory and Compliance](regulatory-compliance.md) section.

## 4. Development Environment

The Gorzo platform is built using the following technology stack:

- **Frontend (Customer Mobile App and Vendor PWA):**  
  Developed using **Kotlin Jetpack Compose**, a modern toolkit for building native Android applications with declarative UI. Both the customer app and vendor app leverage Kotlin Jetpack Compose to provide a responsive and efficient user interface experience.

- **Backend:**  
  The server-side application is developed using **Python** with the **Django** web framework. Django provides a robust, scalable, and secure framework for handling the business logic, API endpoints, authentication, and integration with external services.

- **Database:**  
  Data is stored using **PostgreSQL**, a powerful, open-source relational database system well-suited for complex queries, transactional integrity, and scaling.

- **Hosting:**  
  The backend APIs and services are hosted on **Heroku**, a cloud platform that supports easy deployment, scaling, and management of applications.

This stack ensures a maintainable, scalable, and performant architecture tailored to the needs of both vendors and customers on the Gorzo platform.

For detailed guides, please proceed to the [Getting Started](getting-started.md) section.

