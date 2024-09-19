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
![306323977-c35eee39-b77b-42f5-ae91-42caecdd52da](https://github.com/user-attachments/assets/1f97bf15-c4ab-4b5c-bfeb-280ad9249eeb)



cat < file2
## OUTPUT
![306324035-682bbd9a-6678-4624-b5f7-6daaf396807c](https://github.com/user-attachments/assets/207892c9-441e-477e-8053-4a1da3533718)



# Comparing Files
cmp file1 file2
## OUTPUT

 
comm file1 file2
 ## OUTPUT
![306323621-8640faa3-8194-4ee4-a16c-dd365e6905ec](https://github.com/user-attachments/assets/2b36f241-440d-4dbb-89e2-d70c92f637a0)

 
diff file1 file2
## OUTPUT
![306323426-59e72bbd-0260-45a8-b1a4-1b685695971c](https://github.com/user-attachments/assets/0c6e83ff-8797-4763-8a3c-023dcfbf7e38)



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
![306324216-2464b3f4-6b08-41be-aa67-e117fd96dfc1](https://github.com/user-attachments/assets/078f184c-56ad-48b5-95f0-1d985390ec31)





cut -d "|" -f 1 file22
## OUTPUT
![306324281-86de4428-9ee0-485d-9696-cbac521429a0](https://github.com/user-attachments/assets/4cd60c1f-a31c-4a60-81ec-dcb3580c630e)




cut -d "|" -f 2 file22
## OUTPUT
![306324345-68a6922d-20c0-4af8-921a-d7a14af1d483](https://github.com/user-attachments/assets/50d4f7f9-7808-49fe-a49d-40b9fead1b47)


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
![306324464-5225be44-5ded-479f-81c0-1b08a43a3db2](https://github.com/user-attachments/assets/26c2d241-3a9b-46d1-8c51-10e287eb9fb1)




grep hello newfile 
## OUTPUT
![306324533-78ef312e-f2f6-4d3d-a656-eb5f93641a61](https://github.com/user-attachments/assets/504606a1-f20b-4e8f-812b-5829efb9f647)





grep -v hello newfile 
## OUTPUT
![306324701-2e1628ca-d122-4a5c-8616-8c6c318f224b](https://github.com/user-attachments/assets/23f510e8-b27d-47d2-a437-03c6a04671ca)




cat newfile | grep -i "hello"
## OUTPUT
![306324795-79b59c5f-d111-43af-a1b8-1cd24831653c](https://github.com/user-attachments/assets/f8c24718-da15-4d78-a14b-0bf6f35dd66c)





cat newfile | grep -i -c "hello"
## OUTPUT
![306325009-fd5bc91e-6d16-42f4-913b-8baedfae7d67](https://github.com/user-attachments/assets/4e63dac7-692e-42ce-a018-1276755ea0fc)





grep -R ubuntu /etc
## OUTPUT




grep -w -n world newfile   
## OUTPUT
![306325468-10e88fba-0b66-41aa-bf4d-1eec3ec8bb73](https://github.com/user-attachments/assets/364bfc42-b0dd-45fe-9bbf-b0ddc339ab53)



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
![306325633-2f7618eb-26c9-4a06-b037-6e2a05e035a8](https://github.com/user-attachments/assets/b29f9b9f-d961-488c-9426-a642e71625b0)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![306325688-1586acca-2c82-4c42-98bc-4ae798eef1a8](https://github.com/user-attachments/assets/6cd32973-b5b1-4cc8-a349-f252aae47453)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![306325797-8688c525-73fb-44c1-aedc-42c6bf61741e](https://github.com/user-attachments/assets/e3ab526e-62f6-422c-b170-b2842f795cce)





egrep '(^hello)' newfile 
## OUTPUT
![306326121-4980783d-eee0-4468-a932-ed98b32fb05f](https://github.com/user-attachments/assets/6f724ea9-0683-457d-a2f0-f7567b5897ea)




egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT
![306326236-0c3b9da2-1ec3-4ed6-afdf-d97b3ec65697](https://github.com/user-attachments/assets/1e94f221-1f66-48ff-a16c-6a6e4bc12573)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![306326400-228361e3-4c51-408b-acae-b547654c8d92](https://github.com/user-attachments/assets/4a2a6c48-2cb3-44f4-88b7-50dedec3f210)




egrep '[1-9]' newfile 
## OUTPUT
![306326507-78841f5b-a1d6-42da-a170-f873f2db1c02](https://github.com/user-attachments/assets/4edc1b18-93fd-47c1-813a-73d41f22a458)




egrep 'Linux.*world' newfile 
## OUTPUT
![306326696-218b2ba3-76f4-4fe8-8822-3d64fc006de9](https://github.com/user-attachments/assets/e9327368-0607-4775-8a5d-7d485861bae1)



egrep 'Linux.*World' newfile 
## OUTPUT
![306327153-e0fb9fd4-0e34-4bb0-b447-480e7353e23c](https://github.com/user-attachments/assets/23662448-f37c-419c-bd65-11e26d5f8bc2)


egrep l{2} newfile
## OUTPUT
![306327065-455cefd1-c3cf-4a56-9626-22f5acc9d758](https://github.com/user-attachments/assets/ce3ca0f0-82d9-4f1c-8f04-6eca49b5a6e2)




egrep 's{1,2}' newfile
## OUTPUT 
![306327376-8b7b973d-2ecb-4adf-b3b0-b4a6090238f4](https://github.com/user-attachments/assets/8a294de0-ee2a-4f3b-a2ca-865557cbe659)



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
![306327645-6ed8eeb2-98aa-489d-b7b5-502fad1fa948](https://github.com/user-attachments/assets/5953d2eb-1fe0-41c1-a10b-6f11d1acda39)




sed -n -e '$p' file23
## OUTPUT
![306327739-a525b7f6-5451-4607-bf43-47e41df195cc](https://github.com/user-attachments/assets/f86f14cb-b7fd-440b-bc96-4a528c08bef4)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![306327903-2dec5d41-9a09-4e5e-8b9e-124614c5ba56](https://github.com/user-attachments/assets/1674c479-ee3d-4cb7-85c0-d0dd6d2f6326)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![306328067-18fb9a8e-d5ce-4f68-8d04-799b2e781cd6](https://github.com/user-attachments/assets/d4ba7026-b067-42d6-9370-063cc9c5bbf9)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![306328125-5209fed2-c815-4dd9-bbfc-885f9104d28a](https://github.com/user-attachments/assets/3cf62747-9bb6-473a-905e-d3d044a17956)




sed -n -e '1,5p' file23
## OUTPUT
![306328252-59481f62-1000-4099-be96-30a15f0f9f9f](https://github.com/user-attachments/assets/aa8323e4-4e3b-4b5f-a46a-2cbb1ee9f477)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![306328320-c1935ffc-35e7-488e-a332-e3dd4c0b4220](https://github.com/user-attachments/assets/5f459ab0-cb91-45c4-aa2f-64275d0b7cb6)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![306328404-3156abad-90b0-40bc-82f2-7e288e6776c9](https://github.com/user-attachments/assets/54a8550e-4393-40aa-bd9e-96fc30173e98)



seq 10 
## OUTPUT
![306328511-ea0f93d4-b7fe-4b56-83f8-5df261f74fcb](https://github.com/user-attachments/assets/f7211d60-d7fd-4216-846f-f40c0db37ac6)




seq 10 | sed -n '4,6p'
## OUTPUT
![306328612-bc5e24b5-5130-4756-b972-bd061802099e](https://github.com/user-attachments/assets/281e63cc-f030-4927-8971-9c243f60f39f)




seq 10 | sed -n '2,~4p'
## OUTPUT
![306328704-af99d8d5-a0fb-4a3f-8391-4ce396c27f9f](https://github.com/user-attachments/assets/84537662-b110-451c-a898-9d26133fb05e)




seq 3 | sed '2a hello'
## OUTPUT
![306328812-ebff4972-2af6-4823-8af3-5a2218ed0f9e](https://github.com/user-attachments/assets/78dd0f17-d5ac-4003-85bc-5436b897126a)



seq 2 | sed '2i hello'
## OUTPUT
![306329113-6a7d5a34-213f-4d78-a264-72be126d9325](https://github.com/user-attachments/assets/c00bcdb1-57ff-42c1-8ffb-1e21fa86d61b)


seq 10 | sed '2,9c hello'
## OUTPUT
![306329230-56f96442-9167-4513-812b-07e8b22b9252](https://github.com/user-attachments/assets/5eb75093-9159-400a-9778-86fdf23de38f)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![306329333-cbadd6df-119c-4a6a-b7ac-8888a033311e](https://github.com/user-attachments/assets/1908e0a1-d568-4427-bbc2-ee38c08c6925)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![306329585-36d38ad5-fd86-4e5d-86f3-734e1c0390bc](https://github.com/user-attachments/assets/fae2c55d-679e-42f5-b089-799fafb26ddb)


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
![306329910-b947d6ba-4de8-436b-a7b7-fd88455c4fa3](https://github.com/user-attachments/assets/94736883-6aca-4022-8454-f1c9e0d92d7d)



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
![306329989-df15d132-7d04-43d4-ae87-87bb88a3e002](https://github.com/user-attachments/assets/047072f3-05ec-4e35-b8a2-5c9697cd219f)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![306330077-2fe37e25-e5ba-4bbb-9209-9980e7b79ff5](https://github.com/user-attachments/assets/8aa303a6-e1c8-4cf0-bf09-0694fb123f36)


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
 ![306330127-3d90c98b-a7b3-43f6-8674-b310a5ab193b](https://github.com/user-attachments/assets/102c90b3-d4d4-427b-9eb8-ccb96a25bee0)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![306330188-ca555058-30ad-4a25-899a-81179c28d117](https://github.com/user-attachments/assets/98f739d5-dfef-42d3-8dba-af6976527487)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![307496539-d813cb49-6684-4e3c-8570-ea7d6368b688](https://github.com/user-attachments/assets/894ed183-2cbb-4da1-b74b-90df3899f67f)

![307496550-70216941-d36d-4b4a-88a5-8243e9fd3ebf](https://github.com/user-attachments/assets/cf522a8d-8247-4ed8-8126-44cebfdd8fe2)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image-43](https://github.com/user-attachments/assets/79bf9546-55d1-4900-b9ac-06afda05aa84)




tar -xvf backup.tar
## OUTPUT
![image-43](https://github.com/user-attachments/assets/ee17b530-3c71-45c1-9ea2-4fc8d6e82415)

gzip backup.tar

ls .gz
## OUTPUT

 
gunzip backup.tar.gz
## OUTPUT
![image-44](https://github.com/user-attachments/assets/a7db0349-f391-4da3-a5ce-312816aeb8f1)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image-49](https://github.com/user-attachments/assets/23eddb21-24fa-4e9f-a31f-1c5e624f0dd3)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image-50](https://github.com/user-attachments/assets/a5b23c3c-2626-4f39-80a1-db3e20fe4b47)



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
![image-51](https://github.com/user-attachments/assets/dc269211-a2e5-472c-a0bb-1d4d5a6c2f99)

echo $?

 
ls file1
## OUTPUT
![image-52](https://github.com/user-attachments/assets/9ecff057-3e81-4f00-a81a-6418a3bc8689)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image-53](https://github.com/user-attachments/assets/e11e68ae-0a75-4dfa-966e-ff292c042c3c)

 
abcd
 
echo $?
 ## OUTPUT
 ![image-54](https://github.com/user-attachments/assets/e48350e2-1037-4c66-bec3-439d504f84cd)



 
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
## OUTPUT
![image-55](https://github.com/user-attachments/assets/3035e6b9-5cd7-4445-809c-d3a192694770)



chmod 755 strcomp.sh

 
./strcomp.sh 
## OUTPUT
![image-56](https://github.com/user-attachments/assets/13bd8d21-1629-4050-8f9f-d43d9c7236e2)


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
![image-57](https://github.com/user-attachments/assets/3fb8e135-8dde-4c3e-ba70-eb0d9ebcacae)


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
![image-58](https://github.com/user-attachments/assets/919321bb-2664-4c95-8822-200cae8cc551)




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
## OUTPUT
![image-59](https://github.com/user-attachments/assets/7c869d59-8080-49ea-9d11-cbd06f2f73d7)

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
![image-61](https://github.com/user-attachments/assets/dbb25a2d-c6ca-4668-8356-8604d827f780)


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
![image-62](https://github.com/user-attachments/assets/bb843874-dafe-43d7-8a62-92ecad865855)


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
![image-63](https://github.com/user-attachments/assets/2ef4b9c8-0c63-4b17-9c9c-5eb9f13fafca)

 
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
 ![image-64](https://github.com/user-attachments/assets/e7a75aef-12e4-45a2-9e06-69979bf87895)

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
## OUTPUT
![image-65](https://github.com/user-attachments/assets/223379b1-1eb8-4617-9340-978689a42f1e)

 
 
 
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
## OUTPUT
![image-66](https://github.com/user-attachments/assets/b1d096ed-cc1a-49c7-9a7a-fa10a492030f)

 
 
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
![image-67](https://github.com/user-attachments/assets/4c2e54cf-33e1-4bfc-97df-f5d0eeed2939)

 
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
![image-68](https://github.com/user-attachments/assets/61dbbf0a-b870-4130-b818-0286f02256c3)

 
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
![image-69](https://github.com/user-attachments/assets/dc0a63f6-8790-4324-8826-bfb2b7a3fdd1)


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
![image-70](https://github.com/user-attachments/assets/90675ccc-d9cd-4ff6-9fa2-02e4fb791b3b)


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
![image-73](https://github.com/user-attachments/assets/9f21d84e-86bf-46ea-9fed-9ae7238d0134)


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![image-74](https://github.com/user-attachments/assets/8fa18650-5eeb-4060-a181-2cf0c52f2bf1)

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
 ![image-75](https://github.com/user-attachments/assets/a51c1b3b-a098-447b-87de-7e881fa5ed76)

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
![image-76](https://github.com/user-attachments/assets/03dfde87-75d6-4859-8661-92f68b5d6d75)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image-77](https://github.com/user-attachments/assets/da004b67-6877-48a7-bc1a-debe0efa45d7)



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
![image-78](https://github.com/user-attachments/assets/9836ad0b-ccbc-4db8-930e-cf1391283ef1)

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
![image-79](https://github.com/user-attachments/assets/68ff5330-be68-4f8c-8eb9-a1bc72f86033)

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
![image-80](https://github.com/user-attachments/assets/7f29a742-4b58-4fd6-aff4-fff078351919)

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
![image-83](https://github.com/user-attachments/assets/1a07daff-0f26-4b4d-81e2-3bf81861d91d)

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
![image-82](https://github.com/user-attachments/assets/e8ab84cc-e4fd-4ecc-b6a5-86828c86d5d4)
 
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
![image-84](https://github.com/user-attachments/assets/5370795c-d5cd-4a1b-8149-5d898cd803e3)


# RESULT:
The Commands are executed successfully.
