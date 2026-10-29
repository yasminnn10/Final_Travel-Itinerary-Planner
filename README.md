# 🇰🇿 QazaqTrip — Travel Itinerary Planner

### Final Project — Software Design Patterns

**Group:** SE-2532
**Team Members:**

- Kashtayeva Yasmina
- Byerik Farida

**Project Status:** Planning / Development

---

## 1. Project Overview

**QazaqTrip** is a planned Java-based travel itinerary planner designed to help tourists organize trips to popular destinations in Kazakhstan.

The application will allow users to select a city, choose multiple attractions, explore accommodation and dining options, compare travel routes, and generate a personalized itinerary.

Our goal is to create a user-friendly application that combines real tourist information with practical trip-planning features while demonstrating the integration of **six software design patterns**.

The initial version will focus on three cities:

- **Astana** — Modern architecture and cultural attractions.
- **Almaty** — Mountains, nature, and city sightseeing.
- **Turkistan** — Historical landmarks and cultural heritage.

---

## 2. Planned Application Features

### 2.1 City Selection

Users will be able to choose one of three destinations: Astana, Almaty, or Turkistan.

### 2.2 Trip Details

Users will specify:

- Trip duration (1–3 days).
- Preferred starting time for daily activities.

### 2.3 Multiple Attraction Selection

Users will be able to select several attractions at once.

Each attraction will include:

- Name and location.
- Short description.
- Estimated visit duration.
- Opening hours.
- Entrance fee, where available.

The application will use information about real attractions in Kazakhstan.

### 2.4 Route Planning

Users will be able to compare two routing strategies:

**Fastest Route**

- Prioritizes shorter travel time.
- Selects faster routes from available alternatives.

**Scenic Route**

- Prioritizes sightseeing and scenic locations.
- May include additional viewpoints or walking routes.

### 2.5 Transportation Selection

Users will be able to choose transportation separately for each part of their itinerary.

Planned transportation options include:

- Walking.
- Taxi.
- Bus.
- Metro (where available).
- LRT (where available).
- Bicycle or electric scooter (where available).

The application will display estimated travel times and costs.

For the initial version, route and transportation information will be based on predefined demonstration data rather than live navigation services.

### 2.6 Hotel Selection

Users will be able to explore and select hotels in their chosen city.

Hotel information will include:

- Hotel name and location.
- Estimated price per night.
- Check-in and check-out times.

### 2.7 Cafes and Meal Breaks

The itinerary will include meal breaks between attractions.

Users will be able to choose cafes based on:

- Location.
- Opening hours.
- Estimated meal prices.

### 2.8 Flight Information

The application will provide sample flight information between selected cities.

Flight and hotel services will initially use **mock implementations**, allowing us to demonstrate the Facade pattern without connecting to external booking platforms.

### 2.9 Itinerary Generation

The application will generate a day-by-day travel plan containing:

- Selected attractions.
- Estimated arrival and departure times.
- Travel time between locations.
- Selected transportation.
- Meal breaks.
- Hotel information.
- Estimated total trip cost.

The application will also aim to detect basic scheduling conflicts, such as visiting an attraction after its closing time.

---

## 3. Design Patterns

The project will integrate **six design patterns** into one application.

| Design Pattern | Planned Implementation                                                                       |
| -------------- | -------------------------------------------------------------------------------------------- |
| **Factory**    | Creates attraction objects based on their categories, such as museums, parks, and landmarks. |
| **Builder**    | Assembles a complete `TripPlan` from the user's selections.                                  |
| **Strategy**   | Implements Fastest and Scenic routing algorithms.                                            |
| **Facade**     | Provides a simplified interface to mock hotel and flight services.                           |
| **Decorator**  | Adds optional activities or guided tours to the trip and updates its cost.                   |
| **Observer**   | Notifies the application when the itinerary is modified.                                     |

All six patterns will be implemented within the same application and demonstrated during the project defense.

---

## 4. Team Responsibilities

| Team Member            | Design Patterns             |
| ---------------------- | --------------------------- |
| **Byerik Farida**      | Factory, Builder, Strategy  |
| **Kashtayeva Yasmina** | Facade, Decorator, Observer |

Both team members will participate in application integration, testing, documentation, and preparation for the final defense.

---

## 5. Planned Technologies

- **Programming Language:** Java
- **Development Environment:** IntelliJ IDEA
- **User Interface:** JavaFX
- **Version Control:** Git and GitHub
- **Data Storage:** Local files (CSV or JSON)
- **Hotel and Flight Services:** Mock implementations
- **UML Diagrams:** To be developed during implementation

The application is planned to have multiple screens with clickable buttons and a graphical interface.

---

## 6. Planned Application Screens

1. **Welcome Page** — Introduction and Start Planning button.
2. **City Selection** — Choose Astana, Almaty, or Turkistan.
3. **Trip Details** — Select trip duration and starting time.
4. **Attractions** — Select multiple places to visit.
5. **Hotel Selection** — Explore and choose accommodation.
6. **Cafe Selection** — Choose dining options and meal breaks.
7. **Route & Transportation** — Select Fastest/Scenic routes and transportation for individual segments.
8. **Additional Activities** — Add optional tours or services.
9. **Final Itinerary** — View the complete schedule and estimated costs.

---

## 7. Development Plan

**Phase 1 — Research and Data Collection**

- Collect information about real attractions, cafes, and hotels in the selected cities.
- Prepare sample transportation routes and estimated travel times.
- Organize data into local files.

**Phase 2 — Core Java Development**

- Create the main application models.
- Implement Factory, Builder, and Strategy.
- Implement Facade, Decorator, and Observer.
- Integrate the six patterns.

**Phase 3 — Application Interface**

- Develop the JavaFX screens.
- Connect user actions to the Java logic.
- Implement navigation between screens.

**Phase 4 — Testing**

- Test each design pattern.
- Test itinerary generation.
- Test route selection and transportation options.
- Check basic scheduling conflicts and cost calculations.

**Phase 5 — Documentation and Defense**

- Prepare UML diagrams.
- Capture application screenshots.
- Write the final PDF report.
- Prepare the source code ZIP archive.
- Demonstrate the application and explain the implemented design patterns.

---

## 8. Future Improvements

Possible improvements after the initial version include:

- Integration with real hotel and flight APIs.
- Live public transportation information.
- Interactive maps and navigation.
- More destinations across Kazakhstan.
- Real-time ticket prices and availability.
- Online hotel and flight booking.

---
