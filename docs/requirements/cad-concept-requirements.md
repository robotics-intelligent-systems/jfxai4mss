# CAD-aligned high-level requirements

The proposed baseline contains four editable diagrams: common marine requirements and three asset specifications. The original filenames of the catamaran and RV diagrams remain stable for repository links; their historical names do not select amphibious, hydrogen or solar hardware.

| Concept source | Requirements diagram | Baseline interpretation |
| --- | --- | --- |
| [Catamaran concept](../../MBSE/CAD/solar-powered-amphibious-catamaran-concept.jpg) | [Catamaran](../../MBSE/CAS/Drawio/OpenTwin_Amphibious_Catamaran_Hybrid_H2_Renewable_Requirements_v2.drawio) | Twin hulls, modular marine propulsion, passenger/mission modules, sensors, local helm, energy and twin. The solar filename is not supported by a visible PV callout. |
| [RV concept](../../MBSE/CAD/amphibious-rv-concept.jpg) | [RV](../../MBSE/CAS/Drawio/OpenTwin_Modular_Amphibious_RV_High_Level_Requirements.drawio) | Living spaces, roof PV and roof deck, modular batteries, water/waste tanks, inverter, HVAC, electric marine propulsion and IoT. Land transport hardware is unresolved. |
| [River cruiser concept](../../MBSE/CAD/river-cruiser-ship-concept.jpg) | [River cruiser](../../MBSE/CAS/Drawio/OpenTwin_River_Cruiser_High_Level_Requirements.drawio) | River hull, multiple passenger decks, hotel loads, navigation, energy and interchangeable mission modules, with optional ROV/AUV handling. |
| All three | [Common marine requirements](../../MBSE/CAS/Drawio/OpenTwin_Marine_Common_High_Level_Requirements.drawio) | Configuration, telemetry, local safety, interfaces, simulation, hydrostatics, structure, energy protection, human safety, cybersecurity, twin verification and envelope management. |

These JPEGs are illustrated concepts, not dimensioned CAD models. Text callouts and visually evident arrangements support proposed requirements; neither establishes validated geometry, feasibility, performance or compliance. The catamaran image's “all-weather” and “zero-emission” labels are aspirations requiring environmental and energy evidence. Depicted foils are not selected hardware. RV display percentages, coordinates and 5.2 kn are interface examples, not acceptance limits. LiFePO4 is a depicted candidate chemistry. AIS/automation callouts do not establish operational approval.

## Traceability and acceptance

[The register](cad-requirements-traceability.csv) contains 39 uniquely identified requirements, design allocation, proposed engineering owner role, verification method, acceptance criterion and planned evidence ID. COM-01 through COM-12 apply alongside each asset's own requirements. Common acceptance evidence must be evaluated for each installed configuration; reuse needs a documented applicability decision. Proposed roles are not assigned people. Dates, quantitative budgets, final criteria and evidence remain open.

Diagrams cover scope, requirements, logical architecture, interfaces/modes, traceability and budget/verification gates. Architecture arrows represent selected logical exchanges, not a complete wiring or deployment design. ROS 2, DDS, MQTT, Modelica and other repository technologies are implementation candidates to bind through the open interface contracts; no product is mandated by an illustration.

Before baseline approval, assign named owners and dates; define mission/occupancy and configuration; resolve critical physical, energy, environmental and data budgets; approve mode/guard and fault-response tables; and fix measurable acceptance limits before qualification tests. I = inspection, A = analysis, D = demonstration, T = test. No engineering verification evidence has been produced by this document refactor.

## Migration decisions

The two earlier requirements diagrams are replaced by a consistent proposed baseline. Original revisions remain in Git history. IDs have changed; [the migration crosswalk](legacy-requirement-crosswalk.csv) records every explicitly numbered requirement found in the original two diagrams. Entries consolidated into common requirements require review before updating external references. Removed or deferred requirements are recorded rather than silently treated as satisfied.

- Catamaran wheel/landing gear, land speeds, beach/ramp transitions and ground-load verification are deferred under CAT-08. No amphibious mechanism is visible in the concept.
- Mandatory hydrogen turbine, onboard electrolyzer, hydrogen-production sequence and wind generator are deferred as unselected energy variants under CAT-06/CAT-07. The illustration labels battery/hydrogen/hybrid alternatives but specifies none of those machines. A future hydrogen design needs its own energy balance, fuel-system interfaces and hazard/verification plan.
- RV road-towable requirements, hitch/brake/lighting and road-to-water sequences are deferred under RV-09. “Land & Water” is a concept label, with no transport mechanism defined.
- Catamaran mission handling and river ROV/AUV handling are candidate functions requiring detailed mechanical and safety design before activation.
- Sonar simulation, sailing-robot hardware and submarine design diagrams retain their research purpose; they have no corresponding CAD asset in this baseline and are unchanged.

[The source manifest](cad-source-baseline.json) records the input commit and SHA-256 hashes of the three JPEG references. CAD source files are unchanged.
