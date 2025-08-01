# Technical Information

This section provides an overview of the Gorzo platform's technical architecture. It is intended for developers, system administrators, or anyone interested in the underlying technical aspects of the platform.


## 1. System Architecture Overview

The Gorzo platform utilizes a dual-application approach supported by a centralized backend.

-   **Customer Mobile App:** A native mobile application developed for both iOS and Android platforms.
-   **Mama Mboga Mobile App:** A mobile application accessible via the phone store, designed to provide a native-like experience for vendors.
-   **Backend System:** A robust and scalable server-side infrastructure that handles data storage, business logic, API management, and integration services. This system orchestrates interactions between the mobile app and third-party services such as location and M-Pesa.

*For a detailed visual representation of the system components and their interactions, please refer to the [System Architecture Link](https://lucid.app/lucidchart/6bd58d2a-b47f-4787-b17b-04b7e7fb3fe0/edit?invitationId=inv_1252e4ca-25ed-4e2d-84ac-37266019ae13&referringApp=slack&page=0_0#)


## 2. API Architecture and Endpoints

The Gorzo platform exposes a RESTful API that enables communication between the mobile appications (customer and Mama Mboga) and the backend services. The API supports functionalities such as user authentication, producr and inventory management, order processing, group buying coordination, and payment integration. 

## 2.1 Key API Modules

- **Authentication:** Handles user registration, login, and secure access management.
- **Products & Inventory:** Allows mama mboga to manage their inventory and customers to browse availabel groceries. 
- **Orders & Group Buying:** Manages placing orders, joining group buys, and tracking order status.
- **Payments:** Integrates with M-Pesa for seamless mobile money transactions.
- **Notifications:** Sends alerts related to group buying deals and payment confirmations.


### 2.2 Authentication & Security

The API uses Django auth token for authenticating requests, ensuring secure access control. Sensitive information is encrypted in transit using HTTPS.


### 2.3 Integration with Third-Party Services

- **Location Services:** For accurate vendor and group order location mapping.
- **M-Pesa Payment Gateway:** For processing mobile money payments via STK Push requests and receiving payment confirmations asynchronously.

