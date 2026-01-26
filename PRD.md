# Hardware Product Requirements Document

> NewNorth Routing Compass — Hardware PRD

| Metadata        | Details                    |
| --------------- | -------------------------- |
| Author          | Camden Montgomery          |
| Product Manager | Camden Montgomery          |
| Lead Engineer   | Camden Montgomery          |
| Designer        | Camden Montgomery          |
| QA / Test Lead  | Camden Montgomery          |
| Last Updated    | 2026-01-26                 |
| Version         | v2.0                       |

---

## Introduction

This Hardware Product Requirements Document (PRD) defines the scope, goals, functional and non-functional requirements, constraints, and staged release plan for the **hardware component** of the NewNorth Routing Compass. Its purpose is to provide a single source of truth for stakeholders and engineering teams responsible for the physical device, guiding design and development decisions, ensuring traceability of hardware requirements, and aligning priorities across MVP, V1, and V2 hardware releases.

> Note: Software/mobile app functionality is referenced only to the extent it interacts with the hardware. A separate PRD will define the mobile app in detail.

---

## 1. Product Overview

The NewNorth hardware is a **wrist-mounted compass device** that points directly toward user-defined locations. Its core function is **direct pointing to destinations** with a visible compass needle. The hardware will eventually support expanded navigation behaviors such as **turn-by-turn guidance** in V2 via software updates, but early versions focus on single and multi-location pointing.

The device operates **independently of a phone during active use**, combining durability, simplicity, and tactile feedback to create an intentional navigation experience.

---

## 2. Problem Statement

Smartphone-based navigation encourages constant screen engagement and reduces environmental awareness during walking and exploration. Existing alternatives are either fully digital or purely decorative, offering little middle ground between usability and intentional disconnection.

The NewNorth hardware provides a **single-purpose, standalone navigation device** that supports orientation and wayfinding while maintaining the tactile, focused experience of a traditional compass.

---

## 3. Goals

* Enable users to orient themselves toward meaningful locations without using a phone screen during use
* Provide a durable, wrist-mounted navigation tool that feels intentional and reliable
* Deliver a hardware experience that scales from MVP to full-featured V2 while maintaining focus and usability

---

## 3.5 Product Scope & Release Definition

### Minimum Viable Product (MVP)

**Objective:** Validate the core value proposition: a standalone device that reliably points toward a single predefined location.

**Included Capabilities:**

* Wrist-mounted device pointing toward one configured destination
* Visible, continuously spinning compass needle
* Bluetooth connectivity with a mobile application for initial configuration
* Mobile app functionality limited to setting/updating destination
* Internal rechargeable battery
* USB-C charging

**Explicitly Excluded:**

* Rotating bezel or multiple location selection
* Advanced interaction modes beyond direct pointing
* Turn-by-turn navigation

### Version 1 (V1)

**Objective:** Deliver a sellable product supporting intentional, screen-free navigation toward multiple meaningful locations.

**Included Capabilities:**

* All MVP capabilities
* Support for multiple user-defined locations
* Rotating bezel to switch between locations
* Abstract, non-textual labels for location selection
* Improved durability and wearability

### Version 2 (V2)

**Objective:** Expand navigation flexibility and experiential depth while preserving single-purpose, low-distraction philosophy.

**Included Capabilities:**

* All V1 capabilities
* Turn-by-turn or advanced navigation behaviors (software-enabled updates)
* Battery life optimizations and efficiency improvements

---

## 4. Non-Goals

The following capabilities are explicitly excluded and should not appear in any version unless future requirements redefine them:

* Continuous phone dependency during active use
* Visual map display
* Spoken or audio guidance

---

## 5. Target Users

### 5.1 Primary Users

* Pedestrians enjoying walking, exploration, and orientation-based navigation
* Users seeking reduced phone interaction during outdoor activities
* Individuals drawn to novelty tools with real-world function

### 5.2 Usage Context

* Urban and suburban walking environments
* Short to moderate walking sessions
* Casual, intentional exploration rather than optimized travel

---

## 6. Core Use Cases

Use cases are described as detailed **user scenarios** for the hardware:

1. **Single Location Navigation**
   A user selects a location via the mobile app. While walking, they glance at the compass needle, which continuously points toward the selected destination. The device remains fully usable without interacting with the phone.

2. **Multi-Location Navigation (V1+)**
   A user predefines multiple locations in the mobile app. They use the bezel to switch between destinations during a walk, with the needle immediately updating to point to the selected location. The device maintains accurate directional feedback without phone interaction.

3. **Wrist Fit and Wearability**
   A user adjusts the strap to their wrist size (140–210mm). The device remains secure and comfortable during walking, with no shifting or rotation affecting needle accuracy.

4. **Battery and Charging**
   A user charges the device using the USB-C port. During normal use, the device operates for a minimum of 3 hours without losing accuracy or responsiveness.

---

## 7. Functional Requirements

