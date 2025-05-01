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
![WhatsApp Image 2025-05-01 at 10 55 48_06c390da(1)](https://github.com/user-attachments/assets/d0b9eee7-9cc8-47e8-a61a-566a5e1a5f84)

cat < file2
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_06c390da(1)](https://github.com/user-attachments/assets/0866b643-b643-40a1-a979-13623853d399)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_06c390da(1)](https://github.com/user-attachments/assets/bf39c8b6-6a4f-45da-9a54-0298e5412989)

comm file1 file2
 ## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_06c390da(1)](https://github.com/user-attachments/assets/e6207e05-9c95-4d92-944f-ab95d84604d6)
 
diff file1 file2
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_06c390da(1)](https://github.com/user-attachments/assets/48daba42-7dc7-4504-9a2b-842dacdb1904)

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
![WhatsApp Image 2025-05-01 at 10 55 48_b60c31bd(1)](https://github.com/user-attachments/assets/3bd1edc5-5803-4614-ac0a-158fb99037f8)

cut -d "|" -f 1 file22
## OUTPUT
![WhatsApp Image 2025-05-01 at 12 00 38_1535b7b7(1)](https://github.com/user-attachments/assets/182dd511-b292-41e0-8662-55343db017e3)


cut -d "|" -f 2 file22
## OUTPUT
![WhatsApp Image 2025-05-01 at 12 00 38_1535b7b7(1)](https://github.com/user-attachments/assets/759e8a2e-0788-416f-9be3-eafb281a1346)

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
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/edb82ce1-2225-4181-946d-27d9358eb928)

grep hello newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/48fb754f-e96d-44d6-912c-d9961fed3355)

grep -v hello newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/f93a51c4-5a5a-4019-aadd-f2c591bc8c8e)

cat newfile | grep -i "hello"
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/3e7b9028-d71d-4eb8-b277-72f049f7d1a0)

cat newfile | grep -i -c "hello"
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/97348edf-cf59-4c4b-86e5-ac5d7d819afc)

grep -R ubuntu /etc
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_376170f2(1)](https://github.com/user-attachments/assets/0ba20ffa-762f-40a1-803f-3350c495002e)

grep -w -n world newfile   
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/196ab46c-5a23-4ff9-87af-4d426dfe1ae2)

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
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/e80c771e-d616-41cd-baa9-8ade9763ad8a)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/babc576d-127c-4f16-80ea-c9399288a12e)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/0a1a5cc1-19e9-4348-87de-0df6c5fe6356)

egrep '(^hello)' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/7edae172-d32f-44ff-acd2-edaf32b013ac)

egrep '(world$)' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/f5624f04-ea70-430e-8f2e-11f4a9e60891)

egrep '(World$)' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/f5624f04-ea70-430e-8f2e-11f4a9e60891)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/b36448f7-4244-4160-8504-eeea0e5bd094)

egrep '[1-9]' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/4280a67d-204e-42cb-8ec9-e92531e45dfe)

egrep 'Linux.*world' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/787db7f2-377c-48ec-a63c-140567218c89)

egrep 'Linux.*World' newfile 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/ffac0fd0-5170-4288-9b9d-35f3029c2ab4)

egrep l{2} newfile
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/5bdc558a-6f8d-4a5e-8d65-c271b20313f0)

egrep 's{1,2}' newfile
## OUTPUT 
![WhatsApp Image 2025-05-01 at 10 55 48_e1507ae9(1)](https://github.com/user-attachments/assets/10e3046d-a1e1-4f96-90ef-795b8a1fad6e)

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
![WhatsApp Image 2025-05-01 at 10 55 48_f9f9d7c7(1)](https://github.com/user-attachments/assets/93fead7c-4788-4f31-a45a-5830557aae61)

sed -n -e '$p' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_f9f9d7c7(1)](https://github.com/user-attachments/assets/ee57cb56-6db7-40ab-922a-3413cb1ec983)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_f9f9d7c7(1)](https://github.com/user-attachments/assets/54abcecb-a383-41c7-9d50-ec342262c2f1)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_f9f9d7c7(1)](https://github.com/user-attachments/assets/25796b20-d2d6-4722-b9d8-9498dff4c335)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_bc6116b7(1)](https://github.com/user-attachments/assets/73d25147-7266-4236-9eb0-c90c141567fe)

sed -n -e '1,5p' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_bc6116b7(1)](https://github.com/user-attachments/assets/086a8093-f917-4e12-9054-4a39f0ac9c28)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_bc6116b7(1)](https://github.com/user-attachments/assets/68dbe861-1452-4885-92a6-d22b54bf384f)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_bc6116b7(1)](https://github.com/user-attachments/assets/1c20bff7-c65c-402c-a2c7-08294783777c)

seq 10 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_bc6116b7(1)](https://github.com/user-attachments/assets/698a1f55-dfec-445f-847c-4264ab5e477a)

seq 10 | sed -n '4,6p'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/92361837-9531-46eb-b262-f752538d1a51)

seq 10 | sed -n '2,~4p'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/53a2cf8d-0f46-4834-8284-f969867861a1)

