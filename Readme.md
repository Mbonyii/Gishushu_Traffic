# Gishushu Traffic Light State Diagram

## Overview
This state diagram represents the traffic light sequence for a four-way intersection. Each directional flow (North-South, East-West, South-North, and West-East) has its own phase in the cycle, allowing vehicles from specific directions to move while others wait. This structure follows a continuous loop, transitioning smoothly between directions with green, yellow, and red light phases.

## Diagram Explanation
The state diagram is structured into four main states, each representing a directional flow at the intersection. Each directional flow has:
- **Green Light**: Vehicles can proceed.
- **Yellow Light**: Warning that the light will change to red soon.
- **Red Light**: Vehicles must stop.

The transitions between each directional flow are controlled by timed events, ensuring each flow completes its green, yellow, and red phases before moving to the next.

## State Flow
1. **North-South Flow**:
   - **NS_Green**: Green light for North-South traffic (Duration: 60 seconds).
   - **NS_Yellow**: Yellow light for North-South traffic (Duration: 5 seconds).
   - **NS_Red**: Transition to the red light, ending the North-South flow phase.

2. **East-West Flow**:
   - **EW_Green**: Green light for East-West traffic (Duration: 60 seconds).
   - **EW_Yellow**: Yellow light for East-West traffic (Duration: 5 seconds).
   - **EW_Red**: Transition to the red light, ending the East-West flow phase.

3. **South-North Flow**:
   - **SN_Green**: Green light for South-North traffic (Duration: 60 seconds).
   - **SN_Yellow**: Yellow light for South-North traffic (Duration: 5 seconds).
   - **SN_Red**: Transition to the red light, ending the South-North flow phase.

4. **West-East Flow**:
   - **WE_Green**: Green light for West-East traffic (Duration: 60 seconds).
   - **WE_Yellow**: Yellow light for West-East traffic (Duration: 5 seconds).
   - **WE_Red**: Transition to the red light, ending the West-East flow phase.

### Transition Logic
- The sequence starts with **North-South** flow and moves to **East-West**, then **South-North**, and **West-East**.
- Each flow completes its green, yellow, and red phases before the next flow begins.
- This sequence loops continuously, ensuring that each direction receives an equal amount of time for traffic flow.

## Timing and Duration
Each directional flow has:
- **Green Phase**: 60 seconds
- **Yellow Phase**: 5 seconds
- **Red Phase**: This phase is implied by the transition to the next directional flow and allows for stopping time as the next green phase begins in a different direction.

This consistent timing helps regulate traffic efficiently, minimizing wait times and enhancing safety at the intersection.

## Future Modifications
The diagram can be expanded to include additional states if the intersection layout changes (e.g., adding turn signals or pedestrian phases). Timing durations can also be adjusted depending on real-time traffic data to optimize flow.

## Example
If the sequence starts with North-South flow:
1. North-South traffic proceeds with a green light for 60 seconds.
2. A yellow light appears for 5 seconds, warning the North-South traffic to prepare to stop.
3. North-South flow transitions to red, and East-West flow begins its green phase, following the same duration pattern.

## Usage
This state diagram provides a clear, predictable traffic light sequence, useful for designing intersection traffic control systems or simulations to improve traffic management.

---
