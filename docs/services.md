# Linux Service Management

## Objective

Understand service management in a Termux/Android environment and identify the differences from a traditional Linux distribution using systemd.

## Environment

The lab is running on Android 11 through Termux.

Android does not use systemd as the service manager for the Termux user environment.

## Service Management Limitation

On a traditional Linux server using systemd, services are commonly managed with commands such as:

systemctl status <service>

systemctl start <service>

systemctl stop <service>

In this Termux/Android environment, systemd is not available as the service manager for the user environment.

Therefore, `systemctl` is not used as the primary service-management method in this lab.

## Practical Approach

Instead of assuming that every Linux command works identically across platforms, service and process behavior must be inspected according to the operating environment.

Process inspection was performed using:

ps
ps -ef
pstree

These commands provided visibility into processes running inside the Termux environment.

## Analysis

The exercise demonstrates an important system administration principle:

Linux commands and administration methods can differ depending on the operating environment.

Termux provides a Linux userland on top of Android, but it is not equivalent to a conventional Linux server distribution.

## Conclusion

Service management was documented as an environment limitation rather than simulated as a conventional systemd workflow.

This prevents incorrect conclusions about the capabilities of the Android/Termux environment and demonstrates awareness of platform-specific system administration.	
