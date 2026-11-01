# Performance notes and validation status

The hybrid generator is a small experimental prototype. The photographs establish that hardware was fabricated and assembled; the CAD and analysis views document mechanical design work. Neither type of image, on its own, measures electrical generation under controlled conditions.

## Preliminary figures

The earlier project notes describe approximate *wind-side* power levels in different qualitative wind conditions:

| Condition as described | Approximate power from earlier notes |
| --- | ---: |
| Low wind | ~0.05 W |
| Moderate wind | ~2.5–3 W |
| Stronger wind | ~3–4 W |

These are **informal historical figures**, not an independently reproduced power curve. Wind speed, electrical load, RPM, sensor accuracy, measurement placement and repetition count are not specified in the available notes. They should **not** be described as guaranteed continuous power, a standardized wind-tunnel result, or combined wind-plus-solar output.

The solar section contains four small modules described as approximately 5 V / 200 mA each. Approximately 4 W is their **sum of nominal panel ratings**; it is not a measured full-system charge rate.

## How to read the design analysis

The supplied screenshots show a modeled rotor, a safety-factor visualization with a target marker, and a velocity result from a simulation interface. The screenshots do not include mesh settings, boundary conditions, material properties, applied loads or solver-validation checks. No field safety factor, fatigue limit, certified maximum wind speed or aerodynamic power coefficient is claimed.

## Suggested reproducible measurement record

A useful future dataset would capture these fields in a CSV:

| Field | Unit | Why it matters |
| --- | --- | --- |
| Timestamp / test ID | ISO date-time / text | Associates weather and electrical data |
| Wind speed at rotor | m/s | Makes output comparisons meaningful |
| Solar irradiance | W/m² | Separates panel behavior from weather |
| Rotor speed | rpm | Distinguishes startup from steady operation |
| Wind-generator output | V and A | Determines actual electrical power at a defined load |
| Solar-branch output | V and A | Measures solar contribution separately |
| Combined input to charge board | V and A | Captures conversion and diode losses |
| USB output to a defined load | V and A | Measures power delivered to the device |
| Battery state / voltage | as documented | Helps separate stored and generated energy |
| Ambient conditions and configuration | text | Records repeatability limits |

At a measured electrical interface, DC power is P = V × I. A credible efficiency calculation also requires measuring or estimating the incoming source power. For wind, the incident flow power is approximately 0.5 × air density × swept area × wind speed³, with clear assumptions on which area and wind speed were used. **Open-circuit voltage is not output power**; measurements need a known load and simultaneous voltage and current.

## Current boundaries

- No publicly documented calibrated wind-speed-versus-output curve is available in this repository.
- No verified continuous USB-C charging rating or runtime claim is made.
- A screenshot of finite-element analysis is not a substitute for physical proof testing.
- The design is intended as a compact educational microgeneration prototype, not an emergency-grade power supply or certified outdoor appliance.