| Req ID   | Requirement                                                       | Applies To | Notes                               |
| -------- | ----------------------------------------------------------------- | ---------- | ----------------------------------- |
| REQ-001  | Device shall point toward a configured location                   | MVP        | Single destination in MVP           |
| REQ-002  | Device shall provide continuous directional feedback              | MVP        | Needle spins continuously           |
| REQ-003  | Device shall operate without requiring an active phone            | All        | Applies to all versions             |
| REQ-004  | Device shall support multiple user-defined locations              | V1         | Rotating bezel required             |
| REQ-005  | Device shall allow bezel to switch active location                | V1         | Abstract, non-textual labels        |
| REQ-006  | Device shall connect to mobile app via Bluetooth                  | MVP        | For initial configuration           |
| REQ-007  | Mobile app shall allow defining/updating locations                | MVP        | Configuration only                  |
| REQ-008  | Device shall retain configuration data locally                    | MVP        | Internal storage                    |
| REQ-009  | Device shall be wrist-mounted and wearable                        | MVP        | Watch-style band                    |
| REQ-009A | Device shall accommodate wrist circumferences from 140mm to 210mm | MVP        | Adjustable strap required           |
| REQ-009B | Device shall securely fasten to the wrist during normal use       | MVP        | Ensure stability without discomfort |
| REQ-010  | Compass needle shall indicate heading within ±5°                  | MVP        | Accuracy standard                   |
| REQ-011  | Device shall support minimum 3h active use                        | MVP        | Battery life target                 |
| REQ-012  | Device shall include rechargeable battery                         | MVP        | USB-C charging                      |
| REQ-013  | Device shall be durable against drops                             | MVP        | Enclosure and glass integrity       |
| REQ-014  | Device shall present compass-inspired aesthetic                   | MVP        | No screens or modern UI elements    |
| REQ-015  | Device shall support turn-by-turn navigation                      | V2         | Software-enabled feature, optional  |
| REQ-016  | Device shall allow software-enabled updates                       | V2         | For V2 expansion                    |
| REQ-017  | Battery life optimizations for longer use                         | V2         | Efficiency improvements             |

---

## 8. Non-Functional Requirements

| Requirement                          | Applies To | Notes              |
| ------------------------------------ | ---------- | ------------------ |
| Accuracy ±5°                         | MVP        | REQ-010            |
| Minimum 3h battery life              | MVP        | REQ-011            |
| Durable enclosure and glass          | MVP        | REQ-013            |
| Rechargeable battery, USB-C charging | MVP        | REQ-012            |
| Retail cost below $150 USD           | MVP        | Budget constraint  |
| Wrist fit and comfort                | MVP        | REQ-009A, REQ-009B |

---

## 9. Physical and Design Constraints

| Constraint                                      | Applies To | Notes    |
| ----------------------------------------------- | ---------- | -------- |
| Visible compass needle                          | MVP        | REQ-002  |
| Durable glass enclosure with cylindrical form   | MVP        | REQ-013  |
| Rotating bezel for multi-location selection     | V1+        | REQ-005  |
| Adjustable wrist strap for 140–210mm            | MVP        | REQ-009A |
| Secure fasten during activity                   | MVP        | REQ-009B |
| Rustic, compass-inspired aesthetic              | MVP        | REQ-014  |
| No screens, audio output, or modern UI elements | MVP        | REQ-014  |

---

## 10. Success Criteria

* Accuracy and reliability of point-to-location guidance
* User willingness to use device without a phone
* Perceived durability and quality
* Ability to deliver product within defined cost constraints

---

## 11. Traceability Matrix

| Requirement | Product Goal            | Functional Block     | Verification                              |
| ----------- | ----------------------- | -------------------- | ----------------------------------------- |
| REQ-001     | Orient toward location  | Navigation subsystem | Functional test: single location pointing |
| REQ-002     | Continuous feedback     | Needle actuation     | Observation during use                    |
| REQ-003     | Phone-free operation    | Firmware             | Test without phone connected              |
| REQ-004     | Multi-location          | Navigation + bezel   | User test with multiple destinations      |
| REQ-005     | Switch locations        | Bezel mechanism      | Physical interaction test                 |
| REQ-006     | Mobile config           | Bluetooth module     | Connection test with app                  |
| REQ-007     | Define locations        | App                  | Test adding/updating location             |
| REQ-008     | Local storage           | MCU memory           | Data persistence test                     |
| REQ-010     | Accuracy ±5°            | Needle + sensor      | Lab compass calibration test              |
| REQ-011     | Battery life            | Power subsystem      | Runtime test                              |
| REQ-012     | Rechargeable battery    | Power subsystem      | Charging test                             |
| REQ-013     | Durability              | Enclosure            | Drop test                                 |
| REQ-015     | Turn-by-turn navigation | Firmware + software  | Simulation test                           |

---

*This Hardware PRD defines the scope, intent, staged delivery plan, and traceability for the physical NewNorth Routing Compass device across multiple releases.*
