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
<img width="416" height="66" alt="Screenshot from 2025-09-13 14-55-53" src="https://github.com/user-attachments/assets/7c944069-fe79-48fc-a4ed-aa943f9bce74" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="425" height="88" alt="Screenshot from 2025-09-13 14-56-29" src="https://github.com/user-attachments/assets/892d1516-6810-4099-a535-1745016f0492" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="425" height="88" alt="Screenshot from 2025-09-13 14-57-44" src="https://github.com/user-attachments/assets/2cad3a9e-edb4-4a73-9ae1-2ae789ba8662" />


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
<img width="425" height="88" alt="Screenshot from 2025-09-13 14-58-02" src="https://github.com/user-attachments/assets/247aebc6-0ccb-4e60-ba43-d80b8f103519" />




grep hello newfile 
## OUTPUT
<img width="425" height="88" alt="Screenshot from 2025-09-13 14-58-02" src="https://github.com/user-attachments/assets/6a161de6-e757-4216-8935-8acdfb56a461" />





grep -v hello newfile 
## OUTPUT
<img width="435" height="105" alt="Screenshot from 2025-09-13 14-58-35" src="https://github.com/user-attachments/assets/2b7ff06a-a297-426c-8ce2-0e8ae22dabba" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="487" height="68" alt="Screenshot from 2025-09-13 14-59-02" src="https://github.com/user-attachments/assets/c82ace44-a56d-4a08-a53c-5bdf0b7f0a29" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="495" height="61" alt="Screenshot from 2025-08-31 18-11-47" src="https://github.com/user-attachments/assets/1f966f11-3ea7-4dc6-86d3-af803248a1a0" />




grep -R ubuntu /etc
## OUTPUT
<img width="735" height="443" alt="Screenshot from 2025-09-13 16-59-29" src="https://github.com/user-attachments/assets/5936cd7c-2ff6-4075-8a3e-032005431961" />


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
<img width="621" height="64" alt="Screenshot from 2025-09-13 17-03-42" src="https://github.com/user-attachments/assets/761ea19d-520f-4eba-aa03-f4ec9aa42e1e" />


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
<img width="617" height="60" alt="Screenshot from 2025-09-13 17-05-59" src="https://github.com/user-attachments/assets/709ee0f1-f9ce-4f1f-92d4-5421d975583d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="452" height="83" alt="Screenshot from 2025-09-01 10-10-32" src="https://github.com/user-attachments/assets/f37ec4e6-a481-4af3-9f0a-7adfe8c7f181" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="446" height="56" alt="Screenshot from 2025-09-01 10-10-40" src="https://github.com/user-attachments/assets/dcc57e4e-82f5-4958-9ada-3de3c802b74d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="628" height="62" alt="Screenshot from 2025-09-13 17-07-43" src="https://github.com/user-attachments/assets/1608786f-9503-4ae1-b464-bbf2178da1e8" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="628" height="62" alt="Screenshot from 2025-09-13 17-07-43" src="https://github.com/user-attachments/assets/cb1590e4-1c31-421f-9f61-34cc71c377d2" />


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
<img width="635" height="60" alt="Screenshot from 2025-09-13 17-10-15" src="https://github.com/user-attachments/assets/cfef66a8-1e28-4ea6-81ac-a8099aea2bcd" />




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
<img width="646" height="113" alt="Screenshot from 2025-09-13 17-13-58" src="https://github.com/user-attachments/assets/f0fc3950-63cf-4a28-8765-126614a2501b" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="644" height="103" alt="Screenshot from 2025-09-13 17-27-38" src="https://github.com/user-attachments/assets/e8723c09-a4e1-435e-8088-38eb637fa738" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="644" height="97" alt="Screenshot from 2025-09-13 17-28-09" src="https://github.com/user-attachments/assets/7fb86193-b9c3-41ac-9dd7-f8a313e5336a" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="644" height="97" alt="Screenshot from 2025-09-13 17-33-09" src="https://github.com/user-attachments/assets/d1dd1d7f-fc9e-4492-b2e6-fdaaa1f3bbee" />



