<p align="center"><img src="https://raw.githubusercontent.com/headspeed/headspeed/main/docs/src/media/banner.png" alt="Headspeed: rotorcraft flight physics, checked against real flight logs" width="100%"></p>

**Headspeed** is an open-source, deterministic physics engine for RC rotorcraft, written in
Rust: 380–760 class collective-pitch helicopters and a 5-inch FPV quad. It runs headless and
bit-identically on every platform, and every fidelity claim is backed by a test.

<p align="center"><img src="https://raw.githubusercontent.com/headspeed/headspeed/main/docs/src/media/flight.jpg" alt="The reference 700 hovering over the field in the Godot frontend" width="100%"></p>

### What is in it

- **Rotor physics:** blade-element rotors with flapping and lagging blades, dynamic inflow,
  vortex ring state, ground effect, measured airfoil data and dynamic stall.
- **The real flight controllers:** Rotorflight 2's control law and governor, and Betaflight's,
  in Configurator numbers; or Rotorflight and Betaflight's own SITL firmware flying it.
- **Real hardware:** a catalogue of real parts with cited specs (blades, motors, ESCs, packs,
  servos, flybarless units, radio links), servo dynamics, receiver latency and IMU noise.
- **Logs:** replay Rotorflight and Betaflight blackbox logs against the engine, and fit
  parameters to them.
- **A simulator to fly it:** a Godot frontend with your own transmitter, training drills,
  a Hangar, flight replay, crashes that break things, and English and Thai.
- **Elsewhere:** ArduPilot SITL, a C ABI and Python with Gymnasium.

| | |
|---|---|
| ![The Hangar](https://raw.githubusercontent.com/headspeed/headspeed/main/docs/src/media/blades.jpg) | ![Replay](https://raw.githubusercontent.com/headspeed/headspeed/main/docs/src/media/replay.jpg) |
| **Hangar:** real parts drawn from their published numbers | **Replay:** a blackbox log against the engine |

### Start here

- **Repository:** [headspeed/headspeed](https://github.com/headspeed/headspeed)
- **Documentation:** [headspeed.github.io/headspeed](https://headspeed.github.io/headspeed/), with
  [getting started](https://headspeed.github.io/headspeed/guide/getting-started.html) and the
  [Godot frontend](https://headspeed.github.io/headspeed/guide/godot.html)
- **Status:** alpha. Against a real Raptor E720 flight log, the generic 700's hover power is
  within 0.7% and the logged rates replay at a median correlation of 0.95–0.98. We are
  looking for more logs, ones that can be published, to validate in CI. See
  [Validation](https://headspeed.github.io/headspeed/guide/validation.html) if you can share one.

Code: MIT or Apache-2.0, at your option. Vehicle models and data: CC-BY-4.0.
