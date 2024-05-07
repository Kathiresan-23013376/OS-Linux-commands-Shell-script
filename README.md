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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/13feb7bd-14f8-40b7-a946-9b656940dd38)




cat < file2
## OUTPUT
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/d31054dc-21e2-4772-9b86-081a85980317)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/2d42af7b-e1f5-4660-a518-070fdd3e44ad)

 
comm file1 file2
 ## OUTPUT
![4](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/ee011618-70bd-4697-aed0-1455dbc16071)

 
diff file1 file2
## OUTPUT
![5](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/96b75334-9f63-4429-8f89-4c33c5d346b1)


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
![6](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/dad7933c-ba67-4e7a-bab5-5aa74d2c137a)




cut -d "|" -f 1 file22
## OUTPUT
![7](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/21c9aaf1-04e1-4bf7-8814-05d614293ce0)


cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/22e358ce-5463-442e-8ece-487e15ede4ee)


cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
```
Hello world
hello world
```

grep Hello newfile 
## OUTPUT
![9](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/2be0969b-be3d-4138-89e8-c3dbb29d02b7)



grep hello newfile 
## OUTPUT
![10](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/1e2ca806-c39e-4e95-9d29-7428ed01bf18)




grep -v hello newfile 
## OUTPUT

![11](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/50c0e829-d7bd-46f5-8f5e-a26d7117c4d6)

cat newfile | grep -i "hello"
## OUTPUT

![12](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/3dca4739-a026-497d-a0e5-64073f9913c4)


cat newfile | grep -i -c "hello"
## OUTPUT
![13](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/9d4d7206-97c9-4cb8-b781-a0ba3620ee10)


grep -R ubuntu /etc
## OUTPUT
![14](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/d1159dec-197e-4bac-b1c3-e61518750a3b)



grep -w -n world newfile   
## OUTPUT
![15](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/d54a3dc3-a880-4198-af73-9b93e6996d28)

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

![16](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/66cbede3-3f9c-4a34-9931-47256d1d17b7)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![17](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/9a6fc7c8-604b-4bc9-a458-4936f4574c09)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/47f302eb-2165-4b0e-a07e-98ceb9c14ef2)



egrep '(^hello)' newfile 
## OUTPUT
![19](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/0f13fbea-a51e-44ff-a4b9-2bd62127d062)



egrep '(world$)' newfile 
## OUTPUT
![20](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/7f899e69-1ea1-4ff1-92e7-53523884dd99)



egrep '(World$)' newfile 
## OUTPUT
![21](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/59885702-0ef8-403d-ba93-a5eabd1fc86d)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![22](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/cb335030-9add-4fdf-bf5d-0f038c9ead0b)


egrep '[1-9]' newfile 
## OUTPUT
![23](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/66e9e11a-ed22-42be-8655-2ca3c75f0457)


egrep 'Linux.*world' newfile 
## OUTPUT
![24](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/a4e89507-e805-41bb-adc8-c9f9ad362c69)
egrep 'Linux.*World' newfile 
## OUTPUT
![25](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/f36e948d-771b-4824-adff-afe4cfa3b649)

egrep l{2} newfile
## OUTPUT

![26](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/1ec909a7-8b25-408d-8cd6-3a1e27926543)


egrep 's{1,2}' newfile
## OUTPUT
![27](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/bd2df88e-1779-44a5-864e-849659691e6f)

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

![28](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/2babcfc5-6b97-4e82-b065-8bc6bcf1f2ec)


sed -n -e '$p' file23
## OUTPUT

![29](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/dee448b3-9cfa-4659-a551-692b1b62ff42)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![30](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/bba823a6-50f6-4115-86b3-1ea0ba7c3324)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![31](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/c2477d72-ab09-414f-bc4c-0902d1b30072)


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![54](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/4558ad90-6287-454f-b45b-590a85543664)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![55](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/2b2f2f33-54ff-4a67-8e75-aed4ced63e98)


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

 ![56](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/43a44139-74ae-45c6-83e5-175f4aedfcfa)

ls file1
## OUTPUT
![57](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/eeefccef-7282-457c-8d38-d115071aeb20)
echo $?

## OUTPUT 
![58](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/f0c0e7ba-3e17-4f33-85b6-b066ab1de0fb)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![59](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/c7df69ad-9abd-4fce-95de-cf2afb2c4d60)

abcd
 
echo $?
 ## OUTPUT
 ![60](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/b544b117-25ea-4354-8cd7-a5d9f1916227)



 
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
![output](./61.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![62](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/c8ef8701-bc4d-4b01-a4f9-4692a8fa0718)

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
![63](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/fb2b02d2-db83-4d37-a795-efed16ccaf55)

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

![64](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/160610fa-1572-442b-a9c7-848bed944da9)

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
![65](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/186b5cd9-c7cc-4c71-9a51-10fdd355e404)

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


![66](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/71828d19-87e0-429a-9fcc-15ca0c97d96d)

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
![67](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/b07b4936-4352-431d-aeab-1d9369d82688)

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
![68](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/813a3f6e-51b0-4ee1-8d10-e572196ae8a9)

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
## output
 ![69](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/23478268-79f9-4e15-9914-cc35fd46c777)

cat > whiletest
```bash
\#!/bin/bash
\#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## output
 ![70](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/6e03f576-8ac8-4c22-8b0a-b4c03eb21f94)

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
## output
 ![71](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/c684bd09-b5a0-48ca-8de5-75a6db253604)

 
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
 ```
cat forin1.sh 
```bash
#!/bin/bash
# basic for command!
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![72](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/911cac86-4b8e-4f75-8801-d55dd36b96ba)

![74](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/68de3b5a-0bdb-46b5-ad88-db97d57e2d8b)
![76](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/57717fb1-d562-4094-8597-8fc8ca1e2ce4)



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
![73](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/34a74755-de61-4ff0-8f81-a980f9a41d49)

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
![77](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/9458082e-e8ad-4487-adb5-3f0651bbe005)

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
![78](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/e40617a3-a150-493c-86da-933003974101)

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
 ![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/ade4ef7c-4022-444b-842d-421a704049b7)


 
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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/85626b0e-707b-4be6-a8e1-34308820a10d)


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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/452434ca-05e1-4484-a5f0-f8aa50be33fd)

 
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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/17a22081-c540-4669-85dc-a1fb3628a3da)



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/e185af2e-cb0a-4f16-8c82-009f9669fe0e)



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
 ### ./funcex.sh 
 ![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/c590977e-7b0d-4ad3-8982-e6cca0cbaa91)

 
 ### ./funcex.sh 1 2
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/b9eac82e-2197-41d6-af85-521feab8e0ab)

 
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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/1ea0be83-dbbd-4e44-a4e8-4dd7fafd7265)

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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/9515d1d0-267e-48b4-923c-758df725863a)

 
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
 ![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/9d673bf9-9f28-4858-9af3-b319a3021196)

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
![image](https://github.com/Kathiresan-23013376/OS-Linux-commands-Shell-script/assets/150008375/dae5140d-b17b-46c1-a222-dee6a68d35e5)



# RESULT:
The Commands are executed successfully.