seq 3 | sed '2a hello'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/93a90cda-3d76-42c7-a9ec-f26ad6ed3b21)

seq 2 | sed '2i hello'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/09bc7015-6b0f-4cc1-9ced-f345b6e97f81)

seq 10 | sed '2,9c hello'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/a3554f23-78f4-46fb-be2d-42d99bc4e34b)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/52d99ce6-c453-4a73-88f1-9cbd068cb33a)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_4ff011d5(1)](https://github.com/user-attachments/assets/963b5215-e6f8-4324-980b-c224085e3081)

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
![WhatsApp Image 2025-05-01 at 10 55 48_2dd401d9(1)](https://github.com/user-attachments/assets/69944d08-26e9-4b41-b848-c6345c4f9af0)

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
![WhatsApp Image 2025-05-01 at 10 55 48_2dd401d9(1)](https://github.com/user-attachments/assets/e40c5508-5ede-49ff-bc06-f7e454621296)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_2dd401d9(1)](https://github.com/user-attachments/assets/05c89966-f8f6-4eb7-b042-da7e2183c7df)

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
![WhatsApp Image 2025-05-01 at 10 55 48_568eb1d8(1)](https://github.com/user-attachments/assets/63e6c818-b926-4db3-9a08-da013e60d95e)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_568eb1d8(1)](https://github.com/user-attachments/assets/4681ade5-91e0-4b66-92e9-376db8d57f8e)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_568eb1d8(1)](https://github.com/user-attachments/assets/2ae8e19a-b19c-400c-9453-d9957a4eabe5)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/feb3b0c2-a504-4e13-a527-1236c4aff072)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/f4d1e8a0-d533-4807-ad38-2cedab2d3ef9)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/60b08129-4a47-48de-a831-f7b4901c43ce)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/7f2af1f3-a0d7-40b7-a740-75442d306a65)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_5991f3d5(1)](https://github.com/user-attachments/assets/fe6994a4-e656-4735-9429-539ad5a3d7e6)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_5991f3d5(1)](https://github.com/user-attachments/assets/b8ea409f-f4aa-436a-b919-c31eff9f4e80)

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
![WhatsApp Image 2025-05-01 at 10 55 48_91cc85eb(1)](https://github.com/user-attachments/assets/83a27aa1-7685-46d6-9ce6-91a410f00f95)

ls file1
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_91cc85eb(1)](https://github.com/user-attachments/assets/defe19f1-a79d-4b1f-b9cf-4c6cd5f20c99)

echo $?
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_064542ed(1)](https://github.com/user-attachments/assets/e815d40f-8ceb-4a75-9ddd-d30c600b76e4)
 
abcd
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_064542ed(1)](https://github.com/user-attachments/assets/5c25c908-6a92-418e-9b61-5e47ad002294)

echo $?
 ## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_064542ed(1)](https://github.com/user-attachments/assets/961f6095-c22d-46db-988f-102c2c827c56)

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
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_064542ed(1)](https://github.com/user-attachments/assets/eb5bb622-bc21-4197-ae27-3c59186ee1d0)

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
![WhatsApp Image 2025-05-01 at 10 55 48_d14ed9bc(1)](https://github.com/user-attachments/assets/f84154ca-eae4-49f8-a52d-c8c7cc0d194a)

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
![WhatsApp Image 2025-05-01 at 10 55 48_dfd83b32(1)](https://github.com/user-attachments/assets/f4e842ed-e4f2-47a8-9a2e-611996bb5735)

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
![WhatsApp Image 2025-05-01 at 10 55 48_767e293b(1)](https://github.com/user-attachments/assets/4079c3ad-140a-4d8d-8000-2cda14c1ac9e)

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
![WhatsApp Image 2025-05-01 at 10 55 48_dfd83b32(1)](https://github.com/user-attachments/assets/2bec0892-9d2e-4894-a889-0d852332473b)

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
![WhatsApp Image 2025-05-01 at 10 55 48_92b727c0(1)](https://github.com/user-attachments/assets/2cc37c2d-587f-4668-bf12-6e28d880755b)

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
![WhatsApp Image 2025-05-01 at 10 55 48_0aec19e7(1)](https://github.com/user-attachments/assets/79e1389d-4a6c-4b51-b29a-b08ff553b981)

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
## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_33b2df8b(1)](https://github.com/user-attachments/assets/addbb8b7-930d-4c25-94ae-6e3f5813a834)

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
 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_e38a6da8(1)](https://github.com/user-attachments/assets/25830546-d546-4654-be8f-85d461c8cfdb)

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
 $ ./untiltest.sh
 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_b78bbe28(1)](https://github.com/user-attachments/assets/d0f533f9-83f6-40cb-8c98-446ff45e49ab)

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
 $ ./forin1.sh
 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_542327dd(1)](https://github.com/user-attachments/assets/c3d3e05d-6d4b-4f46-a65b-579b0572c7f7)

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
 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_c13e41b4(1)](https://github.com/user-attachments/assets/8608bba8-4afe-4fc0-9535-21c43f9375b1)

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
 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_c13e41b4(1)](https://github.com/user-attachments/assets/7dafae92-6da5-461c-a736-b8929bbe9054)

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
![WhatsApp Image 2025-05-01 at 10 55 48_a9876897(1)](https://github.com/user-attachments/assets/8ec1c6bb-cf10-4cfa-9d55-c53c32e74256)

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
![WhatsApp Image 2025-05-01 at 10 55 48_24a4e495(1)](https://github.com/user-attachments/assets/0454d403-0d69-4908-a9c8-a1127a81eb38)

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
![WhatsApp Image 2025-05-01 at 10 55 48_9d380768(1)](https://github.com/user-attachments/assets/dcb44fda-8602-44fd-ba8a-8452de528eae)

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
![WhatsApp Image 2025-05-01 at 10 55 48_d2faa0a9(1)](https://github.com/user-attachments/assets/50320b7a-1872-4af6-8427-95bb3d54c8ef)

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
 ![WhatsApp Image 2025-05-01 at 10 55 48_462ed736(1)](https://github.com/user-attachments/assets/c99d454c-f178-449f-99c4-c9bfdf4839e9)

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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
##OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_02f0ee5c(1)](https://github.com/user-attachments/assets/ac7ac051-8042-43b6-a540-969aafda76b1)

 
cat forcontinue.sh 
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
 ![WhatsApp Image 2025-05-01 at 10 55 48_64767270(1)](https://github.com/user-attachments/assets/92e6a7e3-dc89-4cc1-98ed-711adfd2d6e3)

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
![WhatsApp Image 2025-05-01 at 10 55 48_e8643385(1)](https://github.com/user-attachments/assets/d192d85c-abef-4c48-9c8c-d173256af903)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_a67630a5(1)](https://github.com/user-attachments/assets/3431b4b6-39bc-46a5-99d1-36b7673f8be1) 
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
 ./funcex.sh 

 ./funcex.sh 1 2 

 ## OUTPUT
 ![WhatsApp Image 2025-05-01 at 10 55 48_772d0791(1)](https://github.com/user-attachments/assets/1da58d81-a010-47ed-b52d-4991066661e4)

cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3

## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_fb102993(1)](https://github.com/user-attachments/assets/b1ec9331-0c0a-4151-9b91-054ccabae7f6)

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

$ ./argshift.sh 1 2 3

## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_7ce60b3a(1)](https://github.com/user-attachments/assets/572f173b-05a9-4311-bebf-c1c9cebbb669)
 
cat argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```

 ./argshift2.sh 1 2 3

 ## OUTPUT
![WhatsApp Image 2025-05-01 at 10 55 48_7f5963fa(1)](https://github.com/user-attachments/assets/0e894efe-8e95-45db-9773-6fb61ffdd1b7)

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
 ![WhatsApp Image 2025-05-01 at 10 55 48_f52e03ac(1)](https://github.com/user-attachments/assets/f66bdb46-5ca5-44e8-8adb-6ba6c8bd3d88)

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
![WhatsApp Image 2025-05-01 at 10 55 48_2e5deb59(1)](https://github.com/user-attachments/assets/6fbb87a5-edf0-4393-9a47-7008f4d9b58b)



# RESULT:
The Commands are executed successfully.
