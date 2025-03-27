# Angry Birds FPGA Implementation (Project Winter 2025 - Lab A1)

## Overview

This project implements a hardware version of an "Angry Birds"-style game on an Intel DE-10 FPGA board. Players use a keyboard-controlled slingshot to launch birds with ballistic physics, aiming to hit pig targets amidst various obstacles. The game state, physics, rendering, and controls are all managed by custom modules.

## Core Features

*   **Slingshot Mechanics:** Aim (up/down keys), power up (hold key), and launch (release key).
*   **Ballistic Physics:** Birds follow a calculated trajectory.
*   **Targets & Obstacles:** Hit pigs, navigate breakable/unbreakable obstacles.
*   **VGA Output:** Game displayed on a 640x480 monitor.
*   **Keyboard Input:** Numeric keypad controls aiming and firing.
*   **Scoring & Lives:** Basic game progression elements.
*   **Sound Effects:** Audio feedback for key events.
*   **Enhancements:** Includes features like randomized level elements and efficient bitmap rendering using MIFs.

## Technology

*   **Platform:** Intel DE-10 FPGA
*   **Language:** Verilog
*   **Tools:** Intel Quartus Prime, SignalTap Logic Analyzer
*   **I/O:** VGA, PS/2 Keyboard, Audio Out

## Architecture Highlights

The system uses a modular design:

*   **`Game_control`:** Central FSM managing game state, collisions, and overall flow.
*   **`Slingshot_block`:** Handles aiming, power calculation, and launch initiation.
*   **`Bird_block_t`:** Calculates and renders the bird's flight path.
*   **`Rendering Modules`:** Dedicated blocks for pigs, obstacles, and background.
*   **`VGA_Controller`:** Aggregates pixel data via a MUX and drives the display.

