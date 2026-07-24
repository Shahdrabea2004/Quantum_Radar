# Quantum Radar

A Java-based traffic monitoring system that processes vehicle observations
and detects traffic violations using a flexible rule-based architecture.

## Overview

Quantum Radar receives vehicle data from a radar system, including plate
number, date, vehicle type, speed, and seatbelt status. The system evaluates
each observation against a set of configurable rules and generates fines for
detected violations.

## Features

- Processes vehicle observations and traffic data
- Supports multiple vehicle types (Private, Truck, Bus)
- Applies configurable traffic rules
- Generates fines containing violation details and fees
- Provides total fines and violation statistics
- Allows adding new rules without modifying the radar system

## Design & Architecture

The project follows clean Object-Oriented Design principles:

- Strategy Design Pattern for flexible rule handling
- SOLID Principles for maintainable and extensible code
- Interface-based design to support adding new rules easily
- Separation of responsibilities between models, rules, and radar logic

## Technologies

- Java
- Object-Oriented Programming (OOP)
- SOLID Principles
- Strategy Design Pattern
- Java Collections Framework
  - ArrayList
  - HashMap
  - List
  - Map

## Project Structure
```
src
├── model
│   ├── Observation.java
│   ├── Violation.java
│   └── Fine.java
├── rules
│   ├── Rule.java
│   ├── MaxSpeedRule.java
│   └── SeatbeltRule.java
├── radar
│   └── QuRadar.java
└── Main.java
```


## How It Works

1. Vehicle information is received as an Observation.
2. QuRadar evaluates the observation against all registered rules.
3. Violations are collected.
4. A Fine is generated if violations exist.
5. Statistics about violated rules can be retrieved.
