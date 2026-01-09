# Product Requirements Document

> NewNorth Routing Compass — V1

| Metadata        | Details              |
| --------------- | -------------------- |
| Author          | Camden Montgomery    |
| Product Manager | Camden Montgomery    |
| Lead Engineer   | Camden Montgomery    |
| Designer        | Camden Montgomery    |
| QA / Test Lead  | Camden Montgomery    |
| Last Updated    | 2026-01-14           |
| Version         | v1.0 (V1 Definition) |

---

## 1. Product Overview

NewNorth is a **wrist-mounted compass device** whose primary purpose is to **point directly toward user-defined locations**, rather than simply indicating magnetic north. It is designed to function as a modern interpretation of a traditional compass, combining novelty, durability, and purposeful utility.

This V1 focuses on **direct-to-location pointing only** and intentionally excludes map-based routing or turn-by-turn navigation.

---

## 2. Problem Statement

Smartphone-based navigation encourages constant screen engagement and reduces environmental awareness during walking and exploration. Existing alternatives are either fully digital or purely decorative, offering little middle ground between usability and intentional disconnection.

There is an opportunity for a **single-purpose navigation object** that supports orientation and wayfinding while maintaining the tactile, focused experience of a traditional compass.

---

## 3. Goals

* Enable users to orient themselves toward meaningful locations without using a phone screen during use
* Provide a durable, wrist-mounted navigation tool that feels intentional and reliable
* Deliver a focused V1 experience centered on pointing accuracy and simplicity

---

## 4. Non-Goals (V1)

The following capabilities are explicitly excluded from V1:

* Visual map display
* Turn-by-turn or route-based navigation
* Spoken or audio guidance
* Continuous phone dependency during use

---

## 5. Target Users

### 5.1 Primary Users

* Pedestrians who enjoy walking, exploration, and orientation-based navigation
* Users seeking reduced phone interaction during outdoor activities
* Individuals drawn to novelty tools with real-world function

### 5.2 Usage Context

* Urban and suburban walking environments
* Short to moderate walking sessions
* Casual, intentional exploration rather than optimized travel

---

## 6. Core Use Cases

1. **Point-to-Location Navigation**
   A user selects a location and uses the device to orient themselves toward it during a walk.

2. **Multi-Location Selection**
   A user switches between preconfigured locations using the bezel to change directional context.

---

## 7. Functional Requirements

### 7.1 Core Navigation

* The device shall function as a wrist-mounted compass that points toward configured locations.
* The device shall provide continuous directional feedback toward the selected location.
* The device shall operate without requiring an active phone connection during use.

### 7.2 Location Selection

* The device shall support **six distinct location selections**.
* Each location shall be represented using **abstract, non-textual labels** on the bezel.
* The bezel shall allow the user to switch the active target location.

### 7.3 Configuration

* The device shall connect to a mobile application via Bluetooth for configuration.
* The mobile application shall allow users to:

  * Define and manage locations
  * Select operating modes (defined separately)
* The device shall retain configuration data locally.

### 7.4 Wearability

* The device shall be worn on the wrist using a watch-style band.
* The device shall be usable without buttons, screens, or exposed interactive controls.

---

## 8. Non-Functional Requirements

### 8.1 Accuracy

* The compass needle shall point toward the configured location within a **maximum error of 5 degrees** under normal operating conditions.

### 8.2 Battery Life

* The device shall support a minimum of **3 hours of active use** on a single charge.

### 8.3 Durability

* The device shall be durable enough to withstand accidental drops without functional failure.
* The enclosure and glass shall be resistant to cracking during typical use.

### 8.4 Power and Charging

* The device shall use a rechargeable internal battery.
* The device shall be rechargeable via **USB-C**.
* The device shall include appropriate electrical protections to ensure safe charging and operation.

### 8.5 Cost Constraint

* The target retail price for the product shall remain **below $150 USD**.

---

## 9. Physical and Design Constraints

* The device shall include a visible compass needle.
* The device shall use a **durable glass enclosure** with a cylindrical form factor.
* The product shall present a **rustic, compass-inspired aesthetic**.
* The rotating bezel shall be a primary interaction surface.
* No screens, audio output, or overtly modern UI elements shall be present.

---

## 10. Success Criteria (V1)

Success for V1 will be evaluated based on:

* Accuracy and reliability of point-to-location guidance
* User willingness to use the device without a phone during walks
* Perceived durability and quality
* Ability to deliver the product within the defined cost constraints

---

## 11. Open Questions and Future Considerations

* Expanded navigation behaviors beyond direct pointing
* Battery life improvements in future revisions
* Additional modes enabled through software updates

---

*This PRD defines the finalized scope and intent for the NewNorth Routing Compass V1.*
