# LittleFoot ZMK config

ZMK user configuration for the LittleFoot keyboard using a nice!nano nRF52840 controller in the Pro Micro footprint.

## Build targets

`build.yaml` builds the LittleFoot firmware and a settings-reset firmware for `nice_nano//zmk`.

## Matrix setup

The overlay uses a 5-row by 10-column matrix, `col2row` diode direction, active-high columns, and pulled-down row inputs. GPIO assignments follow the LittleFoot schematic and the nice!nano Pro Micro pin mapping.

**Check before flashing:** the schematic labels the nice!nano D2 connection as `row10`, while the matrix labels its rightmost net `col10`. The overlay maps D2 as column 10 to match the existing LittleFoot ZMK configuration. If the PCB follows the schematic as drawn, confirm the actual D2-to-col10 continuity; firmware cannot correct a missing PCB connection.
