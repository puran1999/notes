---
title: A New Hope # This is a text property
year: 1977
favorite: true
cast: # This is a list property
  - Mark Hamill
  - Harrison Ford
  - Carrie Fisher
---

# Communication Test
## Hardware Setup
- Logic analyzer Channel 0 & 1 connected to MCU RX and TX respectively.
- Gateway DID: 0013A200421AC49D
- Device DID: 0013A200421AC5B9




---
# Rough work

7E 00 19 90 00 13 A2 00 42 1A C4 9D 00 00 01 01 46 46 02 31 30 30 45 03 30 2C 32 04 02
|---------------|----------GATEWAY-DID----------|-------------------------|--CMD--|--|VAL|------------
~ \0 \x19 \x90 \0 \x13 \xA2 \0 B \x1A \xC4 \x9D \0 \0 \x01 \x01 F F \x02 1 0 0 E \x03 0 , 2 \x04 \x02
~ \0 \x19 \x90 \0 \x13 \xA2 \0 B \x1A \xC4 \x9D \0 \0 \x01 \x01 F F \x02 1 0 0 D \x03 0 , 2 \x04 \x03
~ \0 \x19 \x90 \0 \x13 \xA2 \0 B \x1A \xC4 \x9D \0 \0 \x01 \x01 F F \x02 1 0 1 8 \x03 0 , 2 \x04 \x0E
~ \0 \x19 \x90 \0 \x13 \xA2 \0 B \x1A \xC4 \x9D \0 \0 \x01 \x01 F F \x02 1 0 0 5 \x03 0 , 2 \x04 \x12


