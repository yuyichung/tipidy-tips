# Text Processing

- Retrieving the middle chunk of a file: sed -e '%start line, %end lined' | head -n -%number of lines to cut off
- If you need to grep a text file that is interpreted as a binary file, use "grep -a" (works with zgrep also)