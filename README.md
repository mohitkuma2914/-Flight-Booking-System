# ✈️ Flight Booking System (Spring Boot)

A simple **Flight Booking Backend Application** built using **Spring Boot**.
This project allows users to book flights using wallet balance and manage flights & bookings.

---

## 🚀 Features

### 👤 User Management

* Create new user
* View all users
* Get user by ID
* Add money to wallet
* Delete user

### ✈️ Flight Management

* Add new flight
* View all flights
* Search flights (origin → destination)
* Delete flight

### 🎫 Booking Management

* Book a flight
* Cancel booking
* View all bookings
* View bookings by user

---

## 🛠️ Tech Stack

* Java 22
* Spring Boot
* Spring Data JPA
* Hibernate
* MySQL
* Maven

---

## 📁 Project Structure

```
com.flightapp
│
├── Controller
│   ├── BookingController
│   ├── FlightController
│   └── UserController
│
├── Service
│   ├── BookingService
│   ├── FlightService
│   └── UserService
│
├── Model
│   ├── Booking
│   ├── Flight
│   └── User
│
├── Repository
│   ├── BookingRepository
│   ├── FlightRepository
│   └── UserRepository
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone Repository

```
git clone https://github.com/your-username/flight-booking-system.git
cd flight-booking-system
```

---

### 2️⃣ Create Database

```
CREATE DATABASE flightdb;
```

⚠️ Important:
Agar database create nahi karoge to error aayega:

```
Unknown database 'flightdb'
```

---

### 3️⃣ Configure application.properties

```
spring.datasource.url=jdbc:mysql://localhost:3306/flightdb
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

### 4️⃣ Run Application

```
mvn spring-boot:run
```

Server start hoga:

```
http://localhost:8080
```

---

## 📡 API Endpoints

### 👤 User APIs

| Method | Endpoint                          | Description   |
| ------ | --------------------------------- | ------------- |
| GET    | /api/users                        | Get all users |
| GET    | /api/users/{id}                   | Get user      |
| POST   | /api/users                        | Create user   |
| PUT    | /api/users/{id}/wallet?amount=500 | Add money     |
| DELETE | /api/users/{id}                   | Delete user   |

---

### ✈️ Flight APIs

| Method | Endpoint                                       | Description     |
| ------ | ---------------------------------------------- | --------------- |
| GET    | /api/flights                                   | Get all flights |
| GET    | /api/flights/{id}                              | Get flight      |
| GET    | /api/flights/search?origin=DEL&destination=MUM | Search flights  |
| POST   | /api/flights                                   | Add flight      |
| DELETE | /api/flights/{id}                              | Delete flight   |

---

### 🎫 Booking APIs

| Method | Endpoint                          | Description          |
| ------ | --------------------------------- | -------------------- |
| GET    | /api/bookings                     | Get all bookings     |
| GET    | /api/bookings/user/{userId}       | Get bookings by user |
| POST   | /api/bookings?userId=1&flightId=2 | Book flight          |
| PUT    | /api/bookings/{id}/cancel         | Cancel booking       |

---

## 🔁 Booking Logic

* Check seat availability
* Check wallet balance
* Deduct amount from wallet
* Reduce flight seats
* Create booking

💡 Transaction used → agar koi step fail hua to pura rollback

---

## 🧠 Future Improvements

* JWT Authentication
* Payment Integration
* Admin Dashboard
* UI (Frontend)

---

## 👨‍💻 Author

**Mohit Kumar**

---

⭐ Agar project pasand aaye to GitHub pe star zaroor do!
