# Pattern name

## Abstract

Describe the pattern briefly here.
Include the purpose of the pattern, where it is expected to be used, and a one-sentence description of what the pattern consists of.
This section should be no more than 200 words.


## Pattern goal

Describe the purpose of the pattern.
What is it intended to achieve?
Do not focus on architectural concepts, but on what it achieves in a safety-critical system.
For example, "This pattern provides a redundant structure for getting a result from a service via a voting mechanism, allowing one service provider out of three to be incorrect."


## Architecture

Describe in detail the pattern works as an architecture.
This section should be relatively agnostic to ROS.

An architecture diagram is recommended.


## ROS 2 implementation

Describe how the architecture described in the previous section is implemented using ROS 2.
This section should be as concrete as possible, describing nodes, executor usage, suitable QoS settings, parameters, etc.

Sample code can be provided.


## Use cases

Describe here in detail where the pattern is expected to be used.
Also describe cases where it is *not* appropriate to use.


## Formating

Your pattern description must comply with the following formatting guidelines.

- Follow the [GitHub Markdown guide](https://guides.github.com/features/mastering-markdown/).
- One sentence per line.
- Do not wrap sentences across multiple lines.
