# Quick Stay (Backend)

**Quick Stay** is a Spring Boot backend for a short-term rental platform, crafted with a strong focus on ensuring the safety and comfort of female travelers. This backend enables seamless property booking, management, and search functionalities, enhancing the overall booking experience while maintaining security and ease of use.

## Description
Quick Stay is engineered to deliver core features of a rental platform, such as robust booking management, property search, and role-based access control, with an emphasis on security and scalability. The backend's design adopts **Domain-Driven Design (DDD)** to ensure maintainability and future extensibility, allowing it to scale with the addition of new features and integrations.

## Objective
The primary objective of Quick Stay is to build a secure, reliable, and user-friendly platform that addresses the unique needs of female travelers, ensuring safety and comfort in short-term rentals. By providing streamlined booking, reservation management, and comprehensive search capabilities, Quick Stay supports users in finding accommodations that meet specific criteria and provides landlords with tools to manage reservations efficiently.


## Scope of the Project
The Quick Stay backend provides the following core functionalities:
- **Booking Management**: Enables travelers to easily manage bookings and landlords to manage reservations.
- **Search and Filter Options**: Allows users to search for properties based on location, number of guests, date, amenities, and more.
- **Secure Authentication and Authorization**: Implements role-based access with Auth0 and OAuth2 for secure user authentication.
- **Domain-Driven Architecture**: Organizes code into cohesive domains, promoting scalability and ease of maintenance.

Future enhancements could include integration with third-party APIs, real-time notifications, and advanced analytics.

## System Requirements
To build and run Quick Stay, the following software requirements must be met:
- **JDK 21**: Required to compile and run the Spring Boot application. Install from [Adoptium Temurin](https://adoptium.net/temurin/releases/).
- **IDE**: Use an IDE that supports Java, such as [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) or [VSCode](https://code.visualstudio.com/download).
- **Maven**: Used for managing dependencies and building the project. Maven is included within the project structure.

## Design
The backend of Quick Stay is structured following the **Model-View-Controller (MVC) pattern**, ensuring a clean separation of concerns and a modular, maintainable codebase. Each component has a specific role in handling the application’s data flow and user interactions:
- **`controller/`**: Acts as the interface between the client and server, managing HTTP requests, handling responses, and directing requests to the appropriate services.
- **`service/`**: Contains the business logic of the application, processing data, managing transactions, and coordinating between controllers and repositories.
- **`repository/`**: Responsible for data persistence and retrieval, interacting directly with the database to perform CRUD (Create, Read, Update, Delete) operations.
  
Additionally, **Auth0** is implemented for secure user authentication, utilizing **OAuth2** to enforce role-based access control, allowing users (such as travelers and landlords) to securely log in and access the platform based on their assigned roles.

## Implementation

### Technology Stack
- **Backend Framework**: Spring Boot, chosen for its robust ecosystem and ease of configuration for building RESTful APIs.
- **Database**: Configurable for either MySQL or PostgreSQL, providing flexibility in data storage and retrieval.
- **Authentication**: Auth0 with OAuth2 integration for secure, role-based access control.
- **Build Tool**: Maven for dependency management and project building.

### Project Structure
The backend application follows a modular structure to facilitate scalability:
- **Booking Management Module**: Manages bookings for both travelers and landlords, enabling CRUD operations on reservations.
- **Search Module**: Handles complex filtering and search queries based on multiple criteria like location, availability dates, number of guests, and amenities.
- **Authentication Module**: Manages user roles and access levels, implementing OAuth2 with Auth0 for secure and streamlined user authentication.


## Key Features
The Quick Stay backend incorporates the following features:

1. **Booking Management**  
   - Allows travelers to book and manage their reservations.
   - Provides landlords with tools to approve or reject bookings, manage availability, and view booking history.
   
2. **Landlord Reservation Management**  
   - Enables landlords to view, update, and delete property reservations.
   - Facilitates availability and schedule management for multiple properties.

3. **Advanced Search Functionality**  
   - Provides travelers with flexible search options, allowing them to filter properties by location, date, number of guests, beds, amenities, and other criteria.
   - Ensures efficient data retrieval with optimized database queries.

4. **Authentication and Authorization**  
   - Implements Auth0 with OAuth2 to provide secure login and access control.
   - Role-based access for travelers, landlords, and administrators to limit permissions and protect data.

5. **Domain-Driven Design (DDD)**  
   - Employs DDD principles to organize the codebase into meaningful domains, improving modularity and easing future development.
   - Enhances scalability by separating business logic, data management, and service orchestration into distinct modules.


## Usage

### Prerequisites
Ensure you have the following installed:
- [JDK 21](https://adoptium.net/temurin/releases/) - Required to run Spring Boot.
- An IDE that supports Java development, such as [IntelliJ IDEA](https://www.jetbrains.com/idea/download) or [VSCode](https://code.visualstudio.com/download).

### Launch Instructions

#### Using Maven
To run the application via Maven, execute the following command in your terminal:
```bash
./mvnw spring-boot:run -Dspring-boot.run.arguments="--AUTH0_CLIENT_ID=<client-id> --AUTH0_CLIENT_SECRET=<client-secret>"
```
Replace <client-id> and <client-secret> with your Auth0 credentials to authenticate with OAuth2.



#### Using IntelliJ
1. Open the project in IntelliJ.
2. Navigate to **Run > Edit Configurations**.
3. Add `AUTH0_CLIENT_ID` and `AUTH0_CLIENT_SECRET` as environment variables with your Auth0 credentials.
4. Run the project from the **Run** menu.

## Future Enhancements
While Quick Stay already provides robust booking and search functionality, future versions may include:

- **Integration with External APIs**: Integrate with mapping or payment APIs to enhance the booking experience.
- **Advanced Analytics**: Provide landlords and admins with tools to gain insights into booking trends, occupancy rates, and more.
- **Real-Time Notifications**: Enable SMS or email notifications for booking confirmations and updates.
- **Wearable Device Integration**: Add features for health and safety monitoring for travelers, enhancing comfort and security for female guests.

