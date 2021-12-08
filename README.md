 **oneLiners**
 ---
 *Useful things (for me, at some point) that can be done in one line using shell script*

1. Comment out all lines of a text file and writes the command output in a new text file;

`sed -E '/^[[:space:]]*(#|$)/! s/^/#/' [file] >> [newfile]`

2. Do the same thing as the previous command, however, overwrites the original file with the changes. Use this form very carefully!

`sed -iE '/^[[:space:]]*(#|$)/! s/^/#/' [file]`

3. The following command allows define a line range to comment out and sends the output to a new text file.

`sed -nE -e 'startline,endline p' [file] | sed -E '/^[[:space:]]*(#|$)/! s/^/#/' >> [newfile]`

