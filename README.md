 oneLiners - 
 Useful things (for me, at some point) that can be done in one line using shell script


sed -E '/^[[:space:]]*(#|$)/! s/^/#/' >> [newfile]

sed -nE -e 'startline,endlinep' [file] | sed -E '/^[[:space:]]*(#|$)/! s/^/#/'

