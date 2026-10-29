# 🇰🇿 QazaqTrip — Travel Itinerary Planner

### Final Project — Software Design Patterns

**Group:** SE-2532  
**Team Members:**
- Kashtayeva Yasmina
- Byerik Farida

**Project Status:** Planning / Development

---

## 1. Project Overview

**QazaqTrip** is a Java-based travel itinerary planner designed to help tourists organize personalized trips across Kazakhstan.

The application will guide users through a step-by-step planning process. Users will choose their travel destination and dates, select attractions, customize transportation between locations, specify their travel group, and decide whether they want hotel, flight, and cafe suggestions.

Based on these selections, QazaqTrip will generate a **personalized day-by-day travel itinerary** with estimated arrival times, attraction visits, transportation details, meal breaks, and trip costs.

The project will demonstrate the practical integration of **six software design patterns** within one application.

### Initial Destinations

The first version will focus on three cities in Kazakhstan:

- **Astana** — Modern architecture, museums, and cultural landmarks.
- **Almaty** — Mountain attractions, parks, and urban sightseeing.
- **Turkistan** — Historical sites and cultural heritage.

Our goal is to create an interactive and visually appealing application that makes travel planning easier while demonstrating object-oriented design principles.

---

## 2. Application Workflow

QazaqTrip will have a **welcome page, four planning steps, and a final itinerary page**.

Users will navigate between screens using clickable **Back** and **Continue** buttons.

### Welcome Page — Discover Kazakhstan

The application will open with a welcoming screen featuring:

- QazaqTrip branding.
- A short introduction to the application.
- Visuals of Kazakhstan's travel destinations.
- A **Start Planning** button.

Clicking **Start Planning** will open the trip-planning process.

### Step 1 — The Trip: Where and When?

Users will provide the basic details of their trip:

- **Starting From:** Departure city.
- **Destination:** Astana, Almaty, or Turkistan.
- **Travel Dates:** Start and end dates.

The application will calculate the trip duration from the selected dates.

For the initial version, itinerary generation will focus on trips lasting **1–3 days**.

### Step 2 — Explore Places: What to Visit?

After choosing a destination, users will see attractions available in that city.

Users will be able to **select multiple attractions**.

Each attraction will display:

- Name and photograph.
- Short description.
- Location.
- Opening hours.
- Estimated visit duration.
- Entrance fee, where available.

For example, a user visiting Almaty might select:

- Kok-Tobe.
- Medeu.
- Shymbulak.
- Panfilov Park.

The application will use information about real tourist attractions in Kazakhstan.

### Step 3 — Route & Transportation: How to Travel?

After selecting attractions, users will customize their route.

#### Route Preferences

Users will choose between two route-planning strategies:

**Fastest Route**
- Prioritizes shorter travel times.
- Selects faster alternatives from the available route data.

**Scenic Route**
- Prioritizes more scenic travel options.
- May favor routes with sightseeing opportunities, even when they take longer.

#### Transportation Selection

Users will be able to choose transportation **separately for each segment of the route**.

Planned options include:

- Walking.
- Taxi.
- Bus.
- Metro, where applicable.
- LRT, where applicable.
- Bicycle or electric scooter, where applicable.

Available transportation options will depend on the city and route segment.

The application will display:

- Starting point and destination.
- Available transportation options.
- Estimated travel duration.
- Estimated transportation cost.

Users will also be able to review the order of their selected attractions.

**Initial implementation:** Route alternatives, travel times, and transportation costs will use predefined demonstration data rather than live navigation services.

### Step 4 — Who's Going?

Users will specify who they are traveling with.

The application will provide four options:

- **Solo** — Traveling alone.
- **Couple** — Traveling with a partner.
- **Friends** — Traveling with friends.
- **Family** — Traveling with family members.

Users will also be able to specify the **number of travelers**.

#### Optional Travel Suggestions

This page will include switches for:

**Hotel Suggestions**
- When enabled, the final itinerary will display hotel recommendations.
- Hotel information will include estimated prices, location, and check-in/check-out times.

**Flight Suggestions**
- When enabled, the application will display sample flight options between the departure city and destination, where applicable.

**Cafe Suggestions**
- When enabled, the application will recommend cafes near selected attractions and suggest meal breaks.

These options will be **optional**. Users can generate a travel itinerary without requesting hotel, flight, or cafe suggestions.

The initial version will not support real bookings or payments.

### Final Page — My Itinerary

After completing the planning steps, users will click **Generate My Itinerary**.

QazaqTrip will generate a personalized travel schedule based on the user's selections.

The final page will include:

#### Daily Schedule
- Attractions organized by day.
- Estimated arrival and departure times.
- Duration of each visit.
- Transportation between locations.
- Meal breaks, when selected.
- Basic checks against attraction and cafe opening hours.

#### Route Overview
- The order of selected attractions.
- Transportation for each route segment.
- Estimated travel durations and costs.
- Selected Fastest or Scenic route preference.

#### Hotel Suggestions
Displayed when the user enables hotel recommendations.

#### Flight Suggestions
Displayed when the user enables flight recommendations.

#### Estimated Costs
A breakdown of:
- Attraction entrance fees.
- Transportation costs.
- Estimated meal expenses, when included.
- Optional activities.
- Hotel and flight costs, if the user selects specific options.

Suggested hotels and flights that have not been selected will be displayed separately and will not automatically be included in the trip total.

Users will be able to return to previous steps to edit their choices and regenerate the itinerary.

---

## 3. Design Patterns

The project will implement **six design patterns**.

