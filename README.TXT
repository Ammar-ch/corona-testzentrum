# COVID-19 Test Appointment System

This Java console application simulates a simplified COVID-19 test booking system for customers in Germany. It allows customers to enter personal information, select a test type, choose a test station, and generate an appointment. The system also determines if the test is free based on age or specific conditions (e.g. pregnancy or foreign students).

---

## Features

* Customer data input with address and email validation
* Different types of COVID-19 tests with pricing and result status
* Free test eligibility checks
* Test stations stored with location and capacity
* Appointment creation with random date & time generation
* Console and graphical alerts via `JOptionPane`

---

## Classes Overview

### `Anschrift`

Represents a postal address with:

* `strasse`, `hausnummer`, `Postleitzahl`, `Stadt`
* Constructor and getters/setters
* `toString()` for formatted output

### `COVID19_Test`

Encapsulates test information:

* `id`, `name`, `preis`, `dauer_Std`, `ergebnis`
* Method to mark result as positive
* Accessors and `toString()`

### `Console`

Provides input/output and validation utilities:

* `read_data_kunde()`: reads customer data from console
* `controlEmail()`: validates email using regex
* `controlTestGratis()`: checks if test is free based on age or condition
* `alert()`: shows GUI alert using Swing
* `clearConsole()`: clears console output (not fully functional)

### `Termin`

Represents a test appointment:

* Holds references to a `Kunde`, `COVID19_Test`, and `Test_station`
* Randomly generates appointment date and time
* Calculates and prints test cost or confirms free eligibility

### `main`

Handles:

* Initializing test types and stations
* Reading user input and data
* Offering test selection and creating an appointment
* Matching the customer’s city with a nearby test station

---

## Usage

1. Compile the program with `javac *.java`
2. Run it using `java main`
3. Follow the prompts to enter your personal data
4. Choose a COVID-19 test
5. The system finds a matching test station and schedules your appointment

---

## Requirements

* Java 8 or higher
* Console environment with standard input/output

---

## Notes

* Input is validated (email, postal code)
* Test ID 2 (Antigen Schnelltest) may be free under certain conditions
* Random date/time generation ensures realistic scheduling
* Designed for German users but supports internationalization


