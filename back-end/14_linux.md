# Linux

## How to use the commands

**Requirement**

- Explain the meaning of the command (by Vietnamese)
- Run command with at least 3 options
- Take screenshot of the result

**Example**

`ls`: liệt kê nội dung của folder hiện tại

**Option:**:
- `a`: Liệt kê các tệp và hiển thị quyền, người dùng chủ sở hữu, nhóm chủ sở hữu, ngày sửa đổi / ngày tạo
- `t`: Sắp xếp theo thời gian được sửa đổi
- `S`: Sắp xếp theo kích thước

Tip: Can combine some options to get best result (ex: ls -al -S)

Run and take the screenshot:

`ls -a`

[Image screenshot here]

`ls -t`

[Image screenshot here]

`ls -S`

[Image screenshot here]

**Command list:**
- ls
- man
- cd
- rm
- cp
- mv
- ln -s
- touch
- ps
- top
- tail
- chmod
- ssh
- scp
- grep
- cat
- whoami
- whereis
- which
- tar
- gzip

### User and group

1. Create user `linux_test`
2. Create group `linux_group`
3. Add user `linux_test` to the group `linux_group`.
4. Create a folder `linux_document` with the user owner is `linux_test`
5. Create a user `linux_user` and add to group `linux_group`
6. Add permissions for the folder `linux_document` with:

- User: read + write + execute
- Group: read + write
- Other: - (No permissions)

Run `ll -al` to check permission again  (take screenshot here also)

7. Login by `linux_user` user. Try to create a file `file.txt` inside folder `linux_document`
8. Create user `guest` . Login to user guest and try to create a file `guest.txt` inside folder `linux_document`
9. Delete user `linux_test`, `linux_test`, `guest`
10. Delete group `linux_group`

### SSH/Download and Upload

You just need to learn how to use SSH and upload/download files from the server and list commands to execute it.

**Requirement:**

1. Create a file name with format `[Yourname_php].txt` . Example: Trungtran_php.txt
2. Upload file `[Yourname_php]_php.txt` to folder `\home\ec2-user\linux_practice`
of the remote server .
3. Access to the remote server with  above info, check if the file already uploaded exists in the folder or not.
4. Download the file `server_file.txt` from folder `linux_practice` on the remote server.
