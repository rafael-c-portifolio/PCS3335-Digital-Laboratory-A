# PCS3335 Digital Laboratory A - FPGA-Based Flight Simulator
# Project Overview
This project is part of the PCS3335 Digital Laboratory A course and involves designing a simple flight simulator using an FPGA. The system simulates a drone's movement in a 3D space (XYZ coordinate system) and displays the drone’s coordinates on an 8-digit 7-segment display. The movement is controlled using the FPGA’s levers to simulate forces in each direction. The simulation also takes into account gravity and limits the drone's movement to stay within a confined room.

# Objectives
Implement a flight simulator using VHDL on an FPGA.

Simulate and display the drone's coordinates in a 3D space (X, Y, Z axes).

Control the drone’s movement via levers on the FPGA, simulating forces acting in the positive and negative directions of each axis.

Apply gravity as a constant force acting on the drone's vertical position (Z-axis).

Constrain the drone’s movement within a predefined space, representing the limits of a room.

Display the real-time coordinates on an 8-digit 7-segment display.

# Hardware Components

FPGA Board: Used for implementing the VHDL code, processing inputs from the levers, and controlling the 7-segment display.

Levers (Switches): Used to control the drone's movement by simulating forces in the positive and negative directions along the X, Y, and Z axes.

8-Digit 7-Segment Display: Displays the current coordinates (X, Y, Z) of the simulated drone in real-time.

# Software Components

VHDL Code: Implements the logic for simulating the drone’s motion, applying gravity, limiting the drone's movement within a room, and driving the 7-segment display to show the coordinates.

FPGA Development Tools: Used to write, compile, and upload the VHDL code to the FPGA board.
# How It Works

Coordinate System: The system starts with the drone at the origin (0, 0, 0) in the XYZ coordinate system. The coordinates are initialized to this point on the 7-segment display.

Drone Movement Control: The FPGA’s levers are used to apply forces in each direction:

Levers for the X-axis control movement in the positive (+X) or negative (-X) direction.

Levers for the Y-axis control movement in the positive (+Y) or negative (-Y) direction.

Levers for the Z-axis control movement in the positive (+Z) or negative (-Z) direction, but gravity continually pulls the drone downward.

Gravity Simulation: Gravity is implemented as a constant force pulling the drone downward along the Z-axis unless a counteracting force is applied by moving the lever to the +Z direction.

Movement Constraints: The drone's movement is confined to a room, meaning the coordinates are limited by predefined boundaries in all directions. If the drone reaches the maximum or minimum coordinate on any axis, further movement in that direction is restricted.

Coordinate Display: The 8-digit 7-segment display shows the current coordinates of the drone in the format (X, Y, Z).
# Results
The FPGA-based flight simulator successfully simulates a drone’s movement in 3D space, accounting for user-controlled forces and gravity. The system displays the drone's real-time coordinates and restricts movement within the boundaries of a virtual room, making it a simple yet effective demonstration of digital logic control and simulation in VHDL.

# Usage

Program the FPGA board with the provided VHDL code using your FPGA development toolchain.

Use the FPGA's levers to control the drone's movement in the X, Y, and Z directions.

Observe the drone’s current position on the 8-digit 7-segment display.
The drone’s movement will be affected by gravity (on the Z-axis) and will be constrained by the room's boundaries.
