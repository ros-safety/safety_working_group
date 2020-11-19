# ROS 2 Safety-Critical Working Group

This document defines the scope and governance of the ROS 2 Safety-Critical Working Group (WG).

The ROS 2 Safety-Critical Working Group's mission is to support the creation of robots and other systems using ROS that are safe.

This Working Group focuses on a mix of tools, libraries and documents.

* We support the development of tools that can be applied to safety-critical system engineering.
  For example, our on-going project to improve the open-source Doorstop requirements management tool and integrate it with the ROS ecosystem.
* We produce libraries, particularly re-usable nodes, that can be used to create robust systems.
  An example is the watchdog nodes created originally by Philipp Robbel and now maintained by this working group.
* We produce documentation to educate and guide developers in creating more reliable or more available systems, in order to enable the creation of safer robots using ROS.
  The documentation includes tutorials, guidance documents, and best practices.

## Subprojects

This Working Group owns and maintains the following subprojects.
Its meetings and membership are largely focused on the direction, design, and work on the projects.

### Subproject List

The following subprojects are owned by the Working Group.

* [Software Watchdogs](https://github.com/ros-safety/software_watchdogs/)
  * A library of software watchdogs based on DDS Quality of Service (QoS) policies and ROS 2 life cycle nodes.
  * A presentation including this library is [available here](https://raw.githubusercontent.com/ros-safety/safety_working_group/main/presentations/Mapless%20AI%20-%20Autoware%20Workshop%20Presentation%20IV2020.pdf).
  * Repositories
    * https://github.com/ros-safety/software_watchdogs
    
* [C++ contracts](https://github.com/ros-safety/contracts_lite)
  * A library for defining and enforcing contracts.
  * A presentation including this library is [available here](https://raw.githubusercontent.com/ros-safety/safety_working_group/main/presentations/Mapless%20AI%20-%20Autoware%20Workshop%20Presentation%20IV2020.pdf).
  * Repositories
    * https://github.com/ros-safety/contracts_lite

* [Doorstop requirements tool - extensions for ROS](https://github.com/doorstop-dev/doorstop)
  * An open-source tool for managing and tracing requirements.
    The tool itself is not owned by this Working Group.
    This Working Group is contributing to this tool in order to improve it.
    This Working Group is also working to integrate the creation and use of requirements, assisted by this tool, into ROS development activities.
  * Repositories
    * https://github.com/doorstop-dev/doorstop (not owned by the Working Group)

* [Safety Patterns Catalogue](http://ros-safety.github.io/safety_working_group/safety_patterns_catalogue/)
  * A catalogue of software structures commonly-used in safety-critical systems, and sample implementations using ROS.
  * Websites
    * [http://ros-safety.github.io/safety_working_group/safety_patterns_catalogue/](http://ros-safety.github.io/safety_working_group/safety_patterns_catalogue/)
  * Repositories
    * [https://github.com/ros-safety/safety_working_group/tree/master/safety_patterns_catalogue](https://github.com/ros2/safety_working_group/tree/master/safety_patterns_catalogue)

* [Safety-Critical ROS Cookbook](http://ros-safety.github.io/safety_working_group/safety_critical_ros_cookbook/)
  * A collection of guidance on how to use ROS as part of building safe robots.
  * Websites
    * [http://ros-safety.github.io/safety_working_group/safety_critical_ros_cookbook/](http://ros-safety.github.io/safety_working_group/safety_critical_ros_cookbook/)
  * Repositories
    * [https://github.com/ros-safety/safety_working_group/tree/master/safety_critical_ros_cookbook](https://github.com/ros2/safety_working_group/tree/master/safety_critical_ros_cookbook)

### Standards for subprojects

Subprojects must meet the following criteria (and the Working Group agrees to maintain them upon adoption).

* Build passes against ROS 2 master
* The ROS 2 standard linter set is enabled and adhered to
* If packages are part of nightly builds on the ROS build farm, there are no reported warnings or test failures
* Quality builds are green (address sanitizer, thread sanitizer, clang thread safety analysis)
* Test suite passes
* Code coverage is measured, and non-decreasing level is enforced in PRs
* Issues and pull requests receive prompt responses
* Releases go out regularly when bugfixes or new features are introduced
* The backlog is maintained, avoiding longstanding stale issues

### Adding new subprojects

To request adoption of a new subproject, add a list item to the "Subprojects" section and open a Pull Request to this repository.
Follow the default Pull Request Template to populate the text of the PR.

The PR will be merged upon unanimous approval from Approvers.

### Subproject changes

Modify the relevant list item in the "Subprojects" section and open a Pull Request to this repository.
Follow the default Pull Request Template to populate the text of the PR.

The PR will be merged upon unanimous approval from Approvers.

### Deprecating subprojects

A subproject may cease to be useful, or the Working Group may decide it is no longer in their interest to maintain it.
We do not commit to maintaining every subproject in perpetuity.

To suggest removal of a subproject, remove the relevant list item in the "Subprojects" section and open a Pull Request in this repository.
Follow the instructions in the Pull Request Template to populate the text of the PR.

The PR will be merged upon unanimous approval from Approvers.

If the repositories of the subproject are under the WG's GitHub organization, they will be transferred out of the organization or archived at this time.

## Governance

### Meetings

* Regular Working Group Meeting: On the first and third Wednesdays of the month at 14:00 UTC for one hour
  * Meetings are scheduled in the [ROS Events Calendar](https://calendar.google.com/calendar/embed?src=agf3kajirket8khktupm9go748%40group.calendar.google.com&ctz=America%2FLos_Angeles).
    This is the most reliable method to find the next meeting time.
    To get automated invitations to the Working Group meetings, join the [Working Group's invite group](https://groups.google.com/forum/#!forum/ros-safety-working-group-invites).
    Meetings are also announced on Discourse using the [`wg-safety-critical` tag](https://discourse.ros.org/tags/wg-safety-critical).
  * Minutes of each Working Group meeting are posted in this repository and at the [generated website](http://ros-safety.github.io/safety_working_group/meeting_minutes/).

### Communication Channels

Working Group members communicate using Discourse.
Post topics using the [`wg-safety-critical` tag](https://discourse.ros.org/tags/wg-safety-critical) so that other members can easily find them.

Members may also communicate in GitHub pull requests and issues if the discussion is relevant to a particular topic for a particular subproject.

### Backlog Management

Each subproject uses its own issue tracking and pull request management.
Complex subprojects may use a project board to manage tasks and release-related activities.

Activities of the working group itself are managed using [issues](https://github.com/ros2/safety_working_group/issues) and [pull requests](https://github.com/ros2/safety_working_group/pulls) on this repository.
A project board is not used.

### Membership, Roles and Organization Management

Working Group members may act in one or more of the following roles:

* **Member**
  * Prerequisite: Attend at least one out of the last three Working Group meetings
  * Responsible for triaging issues
* **Reviewer**
  * All reviewers are members
  * Prerequisite: Proven track record of high-quality reviews to the Working Group's subprojects
  * Responsible for reviewing pull requests
* **Approver**
  * All approvers are reviewers
  * Prerequisite: Proven track record of high-quality contributions and reviews to the Working Group's subprojects
  * Responsible for approving and merging pull requests
  * Responsible for vetting and accepting new projects into the Working Group
* **Lead**
  * TSC member or their delegate
  * Responsible for organizing and moderating working group meetings
  * Responsible for posting meeting materials (minutes, recordings, etc.)
  * Responsible for breaking ties

To become a member or change role, create an issue in this repository using the appropriate issue template.
Such applications are accepted upon unanimous agreement from Approvers, and are typically based on the applicant's history with the subprojects of the Working Group.
The Lead role cannot be applied for, as it is an appointee of the ROS 2 TSC.

### Modifying this governance document

Changes to this document will be made via pull request.
The pull request will be merged on unanimous agreement from Approvers.
