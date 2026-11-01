# Mechanical design and CAD guide

The physical design combines a helical vertical-axis wind turbine (VAWT) with a compact solar-panel and electronics enclosure. The rotor mounts above the base; the motor/generator sits on the rotation axis. In the photographs, the rotor and enclosure are separate parts during fabrication and form a single stacked assembly when deployed.

The rotor's helical profile is intended to accept wind from different horizontal directions without a yaw mechanism. The design is inspired by Gorlov-style helical VAWTs. The images show successive stages: hand sketch, separable CAD components, an assembled model, a structural-analysis view, a printed rotor, and the finished solar-panel base.

## Dimensions shown in the design sketch

| Parameter | Sketch value | Interpretation |
| --- | ---: | --- |
| Rotor diameter | 330 mm | Approximate horizontal extent of the turbine |
| Rotor height | 350 mm | Approximate blade assembly height |
| Swept area | 0.115 m² | Approximately diameter × height: 0.330 × 0.350 = 0.1155 m² |
| Helical angle annotation | 60° | Angle marked in the early drawing; verify against the final CAD |
| Base width | 260 mm | Dimension marked in the side/front enclosure sketch |
| Base height | 100 mm | Dimension marked in the enclosure sketch |
| Shaft speed annotation | 300 rpm | A note in the concept drawing, **not** a verified measured operating speed |

**These dimensions come from an early drawing, not an audit of the final CAD geometry.** Users who fabricate parts should check dimensions, scale, shaft fit and clearances in the linked model files rather than treating this table as a tolerance drawing.

## Files in this repository

### Print-ready / slicer-oriented models (3MF)

| File | Intended part or assembly |
| --- | --- |
| [gorlov+case.3mf](../3MF%20files/gorlov%2Bcase.3mf) | Turbine and case assembly |
| [gorlovBase.3mf](../3MF%20files/gorlovBase.3mf) | Rotor lower piece |
| [gorlovBlades.3mf](../3MF%20files/gorlovBlades.3mf) | Helical blade pieces |
| [gorlovTop.3mf](../3MF%20files/gorlovTop.3mf) | Rotor upper piece |
| [motorstand.3mf](../3MF%20files/motorstand.3mf) | Motor support |
| [peg.3mf](../3MF%20files/peg.3mf) | Connecting / locating peg |

### Editable Fusion 360 models (F3D)

[Assembly](../F3D%20files/gorlov%2Bcase.f3d) · [Rotor base](../F3D%20files/gorlovBase.f3d) · [Rotor top](../F3D%20files/gorlovTop.f3d) · [Motor stand](../F3D%20files/motorstand.f3d) · [Peg](../F3D%20files/peg.f3d)

The repository has a 3MF file for the blades, but there is no corresponding blade-only F3D file in the current directory.

## Prototype progression

1. **Concept:** A roughly 330 mm diameter by 350 mm tall helical rotor was drawn above a compact base. The sketches also considered the usable swept area and the motor connection.
2. **Modular modeling:** The top, bottom, blades, motor mount, pegs and enclosure were modeled as parts. Exploded CAD views show which pieces are separable.
3. **Structural exploration:** The supplied analysis screenshots display a safety-factor scale with a target value of 4 and a separate velocity contour. These are **simulation visualizations**, not field load tests or proof of a safety factor for the printed assembly.
4. **Fabrication:** The photographed orange rotor is a 3D-printed physical prototype with a helical blade profile.
5. **Integration:** A red case with end caps holds the solar-panel modules. The wind rotor is attached above the case on the central shaft.

## Mechanical considerations

The prototype's small size makes shaft concentricity, bearing losses, rotor balance and friction important. The starting torque available from the wind must overcome these losses and any electrical load imposed by the generator and converter.

Printed parts also depend on material, print orientation, infill, layer adhesion, UV exposure and temperature. The CAD model and structural screenshots do not establish safe operation in strong winds. Rotating assemblies should be physically secured and kept clear of people and loose objects. This project is documented as an experimental small-scale prototype.

For the photographed assembly sequence, see the [Instructables build article](https://www.instructables.com/Portable-Hybrid-Rapid-Deploy-Renewable-Generator/).