sed -n '2,4{s/$/*/;p}' file23
## output
<img width="644" height="97" alt="Screenshot from 2025-09-13 17-33-36" src="https://github.com/user-attachments/assets/18a8d404-e8de-4fc0-98d8-d41d808d9255" />


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
 <img width="512" height="65" alt="Screenshot from 2025-09-07 22-29-35" src="https://github.com/user-attachments/assets/af8f776a-7584-431a-8717-114f605b1583" />

gunzip backup.tar.gz
## OUTPUT
<img width="699" height="408" alt="Screenshot from 2025-09-07 22-30-10" src="https://github.com/user-attachments/assets/503370e5-ae94-41a8-8e66-39111d7449f9" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1110" height="134" alt="437512669-d43e1c06-4292-4f0d-91d0-79389355bfe8" src="https://github.com/user-attachments/assets/37383388-a816-409a-9a06-0060f3d0918c" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="942" height="161" alt="437513073-880f5adc-41d9-4385-bdb0-85eec925813b" src="https://github.com/user-attachments/assets/e6227eb7-17b7-4400-a2bb-cd048c299198" />


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
<img width="901" height="507" alt="437513340-02e98cb0-0823-4a6d-9841-1a7213aef79b" src="https://github.com/user-attachments/assets/fd8c2134-e806-45ef-9867-b7e99b5f30e6" />

 
ls file1
## OUTPUT
<img width="773" height="35" alt="437513490-2e852b13-1588-45e0-a9b1-ec8e48fab55c" src="https://github.com/user-attachments/assets/916e4c97-4639-4385-8023-3fb09dd7035b" />

echo $?
## OUTPUT 
<img width="773" height="45" alt="437513639-2d221705-b0a6-4cff-9c7a-63d35e181b21" src="https://github.com/user-attachments/assets/d65e6049-33ca-43b7-ad45-314ebd278cbf" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="769" height="185" alt="437513753-920d7501-867e-4eaf-bf9d-a01369f9f077" src="https://github.com/user-attachments/assets/ece15959-8c14-4d07-a26b-b299d95ffbdc" />


 
abcd
 
echo $?
 ## OUTPUT
<img width="769" height="185" alt="437513908-6e3ff907-6662-465b-b873-3caf3a85d86c" src="https://github.com/user-attachments/assets/f8668ff0-9ec7-4189-b0d3-6bf440b62fbc" />


 
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
<img width="840" height="186" alt="437514068-68445397-8903-455a-8944-05a9c743bb77" src="https://github.com/user-attachments/assets/c7c21abe-d8e2-4fa8-b903-cc75f60d1bc0" />


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
<img width="824" height="47" alt="437514310-a6269750-5552-40c1-a460-c0102d92478b" src="https://github.com/user-attachments/assets/72f00cf6-bf7e-4887-b394-7329eb3c98c0" />

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

<img width="820" height="82" alt="437514439-7bc5d0e0-8ef8-47b6-9be5-1cb0cb322bf9" src="https://github.com/user-attachments/assets/b345d737-6ad9-4ff0-8785-a603ea338b0f" />



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
## OUTPUT

<img width="792" height="62" alt="437514567-bd3fa98c-918f-4fe9-87e8-83aa78955a55" src="https://github.com/user-attachments/assets/848acb65-c38b-4977-b575-ded1d0d1994e" />

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
## OUTPUT

<img width="820" height="82" alt="437514704-0b1ec023-85da-4ffb-bd59-bb43312cfe95" src="https://github.com/user-attachments/assets/2fb12f18-a173-4f73-91f6-6dbd1559be63" />

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

<img width="823" height="44" alt="437514825-e13003ae-4cf7-4e8a-a9c8-23f36be3cd84" src="https://github.com/user-attachments/assets/b35befcb-380f-42f0-909d-38c5768fea2a" />


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