| Design Pattern | Planned Implementation |
|---|---|
| **Factory** | Creates attraction objects based on categories such as museums, parks, and landmarks. |
| **Builder** | Constructs a complete `TripPlan` using the information collected during the planning process. |
| **Strategy** | Implements Fastest and Scenic route-selection strategies. |
| **Facade** | Provides a simplified interface for retrieving hotel and flight suggestions from mock services. |
| **Decorator** | Adds optional activities or guided tours to an existing trip and updates its description and estimated cost. |
| **Observer** | Notifies relevant application components when itinerary selections change, allowing displayed information to be updated. |

The six patterns will be integrated into a single application rather than implemented as unrelated examples.

### Design Pattern Integration

The planned workflow is:

1. **Factory** creates objects representing selected attractions.
2. **Strategy** selects route alternatives according to the user's preference.
3. **Builder** assembles the trip schedule and selected information into a `TripPlan`.
4. **Facade** retrieves optional hotel and flight suggestions.
5. **Decorator** adds optional activities to the trip.
6. **Observer** responds to itinerary changes and triggers relevant updates.

---

## 4. Team Responsibilities

| Team Member | Assigned Design Patterns |
|---|---|
| **Byerik Farida** | Factory, Builder, Strategy |
| **Kashtayeva Yasmina** | Facade, Decorator, Observer |

Both team members will also contribute to:

- Integration of the design patterns.
- JavaFX interface development.
- Testing and debugging.
- UML diagrams.
- Final project report.
- Project presentation and defense.

---

## 5. Planned Technologies

| Technology | Purpose |
|---|---|
| **Java** | Main programming language |
| **JavaFX** | Graphical user interface |
| **IntelliJ IDEA** | Development environment |
| **Git & GitHub** | Version control and collaboration |
| **JSON or CSV** | Local storage of tourist and route data |
| **Mock Services** | Demonstration hotel and flight data |
| **UML** | Documentation of application architecture and design patterns |

### User Interface

The application will use a **multi-step graphical interface**, inspired by modern travel-planning applications.

Planned interface elements include:

- A welcome screen.
- A progress indicator showing the current planning step.
- Destination and attraction cards.
- Clickable buttons.
- Date selection controls.
- Transportation selection controls.
- Solo/Couple/Friends/Family cards.
- Optional-service switches.
- Back and Continue navigation.
- A final itinerary page with separate sections or tabs.

The interface will be implemented in JavaFX.

---

## 6. Itinerary Scheduling

The application will generate a daily schedule using predefined estimates for:

- Attraction visit durations.
- Travel times between locations.
- Transportation choices.
- Meal breaks.
- Opening hours.

For example, a generated day might contain:

| Time | Activity | Transportation |
|---|---|---|
| 09:00–09:20 | Travel to the first attraction | Taxi |
| 09:20–10:20 | Visit Attraction A | — |
| 10:20–10:40 | Travel to Attraction B | Bus |
| 10:40–12:10 | Visit Attraction B | — |
| 12:10–12:25 | Travel to a cafe | Walking |
| 12:25–13:25 | Lunch break | — |
| 13:25–13:45 | Travel to Attraction C | Taxi |
| 13:45–15:15 | Visit Attraction C | — |

*This is an illustrative schedule, not a verified real-world route.*

The planner will aim to prevent basic scheduling conflicts, such as assigning a visit outside an attraction's opening hours.

If too many attractions are selected for the available time, the application will notify the user and request adjustments.

---

## 7. Data and Project Scope

The initial version will use a curated local dataset containing:

- Real attractions in Astana, Almaty, and Turkistan.
- Attraction descriptions and opening hours.
- Estimated visit durations and entrance fees.
- Selected transportation alternatives between supported locations.
- Sample hotel information.
- Sample flight information.
- Cafe information for optional meal recommendations.

Prices and travel times will be clearly identified as **estimates or demonstration data**.

The application will not provide live traffic conditions, real-time ticket availability, or guaranteed booking prices.

### Initial Scope Limitations

To keep the project manageable for a two-person team:

- Only three Kazakhstan destinations will be supported initially.
- Trips will be limited to 1–3 days.
- Route planning will use predefined alternatives.
- Hotel and flight suggestions will use mock services.
- No online booking or payment processing will be implemented.
- No AI-generated travel recommendations will be required.

---

## 8. Development Plan

### Phase 1 — Planning and Data Collection
- Finalize application requirements.
- Collect information about selected Kazakhstan attractions.
- Prepare sample route, transportation, hotel, flight, and cafe data.
- Design the main Java classes and UML diagrams.

### Phase 2 — Core Java Implementation
- Implement the main domain models.
- Develop Factory, Builder, and Strategy.
- Develop Facade, Decorator, and Observer.
- Integrate the patterns into one trip-planning workflow.

### Phase 3 — JavaFX Interface
- Create the welcome page.
- Implement the four planning steps.
- Implement the final itinerary page.
- Connect user interactions to the Java application logic.
- Preserve user selections when navigating between pages.

### Phase 4 — Testing and Improvements
- Test each design pattern.
- Test multiple-attraction selection.
- Test Fastest and Scenic routing.
- Test transportation choices for individual route segments.
- Test optional hotel, flight, and cafe suggestions.
- Test itinerary generation, scheduling conflicts, and cost calculations.

### Phase 5 — Documentation and Defense
- Prepare UML diagrams.
- Capture application screenshots.
- Write the final PDF report.
- Prepare the source code ZIP archive.
- Demonstrate the application and explain the six design patterns.

---

## 9. Possible Future Improvements

Potential improvements include:

- Integration with real flight and hotel APIs.
- Live public transportation schedules.
- Interactive maps.
- Real-time route calculations.
- More destinations across Kazakhstan.
- User accounts and saved trips.
- Online booking and payments.
- AI-assisted travel recommendations.

---
