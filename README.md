# HomePLC-DIO

TwinCAT library for digital in- and output control that is part of the HomePLC library.

## Dependencies

- [HomePLC Logging](https://github.com/irtom/HomePLC-Logging)

## Required hardware

The library works with the following hardware:

- Digital inputs
- Digital outputs
 
## Contents

Since the library is used for home automation the digital inputs are meant to be used for buttons and the digital outputs for switching relays (lights, sockets) or LEDs.

- FB_DIO
  - Abstract parent class that contains general functionality for both DI and DO
- FB_DI
  - Can detect short presses, long presses, double presses and when it is continuously held (commands)
  - Once a command is detected the digital input can defer other commands temporarily (prevent accidental double pressing)
- FB_DO
   - Can turn a digital output on/off, toggle it, make it blink continuously and let it flash once (on if off, off if on)

All digital in- and output switches are counted and stored in retain memory. The counter also works for digital outputs when it is manipulated externally (e.g. through ADS)

## Example usage
See the [example repository](https://github.com/irtom/HomePLC-Example).
