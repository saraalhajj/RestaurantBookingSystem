## Project Description

The Restaurant Booking System is a web-based application designed to streamline table reservations for both customers and restaurant administrators. The application allows users to discover local dining options, check real-time seating availability, and secure their reservations instantly. On the administrative side, restaurant managers can oversee seat capacities, update operating hours, and approve or decline incoming booking requests.

Following enterprise architectural standards, the project is structured using Clean Architecture principles to ensure complete separation of concerns and peak scalability:

### 1. RestaurantBooking.Core (Domain & Business Logic)
* **Entities**: Includes key business models such as `User`, `Restaurant`, and `Reservation` using strict singular naming and PascalCase[cite: 1, 2].
* **Interfaces**: Defines repository and service blueprints (e.g., `IUserService`, `IReservationService`) starting with the standard 'I' prefix[cite: 2].

### 2. RestaurantBooking.Infrastructure (Data & External Services)
* **Database Schema**: Structured using strict SQL Server guidelines with identity primary keys (`UserId`, `RestaurantId`)[cite: 1] and explicit relational constraints (e.g., `PkUser_UserId`, `FkReservation_UserId`)[cite: 1].
* **Persistence**: Handles direct database communication, ensuring optimized query performance with ANSI-Standard joins and avoiding performance-heavy operations[cite: 1].
