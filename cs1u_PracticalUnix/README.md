Practical Unix
================
Course Web: https://practicalunix.org/
----------------
default: https://code.google.com/p/samking-config-files/source/browse/#git
video lecture: http://openclassroom.stanford.edu/MainFolder/CoursePage.php?course=PracticalUnix

----------------
important notes:
use zsh
chsh to change default shell
echo **/*(*)
echo **/*    -> recursivly show all the files
ls ** -al
echo **/*(rwxAIERWX)
echo **/*(rw)
echo **/*(mM-5)  -> all files modified within last 5 months
echo **/*(mm+1)
echo **/*(a+1)    ->access a day ago
echo **/*(*m-1)
echo **/*(.m-1)
echo **/*(L+5)   ->file greater than 5 bytes, m for mb, k for kb
