# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="479" height="188" alt="Screenshot from 2025-08-31 17-48-13" src="https://github.com/user-attachments/assets/8663f89b-47f9-40bc-b6b8-8363e4685b91" />



cat < file2
## OUTPUT
<img width="348" height="148" alt="Screenshot from 2025-08-31 17-52-22" src="https://github.com/user-attachments/assets/11a23100-25d9-4254-b76b-e96b51b3bfa8" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="341" height="86" alt="Screenshot from 2025-08-31 17-53-11" src="https://github.com/user-attachments/assets/cd723b1e-5450-4ce6-8721-ac728d1e79ea" />

comm file1 file2
 ## OUTPUT
<img width="369" height="179" alt="Screenshot from 2025-08-31 17-53-45" src="https://github.com/user-attachments/assets/7d7740c8-e1e4-497e-92d8-fc4172408beb" />


 
diff file1 file2
## OUTPUT
<img width="384" height="231" alt="Screenshot from 2025-08-31 17-54-13" src="https://github.com/user-attachments/assets/2f398698-ac27-455c-bda1-9d9a8fa9c1b4" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT




cut -d "|" -f 1 file22
## OUTPUT
<img width="385" height="90" alt="Screenshot from 2025-08-31 18-02-51" src="https://github.com/user-attachments/assets/28ca4dfc-4e56-44b4-8a87-6093d09b0b05" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="385" height="90" alt="Screenshot from 2025-08-31 18-02-58" src="https://github.com/user-attachments/assets/6c339b7b-b82b-4c4c-83bf-83a8f549a3de" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="382" height="73" alt="Screenshot from 2025-08-31 18-06-04" src="https://github.com/user-attachments/assets/e2819387-5f5c-4181-bbaa-0669c4f02614" />



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT
<img width="405" height="47" alt="Screenshot from 2025-08-31 18-11-26" src="https://github.com/user-attachments/assets/79865e71-62c1-456d-b8cd-24400d26ce46" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="480" height="64" alt="Screenshot from 2025-08-31 18-11-35" src="https://github.com/user-attachments/assets/baafec32-e4ce-420c-aff4-189eb65cfbb7" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="495" height="61" alt="Screenshot from 2025-08-31 18-11-47" src="https://github.com/user-attachments/assets/1f966f11-3ea7-4dc6-86d3-af803248a1a0" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="626" height="51" alt="Screenshot from 2025-08-31 18-16-03" src="https://github.com/user-attachments/assets/220f13b1-2804-4a95-9fb1-54d5e4106267" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="618" height="87" alt="Screenshot from 2025-08-31 18-16-22" src="https://github.com/user-attachments/assets/789638b2-e412-47ee-8fc7-c3e9b4a189b0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="613" height="69" alt="Screenshot from 2025-08-31 18-21-05" src="https://github.com/user-attachments/assets/b49ce8e7-d320-4484-a533-c8aecb13ce50" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="613" height="69" alt="Screenshot from 2025-08-31 18-21-10" src="https://github.com/user-attachments/assets/3995f249-3c37-417d-8073-fdb8e5bebc83" />



egrep '(world$)' newfile 
## OUTPUT
<img width="452" height="83" alt="Screenshot from 2025-09-01 10-10-25" src="https://github.com/user-attachments/assets/3ccad627-99a6-442b-a36b-4e1dc8b9a884" />



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="452" height="83" alt="Screenshot from 2025-09-01 10-10-32" src="https://github.com/user-attachments/assets/f37ec4e6-a481-4af3-9f0a-7adfe8c7f181" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="446" height="56" alt="Screenshot from 2025-09-01 10-10-40" src="https://github.com/user-attachments/assets/dcc57e4e-82f5-4958-9ada-3de3c802b74d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="471" height="65" alt="Screenshot from 2025-09-01 10-10-53" src="https://github.com/user-attachments/assets/32539b1e-4239-4e2b-ad8f-a3995a2b4a1d" />


egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT
<img width="471" height="65" alt="Screenshot from 2025-09-01 10-11-00" src="https://github.com/user-attachments/assets/98b98166-b91f-4b80-9657-cc04f35fc1af" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="489" height="86" alt="Screenshot from 2025-09-01 10-11-12" src="https://github.com/user-attachments/assets/4de53d9e-4e1f-4700-a1e4-38e7ffb2ed0b" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="508" height="65" alt="Screenshot from 2025-09-05 13-00-02" src="https://github.com/user-attachments/assets/a055223e-b9d3-4055-a7ce-7eb8a5135ddc" />



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="515" height="205" alt="Screenshot from 2025-09-05 13-01-44" src="https://github.com/user-attachments/assets/12c4152b-3396-4596-96ca-a7f2e8c339d2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="515" height="205" alt="Screenshot from 2025-09-05 13-02-10" src="https://github.com/user-attachments/assets/eeea5309-3a11-4146-a2de-9b7e72ca6a49" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="515" height="205" alt="Screenshot from 2025-09-05 13-04-05" src="https://github.com/user-attachments/assets/5ab47fc5-a37a-44b7-a83b-d3145c8f7f1c" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="516" height="136" alt="Screenshot from 2025-09-05 13-04-42" src="https://github.com/user-attachments/assets/6533d4d5-13e3-4999-ac90-e7d82fed620d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="526" height="96" alt="Screenshot from 2025-09-05 13-05-22" src="https://github.com/user-attachments/assets/da631b72-af6a-4ec9-a06d-dd320c00f5e8" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="540" height="79" alt="Screenshot from 2025-09-05 13-05-55" src="https://github.com/user-attachments/assets/c0da8470-a7d9-402c-aab8-1b94afb35bd3" />



seq 10 
## OUTPUT
<img width="547" height="224" alt="Screenshot from 2025-09-05 13-06-14" src="https://github.com/user-attachments/assets/e92f4bf4-d726-4ee9-ab1a-aee3c5f07a95" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="541" height="97" alt="Screenshot from 2025-09-05 13-07-09" src="https://github.com/user-attachments/assets/c913bfce-eeb8-4a87-a2a9-b45d6cd26002" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="541" height="97" alt="Screenshot from 2025-09-05 13-07-34" src="https://github.com/user-attachments/assets/51e508f5-88ac-4830-8572-abee3eea4cb7" />



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="446" height="98" alt="Screenshot from 2025-09-07 13-51-59" src="https://github.com/user-attachments/assets/46bbdd4b-c239-4d58-a91e-76ea711b348f" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="444" height="120" alt="Screenshot from 2025-09-07 13-55-00" src="https://github.com/user-attachments/assets/6da4408c-b3f1-46f1-98ac-b7456554e1e5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="532" height="211" alt="Screenshot from 2025-09-07 13-55-48" src="https://github.com/user-attachments/assets/197e50a7-283d-4fbe-ac92-3e2f52f558f8" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="539" height="102" alt="Screenshot from 2025-09-07 13-57-33" src="https://github.com/user-attachments/assets/8d208fe6-75da-478b-88a6-7ba1aeae69be" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="539" height="102" alt="Screenshot from 2025-09-07 13-57-59" src="https://github.com/user-attachments/assets/e75f927e-7588-47bf-a49c-8743999ceef5" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="570" height="111" alt="Screenshot from 2025-09-07 14-00-11" src="https://github.com/user-attachments/assets/7be0491b-e00d-4526-9674-ee3d0bda0e91" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1065" height="736" alt="Screenshot from 2025-09-07 14-01-49" src="https://github.com/user-attachments/assets/999800e5-8aa6-4b23-b088-021b5e8bf571" />


tar -xvf backup.tar
## OUTPUT
<img width="1072" height="1028" alt="Screenshot from 2025-09-07 14-02-50" src="https://github.com/user-attachments/assets/83c2aae0-b24e-4d2b-bf18-0f2957db6e0d" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
