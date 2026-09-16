Linux System & Networking Lab

A practical Linux system administration and networking laboratory built in a Termux/Android environment.

This project focuses on understanding Linux fundamentals through hands-on testing, documentation, troubleshooting, and verification rather than only memorizing commands.

Environment

- Platform: Android 11 / Termux
- Linux Kernel: 4.19.127
- Architecture: ARMv7 (32-bit)
- Shell: Bash
- User: "u0_a203"

Objectives

- Understand Linux system and network fundamentals
- Practice user and group management concepts
- Understand Linux file permissions
- Inspect running processes
- Analyze system and security-related logs
- Perform basic network troubleshooting
- Understand platform-specific administration limitations

Lab Areas

1. System & Network Baseline

Verified:

- Network interface configuration
- IPv4 addressing
- Routing
- Default gateway connectivity
- Internet connectivity
- DNS resolution
- HTTPS connectivity

Evidence:

""docs/system-baseline.md"" (docs/system-baseline.md)

2. Users & Groups

Practiced:

- Identifying the current user
- UID and GID
- Primary and supplementary groups
- SELinux security context

Evidence:

""docs/users-groups.md"" (docs/users-groups.md)

3. File Permissions

Practiced:

- Reading file permissions with "ls -l"
- Changing permissions with "chmod"
- Verifying access restrictions through an actual write attempt

Example:

"chmod 400"

Evidence:

""docs/permissions.md"" (docs/permissions.md)

4. Process Management

Practiced:

- "ps"
- "ps -ef"
- "ps -A"
- "pstree"
- Understanding PID and PPID
- Observing parent-child process relationships

Evidence:

""docs/processes.md"" (docs/processes.md)

5. Log Analysis

Practiced:

- Collecting Android system logs with "logcat"
- Identifying informational, warning, and error messages
- Observing Android SELinux audit events
- Interpreting "avc: granted" entries in context

Evidence:

""docs/logs.md"" (docs/logs.md)

6. Service Management

Documented the differences between a conventional Linux distribution using systemd and the Android/Termux environment.

Rather than assuming "systemctl" is available, the lab records the platform limitation and uses process inspection where appropriate.

Evidence:

""docs/services.md"" (docs/services.md)

Troubleshooting Approach

The lab follows a simple troubleshooting workflow:

1. Identify the problem
2. Collect evidence
3. Check the relevant system component
4. Test the suspected cause
5. Verify the result
6. Document the findings

For example, network troubleshooting was performed by separating:

"Gateway → Internet → DNS → HTTPS"

This makes it possible to determine which layer is functioning or requires further investigation.

Key Skills Demonstrated

- Linux command-line fundamentals
- Network troubleshooting
- User and group inspection
- File permission management
- Process inspection
- Log analysis
- Basic security concepts
- Technical documentation
- Platform limitation awareness

Project Structure

linux-system-networking-lab/
├── README.md
├── docs/
│   ├── system-baseline.md
│   ├── users-groups.md
│   ├── permissions.md
│   ├── processes.md
│   ├── logs.md
│   └── services.md
└── tests/

Notes

This laboratory is performed in Termux on Android rather than a conventional Linux server.

Some Linux administration features, especially system-level service management, are therefore limited by the Android/Termux environment.

The project documents those limitations instead of presenting unsupported functionality as if it were available.

Status

In progress

Future work may include additional troubleshooting scenarios, security auditing exercises, and more advanced Linux administration tasks.