<img width="823" height="44" alt="437515548-ba3cd1c8-2e21-42aa-ad1f-7e201567440e" src="https://github.com/user-attachments/assets/65f8108a-2f5d-48a4-8cc3-1a413cb3e2bc" />

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


 <img width="823" height="44" alt="437515735-611dd7e7-6094-4ed4-bbc2-dc699bfbec7e" src="https://github.com/user-attachments/assets/0d87c934-1d78-4e61-9bd6-30948de2340b" />

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

<img width="829" height="203" alt="437516171-766969d6-cdba-4352-b458-bc18ddd0f0d4" src="https://github.com/user-attachments/assets/5ed1ff6f-9899-4955-bd0b-ddfa6aa220c7" />

 
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


 <img width="829" height="100" alt="437516323-82ca8200-02c3-4f86-b3af-56fb87280f7c" src="https://github.com/user-attachments/assets/e90dd0a9-2bcc-497d-b99a-1dd0d754f1e2" />

 
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

<img width="789" height="128" alt="437516437-09a67174-2cc7-46ba-bc9e-2045100834c6" src="https://github.com/user-attachments/assets/09c271d6-965c-472a-be58-86df676d11b7" />

 
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


 <img width="784" height="80" alt="437516569-63454b29-1600-4e43-864f-c532f36c497a" src="https://github.com/user-attachments/assets/0c5fcbd0-e01c-41e9-9f02-289a0262eb5c" />

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

<img width="787" height="152" alt="437516740-a73c67cd-2597-46f9-abef-d0b4ae0703bf" src="https://github.com/user-attachments/assets/1db22bba-c11e-483d-880b-d9d5ce9930a5" />


 
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

<img width="816" height="113" alt="437516934-b80b5ac5-8376-4764-8099-a472f57eccc0" src="https://github.com/user-attachments/assets/7753e6a0-2e1e-43da-b7c7-a0830ed133e2" />

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

<img width="833" height="236" alt="437517946-22bb8726-77f3-4928-902a-53312da037e3" src="https://github.com/user-attachments/assets/acd3800a-c013-493a-a61d-578725d21502" />

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
 
<img width="825" height="79" alt="437518303-57b3ca85-f61c-4600-9db7-4488bcabb26e" src="https://github.com/user-attachments/assets/4499234a-7e2c-4c9c-a022-d1412b0d6475" />

 
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

<img width="837" height="113" alt="437518629-54fc3698-e66d-4238-9dd7-4eea6acd66b3" src="https://github.com/user-attachments/assets/89a52cca-bd84-4eb2-a2f7-36298821bd07" />

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

 <img width="837" height="113" alt="437518629-54fc3698-e66d-4238-9dd7-4eea6acd66b3" src="https://github.com/user-attachments/assets/e9931c84-c5d3-4891-ae6a-2043ede64b53" />

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

<img width="799" height="57" alt="437518886-d518a631-c2f0-4a8c-99aa-99bb59b92783" src="https://github.com/user-attachments/assets/a735034a-049d-4398-8bda-c5daa5c977d2" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="808" height="57" alt="437519922-739e8f84-e5ce-4d44-9376-d9fdb6620001" src="https://github.com/user-attachments/assets/b342f4ae-09c4-43b2-a736-f93440713502" />



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
 
<img width="807" height="37" alt="437520149-7a77ec0f-e0c6-4f97-95f3-1bc04bc59320" src="https://github.com/user-attachments/assets/30d4ddc9-abf2-4dc2-af07-61eec5b654c2" />

 
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

 <img width="869" height="72" alt="437521449-49d19cc0-df8d-4b55-9b44-8850ea589337" src="https://github.com/user-attachments/assets/e60f632c-44c1-42a8-accb-8992034bda99" />

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

 <img width="895" height="255" alt="437521835-41c21647-4337-4f8f-8ed9-8c252dd99873" src="https://github.com/user-attachments/assets/2b7a206e-22e6-4973-935a-26c2ee745467" />

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

<img width="839" height="72" alt="437522071-bc055139-9155-41b5-a25f-8ba5e785fda1" src="https://github.com/user-attachments/assets/788ae715-9041-4365-b013-838f195f7c49" />


# RESULT:
The Commands are executed successfully.
