# Integration checklist

1. Identify model, side, revision, firmware and matching source version with Banlumo.
2. Obtain approved pinout, voltage/current limits, mounting drawings and stopping procedure for that exact unit.
3. Confirm host Linux, ROS distribution, dependencies and CAN hardware/driver.
4. Review launch files and code before use. Default interfaces and topics are examples; retain protocol identifiers unless coordinated with firmware.
5. Confirm command units, joint indexing, feedback, timeouts and force/current limits. The presence of a safety_check parameter does not certify a safety function.
6. Build in an isolated ROS workspace before connecting hardware; then carry out an agreed guarded bench procedure.

## Known limitations

The repository has not been built by Banlumo on ROS or tested on a hand. Upstream quick-start text and code may differ; verify executable names and launch parameters against source. Python URDFs reference mesh assets that are not bundled. Tactile support, model mapping, runtime dependencies and hardware compatibility require confirmation. This source cannot be used to claim a certified safety system or a production-ready sorting station.
