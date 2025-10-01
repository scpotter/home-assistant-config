# Home Assistant Entity Naming Standard

## General Rules
- Lowercase letters only
- Words separated by `_`
- Format: `<domain>.<location>_<device>_<type_or_function>`
- `friendly_name` can be human-readable
- Template entities follow same rules
- Avoid duplicate or conflicting entity_ids

## Domain-Specific Conventions

### Sensors
Pattern: `sensor.<location>_<device>_<measurement>`
Examples:
- `sensor.living_room_temperature` → "Living Room Temperature" (physical)
- `sensor.garage_door_status` → "Garage Door Status" (template)

### Binary Sensors
Pattern: `binary_sensor.<location>_<device>_<state>`
Examples:
- `binary_sensor.front_door_locked` → "Front Door Locked"
- `binary_sensor.window_open_alert` → "Window Open Alert" (template)

### Switches
Pattern: `switch.<location>_<device>`
Examples:
- `switch.kitchen_outlet_1` → "Kitchen Outlet 1"
- `switch.living_room_fan_auto` → "Living Room Fan Auto" (template)

### Lights
Pattern: `light.<location>_<device>`
Examples:
- `light.living_room_ceiling` → "Living Room Ceiling Light"
- `light.kitchen_motion_auto` → "Kitchen Motion Auto Light" (template)

### Climate
Pattern: `climate.<location>_<device>`
Examples:
- `climate.master_bedroom_ac` → "Master Bedroom AC"
- `climate.living_room_auto_temp` → "Living Room Auto Temp" (template)

### Covers
Pattern: `cover.<location>_<device>`
Examples:
- `cover.garage_door` → "Garage Door"
- `cover.living_room_blinds_auto` → "Living Room Blinds Auto" (template)

## Template Entity Naming
- Template entities must have entity IDs
- Use `_auto`, `_status`, `_alert` suffixes to distinguish virtual entities
- Reference real devices inside templates
