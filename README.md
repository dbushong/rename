Overview
--------

`rename` is a script which renames files according to a perl expression.

Apparently Larry Wall wrote such a script years ago (with almost identical 
syntax to mine!  great minds think alike!), but I didn't know that or I wouldn't
have reinvented the wheel.  If I do say so, this version's a bit better, and
safer when it comes to clobbering your files.

Examples
--------

    % rename 's/\.bak$//' *.bak           # strips the .bak off all .bak files
    % rename 's/\d+$/$&+1/e' messages.*   # incremements numeric suffixes
    % rename '$_ .= "-" . time()' log*    # adds -seconds-since-epoch to files
