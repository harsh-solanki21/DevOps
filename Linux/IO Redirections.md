# IO Redirections

### Output Redirection

The `>` symbol is used for output (STDOUT) redirection.

`ls -al > listings`
Here the output of command `ls -al` is redirected to file `listings` instead of your screen.

**Note:** Use the correct file name while redirecting command output to a file. If there is an existing file with the same name, the redirected command will delete the contents of that file and then it may be overwritten.

If you do not want a file to be overwritten but want to add more content to an existing file, then you should use `>>` operator.
`ls -al >> listing`

<br />

### Input Redirection

The `<` symbol is used for input (STDIN) redirection.

<br />

### File Descriptor

| File                   | File Descriptor |
| ---------------------- | --------------- |
| Standard Input STDIN   | 0               |
| Standard Output STDOUT | 1               |
| Standard Error STDERR  | 2               |

- we are executing a program names `myProgram`.
  The file descriptor for standard error is `2`.

- Using `2>` we redirect the error output to a file named `errorfile`
  Thus, program output is not cluttered with errors.
  `myProgram 2 > errorsfile`

<br />

- To avoid this, you can pipe the output of the `cat` command to `less` which will show you only one scroll length of content at a time.
  `cat filename | less`
  `cat Filename | more`
- And, you can view the file in digestible bits and scroll down by simply hitting the enter key.

- This command helps in sorting out the contents of a file alphabetically.
  `sort filename`
