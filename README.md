
## Inspiration

During my daily summer commute on the NJ Transit Rail, I noticed a significant issue: if you close the app after checking Schedules or DepartureVision and then board your train, it becomes challenging to access current trip updates. This caused problems for me and fellow commuters. Many passengers would either take quick naps or be unfamiliar with the route, leading them to repeatedly ask other riders about the next stop or their final station.

## What it does

TripMate Notifier lets a rider start an alert on a trip, then surfaces a live, detailed status of the current journey directly in a notification panel/widget — so you always know your next stop and final destination without having to keep the app open or stay alert the whole ride.

## How i built it

We started by analyzing the problem using NJ Transit datasets and outlining potential solutions. From there, we designed the UI components using JavaFX, then built out the backend logic in Java to drive trip state, station sequencing, and alerts. We used Git to collaborate and track changes throughout development.

**Tech stack:**
- Java
- JavaFX (UI + FXML-based views)
- NJ Transit data

## Challenges we ran into

Our biggest challenge was analyzing and cleaning the NJ Transit data to extract meaningful, usable information — raw transit data isn't built for "what's my next stop right now" use cases, so transforming it into something the app could reliably track took real effort.

## What we learned

We learned different approaches to solving real-world problems using data, and how much data analysis matters for innovation in any field — a clean dataset and the right model of the problem made the difference between a clunky prototype and something that actually felt useful on a commute.

## Getting Started

### Prerequisites
- JDK 24 or later
- [JavaFX SDK](https://gluonhq.com/products/javafx/) **matching your machine's architecture** — Apple Silicon Macs need the **aarch64** build, Intel Macs/PCs need **x64**. Mixing these up causes runtime graphics errors.

### Setup
1. Clone the repo
2. Download the JavaFX SDK for your platform and note its `lib` folder path
3. Update `.classpath` and `.vscode/launch.json` to point at your local JavaFX `lib` path
4. Build and run `TransitPanel.app.Transit`

### Running from the terminal
```bash
java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml,javafx.graphics -cp bin TransitPanel.app.Transit
```

## Team

Krish Patel

