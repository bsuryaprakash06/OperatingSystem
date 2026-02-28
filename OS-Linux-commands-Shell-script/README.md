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
![image](https://github.com/user-attachments/assets/2a3d06c8-f169-4c61-95a2-a79a064e5a46)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/ddd67bd0-3792-4d0a-812a-45bc3d3c2bca)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/e585e2f1-125c-49ac-95d4-0d1beacefee2)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c12bc7d7-97a1-4198-826f-e2b48db871ea)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/c03ccb0b-fb33-41a3-ba0c-36113f8b5ad5)


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
![image](https://github.com/user-attachments/assets/94bbbdb9-911f-4361-9743-fae4bfcb24f3)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/95cb1995-b2cf-42a7-a924-a1e5366eb3f7)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/3103b8ca-4929-45cd-a701-db8677d43e63)


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
![image](https://github.com/user-attachments/assets/20789ab8-a13d-4af8-9fd8-6170c68a370b)


grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/308e41e0-8268-4edb-a508-7d72dc120fc3)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/936c448c-cde8-46ba-b8ac-babe47e0bec1)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/ef105829-94ec-4e0c-8647-352e2e0f7b24)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/8f91699f-da08-4f54-a247-d00c4ba5d19e)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/35527bb3-f467-4ab5-98f8-aec49148ea54)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/f5b67441-fb4a-4123-a6ed-0af1b79c47db)


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
![image](https://github.com/user-attachments/assets/09a263e0-310d-4f49-a16a-c9beaff94e75)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a2c2ab75-33e3-4a2e-8e29-7c2a1002b5c1)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f10c5641-a944-4595-9aa0-fed2bbb60be4)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8d8f8d02-0cd4-479c-a52c-25de763b0614)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bb075f5b-e55d-4d59-b5fa-600d43f6151a)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5b0a46f9-f215-4237-8e83-1d372218a90f)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/473ef890-43ee-42d2-95f0-6fffc513c6a8)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9ec35788-9f38-4eb2-9bf3-b1b4dfcd5cbd)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0c9869d6-2e12-432d-8229-71215fc5c028)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b63453c6-cbce-4767-99c2-054b88af4c94)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/51f46bd6-05da-4a8b-b56d-3f011d8fa002)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/382d3742-c29f-4cae-8555-e4851b783268)


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
![image](https://github.com/user-attachments/assets/ad997053-0991-492b-a309-515561f581f2)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8d494242-5007-4d28-a064-e515c6582802)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c67786bc-80c3-420b-97e7-1a87a6b7b87d)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/dc261a8e-65a4-4f66-af3d-c48e77ec09db)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b6940206-b41b-43f3-8ec7-d1f4387bd3b1)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c3131720-35a0-43f4-82c4-212fb536220f)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1827cea7-bf9d-4e7e-8229-7e9238c94640)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b22574b4-7472-4821-ba4f-8f7f9f7b5462)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/c24f4c4b-6569-48ef-aa5a-dbe2899f82fb)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/1cfdcd67-4614-4099-8db3-6a68a1871bb1)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/f9b7a8b5-3277-4773-952d-5e9e7d7f59bd)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/229559cd-83de-40e9-9cf8-b7a4d3d07870)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9938339c-ba56-4a4e-9bd4-607acaefde11)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/76fe9dfd-fec6-4ed5-a12c-599c9c6e9ed3)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/efe2012b-4bf3-40f2-b760-38cac1577b39)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/f57c3530-460d-45fc-9c58-90436a463594)

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
![image](https://github.com/user-attachments/assets/7ff84a89-989f-477c-8838-3ed8a28e0a49)


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
![image](https://github.com/user-attachments/assets/56622de9-518f-4ef2-a996-b840ddc4e0be)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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
![image](https://github.com/user-attachments/assets/ae07f2bf-1519-496c-b411-df3319365c79)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/aa061563-eca5-41c9-a1ff-2cb23ffddbe3)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/3635f91d-8c6f-4749-adef-3bafbf215f7a)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/aba42a7e-7603-4e66-980d-b148e7ebdd5a)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/33d394c5-d94e-491d-bda1-96e8ff3270da)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/0e93656a-dc9c-4159-92c0-bab8f1d45ddc)
 
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/9a18656a-450b-4130-b00a-05f4ba287de4)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/dcd54b1e-f97d-4e97-8c0f-85883a5ba100)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/850e2b56-3309-40c1-a3c5-25a7c546075f)


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
![image](https://github.com/user-attachments/assets/75e5fc5c-54be-4281-bb0d-88d2e2076502)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/9ae80cbc-1b7f-4436-804d-d8ddca643688)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/f218bf1a-1bf7-49bf-9fc1-c79272af311d)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/73d2f686-46f6-4155-8c94-ab49bd3da981)
 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/a929680b-bc44-4140-a2a5-9a1240a6e839)


 
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
![image](https://github.com/user-attachments/assets/8f9313de-20a3-4b32-a130-3f8771b44608)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/e4e2ef66-6c8f-4d68-8769-406a55a78fb5)


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
![image](https://github.com/user-attachments/assets/e9849067-78e7-4614-98bf-0db1656b59a8)

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
![image](https://github.com/user-attachments/assets/95e9facf-e8f9-41b2-bd86-e89b25f67f22)



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
![image](https://github.com/user-attachments/assets/3acb2cf1-1450-46fc-aba6-670440311691)


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
![image](https://github.com/user-attachments/assets/22a230a9-02bc-4f35-8bd3-5df7f135b836)

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
![image](https://github.com/user-attachments/assets/12ac387a-3d27-47c2-bf2e-2af846831ef9)


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
![image](https://github.com/user-attachments/assets/de3c4589-c668-46f2-bf4b-4632bd3b561e)

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
 # OUTPUT
 ![image](https://github.com/user-attachments/assets/eada194d-64ad-4d4e-8f02-1d0890ca3dfd)

 
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
 # OUTPUT
 ![image](https://github.com/user-attachments/assets/34030a4d-918f-474d-b019-d7839f82dbd6)

 
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
 # OUTPUT
 ![image](https://github.com/user-attachments/assets/082b61ba-1fe3-4aa9-8e0a-ce4625d18a5b)

 
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
 
# OUTPUT
 ![image](https://github.com/user-attachments/assets/9539cc26-cc4c-460c-bba0-b6d5fbc1474d)

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
 
# OUTPUT
 
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
![image](https://github.com/user-attachments/assets/55d6c659-aa0b-4c09-b276-2f766aaabf2b)

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
![image](https://github.com/user-attachments/assets/8e244791-db95-42fe-b483-46788cf7de6e)


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
![image](https://github.com/user-attachments/assets/bdc7c7c3-feae-4c30-a916-ce45a5ea914c)

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
![image](https://github.com/user-attachments/assets/af830871-f140-48e1-b699-b7c7b4f236ca)

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
![image](https://github.com/user-attachments/assets/04ce3129-66e7-42bf-aaff-675fb39add5a)

 
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

## OUTPUT
![image](https://github.com/user-attachments/assets/c8b0d3f6-f850-42f5-a498-49c13b197025)

 
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
 ![image](https://github.com/user-attachments/assets/33661709-4fcd-4a88-b290-c0cd52bf5d17)

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
![image](https://github.com/user-attachments/assets/3c4be5d2-3a49-41af-afaa-393d8088dbf5)


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
![image](https://github.com/user-attachments/assets/3b43958b-7924-41c7-9c7f-89f0bff1946d)

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
![image](https://github.com/user-attachments/assets/1e02814a-5006-42fe-bb67-6bdc004e5afb)

 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/2bb055a0-18d9-41f0-868b-21844466ab6f)

 
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
 ![image](https://github.com/user-attachments/assets/ee9d348c-ef70-455e-a602-bef3ec94862e)

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
 ![image](https://github.com/user-attachments/assets/3520dc30-633b-4ab9-887a-9a23e9fe31b6)

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
 ![image](https://github.com/user-attachments/assets/80005b85-4903-4b66-855f-257960c8b5ba)

 
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
![image](https://github.com/user-attachments/assets/5f7dd412-7c15-4cdb-ab05-77ec6b236c28)


# RESULT:
The Commands are executed successfully.
