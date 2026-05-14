# Campus Food Delivery Notification System

This project is a refactored Java application for a university food delivery system.It demonstrates the implementation of **Factory** and **Singleton** design patterns to improve code maintainability and scalability

## Project Description
The system handles food orders for students and sends notifications via different channels.Originally, the system used complex `if-else` logic inside a single class.This refactored version uses design patterns to decouple the notification logic from the main service.

## Design Patterns Used

### 1. Factory Pattern
Used to create notification objects (`EmailNotification`, `SmsNotification`, `PushNotification`) based on the input type.This allows the system to be easily extended with new notification types (like WhatsApp or Telegram) without modifying the core `CampusFoodOrderService` class.

### 2. Singleton Pattern
The `AppConfig` class is implemented as a Singleton.It ensures that system-wide configurations, such as the University Name and Delivery Fee, are managed from a single point and shared across all classes.

## Project Structure
- `Notification.java`: Interface for all notification types.
- `NotificationFactory.java`: The factory class that creates notification instances.
- `AppConfig.java`: Singleton class for global configurations.
- `CampusFoodOrderService.java`: The main class to run the application and place orders.
- `EmailNotification.java`, `SmsNotification.java`, `PushNotification.java`: Concrete implementations of the notification interface.

## How to Run
1.Ensure you have Java Development Kit (JDK) installed.
2. Clone this repository:
   ```bash
https://github.com/Dogukandogan3/Software-homework
