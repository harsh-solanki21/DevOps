# File Ownership and Permissions in Linux

## File Ownership

Every file and directory in Linux has three types of owners:

1. **User (Owner)**

   - The person who created the file.
   - Also sometimes called the owner.

2. **Group**

   - A user-group can contain multiple users.
   - All users in the group have the same access permissions to the file.

3. **Other**
   - Any other user who has access to the file.
   - Neither the creator of the file nor belongs to the group owning the file.
   - Essentially, everybody else.

<br />

## File Permissions

Each file and directory has three types of permissions defined for all three owners:

1. Read (r)
2. Write (w)
3. Execute (x)

### Permission Indicators

- `-` indicates a regular file
- `d` indicates a directory
- `l` indicates a symbolic link
- `rwx` Read, Write, and Execute permissions for the file owner
- `r--` Read, Write, and Execute permissions for the group owning the file
- `r--` Read, Write, and Execute permissions for other users

## Changing File/Directory Permissions with `chmod`

The `chmod` command can be used in two ways:

#### 1. Absolute (Numeric) Mode

| Number | Permission Type        | Symbol |
| ------ | ---------------------- | ------ |
| 0      | No Permission          | ---    |
| 1      | Execute                | --x    |
| 2      | Write                  | -w-    |
| 3      | Execute + Write        | -wx    |
| 4      | Read                   | r--    |
| 5      | Read + Execute         | r-x    |
| 6      | Read + Write           | rw-    |
| 7      | Read + Write + Execute | rwx    |

Example: `chmod 764 filename`

#### 2. Symbolic Mode

| Operator | Description                                         |
| -------- | --------------------------------------------------- |
| +        | Adds a permission                                   |
| -        | Removes a permission                                |
| =        | Sets the permission (overrides earlier permissions) |

#### User Denotations

- `u`: user/owner
- `g`: group
- `o`: other
- `a`: all

<br />

**Examples:**

1. Setting permissions for other users:

```bash
chmod o=rwx filename
```

2. Adding execute permission to the user group:

```bash
 chmod g+x filename
```

3. Removing read permission for the user:

```bash
 chmod u-r filename
```

4. Adding executable permission to the file:

```bash
 chmod +x filename
```

5. Changing Ownership and Group:

```bash
# to change ownership of a file/directory
chown user

# to change the user as well as group for a file or directory
chown user:group filename
```
