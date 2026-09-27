# Salon Appointment Scheduler 💇

A command-line salon appointment scheduling application built with
Bash and PostgreSQL.

The application allows customers to select a salon service, provide
their contact information, and schedule an appointment.

## 📌 How It Works

1. Displays the available salon services.
2. User selects a service.
3. Validates the selected service.
4. Asks for the customer's phone number.
5. Checks whether the customer already exists.
6. Creates a new customer if necessary.
7. Asks for the appointment time.
8. Stores the appointment in the PostgreSQL database.
9. Displays a confirmation message.

## 🗄️ Database Structure

The PostgreSQL database is named `salon`.

It contains three tables:

### `services`

Stores available salon services.

| Column | Description |
|---|---|
| `service_id` | Unique service ID |
| `name` | Service name |

Available services include:
- Cut
- Color
- Style

### `customers`

Stores customer information.

| Column | Description |
|---|---|
| `customer_id` | Unique customer ID |
| `name` | Customer name |
| `phone` | Customer phone number |

The phone number is stored as a unique value.

### `appointments`

Stores appointment information.

| Column | Description |
|---|---|
| `appointment_id` | Unique appointment ID |
| `customer_id` | Customer ID |
| `service_id` | Selected service |
| `time` | Appointment time |

## 🔗 Database Relationships

```text
Customers
    │
    │ customer_id
    ↓
Appointments
    ↑
    │ service_id
    │
Services

## 🛠️ Technologies Used

- Bash
- PostgreSQL
- SQL

## 🎓 Learning Source

This project was completed as part of the
[freeCodeCamp Relational Database curriculum](https://www.freecodecamp.org/learn/relational-database/).
