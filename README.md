# Banlumo Hand SDK

Python / ROS 2 integration source and evaluation documentation for dexterous-hand projects supported through Banlumo.

**Status: development preview. No hardware validation or production release.**

## Start with your configuration

Contact **Banlumo — yinaiguo@gmail.com** with your hand model, hardware revision, firmware, host OS, ROS distribution and intended task. Website: https://www.banlumo.com/

RY-H1 is the product designation currently under evaluation. This source uses RH16 package names. The exact RY-H1 ↔ RH16 hardware/firmware mapping is not confirmed; do not assume compatibility from the product name.

## What is included

- Python controller, CAN and kinematics sources.
- ROS messages, services, launch/config files and URDF descriptions.
- English integration checklist and a proposed mixed-item sorting evaluation.
- An offline source validator that does not connect to hardware.

Precompiled libraries, C++ sources, mesh archives and motion-running shell scripts are not included in this edition. URDF visual mesh references may require separately supplied assets. This is not a complete, tested plug-and-play SDK.

## Review and build

Run the offline checks first:

```bash
python3 tools/validate_source.py
```

The upstream guide references ROS 2 Humble. ROS, Linux dependencies and a supported CAN adapter must be provisioned separately. After reviewing dependencies in each package.xml, in a suitable ROS 2 environment:

```bash
cd ros2_ws
colcon build --symlink-install
```

Building does not establish compatibility. Do not launch controller or motion-test nodes until the configuration-specific wiring, supply, mounting, operating limits and stop procedure have been verified. See [integration checklist](docs/INTEGRATION.md).

## Contact and feedback

For selection, software questions and service coordination, contact Banlumo first. Include reproducible steps and sanitized logs; do not submit credentials, identity documents or confidential customer data in issues.

## Attribution and license

This is a Banlumo-maintained derivative integration edition, not original hardware or firmware. Upstream copyright and MIT permissions remain in [LICENSE](LICENSE). Provenance and the pinned source version are recorded in [UPSTREAM.json](UPSTREAM.json). Banlumo changes are recorded in [CHANGELOG.md](CHANGELOG.md). Third-party dependencies retain their own licenses.

## Other Banlumo source families

- [RH15 C++ / ROS 2 source](https://github.com/StevenAgYin/banlumo-rh15-sdk)
- [RH6 C++ / ROS 2 source](https://github.com/StevenAgYin/banlumo-rh6-sdk)

These are separate hardware/software families, not interchangeable SDKs. Check each repository’s license, missing runtime prerequisites and configuration notes.
