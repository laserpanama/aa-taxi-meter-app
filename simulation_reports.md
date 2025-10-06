# AA Taxi Meter App Simulation Reports

## Introduction

This document contains a series of simulation reports for the AA Taxi Meter App. Each simulation demonstrates how the application calculates taxi fares under different conditions, based on the rules defined in the `taxi_fare_config.json` and `geofences.json` files. These examples are intended to verify the correctness of the fare logic and provide clear illustrations of the app's features.

---

## Simulation 1: Regular Fare Calculation

This simulation demonstrates a standard fare calculation during the day on a weekday.

-   **Input**:
    -   Distance: 10 km
    -   Time: 2023-10-26 10:00:00 (Thursday)
-   **Expected Output**:
    -   Total Fare: $22.50

---

## Simulation 2: Night Fare Calculation

This simulation shows how the fare changes when the trip occurs during night hours, triggering the night rate.

-   **Input**:
    -   Distance: 10 km
    -   Time: 2023-10-26 23:00:00 (Thursday)
-   **Expected Output**:
    -   Total Fare: $28.00

---

## Simulation 3: Weekend Fare Calculation

This simulation demonstrates the fare calculation for a trip on a weekend, which may have a different rate.

-   **Input**:
    -   Distance: 15 km
    -   Time: 2023-10-28 14:00:00 (Saturday)
-   **Expected Output**:
    -   Total Fare: $37.50

---

## Simulation 4: Trip within a Special Geofence

This simulation tests the special fare rules for a trip that occurs entirely within a defined geofence (e.g., an airport).

-   **Input**:
    -   Start Location: (9.00, -79.5)
    -   End Location: (9.01, -79.51)
    -   Distance: 2 km
    -   Time: 2023-10-26 11:00:00 (Thursday)
-   **Expected Output**:
    -   Total Fare: $25.00 (Airport flat rate)

---

## Simulation 5: Trip with Surcharges

This simulation shows how surcharges, such as for extra luggage, are added to the total fare.

-   **Input**:
    -   Distance: 8 km
    -   Time: 2023-10-27 09:00:00 (Friday)
    -   Surcharges: Luggage (2 pieces)
-   **Expected Output**:
    -   Total Fare: $21.00

---

## Simulation 6: Trip with Discounts

This simulation demonstrates how percentage-based discounts, such as for senior citizens, are applied to the fare.

-   **Input**:
    -   Distance: 12 km
    -   Time: 2023-10-26 15:00:00 (Thursday)
    -   Discounts: Senior Citizen
-   **Expected Output**:
    -   Total Fare: $24.75