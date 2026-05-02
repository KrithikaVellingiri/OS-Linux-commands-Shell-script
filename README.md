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
<img width="377" height="169" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_54_493" src="https://github.com/user-attachments/assets/b8925bb2-c00d-4442-b127-4a8078c693d2" />

cat < file2
## OUTPUT
<img width="348" height="221" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_54_49" src="https://github.com/user-attachments/assets/33e34b18-c0aa-41f8-8e4d-b9d35c8bbdda" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="407" height="80" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_55_35" src="https://github.com/user-attachments/assets/1cb868be-1f2c-4715-9ce8-5d1dc7764b6b" />

comm file1 file2
 ## OUTPUT
<img width="414" height="397" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_56_03" src="https://github.com/user-attachments/assets/a7e7dca2-1c30-49ee-a8cb-c77d8c47c298" />

 
diff file1 file2
## OUTPUT
<img width="621" height="277" alt="VirtualBox_Parrot Security 6 0_02_05_2026_02_42_11" src="https://github.com/user-attachments/assets/fc931732-7324-4698-9164-a64808e2426e" />


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
<img width="352" height="125" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_57_13" src="https://github.com/user-attachments/assets/cb3a475b-a560-4e8f-ab06-dd4679773152" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="383" height="171" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_57_35" src="https://github.com/user-attachments/assets/4763d810-c901-4a86-8f90-15c2864251ed" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="600" height="139" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_59_30" src="https://github.com/user-attachments/assets/6e7eece5-a355-4fbf-a180-3d5c10d8463f" />


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
<img width="600" height="139" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_59_30" src="https://github.com/user-attachments/assets/8fa47279-546e-40a4-846d-6d3808e1e856" />



grep hello newfile 
## OUTPUT
<img width="600" height="139" alt="VirtualBox_Parrot Security 6 0_02_05_2026_00_59_30" src="https://github.com/user-attachments/assets/8fa47279-546e-40a4-846d-6d3808e1e856" />





grep -v hello newfile 
## OUTPUT
<img width="397" height="72" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_00_05" src="https://github.com/user-attachments/assets/c79cac1b-9872-4671-9de1-ef046a458cf8" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="508" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_00_19" src="https://github.com/user-attachments/assets/d431234c-c7b3-4b36-9ab3-f5ed33ec4830" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="527" height="79" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_00_33" src="https://github.com/user-attachments/assets/0fd3ffd8-6a8a-4374-b66b-5f8d3ee24034" />




grep -R ubuntu /etc
## OUTPUT
<img width="527" height="79" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_00_33" src="https://github.com/user-attachments/assets/da74c03f-bfe2-4f01-aff0-6593c74d8419" />



grep -w -n world newfile   
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/233c6551-4236-4a82-984f-6acb6ee4b555" />


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
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/e03cd2ce-8c2b-4978-b7eb-38639eca439b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/0cdd6851-f44e-4d60-a162-7dacf43f1b5d" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/c00b54f1-28cf-4bb1-b0ee-3271e9dde5c7" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/58f77b72-36ad-433c-ac9a-8b1a341c92d5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/15562803-7fb5-4b02-8e1d-b8ec3f48a9c6" />



egrep '(World$)' newfile 
## OUTPUT
<img width="722" height="101" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_02_14" src="https://github.com/user-attachments/assets/3c2d1b97-c339-4635-a554-1508ffd39e1e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="576" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_05_42" src="https://github.com/user-attachments/assets/3ce45b08-8e08-408a-bc40-d583d56ec631" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="576" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_05_42" src="https://github.com/user-attachments/assets/5a78b6a4-7062-4d86-8f7d-af55d8bf8aea" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="576" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_05_42" src="https://github.com/user-attachments/assets/3efe5c84-a064-421c-a91e-6db020e95d7f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="576" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_05_42" src="https://github.com/user-attachments/assets/aee24b13-3d97-4b99-b8a7-703848ea7bda" />


egrep l{2} newfile
## OUTPUT
<img width="444" height="90" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_06_52" src="https://github.com/user-attachments/assets/bb23fb48-193b-4ebe-a46c-95b960f99dc2" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="773" height="156" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_07_29" src="https://github.com/user-attachments/assets/aed3b278-389f-4512-ab7d-203ac31a6c46" />


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
<img width="715" height="81" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_07_42" src="https://github.com/user-attachments/assets/53d3a222-d1c7-4498-8362-4b7c51488fbb" />



