# Portable Hybrid Solar–Wind Generator

A compact 3D-printed generator that combines a helical vertical-axis wind turbine with four small solar panels, battery storage and USB output. This README covers the parts, printing, assembly and electrical checks. The repository contains the actual Fusion 360 designs and 3MF files.

![Finished solar-panel enclosure](images/finished-generator.jpg)

## Parts and tools

| Part | Purpose |
| --- | --- |
| 3D-printed helical rotor: blades, top, base and pegs | Wind-energy capture |
| Printed motor stand and solar-panel case | Support and enclosure |
| Small DC motor | Used as the wind generator |
| Four small solar modules, approximately 5 V / 200 mA each in the prototype | Solar input |
| Two suitable DC-DC converter modules | Separate wind and solar conditioning |
| Schottky diodes | Isolate the two source branches |
| Compatible protected LiPo cell and charger / power-bank module | Energy storage and USB output |
| Wiring, connectors, fasteners | Assembly |
| 3D printer, soldering supplies and multimeter | Fabrication and basic checks |

The photos show the parts from this particular build. Exact electronics model numbers and pin assignments are not fully established in the documentation; check the specifications of the modules you actually use.

![Components laid out before assembly](images/components-before-assembly.jpg)

## 1. Print the components

The repository includes printable 3MF files and editable Fusion 360 designs:

| Component | 3MF | Fusion 360 |
| --- | --- | --- |
| Complete turbine and case | [3MF](3MF%20files/gorlov%2Bcase.3mf) | [F3D](F3D%20files/gorlov%2Bcase.f3d) |
| Rotor base | [3MF](3MF%20files/gorlovBase.3mf) | [F3D](F3D%20files/gorlovBase.f3d) |
| Helical blades | [3MF](3MF%20files/gorlovBlades.3mf) | No separate blade F3D provided |
| Rotor top | [3MF](3MF%20files/gorlovTop.3mf) | [F3D](F3D%20files/gorlovTop.f3d) |
| Motor stand | [3MF](3MF%20files/motorstand.3mf) | [F3D](F3D%20files/motorstand.f3d) |
| Peg | [3MF](3MF%20files/peg.3mf) | [F3D](F3D%20files/peg.f3d) |

Check scale, dimensions, tolerances and printer settings in your slicer. An early sketch shows the rotor at roughly 330 mm in diameter and 350 mm high; verify dimensions in the final CAD. Print the assembly pieces separately when appropriate for the available bed size.

## 2. Assemble the helical rotor

The turbine uses curved blade sections joined to top and bottom supports. The exploded view shows how the components fit around the central axis.

![Exploded CAD view showing the rotor parts and shaft](images/rotor-exploded.jpg)

1. Lay out the printed blades, top, bottom and connecting pieces.
2. Test-fit the matching blade ends and locating features before securing the parts.
3. Align the helical blades between the top and bottom supports as shown in the CAD.
4. Check that the completed rotor is centered and that the blade edges are clear of the frame.
5. Gently rotate the unpowered assembly by hand to check for rubbing, wobble or a poor fit.

![Finished printed helical rotor](images/printed-rotor.jpg)

## 3. Install the motor / generator

The DC motor is used as a generator when its shaft is driven by the turbine. Fit it into the printed motor stand and align the shaft with the center of the rotor. Make sure the mount is secure and the rotating assembly has enough clearance.

A small rotor has limited starting torque. Shaft friction, poor balance and an excessive electrical load may prevent it from starting even when wind is present.

## 4. Prepare the solar-panel enclosure

The base consists of two solar-panel housing sections and separate end pieces. The exploded enclosure view shows the center-mounted motor in relation to the case.

![Exploded CAD view of the solar-panel housing, motor and end pieces](images/enclosure-exploded.jpg)

1. Print and test-fit the case components.
2. Check the solar-panel openings against the actual modules.
3. Place the panels in the sloping upper faces, with their active surfaces exposed.
4. Plan space for the low-voltage electronics and wiring inside the enclosure.
5. Keep wires clear of the motor shaft and any enclosure joint or pinch point.

The finished prototype photograph at the top shows the two panel-bearing sections joined at the center.

## 5. Arrange the power electronics

The prototype's electrical concept uses separate conditioning paths for the solar panels and wind generator, followed by a shared low-voltage input to a battery / power-bank module:

- **Solar branch:** Solar modules → DC-DC converter → Schottky isolation diode.
- **Wind branch:** Motor generator → its own DC-DC converter → Schottky isolation diode.
- **Output section:** The two conditioned branches feed a compatible charger / power-bank input, with USB output supplied by that module.

The original drawing labels the converted outputs at approximately 5 V. These are intended values, not proof that the modules regulate at every available input condition. In particular, some converters cannot start at the low voltage generated by the wind motor.

**Battery and charging safety:** The project drawing is a concept, not an independently verified pin-level LiPo wiring plan. Use only compatible charging and protection hardware, and have a knowledgeable adult or electronics supervisor check the design and ratings before connecting or charging a lithium cell. Do not bypass protection circuitry.

For preliminary source checks, keep the storage electronics disconnected and have the source polarity, converter limits and output behavior checked with a multimeter and suitable test conditions.

## 6. Put everything together

This original project image collects the separated rotor sections, assembled turbine, enclosure pieces and final form.

![Original assembly sequence and exploded views](images/assembly-overview.jpg)

1. Verify the printed rotor joints and central motor mount.
2. Fit the solar panels and route the low-voltage wiring inside the case.
3. Position the power-handling modules where they will not touch the moving shaft or be crushed by the enclosure.
4. Check mechanical alignment and the electrical modules' compatibility before closing the enclosure.
5. Close and secure the base sections.
6. Attach the rotor above the base and verify that it turns freely by hand with the system unpowered.

The turbine and solar base are separate assemblies that come together at the motor shaft and mount.

## 7. Check the finished system

Before any outdoor use, check that the assembly is stable, the blades cannot strike the housing, and the solar panels are unobstructed. Do not operate an unsecured spinning rotor or a prototype battery charger unattended. The prototype is not rated for storms or other severe conditions.

To compare performance, measure voltage and current **under a known load**, as well as wind speed and lighting conditions. The earlier project notes report approximate wind-side figures of **0.05 W** in low wind, **2.5–3 W** in moderate wind and **3–4 W** in stronger wind. These were informal observations, not a calibrated power curve or a guaranteed USB output.

## Troubleshooting

| Symptom | Check |
| --- | --- |
| Rotor does not turn | Shaft friction, blade clearance, rotor alignment and generator load |
| Rotor wobbles | Printed joints, motor mount, shaft alignment |
| Wind converter does not start | Startup-voltage threshold and generator behavior under load |
| Solar output is low | Orientation, shading, panel connections and converter losses |
| USB output is inconsistent | Storage module specifications, protected battery state and available source power |

## Project files

- [3MF print files](3MF%20files/)
- [Fusion 360 project files](F3D%20files/)
- [Assembly photos and CAD screenshots](images/)

The images in this README are the author's own project photos and CAD screenshots. The documented build is an experimental small-scale prototype; component compatibility and printing tolerances need to be checked for any reproduction.
