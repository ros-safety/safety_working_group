# Safety patterns catalogue

The safety patterns catalogue provides architectural descriptions and, in some cases, sample code for implementing commonly-used safety-critical architectural patterns in ROS.

If an architecture pattern you know is not in the catalogue, [make a pull request](https://github.com/ros2/safety_working_group/pulls) to add it!

# Patterns

- [1oo2 voting pattern](safety_patterns_catalogue/1oo2.md)
- [2oo2 redundancy pattern](safety_patterns_catalogue/2oo2.md)
- [Cold standby](safety_patterns_catalogue/cold_standby.md)
- [Hot standby](safety_patterns_catalogue/hot_standby.md)
- [Virtual Synchrony](safety_patterns_catalogue/virtual_synchrony.md)

## Related Catalogues

Existing catalogues of design patterns that increase the fault-tolerance, reliability, availability, and safety of a system:

1. **A. Armoush, “[Design patterns for safety-critical embedded systems](https://d-nb.info/1007034963/34),”** RWTH Aachen, Aachen, **2010**
   Armoush first discusses a suitable set of properties to describe a safety mechanism. He then provides a catalogue containing the following general safety patterns.
   Hardware Patterns: Homogeneous Duplex Pattern (Sect. 7.3), Heterogeneous Duplex Pattern (Sect. 7.4), Triple Modular Redundancy Pattern (Sect. 7.5),  M-Out-Of-N Pattern (Sect. 7.6), Monitor-Actuator Pattern (Sect. 7.7), Sanity Check Pattern (Sect. 7.8), Watchdog Pattern (Sect. 7.9), and Safety Executive Pattern (Sect. 7.10).
   Patterns that use software diversity (software redundancy) to tolerate software faults, e.g. N-Version Programming Pattern (Sect. 8.5), Recovery Block Pattern(Sect. 8.6), Acceptance Voting Pattern (Sect. 8.7), N-Self Checking Programming Pattern (Sect. 8.8), and Recovery Block with Backup Voting Pattern (Sect. 8.9).
   Combination of Hardware and Software Patterns: Protected Single Channel Pattern (Sect. 9.1) and 3-Level Safety Monitoring Patter (Sect. 9.2).
1. **L. Grunske, “[Strukturorientierte Optimierung der Qualitätseigenschaften von softwareintensiven technischen Systemen im Architekturentwurf](https://pdfs.semanticscholar.org/16cc/fdb40da681602cdb56078f07dd43d1d0bd35.pdf),”** Universität Potsdam, Potsdam, **2004** (german)
   In his PhD thesis, Grunske uses hyper graphs to model the software architecture of a system. The hyper graphs are then analyzed and transformed to optimize software quality attributes such as safety. In Annex D, Grunske provides a catalogue of eleven safety patterns, which includes a formal description of each pattern as a transformation of a hyper graph.
1. **Safe Automotive soFtware architEcture (SAFE), “[Deliverable D3.6.b: Safety Code Generator Specification](https://itea3.org/project/workpackage/document/download/1556/D3.6.b%20SAFE%20-%20Safety%20Code%20Generator%20Specification.pdf),” 2013**
   Deliverable D3.6.b “Safety Code Generator Specification” of the Safe Automotive soFtware architEcture (SAFE) project identifies software safety mechanisms that fulfil typical software safety requirements that are defined in the SAFE meta-model. These safety requirements are derived from the technical safety concept as defined by the ISO 26262. The underlying idea is that the described software safety mechanisms can be realized automatically (implemented as architectural elements in a model or generated as C code) and linked to the according requirement.
   The described software safety mechanisms Aliveness monitor, context range check, gradient check, comparison, CRC, filter, actuator monitor, CPU self-test, RAM self-test, voter, health monitor, and heartbeat.

## Contributing a new pattern

To add a new pattern to the catalogue, follow this process.

1. Fork the [Safety Working Group's repository](https://github.com/ros2/safety_working_group)
1. Add a new file to the `doc/safety_patterns_catalogue` directory to hold the pattern description.
   Begin with [the pattern description template file](safety_patterns_catalogue/template.md)
1. Make a pull request for your proposed pattern.
1. The pull request review process will allow others a chance to comment on your pattern and for you to improve it.
   Through this process, the proposed pattern will reach a higher level of quality and get closer to something immediately usable by robotics engineers using ROS.
1. Once the pull request has been merged, your proposed pattern will have been accepted and will appear in the catalogue.
