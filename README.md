# VTOL Simulation

Goals of this repository:
* Containerized instances of Gazebo & PX4 Autopilot
* URDF models for VTOL vehicles
* Various scenarios (detect-and-avoid, windy, emergency landing, parcel delivery)
* SITL simulations
* Eventual HITL simulations with flight computer testbed, simulated sensor readings
* Test platform for AI controls

## Mission Roadmap

### Basic

* [ ] Quadcopter model in Gazebo simulation (Dockerized)
    * [ ] GUI window on host
* [ ] PX4 Autopilot (Dockerized)
* [ ] Software adaptors for PX4 Autopilot
  * [ ] Gazebo simulation sensor data
  * [ ] Motor commands translated to motion in simulation
* [ ] Rise and fall scenario
    * [ ] Ascend N meters, hover, spin 360 in place, descend

### GPS Follow

* [ ] [PX4 Mission Mode](https://docs.px4.io/main/en/flight_modes_mc/mission.html)
  * [ ] [Takeoff](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_VTOL_TAKEOFF)
  * [ ] [GPS Follow](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_SPLINE_WAYPOINT)
  * [ ] [Land](https://mavlink.io/en/messages/common.html#MAV_CMD_NAV_VTOL_LAND)

### Parcel Acquire

* [ ] Software adaptor to feed relative parcel location to drone
    * Eventually to be done with computer vision, monocular or stereo, and NN
* [ ] Gripper added to URDF
    * Mechanism design unimportant, package will attach automatically in simulation
* [ ] [PX4 Parcel Delivery Mission](https://docs.px4.io/main/en/flying/package_delivery_mission.html)

### TBD

* Windy
* Other drones
* Foggy
