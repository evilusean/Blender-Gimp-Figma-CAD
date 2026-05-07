### Summary of Internal Systems

The drone’s effectiveness stems from its simplicity. While it is often described as low-tech, the integration of these components into a reliable long-range system is a significant engineering feat:

* **Propulsion:** The **MD-550** engine is the most recognizable part of the drone. It is a four-cylinder, two-stroke engine that provides the necessary thrust for long-range flight while being cheap enough to be expendable.
    
* **Structure:** The **Delta-wing** design is inherently stable and provides a large internal volume for fuel and explosives relative to its surface area. The use of composites rather than metal helps it evade some types of radar detection.
    
* **Electronics:** The guidance system relies on **COTS (Commercial Off-The-Shelf)** electronics. By using industrial-grade components found in consumer electronics, the manufacturers bypass many military-grade export restrictions while keeping the unit price extremely low.
    
* **Guidance:** Most units do not have a "seeker" head (camera). They are pre-programmed with coordinates and use a combination of **GNSS** and **Inertial Navigation Systems (INS)** to reach the target. This makes them "fire-and-forget" weapons.

DETAILED COMPONENT SUMMARY
1. Airframe and Fuselage
The Shahed-136 utilizes a delta-wing configuration which provides high lift and stability at low speeds.

Material: The structure is predominantly composite, consisting of carbon fiber cloth, fiberglass, and a honeycomb core. This non-metallic construction reduces its Radar Cross Section (RCS), making it harder for older radar systems to track.

Modular Design: The drone is designed for easy assembly. The wings are often detachable for transport in standard shipping containers or specialized truck-mounted racks.

2. Propulsion System (The "Moped" Engine)
The heart of the drone is a Mado MD-550 engine, which is an Iranian copy of the German Limbach L550.

Mechanism: It is a horizontal-opposed four-cylinder engine. It is loud and produces a distinct acoustic signature that has led to the nickname "the flying moped."

Propeller: A two-blade wooden or composite pusher propeller is mounted at the rear.

Fuel System: Standard gasoline/petrol tank located in the center of the fuselage.

3. Guidance and Avionics
The drone's "brain" is built using largely Commercial Off-The-Shelf (COTS) components.

Satellite Navigation: It uses multi-constellation GNSS receivers (GPS, GLONASS).

Anti-Jamming: Newer iterations (Russian Geran-2 variants) feature the Kometa-M digital antenna array. This is a CRPA (Controlled Reception Pattern Antenna) that can filter out electronic warfare interference.

Inertial Navigation (INS): If GPS signal is lost, the drone relies on a MEMS-based gyroscope and accelerometer system to maintain course toward a fixed coordinate. It is not capable of "seeking" moving targets; it is a "dumb" GPS-guided missile in terms of targeting logic.

Flight Control: Simple microcontrollers manage the control surfaces (elevons) at the wing edges via commercial servos.

4. Warhead and Lethality
The nose section contains the payload.

Explosive Type: Usually a high-explosive fragmentation (HE-FRAG) warhead.

Fuze: Impact-based fuzing system with a backup electrical trigger.

Optics (Rare): Most Shahed-136s have no cameras (to keep costs low). However, some specialized versions have been seen with gimbaled cameras for man-in-the-loop terminal guidance.

CAD AND REVERSE ENGINEERING RESOURCES
Because this is military hardware, "official" CAD files do not exist in the public domain. However, due to its impact on modern warfare, several organizations and hobbyists have created highly accurate reconstructions:

Conflict Armament Research (CAR): They provide the most detailed "parts lists" and internal diagrams. While not CAD files, their reports provide the exact dimensions and component serial numbers needed to build an accurate model.

GrabCAD: This is the primary source for 3D models. Search for "Shahed 136" or "Geran-2." Note that these are user-generated and may vary in precision. Look for models uploaded by accounts specializing in defense or aerospace modeling.

Sketchfab: Often hosts 3D scans or photogrammetry models of downed drones. These are excellent for studying the external geometry and battle-damage assessment.

Defense Analysis Portals: Sites like Oryx or The Drive: War Zone often feature high-resolution internal photos from Ukrainian intelligence teardowns, which serve as the primary reference for anyone attempting to recreate the internal CAD assembly.

WHY IT RESHAPES WARFARE
The Shahed is significant not because of its tech, but because of its economics. It forces an adversary to use a $1 million surface-to-air missile to intercept a $20,000 drone. This "asymmetric attrition" is the core principle of its strategic utility.

## Navigation Systems :
### Drone Navigation & Learning Path Summary

#### Navigation Systems Architecture
* **GNSS (Global Navigation Satellite System):** Uses multi-constellation receivers (GPS, GLONASS) to calculate 3D positioning via satellite signal time-of-flight[cite: 1].
* **CRPA (Controlled Reception Pattern Antenna):** Utilizing arrays like the "Kometa-M," these systems use spatial filtering to ignore electronic warfare interference and focus on valid satellite signals[cite: 1].
* **INS (Inertial Navigation System):** A self-contained "dead reckoning" system using MEMS gyroscopes and accelerometers to estimate position based on movement when GPS is unavailable[cite: 1].
* **Flight Control Logic:** Onboard microcontrollers process sensor data to drive servos, which adjust the physical control surfaces (elevons) to maintain a programmed flight path[cite: 1].

---

#### Recommended Learning Roadmap

| Domain | Key Concepts to Master |
| :--- | :--- |
| **Mathematics** | Linear Algebra (coordinate transforms), Calculus (rate of change), Trigonometry (unit circle/vectoring). |
| **Physics** | Aerodynamics (lift/drag/thrust), Classical Mechanics (inertia, torque, and angular momentum). |
| **Programming** | C/C++ for real-time systems, Python for data analysis/prototyping, and Linux (Arch/CLI) for development environments. |
| **Control Systems** | PID (Proportional-Integral-Derivative) loops and Sensor Fusion (Kalman Filters) to merge GNSS and INS data. |
| **Embedded Hardware** | Communication protocols (UART, I2C, SPI) and working with STM32 or Pixhawk-based flight controllers. |
| **RF & Signals** | Software Defined Radio (SDR), GNSS signal structures (L1/L2 bands), and signal jamming/spoofing theory. |

---

#### Practical Study Resources
* **Open Source Stacks:** Study the **ArduPilot** or **PX4** firmware codebases to see professional-grade navigation implementation.
* **Simulators:** Use **Gazebo** or **AirSim** to test flight code in a physics-accurate virtual environment without hardware risk.
* **Field Reports:** Monitor **Conflict Armament Research (CAR)** for technical teardowns of hardware found in modern attrition warfare[cite: 1].
