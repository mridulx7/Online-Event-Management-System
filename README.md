# Online Event Management System

A Java-based system designed to manage events, users, tickets, and registrations using Core Java, OOP, JDBC, and MySQL.
This project demonstrates clean architecture, DAO pattern, multithreading, and proper database connectivity.

# Features
## Admin

Manage user accounts

Approve or reject events

Monitor system activities

## Event Organizer

Create and manage events

Handle ticket pricing and availability

Communicate with attendees

## Attendee

Register for events

Purchase tickets

Receive notifications

# Tech Stack

Java (Core Java, OOP, Multithreading)

JDBC (MySQL Connector/J 8.3.0)

MySQL Database

DAO Design Pattern

VS Code

# Project Structure
src/
 └── com.eventmgmt
      ├── model        → User, Admin, Organizer, Attendee, Event, Ticket  
      ├── dao          → GenericDAO, UserDAO, EventDAO, TicketDAO & implementations  
      ├── util         → DBConnection.java  
      ├── thread       → NotificationThread.java, TicketBooking.java  
      └── main         → MainApp.java  
lib/
 └── mysql-connector-j-8.3.0.jar
database/
 └── schema.sql (MySQL table creation scripts)
README.md

# OOP Concepts Implemented
## Inheritance

Admin, Organizer, Attendee extend User.java

## Polymorphism

Overridden showDashboard() in Admin, Organizer, Attendee

## Interfaces

GenericDAO<T>

UserDAO, EventDAO, TicketDAO extend it

## Exception Handling

try/catch blocks used in DAO & DBConnection

Handles SQL exceptions and connection failures

# Collections & Generics
Collections

List<T> used to store Users, Events, Tickets

Implemented in DAO getAll() methods

Generics

GenericDAO<T> interface makes CRUD operations reusable

UserDAO, EventDAO, TicketDAO extend it with specific types

# Multithreading & Synchronization
Multithreading

NotificationThread.java (extends Thread)

Threads started in MainApp.java

Synchronization

TicketBooking.java uses synchronized method

Prevents race conditions while booking tickets

# Database Schema

Database Name: eventdb

Tables:

users

events

tickets

registrations

messages

Includes foreign keys and relationships.
