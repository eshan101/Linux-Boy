grep - print lines matching a pattern
## Terminal commands

Search standard output (i.e. a stream of text)
`grep [options] "search string"`

Search for an exact string in file:
`grep [options] "search string" path/to/file`

Print lines in myfile.txt containing the string "mellon"
`grep 'mellon' myfile.txt`


## Grep Options

| `-i` | grep -i ^DA demo.txt                     | Forgets about case sensitivity                       |
| ---- | ---------------------------------------- | ---------------------------------------------------- |
| `-w` | grep -w "of" demo.txt                    | Search only for the full word                        |
| `-A` | grep -A 3 'Exception' error.log          | Display 3 lines after matching string                |
| `-B` | grep -B 4 'Exception' error.log          | Display 4 lines before matching string               |
| `-C` | grep -C 5 'Exception' error.log          | Display 5 lines around matching string               |
| `-r` | grep -r 'eshan_at_linux' /var/log/nginx/ | Recursive search _(within subdirs)_                  |
| `-v` | grep -v 'warning' /var/log/syslog        | Return all lines which don't match the pattern       |
| `-e` | grep -e '^al' filename                   | Use regex _(lines starting with 'al')_               |
| `-E` | grep -E 'ja(s\|cks)on' filename          | Extended regex _(lines containing jason or jackson)_ |
| `-c` | grep -c 'error' /var/log/syslog          | Count the number of matches                          |
| `-l` | grep -l 'robot' /var/log/*               | Print the name of the file(s) of matches             |
| `-o` | grep -o search_string filename           | Only show the matching part of the string            |
| `-n` | grep -n "go" demo.txt                    | Show the line numbers of the matches                 |

## Using the grep command with piping

`cat /etc/passwd | grep "search word"`