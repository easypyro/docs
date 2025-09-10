# General Technical Notes for SFX Sequencer & Remote

## Common Radio Settings

868.8 MHz
SF7
BW 250 KHz
4/5 coding
16 dBm = 40mW

## Remote Control

### Battery Level
Remote will flash red battery warning LED < 1.25V per cell (so 2.5V at ADC).

### User Interface

#### Buttons

| Button | Description                                                 | Notes                                                        |
| ------ | ----------------------------------------------------------- | ------------------------------------------------------------ |
| DOWN   | < Channel                                                   | Channel LED +                                                |
| UP     | > Channel                                                   | Channel LED -                                                |
| FIRE   | Fire the current channel. 3 TX attempts if no ACK received. | Channel LED +                                                |
| SEQ    | Start the sequence. 3 TX attempts if no ACK received.       | All Channel LEDs on.                                         |
| PWR    | Hold for 2 seconds to switch on/off.                        | Remote LEDs on / off.                                        |
| ARM    | Toggle ARM / SAFE state of remote.                          | Green SAFE LED / Red ARM LED toggle. Remote is polling SEQ at 1 second intervals for status. If SEQ not armed on last status packet received, remote ARM LED will flash. 2 way radio comms in SAFE state. 1 way radio comms in ARM state. |

#### Hidden Modes



| Button                             | Description                                                  | Notes                                                        |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| STEP FIRE + UP ARROW for 2 seconds | Enters hidden **factory test mode.**  POWER button steps through. | All LEDs RED.<br />All LEDs GREEN.<br />Firmware version xx.xx (8 bit, decimal 99 max)<br />Firmware version xx.xx (8 bit, decimanl 99 max)<br />(Basically two numbers representing major (non-compatible) and minor (compatible) versions. Red is 0, green is 1. Eg. 0010 0000 / 1000 000 is Version 4.1 VERSION_MAJOR - 0 to 99 incompatible changes. E.g. API, pin remap, protocol shift VERSION_MINOR - 0 to 99 backward-compatible changes, optimisations, bug fixes. |
| Hold STEP FIRE + SEQ for 2 seconds | **Show RSSI**                                                | Shows RSSI on 8x channel LEDs in orange. LEDs update every second with RSSI of last poll packet received. Release both buttons to return to normal operation. |
| Hold DOWN + UP for 5 seconds       | Enters **bond mode**.                                        | Red LED chase initially. Green LED chase when successfully bonded to sequencer.. Press any button to exit bond mode. |

## Sequencer

1. DOWN + UP for 2 seconds enters bond mode. press any button to exit bond mode.
Red LED LED chase initially. Green LED chase when successfully bonded.

Explanation from Erlend: Basically when sequencer is in bond mode it requests bonding on a special broadcast address with bonding command followed by its new unique address. If a remote is put into bonding mode it sits listening on the special broadcast address, copies the new address and acks. The remote goes green when it gets a bonding address, the sequencer goes green when it gets a bonding ack.

### Channel Self Test

Flash red channel LED when Driver is shorted ON. Note that this will not catch a Driver gate stuck ON (and thus Driver ON) when not in SEQ ARM because V_FIRE rail is only at about 2.5V and won't switch on the MOSFET in the Driver. So, user should be advised to SEQ ARM before any pyro is connected to truly see if there is a Driver stuck ON. 





