# Linux File Permissions

## Objective

Practice Linux file ownership and permission management using a test file.

## Initial Permission

Command:
ls -l tests/permission-test.txt

Result:
-rw-------. 1 u0_a203 u0_a203 0 Sep 16 21:12 tests/permission-test.txt

The owner had read and write permission, while group and others had no permission.

## Changing Permission

Command:
chmod 400 tests/permission-test.txt

Result:
-r--------. 1 u0_a203 u0_a203 0 Sep 16 21:12 tests/permission-test.txt

Permission 400 means:

- Owner: read
- Group: no permission
- Others: no permission

## Verification

Command:
echo "permission test" > tests/permission-test.txt

Result:
bash: tests/permission-test.txt: Permission denied

The write operation was rejected because the owner no longer had write permission.

## Conclusion

This exercise demonstrated practical Linux permission management using ls -l and chmod.

The permission change was verified through an actual write attempt, confirming that the configured access control was enforced.
