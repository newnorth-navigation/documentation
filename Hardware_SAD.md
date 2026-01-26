# Hardware System Architecture Document (SAD)
> NewNorth Routing Compass — Hardware SAD

| Metadata        | Details                    |
| --------------- | -------------------------- |
| Author          | Camden Montgomery          |
| Product Manager | Camden Montgomery          |
| Lead Engineer   | Camden Montgomery          |
| Designer        | Camden Montgomery          |
| QA / Test Lead  | Camden Montgomery          |
| Last Updated    | 2026-01-26                 |
| Version         | v1.0                       |

---
## 1. Purpose and Scope

This document defines the **system-level architecture** for the product, focusing exclusively on the **hardware–software system structure** required to support navigation functionality across MVP, V1, and a forward-looking V2.

The document describes the **target architectural end state** and the constraints that apply to all versions. Feature feasibility beyond V1 is treated as aspirational and non-binding.

---

## 2. System Overview

The system is a compact, wrist-mounted, standalone navigation device designed to:

* Determine geographic position
* Interpret navigation intent
* Communicate directional guidance through a constrained, non-screen interface

The system is composed of the following subsystems:

* Compute & Control
* Positioning (GNSS)
* Orientation & Motion Sensing
* User Interface
* Power Management
* Communications
* Firmware / Software Stack

---

## 3. Subsystem Architecture

### 3.1 Compute & Control

Responsible for:

* Coordinating all subsystems
* Executing navigation-related logic
* Managing power states

**Architectural Assumption:**

* MCU-class processor
* Real-time, event-driven execution model

The architecture must allow for increased computational load in future versions without requiring a fundamental redesign.

---

### 3.2 Positioning (GNSS)

Responsible for:

* Acquiring latitude and longitude
* Providing speed and heading where available

**Constraints:**

* Limited antenna size
* Power-intensive operation

The system architecture assumes GNSS as the primary source of absolute position.

---

### 3.3 Orientation & Motion Sensing

Responsible for:

* Determining device heading
* Supporting directional guidance accuracy

**Architectural Role:**
Orientation data is a first-class input to navigation behavior and UI output.

---

### 3.4 User Interface

Responsible for:

* Communicating directional guidance
* Providing minimal user input

**Architectural Constraint:**

* No screen-based UI

The architecture supports:

* A primary physical directional indicator
* Optional secondary indicators (e.g., haptic or LED)

---

### 3.5 Power Management

Responsible for:

* Energy storage
* Power regulation
* Sleep and wake coordination

**Architectural Requirements:**

* Multiple power states
* Subsystem-level power gating

The system must support extended navigation use within wearable thermal and size constraints.

---

### 3.6 Communications

Responsible for:

* External data exchange
* Configuration and updates

**Architectural Requirement:**

* Communications capability is mandatory

The architecture allows navigation computation to be either fully on-device or partially external.

---

### 3.7 Firmware / Software Stack

Responsible for:

* Hardware abstraction
* Navigation behavior implementation
* UI control logic

**Architectural Principle:**
Navigation logic must be modular and replaceable without hardware changes.

---

## 4. System Data Flow

1. GNSS and orientation data are acquired
2. Navigation intent is derived
3. Directional output is generated
4. UI elements convey guidance
5. Power state is adjusted dynamically

---

## 5. Version Capability Boundaries

### MVP

* Absolute positioning
* Simple bearing-based guidance
* External configuration via communications

### V1

* Waypoint or route segment support
* Improved guidance resolution
* Refined power behavior

### V2 (Target Intent)

* Turn- or event-based guidance
* Increased autonomy from external systems

V2 capabilities are **architectural targets**, not commitments.

---

## 6. Architectural Constraints

The following constraints apply to all versions:

* Wearable form factor
* No visual display
* Limited power and thermal budget
* Hardware must not preclude future navigation complexity

---

## 7. Document Boundaries

This document:

* Defines system structure and responsibilities
* Establishes constraints and invariants

This document does not:

* Specify detailed algorithms
* Define component-level designs
* Guarantee feasibility of future features
