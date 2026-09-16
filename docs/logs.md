# Linux & Android Log Analysis

## Objective

Practice reading system logs and identifying relevant events in a Termux/Android environment.

## Log Collection

Command:

logcat -d -t 20

## Observations

The log output contained Android media codec events, including:

CCodec : Created component [c2.android.vorbis.decoder]

The output also contained Codec2 and FMQ warning/error messages related to media processing.

The log contained SELinux audit events associated with Termux execution, including:

avc: granted { execute }

The events included security context information such as:

scontext=u:r:untrusted_app_27:...

and:

tcontext=u:object_r:app_data_file:...

## Analysis

The log demonstrates that Android provides system and security-related logging that can be inspected from Termux when access is available.

The `avc: granted` entries indicate that the logged access was granted. Log messages should be interpreted based on their severity, context, and surrounding events rather than assuming every warning or error represents a system failure.

## Conclusion

This exercise demonstrated basic log collection and analysis using `logcat` in a Termux/Android environment.

The exercise also provided practical exposure to Android SELinux security contexts and system logging.
