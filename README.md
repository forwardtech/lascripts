# lascripts
Shell Scripts Library for Log Analysis
--------------------------------------

This contains commonly used utilities for general Log Analysis.  Comes 
in handy when doing operations and processing large logs files. Useful for troubleshooting 
and monitoring general application systems, network and security trouble shooting.  

Note: This is a on going project. Please report issues, suggestions and your general comments

How to use:
-----------

1. You could use some of these tools directly.
2. You can use as utility library and write your customized scripts 
     (I expect thats what most people might do). 
3. You can also take some of these and modify to suit your own needs too.

How to Install:
---------------

i.   Download the lascripts.tar
ii.  Untar it under any directory (tar -xvf lascripts.tar)
iii. You will see the following directory structure
       lascripts/bin     - Location of the scripts
       lascripts/testing - Contains simple files for testing
       lascripts/doc     - Documentation  (includes a TIPS.README for specific tips you may find 
                           useful in your log analysis)
iv.  Add the lascripts/bin to your PATH variable (ex. PATH=$PATH:..lascripts/bin)


List of Scripts and usage:
==========================

1. d2u  - Converts dos to unix format

   Usage: d2u filename

   Converts dos format to unix format and *overwrites* the file
   (Its a simple remove of ^M at the end of the line)

2. dups - Find duplicate log files and report them

   Usage: dups [directory_path]

   Find duplicate files under the directory_path specified
   uses current directory if there is no argument specified

3. ffind - Find a file under the current directory recursively
  
   Usage: ffind filename

   Finds location of filename. Recursively searching all subdirectories

4. fsplit - Splits a file to multiple individual files

   Usage: fsplit -a|s|e|o filename pattern

   Splits a file to multiple individual files - splitting where the pattern occurs
    -a pattern seen anywhere in the line"
    -s pattern occurs at the start"
    -e pattern occurs at the end"
    -o only pattern in the line"

5. gdate - List all the lines in a log files with the specified time stamp

   Usage: gdate file_name day month year hr min sec
          ex: gdate first.txt 17 Dec 2015 21 40

   List all the lines in a log files with the specified date and time

6. gfind - Find files containing a pattern

   Usage: gfind pattern

   List files containing a pattern recursively searching all subdirectories

7. isip4 - Checks ip address format

   Usage: isip4 ip4_address"

   Return 0 if its a valid and 1 if its invalid"

8. isip6 - Checks ipv6 format

   Usage: isip6 ipv6_address
   Return 0 if its a valid and 1 if its invalid

9. ismac - Checks MAC address format

   Usage: ismac mac_address

   Return 0 if its a valid and 1 if its invalid

10. numit - Number the fields in an output.

    Usage: <input> | numit  [field_separator]

    Ex.
    cat file1 | numit  

    cat file1 | numit :
       (number the fields separated by ':')

    Numbers the fields in an output. Useful when you want to capture a particular field 
    in a long log line. Instead of counting manually or doing a trail and error
    you could use this script quickly to get the number(s) of the fields you want to process.

11. rep - Replaces words in a file

    Usage: rep filename word replaceword

    Scans the 'filename' and replaces 'word' with 'replaceword'"

12. toepoch - Converts a Date to Epoch time

    Usage: toepoch date"

    Converts date to 'epoch' time". Useful when doing date/time arithmetic and comparisons
    Ex. toepoch "Jan 1 2015 20:1:1"

