# Linux Users & Groups

## Objective

Practice identifying the current Linux user, primary group, supplementary groups, and security context.

## User and Group Information

Command:

id

Result:

uid=10203(u0_a203) gid=10203(u0_a203) groups=10203(u0_a203),3003(inet),9997(everybody),20203(u0_a203_cache),50203(all_a203) context=u:r:untrusted_app_27:s0:c203,c256,c512,c768

## Analysis

The `id` command displays the identity and group membership of the current process.

Key information:

- UID: 10203
- User: u0_a203
- Primary GID: 10203
- Primary group: u0_a203
- Supplementary groups: inet, everybody, u0_a203_cache, all_a203
- SELinux security context: u:r:untrusted_app_27:s0:c203,c256,c512,c768

The `inet` group is associated with network access in the Android environment.

The SELinux context identifies the security domain under which the Termux process operates.

## Group Listing

Command:

id -Gn

Result:

u0_a203 inet everybody u0_a203_cache all_a203

This command displays the names of the groups associated with the current user.

## Conclusion

This exercise demonstrated how to inspect Linux user and group information using `id` and `id -Gn`.

The results also showed how Android adds its own user, group, and SELinux security model on top of the Linux environment.