sed -n -e '$p' file23
## OUTPUT
<img width="715" height="81" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_07_42" src="https://github.com/user-attachments/assets/3c7a704c-5bdf-4559-b615-7f4e85afcdea" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="715" height="81" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_07_42" src="https://github.com/user-attachments/assets/4c9bc5d0-b557-47ff-8df9-80dc02ab95fb" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="514" height="260" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_08_42" src="https://github.com/user-attachments/assets/9bd2c71f-afc1-49ff-9028-866c2bc519b7" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="514" height="260" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_08_42" src="https://github.com/user-attachments/assets/e80e043b-f874-4742-afca-dc60ec10011f" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="831" height="174" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_09_06" src="https://github.com/user-attachments/assets/f4402a1b-dc43-4cd4-b3d6-49130eecd4c4" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="956" height="134" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_09_069" src="https://github.com/user-attachments/assets/3340562d-1406-4599-9ae4-7e11c9ac41d7" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="956" height="134" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_09_069" src="https://github.com/user-attachments/assets/ebb1f846-c84f-48ad-8eda-542dd22160b4" />



seq 10 
## OUTPUT
<img width="849" height="300" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_09_45" src="https://github.com/user-attachments/assets/3b96045e-2ed1-4b52-9c04-558a5868055e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="765" height="118" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_09_59" src="https://github.com/user-attachments/assets/c5ca8d3e-3f80-40cf-9f73-2cfdb7c45e0e" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="745" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_10_11" src="https://github.com/user-attachments/assets/c40e65c7-2fb8-4fdb-ad0c-79f475c0fcff" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="757" height="148" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_10_27" src="https://github.com/user-attachments/assets/c5f7e3b2-056e-4254-88a7-9b99f4f2b474" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="725" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_10_40" src="https://github.com/user-attachments/assets/e1cced51-af4c-46f6-b302-4aeb37a6ca06" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="725" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_10_40" src="https://github.com/user-attachments/assets/c26bb752-d353-47eb-8e2b-566e5905f716" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="795" height="158" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_11_17" src="https://github.com/user-attachments/assets/f1f98527-be76-4b08-b159-5c1fa4dadcf9" />



sed -n '2,4{s/$/*/;p}' file23
<img width="805" height="168" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_11_35" src="https://github.com/user-attachments/assets/41a05656-cc40-4e2c-af1e-53d358a4a2d6" />


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
<img width="701" height="145" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_14_11" src="https://github.com/user-attachments/assets/9ffb000b-a73a-4df1-9c4e-c0a954a02bb5" />


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
<img width="499" height="216" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_14_50" src="https://github.com/user-attachments/assets/0da74870-9e3a-41eb-b9e9-6b03e4a8b35a" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="855" height="292" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_15_07" src="https://github.com/user-attachments/assets/611e3749-bf5b-4643-9170-0779af612b43" />

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
<img width="855" height="292" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_15_07" src="https://github.com/user-attachments/assets/c2df551b-c3dd-4fe1-ac56-7f42b8de59a2" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="706" height="122" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_16_21" src="https://github.com/user-attachments/assets/1c4b63e5-942e-4bc1-8823-9b837461b1f2" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="549" height="584" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_16_43" src="https://github.com/user-attachments/assets/fcc451dc-d5db-4989-8d3f-b0624289d7da" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="932" height="582" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_17_08" src="https://github.com/user-attachments/assets/240b6a3d-e7f6-4445-9760-0654146c594c" />


tar -xvf backup.tar
## OUTPUT
<img width="1010" height="478" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_17_44" src="https://github.com/user-attachments/assets/37e3caf2-f52d-4932-96b9-4adca009c526" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="836" height="99" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_18_36" src="https://github.com/user-attachments/assets/5e5703ce-f3a1-4908-b6fe-0f10601199f0" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="550" height="55" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_19_28" src="https://github.com/user-attachments/assets/a7eba286-6459-4ef7-aa74-296200e03cce" />

 
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
<img width="812" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_20_16" src="https://github.com/user-attachments/assets/8353b5e2-5b48-4cd1-bc61-61a2e44efbed" />


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
<img width="857" height="429" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_23_28" src="https://github.com/user-attachments/assets/3d988dcf-b693-4802-ac02-cf85304cdc7c" />

 
ls file1
## OUTPUT
<img width="821" height="108" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_23_42" src="https://github.com/user-attachments/assets/8f3a011e-e551-48bc-9b49-75dfb4503223" />

