Perfect! Here's the **enhanced and complete detailed game description** for **Attack on Titan: Utopia**, now emphasizing the **Object-Oriented Programming (OOP) architecture** and **JavaFX-based GUI**:

---

# 🛡️ Attack on Titan: Utopia – Game Description

## 🎮 Game Concept

**Attack on Titan: Utopia** is a **2D, single-player, endless tower defense game** built entirely in **Java** using **Object-Oriented Programming (OOP) principles** and a fully interactive **JavaFX graphical user interface**. The game is inspired by the hit anime *Attack on Titan* and places the player in command of the defense of the **Utopia District**, humanity’s final northern outpost of **Wall Rose**, as it faces an unstoppable horde of titans.

The gameplay emphasizes **modular design**, **object-based entity management**, and **scalable UI**, all while delivering fast-paced, tactical tower defense action.

---

## 🧱 Game Setting

Set in an alternate storyline where the **titans breach Wall Maria** and overrun most of the territory, they now push forward toward **Wall Rose**. The **Utopia District**, located at the northern border, becomes the battlefield. As commander, your job is to deploy **anti-titan weapons** to hold the line and prevent complete human extinction.

---

## 🗺️ Battlefield Design

The battlefield is divided into **multiple horizontal lanes**, each with:

1. **Wall Segment (Defensive Base)**

   * Has its own **HP (Health Points)**.
   * If a segment's HP reaches 0, that **lane is lost** and titans will stop being attacked there.

2. **Titans Marching In**

   * Titans advance toward the wall based on their **speed and type**.
   * Each titan has **HP**, **damage**, and **distance from the wall** (custom distance units).

3. **Player-Deployed Weapons**

   * Strategically placed by the player in active lanes.
   * Use **OOP-based polymorphic behavior** for weapon actions (attack types, range, etc.).

Each lane also computes a **danger level** based on the type and number of incoming titans, helping players make quick strategic choices.

---

## 🧨 Game Mechanics

* **Endless Gameplay**:
  No winning condition – your goal is to survive as long as possible and achieve the highest score before all wall segments fall.

* **Turn-Based Waves**:
  Titans move and attack in phases. After each turn, more titans approach and weapons attack them if within range.

* **Battle Phases**:
  The game intensifies over time through three distinct phases:

  1. **Early Phase** – manageable threats
  2. **Intense Phase** – faster titans, higher danger levels
  3. **Grumbling Phase** – massive, high-HP titans like the **Colossal Titan**

---

## 💀 Titans

Each titan is implemented as a distinct **Titan subclass** extending a common **Titan superclass**, each with shared and unique traits:

| Type           | HP   | Damage | Speed | Resource Drop | Danger Level | Special Trait                       |
| -------------- | ---- | ------ | ----- | ------------- | ------------ | ----------------------------------- |
| Pure Titan     | 100  | 15     | 10    | 10            | 1            | —                                   |
| Abnormal Titan | 100  | 20     | 15    | 15            | 2            | Attacks **twice per turn**          |
| Armored Titan  | 200  | 85     | 10    | 30            | 3            | Takes only **25% damage**           |
| Colossal Titan | 1000 | 100    | 5     | 60            | 4+           | **Speed increases** after each move |

---

## 🧰 Weapons & Deployment

The player can view and deploy weapons using a **JavaFX-based control panel**, selecting from a variety of anti-titan weapons, each with its own class and behavior:

* **Cannon**: Deals splash damage.
* **Sniper Tower**: High-damage, low fire rate.
* **Flamethrower**: Area-of-effect weapon.
* **Electro-Net**: Slows titans.

Each weapon inherits from a common `Weapon` abstract class and overrides attack logic via polymorphism.

---

## 🖥️ GUI – Built with JavaFX

The game interface is developed entirely in **JavaFX**, featuring:

* **Interactive Lane View**:
  Displays titans, weapons, wall HP, and distances in each lane in real-time.

* **Side Panel UI**:
  Shows:

  * Resources
  * Score
  * Available weapons
  * Approaching titans
  * Deployment options (drag & drop or button-select)

* **Status Indicators**:
  Visual warnings for high-danger lanes, low wall HP, and phase transitions.

* **Responsive Layout**:
  The interface scales and updates dynamically based on user actions and titan behavior using JavaFX’s animation and event-handling systems.

---

## 🧠 Object-Oriented Design Highlights

* **Class Hierarchy**:

  * `Titan` (base class) → `PureTitan`, `AbnormalTitan`, etc.
  * `Weapon` (abstract class) → `Cannon`, `Flamethrower`, etc.
  * `Lane`, `Wall`, `GameEngine`, and `Player` are modular entities.

* **Encapsulation & Modularity**:
  Each component (UI, titans, weapons, walls) is separated into cohesive classes for scalability and clarity.

* **Polymorphism**:
  Weapons and titans override common behaviors using polymorphic attack and movement logic.

* **Clean Codebase**:
  The architecture allows easy expansion for future features (new titan types, abilities, multiplayer support, etc.).

---

## 🏁 Victory Conditions

This is an **endless survival game**. You win by:

* Lasting as long as possible
* Strategically holding more lanes
* Defeating high-value titans (e.g., Colossal Titan)
* Achieving a high score

---

You can start playing once you launch it on eclipse.
