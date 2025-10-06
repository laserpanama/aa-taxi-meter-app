# AA Taxi Meter App

## About the Project

The AA Taxi Meter App is a simulation tool designed to calculate taxi fares based on a comprehensive set of rules and configurations. It takes into account various factors such as time of day, day of the week, distance traveled, and specific geographical zones (geofences) to determine the final fare. This allows for flexible and precise fare calculations that can be adapted to different pricing schemes.

The application's logic is based on the configuration files `taxi_fare_config.json` and `geofences.json`.

## Configuration

The application's behavior is controlled by two main configuration files:

### `taxi_fare_config.json`

This file defines the core fare structure. Here's a breakdown of the configuration options:

-   **`rates`**: Defines the different fare rates.
    -   `name`: The name of the rate (e.g., "Day Rate", "Night Rate").
    -   `start_time` / `end_time`: The time range for the rate.
    -   `days`: The days of the week the rate applies to (1=Monday, 7=Sunday).
    -   `initial_fare`: The base fare for starting a trip.
    -   `per_km_fare`: The fare charged for each kilometer traveled.
-   **`special_geofences`**: Defines areas with special fare rules.
    -   `name`: The name of the geofence.
    -   `fare`: A special fare that applies within this geofence.
-   **`surcharges`**: Defines additional charges.
    -   `name`: The name of the surcharge (e.g., "Luggage").
    -   `amount`: The amount of the surcharge.
-   **`discounts`**: Defines available discounts.
    -   `name`: The name of the discount (e.g., "Senior Citizen").
    -   `percentage`: The discount percentage.

### `geofences.json`

This file defines the geographical zones used by the application. Each geofence is a polygon defined by a series of latitude and longitude coordinates.

-   **`name`**: The name of the geofence.
-   **`coordinates`**: A list of `[latitude, longitude]` pairs that define the boundary of the geofence.

## How to Run

*Instructions on how to run the application will be added here once the main application script is available.*

## Simulation Reports

For detailed examples and simulation results, please see the [Simulation Reports](simulation_reports.md).