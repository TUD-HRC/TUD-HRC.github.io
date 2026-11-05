<img src="assets/OPEN_reg.png" alt="TU Delft logo" width="300">

# Human Robot Collaboration — Lab Wiki

**TU Delft · Department of Cognitive Robotics (CoR) · Faculty of Mechanical Engineering**

Welcome to the **Human Robot Collaboration group** at TU Delft. This wiki is a hardware and software tutorial for new students joining the group. It covers the KUKA 7 and KUKA 14 robot arms, the KMR mobile platform, the Bota force sensor, and the lab's Cartesian impedance controller.

Follow the onboarding path before running your first experiment. All code and tutorials target **Ubuntu 24.04 LTS and ROS 2 Jazzy**.

Learn more about the department on the [TU Delft Cognitive Robotics (CoR) website](https://www.tudelft.nl/me/over/afdelingen/cognitive-robotics-cor).

> **Draft:** `[TODO]` marks information to be filled in and checked by the lab. Hardware operation requires the lab's approved training and procedures.

## Quick links

| Resource | Location |
| --- | --- |
| Department website | [Cognitive Robotics (CoR), TU Delft](https://www.tudelft.nl/me/over/afdelingen/cognitive-robotics-cor) |
| Main GitHub repository | [TODO: repository URL] |
| Cartesian impedance controller | [TODO: repository or package URL] |
| Lab safety and operating procedures | [TODO: link] |
| Booking system | [TODO: link] |
| Technical contact | [TODO: name / contact] |

## 1. Start here

New students should work through these steps with an experienced lab member.

- [ ] Complete lab access and robot safety training.
- [ ] Identify the emergency stops and learn the approved stop and recovery procedures.
- [ ] Read the hardware overview below.
- [ ] Set up the software environment.
- [ ] Build and run the simulation or offline example, if available.
- [ ] Observe a supervised hardware session.
- [ ] Complete the supervised first experiment.
- [ ] Learn how to save data and shut down the system.

## 2. Hardware overview

| Equipment | Role | Details to document |
| --- | --- | --- |
| KUKA 7 | Robot arm; uses the lab's Cartesian impedance controller | Exact model, controller cabinet, mounting, tools |
| KUKA 14 | Robot arm; uses the lab's Cartesian impedance controller | Exact model, controller cabinet, mounting, tools |
| KMR | Mobile robot platform | Exact model, onboard hardware, navigation software |
| Bota force sensor | Force/torque measurement | Exact model, interface, mounting, calibration |

### KUKA 7 and KUKA 14

Document each robot separately where the setup differs.

- **Identification:** [TODO: model, asset label, location]
- **Controller and interface:** [TODO: cabinet, firmware, communication interface]
- **Wiring:** [TODO: labeled photo and connection diagram]
- **Network:** [TODO: robot IP, workstation IP, subnet, network port]
- **End effector:** [TODO: tool, mounting adapter, payload and center of mass configuration]
- **Coordinate frames:** [TODO: base frame, flange frame, tool frame, axis diagram]
- **Approved operating limits:** [TODO: link to robot-specific configuration and procedure]
- **Startup / shutdown / recovery:** [TODO: links to approved step-by-step procedures]

### KMR

- **Identification and intended use:** [TODO]
- **Charging and battery checks:** [TODO]
- **Network and workstation connection:** [TODO]
- **Operating area and map:** [TODO]
- **Localization and navigation:** [TODO: software, launch procedure, required checks]
- **Startup / shutdown / recovery:** [TODO: approved procedures]
- **Relationship to other platforms:** [TODO: whether an arm or sensor is mounted on the KMR]

### Bota force sensor

- **Model and mounting:** [TODO: include a photo showing sensor axes]
- **Connection:** [TODO: interface, cables, power requirements]
- **Driver and configuration:** [TODO: package, version, configuration file]
- **Data interface:** [TODO: topic/API, message type, rate, units, frame]
- **Bias / zeroing:** [TODO: approved procedure and required loading condition]
- **Validation:** [TODO: expected readings and a simple approved check]
- **Calibration information:** [TODO: location and date]

## 3. Software environment

All lab code, examples, and tutorials must run on **Ubuntu 24.04 LTS (Noble Numbat)** with **ROS 2 Jazzy Jalisco**. Use this environment for development and for verifying the instructions below.

Official resources:

- [Ubuntu 24.04 LTS download](https://releases.ubuntu.com/24.04/)
- [ROS 2 Jazzy documentation](https://docs.ros.org/en/jazzy/)
- [ROS 2 Jazzy installation on Ubuntu 24.04 (Debian packages)](https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html)

| Component | Lab-supported configuration |
| --- | --- |
| Operating system | [Ubuntu 24.04 LTS (Noble Numbat)](https://releases.ubuntu.com/24.04/) |
| ROS distribution | [ROS 2 Jazzy Jalisco](https://docs.ros.org/en/jazzy/) |
| Main repository and tested commit/tag | [TODO] |
| Robot driver / communication interface | [TODO] |
| Cartesian impedance controller package | [TODO] |
| Bota sensor driver | [TODO] |
| KMR software | [TODO] |
| Simulation environment, if available | [TODO] |

### Installation

1. Request access to the required repositories.
2. Install [Ubuntu 24.04 LTS](https://releases.ubuntu.com/24.04/), then follow the [official ROS 2 Jazzy installation guide](https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html) and install the project dependencies.
3. Clone the repositories at the documented versions.
4. Build the workspace and load the environment.
5. Select the configuration for the intended robot.
6. Run the offline or simulation verification.

**Commands:** [TODO: insert commands tested on a clean Ubuntu 24.04 LTS workstation with ROS 2 Jazzy.]

**Expected result:** [TODO: successful build output and verification result.]

**Configuration locations:** [TODO: robot addresses, frames, tool properties, controller gains, sensor settings.]

Keep credentials out of this wiki and the repository.

## 4. Cartesian impedance controller

The lab uses a Cartesian impedance controller for the KUKA robots.

### Before using it

- **Source and entry point:** [TODO: repository, package, launch file]
- **Robot-specific configurations:** [TODO: KUKA 7 and KUKA 14 files]
- **Required robot state / operating mode:** [TODO]
- **Reference pose and frame convention:** [TODO]
- **Stiffness and damping:** [TODO: parameters, units, approved initial values]
- **Redundancy / null-space behavior:** [TODO: describe if implemented]
- **Command and state interfaces:** [TODO: topics, services, actions, or other API]
- **External force input:** [TODO: explain whether and how Bota measurements are used]
- **Command loss and stop behavior:** [TODO: verified behavior and approved operator action]

### First controller example

[TODO: add one minimal, tested example after reviewing the controller repository.]

Include:
1. The required hardware and software state.
2. The exact configuration and launch commands.
3. How the initial reference is established.
4. One approved small motion or interaction task.
5. The expected observed behavior.
6. How to stop and shut down.

## 5. First supervised experiment

**Goal:** Verify the selected robot, controller, and any sensor needed for the experiment.

| Stage | Procedure to add | Success criterion to add |
| --- | --- | --- |
| Prepare | Booking, workspace, mounting, cable and tool checks | [TODO] |
| Connect | Start the approved interfaces and verify communication | [TODO] |
| Inspect state | Check robot state, coordinate frames, and sensor readings | [TODO] |
| Enable controller | Use the approved initial configuration | [TODO] |
| Run example | Execute the lab-approved introductory task | [TODO] |
| Record | Save configuration, software versions, and experiment data | [TODO] |
| Finish | Stop, shut down, and leave the setup ready for the next user | [TODO] |

**Example dataset and expected plots:** [TODO: link]

## 6. Troubleshooting

Add solutions only after they have been verified on the relevant setup.

| Symptom | Checks / verified solution |
| --- | --- |
| Robot communication unavailable | [TODO] |
| Controller does not start | [TODO] |
| Robot state or frames look incorrect | [TODO] |
| Bota data unavailable or unexpected | [TODO] |
| KMR localization or navigation unavailable | [TODO] |
| Build or dependency failure | [TODO] |

When reporting a problem, include the platform, software commit, configuration, reproduction steps, and relevant logs. For unexpected hardware behavior, follow the lab's stop procedure and contact the responsible person before resuming.

## 7. Maintaining this wiki

- Update instructions when hardware, configurations, or software versions change.
- Link to configuration files in GitHub instead of duplicating values here.
- Record which setup was used to verify a procedure.
- Add photos for connectors, switches, mounting, and coordinate frames.

**Maintainer:** [TODO]  
**Last verified:** [TODO: date, platform, software version]

## Suggested future pages

Start with this single page; split it as the tutorials become detailed.

- Getting Started
- Safety and Lab Procedures
- KUKA 7
- KUKA 14
- KMR
- Bota Force Sensor
- Software Installation
- Cartesian Impedance Controller
- First Experiment
- Troubleshooting

