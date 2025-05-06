# 📦 MyProject

This project is a modern backend application built with **.NET 8**, leveraging **Entity Framework Core**, **RabbitMQ**, **Redis**, and **Hangfire**. It follows clean architecture principles and uses **MediatR** for implementing the CQRS pattern.

---

## 🚀 Technologies Used

- **.NET 8**
- **Entity Framework Core**
- **SQL Server**
- **Redis** – Caching
- **RabbitMQ** – Asynchronous messaging
- **Hangfire** – Background job processing
- **MediatR** – CQRS implementation
- **Swagger (Swashbuckle)** – API documentation

---

## 🧰 Prerequisites

Before running the project, make sure the following are installed:

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [SQL Server](https://www.microsoft.com/en-us/sql-server)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) – To run Redis and RabbitMQ
- Optional tools:
  - SQL Server Management Studio (SSMS)
  - Postman (for API testing)

---

## 🐳 Redis & RabbitMQ via Docker

Start Redis and RabbitMQ using Docker:

```bash
# Start Redis
docker run -d --name redis -p 6379:6379 redis

# Start RabbitMQ (with management UI)
docker run -d --hostname rabbit --name rabbitmq \
  -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```
RabbitMQ AMQP: amqp://localhost:5672

RabbitMQ UI: http://localhost:15672
(Username: guest, Password: guest)


⚙️ Getting Started
1. Clone the repository
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
2. Set up the database
```
```bash
Apply EF Core migrations:

```bash
dotnet ef database update
```
If you make changes to models later:

```bash
dotnet ef migrations add MigrationName
dotnet ef database update
```
