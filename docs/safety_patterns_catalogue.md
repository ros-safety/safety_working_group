# Safety patterns catalogue

The safety patterns catalogue provides architectural descriptions and, in some cases, sample code for implementing commonly-used safety-critical architectural patterns in ROS.

# Patterns

- [1oo2 voting pattern](safety_patterns_catalogue/1oo2.md)
- [2oo2 redundancy pattern](safety_patterns_catalogue/2oo2.md)
- [Cold standby](safety_patterns_catalogue/cold_standby.md)
- [Hot standby](safety_patterns_catalogue/hot_standby.md)
- [Virtual Synchrony](safety_patterns_catalogue/virtual_synchrony.md)

## Contributing a new pattern

To add a new pattern to the catalogue, follow this process.

1. Fork the [Safety Working Group's repository](https://github.com/ros2/safety_working_group)
1. Add a new file to the `doc/safety_patterns_catalogue` directory to hold the pattern description.
   Begin with [the pattern description template file](safety_patterns_catalogue/template.md)
1. Make a pull request for your proposed pattern.
1. The pull request review process will allow others a chance to comment on your pattern and for you to improve it.
   Through this process, the proposed pattern will reach a higher level of quality and get closer to something immediately usable by robotics engineers using ROS.
1. Once the pull request has been merged, your proposed pattern will have been accepted and will appear in the catalogue.
