# Arduino Coding Standards — Hybrid RobotiX

Conventions that apply to all Arduino applications in the Hybrid RobotiX ecosystem.

## Sensor Code Requirements

Every sensor must have all four of the following present in code — no exceptions:

1. **`#include`** — library include at the top of the file
2. **Instance declaration** — sensor object declared at file scope
3. **Function implementation** — all sensor read/control functions fully written
4. **`Bridge.provide()` active** — sensor registered with the Bridge

The **only** thing that may be commented out for an unconnected sensor is the `begin()` call. Everything else must be present and compilable.

```cpp
// ✅ Correct — sensor not yet physically connected
#include <Adafruit_SHT4x.h>                   // present
Adafruit_SHT4x sht45;                          // present

void readSHT45(float &temp, float &humidity) { // present
    sensors_event_t h, t;
    sht45.getEvent(&h, &t);
    temp = t.temperature;
    humidity = h.relative_humidity;
}

void setup() {
    // sht45.begin();                           // commented — not connected yet
    Bridge.provide("sht45_read", readSHT45);   // present
}
```

## Bridge Function Naming

All Bridge function names use the **full part number** of the sensor, lowercase.

```cpp
Bridge.provide("scd30_read", readSCD30);
Bridge.provide("sht45_read", readSHT45);
Bridge.provide("bme688_read", readBME688);
Bridge.provide("as7343_read", readAS7343);
Bridge.provide("bno055_read", readBNO055);
```

**Never** use generic names like `bridge_temp` or `bridge_air`.

## File Naming

All scripts follow the `filename-vX.Y.Z` versioning convention. Active symlinks are unversioned.

## I2C Mux Access

Always select the mux channel before accessing a sensor, and deselect after:

```cpp
void selectMuxChannel(uint8_t channel) {
    Wire.beginTransmission(MUX2_ADDR);
    Wire.write(1 << channel);
    Wire.endTransmission();
}

void deselectMux() {
    Wire.beginTransmission(MUX2_ADDR);
    Wire.write(0);
    Wire.endTransmission();
}
```

## UART / JSON Protocol (UNO-Q ↔ Portenta C33)

- Use ArduinoJson for all UART message serialization
- Messages are newline-terminated JSON objects
- All field names use `snake_case`
- Include a `"type"` field in every message for routing

```json
{"type": "locomotion_cmd", "speed": 0.5, "heading": 90.0}
{"type": "sensor_data", "source": "bno055", "yaw": 45.2}
```

## General Rules

- Python exclusively for host-side tooling (no bash/shell scripts)
- Debian-based systems only for deployment targets
- Always file vendor bugs — never use workarounds as permanent solutions
- `newrepo.bash` is never touched