echo $?
## OUTPUT 
<img width="784" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_23_53" src="https://github.com/user-attachments/assets/3d50cdd3-85a0-4087-ab44-c3eda8208491" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="784" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_23_53" src="https://github.com/user-attachments/assets/4a3977a3-28fc-491c-8f7b-b9b4d84ca1b5" />

abcd
 
echo $?
 ## OUTPUT
<img width="784" height="130" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_23_53" src="https://github.com/user-attachments/assets/dc48ce9f-96f1-43b5-9204-c79a60dc723c" />


 
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
<img width="910" height="329" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_24_51" src="https://github.com/user-attachments/assets/259adb35-2826-4a11-a87f-b2b0658c00b9" />



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
<img width="909" height="78" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_26_04" src="https://github.com/user-attachments/assets/a34264f2-c26f-4df7-b998-fce80bacc2b0" />

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
<img width="842" height="179" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_27_33" src="https://github.com/user-attachments/assets/7d01b67f-f402-4b73-8b24-07512b05f2f5" />



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
<img width="896" height="178" alt="VirtualBox_Parrot Security 6 0_02_05_2026_08_12_16" src="https://github.com/user-attachments/assets/462f17a0-9712-4f34-a0ba-4c9ea2f2549e" />

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
<img width="738" height="196" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_28_21" src="https://github.com/user-attachments/assets/a09b0942-f344-4334-b077-764dac68df7c" />

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
<img width="904" height="144" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_30_13" src="https://github.com/user-attachments/assets/235849a2-7748-4c5a-9ba0-b638ba064650" />


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
<img width="809" height="127" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_31_03" src="https://github.com/user-attachments/assets/a62e3590-f902-4a2e-8794-be1aedcb78d8" />

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
<img width="858" height="174" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_36_18" src="https://github.com/user-attachments/assets/a9cdb600-b255-452f-935e-12f75ba1fa55" />


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
<img width="830" height="371" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_38_42" src="https://github.com/user-attachments/assets/c0435db3-4b35-4232-8014-4cdcdcdd8388" />

 
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
<img width="982" height="175" alt="VirtualBox_Parrot Security 6 0_02_05_2026_08_13_26" src="https://github.com/user-attachments/assets/cd79d206-100d-4d15-822d-bad54985908f" />

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
 <img width="988" height="190" alt="VirtualBox_Parrot Security 6 0_02_05_2026_08_13_38" src="https://github.com/user-attachments/assets/1cead397-3380-421c-af87-eba377969681" />

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
<img width="720" height="144" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_41_11" src="https://github.com/user-attachments/assets/b7bb3607-82ea-43ff-9a5f-76a7bcb2ded1" />


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
 <img width="894" height="119" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_41_57" src="https://github.com/user-attachments/assets/89c25e22-f13d-41d6-b849-44d775ff729b" />

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
<img width="588" height="108" alt="VirtualBox_Parrot Security 6 0_02_05_2026_01_44_24" src="https://github.com/user-attachments/assets/db146613-e778-4494-a7cb-27a7e955df92" />

 
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
<img width="627" height="397" alt="VirtualBox_Parrot Security 6 0_02_05_2026_02_01_18" src="https://github.com/user-attachments/assets/3a5f3126-c7ae-4e80-9894-2446e2d242c2" />

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
<img width="627" height="397" alt="VirtualBox_Parrot Security 6 0_02_05_2026_02_01_18" src="https://github.com/user-attachments/assets/190c068f-f61a-40c5-9ee0-ad4f57cf5c7f" />

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
 <img width="872" height="401" alt="VirtualBox_Parrot Security 6 0_02_05_2026_02_02_22" src="https://github.com/user-attachments/assets/e2f6d3d2-f8b6-4484-baa9-66893cea7f14" />

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
<img width="712" height="158" alt="VirtualBox_Parrot Security 6 0_02_05_2026_02_03_08" src="https://github.com/user-attachments/assets/9bcaaa6d-2cf4-4534-84c9-185cdb1e37ec" />


# RESULT:
The Commands are executed successfully.
