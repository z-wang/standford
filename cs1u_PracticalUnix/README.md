Practical Unix
================
Course Web: https://practicalunix.org/
----------------
default: https://code.google.com/p/samking-config-files/source/browse/#git
video lecture: http://openclassroom.stanford.edu/MainFolder/CoursePage.php?course=PracticalUnix

----------------
important notes:

***************zsh globbing*****************

use zsh

chsh to change default shell

echo **/*(*)

echo **/*    -> recursivly show all the files

ls ** -al

echo **/*(rwxAIERWX)

echo **/*(rw)

echo **/*(mM-5)  -> all files modified within last 5 months, [a m c],[Mmwh]

echo **/*(mm+1)

echo **/*(a+1)    ->access a day ago

echo **/*(*m-1)

echo **/*(.m-1)

echo **/*(L+5)   ->file greater than 5 bytes, m for mb, k for kb

diff fromfile1 tofile2   -y --width = 80 mean in the same screen two columns, -b will ignore inline spaces and -B will ignore blank lines

find path command name: 

find . -name "*resume"

find / -perm a=rwx, g=rwx, u=rwx   all,group,user

find . -name "*resume*" -exec echo {} \;

find . -name "*resume*" -exec cp {} \;

locate "*resume*"      need to update db using "sudo updatedb", the search speed will be much faster than find, but cannot search a sepcified dir, the whole system

locate "*resume*" | grep dir    for a sepecific dir.

------------------------

GDB debug for C files:

Compile using gdb with -g, or using -g3 -gdwarf-2 if you want to include things like preprocessor macros. Probably also use -O0 to turn optimizations off.

help

r (run)

list [line|function]

b (break) [file:](line|function)

n (next)

p (print)

disp (display)

c (continue)

q (quit)

bt (backtrace)

up

down

ena (enable)

disa (disable)

delete

info - if you just say info, it tells you what you can get info aboute. some useful things to get info about include args, locals, registers, threads, breakpoints, and frame.

s (step)

ENTER (repeat the last command)

until

finish

return - immediately returns without executing more lines of code until end

jump - immediately goes to line without executing more lines of code inbetween

x (examine) - p and x can look at data as any given type. /i (instruction) /d (digit) /c (character) and /s (string) are useful. with x, you can say something like x/10i to examine 10 instructions starting at the memory address you give it.
watch - sets a watchpoint to notify you whenever a variable's value changes

make

shell

---------------------

Permission:

r:4, w:2, x:1

user, group, others:

chmod 777

chmod u-x some

chmod a+x some

---------------------

scp- copy some through network

scp samking@pup.stanford.edu:foo foo   -> copy the file to current directory

scp foo pup.stanford.edu:bar   -> auto find samking@pup but need password

wget- get something from internet

wget http://stanford.edu/~samking/cslu/scp.mp4  ->save to current directory

----------------------

cURL- do everything about url

curl google.com   -> you will have the page

curl http://google.com:80

curl -L GOOGLE.COM   -> will auto redirect to the new page

curl -O google.com/index.html  -> save this file to current directory

curl -o google.com/index.html google -> save as google

curl --libcurl foo.c google.com 

curl "http://www.googgle.com/serach#q=foo"

curl http://www.htmlcodetutorial.com/cgi-bin/mycgi.pl -d realname=Sam 

curl http://www.example.com --data0urlencode "foo=&bar"

curl stanford.edu/~samking/ -I   -> show headline, -i head and content, -v, detail information **INHERE, you can change User-Agent in curl and get information from internet， 

curl htto://www.htmlcodetutorial.com/cgi-bin/mycgi.pl -d "foo=bar" -d "bar=dzx" -v  -> get information of POST

curl ... -H "foo: bar"   -> add to head line

curl ... -H "Contentlength: "  -> deduce content length

curl ... -X put   -> CHANGE METHOD from get/post to put

curl whatismyipaddr -A "Mozilla/4.05"  -> change user agent

------------------------

Python subprocess and os library

os.chdir

os.system

------------------------

**piping: output to another input

grep cat text1 | grep bird

**redirect to another file: use >, continue >>

grep cat text1 > templfile

somecommand 2> /dev/null   -> nothing will happen

**redirect a file to a standard input

echo "sentence" > name

command < name

**Tee: ouput to stdout and a file

ping google.org | tee ping

tee ping == cat ping | and save to a file




















