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

![Screenshot from 2025-04-06 12-38-47](https://github.com/user-attachments/assets/50b63574-0ce8-43a5-89e9-87d5c7ae637b)


cat < file2
## OUTPUT

![Screenshot from 2025-04-06 12-39-43](https://github.com/user-attachments/assets/a96f39e4-5a27-495f-ab1c-5e7e7ab9cbfd)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-06 09-24-00](https://github.com/user-attachments/assets/cc356473-450c-4584-af53-8162e5d04ad7)

 
comm file1 file2
 ## OUTPUT
 
![Screenshot from 2025-03-06 09-24-26](https://github.com/user-attachments/assets/5d12f9c3-bbbc-41c1-8da3-1a76d1af812c)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-06 09-24-55](https://github.com/user-attachments/assets/64023a16-903d-4c5d-8a1f-45f26629faf0)



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

![Screenshot from 2025-03-06 09-29-36](https://github.com/user-attachments/assets/5a7f8cea-cab6-466a-bcea-68b48e6f9193)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-06 09-31-54](https://github.com/user-attachments/assets/95c669c1-01f0-4d2b-abf0-227446f8768e)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-06 09-32-24](https://github.com/user-attachments/assets/4a5dcf51-fe4c-4644-9fe2-92c8958f3938)



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
![Screenshot from 2025-03-06 09-34-51](https://github.com/user-attachments/assets/927642b9-796a-4d3d-a52e-352db4ff47c5)




grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-06 09-37-20](https://github.com/user-attachments/assets/8d90e52b-3843-4271-ad26-378c229c024e)





grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-06 09-38-14](https://github.com/user-attachments/assets/8fc192b0-ae2b-4336-8014-512e519c5c67)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-06 09-39-04](https://github.com/user-attachments/assets/82b6a16e-db6e-4809-b8ff-afa0d0a816c3)



cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-06 09-39-55](https://github.com/user-attachments/assets/bf07374a-6605-490b-a0ad-ad0a9236b77d)




grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-03-06 20-29-40](https://github.com/user-attachments/assets/3e050edf-09d2-4f93-99fc-9538dffcb2f1)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-03-06 20-43-16](https://github.com/user-attachments/assets/820cfa79-c52b-48d1-a71c-ac08cd59a84c)


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

![Screenshot from 2025-03-06 20-52-01](https://github.com/user-attachments/assets/a627e574-0ac0-440a-94f6-397571f8512c)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-06 20-53-33](https://github.com/user-attachments/assets/ab4ef279-2eb1-4ba7-9ab9-b6e72409f3a8)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 20-53-33](https://github.com/user-attachments/assets/d2c2363e-05f0-4b8d-894f-43df03613447)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-06 20-56-33](https://github.com/user-attachments/assets/9738c5bd-fb14-442b-a312-7ca81d92c5c2)



egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 20-57-30](https://github.com/user-attachments/assets/374f41b5-d171-4bd7-9a1c-164d3e6bfc62)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-06 20-59-27](https://github.com/user-attachments/assets/b67f204c-cf9f-4448-8fc2-a99a2cc2bf0c)


egrep '((W|w)orld$)' newfile 
## OUTPUT


![Screenshot from 2025-03-06 21-00-14](https://github.com/user-attachments/assets/04013c61-2a7e-4acc-a9e6-7938b1421f4f)

egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 21-01-08](https://github.com/user-attachments/assets/43358e19-1dfb-40d4-b8b2-0519cc86137f)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-06 21-15-59](https://github.com/user-attachments/assets/854eb29e-d740-4ef9-9df1-d4f9dc40eb45)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-04-10 08-20-56](https://github.com/user-attachments/assets/739b86c4-1cca-44a2-90ee-d65785f7ba12)



egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-04-10 08-21-58](https://github.com/user-attachments/assets/354fca8b-1b98-4f84-bba5-13fcbee19c23)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-08 13-43-46](https://github.com/user-attachments/assets/ef906b66-b4f7-4ee1-ab96-e08e6a17a539)



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
![Screenshot from 2025-04-10 08-24-26](https://github.com/user-attachments/assets/d745bfd6-184d-4c3f-9553-6785c8309964)





sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-08 13-49-37](https://github.com/user-attachments/assets/81fad30a-75bc-4e6c-83d7-3bc9e39ca25d)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 13-50-27](https://github.com/user-attachments/assets/473dcfc9-8094-4f03-a7d3-cc03af1d3072)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 13-50-27](https://github.com/user-attachments/assets/7fcea58f-5cd9-4489-9591-4d1a5a23064c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-03-08 13-54-01](https://github.com/user-attachments/assets/892bb41b-73a7-4390-8b96-057f92585f7d)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-08 13-55-03](https://github.com/user-attachments/assets/ef964613-d4b9-4772-a22f-c25c45bdb8ea)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-03-08 13-55-47](https://github.com/user-attachments/assets/49d91a21-d014-4168-8311-73caa9b1a664)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-08 13-56-32](https://github.com/user-attachments/assets/dcfdab06-898c-4ddd-94e4-6aed38dfb866)


seq 10 
## OUTPUT
![Screenshot from 2025-03-08 13-56-55](https://github.com/user-attachments/assets/636ff6af-3ace-4aef-8caf-5d51a477a8a3)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-08 13-57-56](https://github.com/user-attachments/assets/bd461b3f-2f25-43d6-b120-9448ef9c776e)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-08 13-59-07](https://github.com/user-attachments/assets/90efc43f-2456-479f-98fe-73dbc6fec260)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-08 14-00-02](https://github.com/user-attachments/assets/fbe9b141-2cfb-4b9b-8579-1fe6b9dee4fc)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-08 14-00-44](https://github.com/user-attachments/assets/388a0666-628f-446e-b93a-4bda9c1e90a9)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-03-08 14-01-29](https://github.com/user-attachments/assets/877b183c-69c3-4720-9242-10fd7fe5bcbd)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-03-08 14-02-40](https://github.com/user-attachments/assets/0d93d714-0c9e-4de4-bffc-e8ad5fb7175a)


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
![Screenshot from 2025-03-08 14-05-20](https://github.com/user-attachments/assets/33095ed3-b0d8-4b96-bd47-9092e4dc1885)


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
![Screenshot from 2025-03-08 14-07-43](https://github.com/user-attachments/assets/34b16c30-5b9c-4a76-960e-c962f092cb1e)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-03-08 14-09-02](https://github.com/user-attachments/assets/9da69d65-0229-4ec5-a7b0-1e11f0e9231a)

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

![Screenshot from 2025-03-08 14-13-06](https://github.com/user-attachments/assets/19a9522f-62e1-4157-8937-98f2a1d27a2d)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-03-09 20-40-50](https://github.com/user-attachments/assets/d48877be-b86a-4701-86e0-901607831d8d)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-09 20-41-11](https://github.com/user-attachments/assets/4bd6a97a-c248-4be5-918d-b730197eff8e)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot from 2025-03-09 20-41-25](https://github.com/user-attachments/assets/02e58673-2b3b-4eff-a6cd-49cdce9c2693)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-09 20-41-37](https://github.com/user-attachments/assets/ed40637e-ecbf-4f47-9ba7-d11032310ccc)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot from 2025-03-09 20-41-54](https://github.com/user-attachments/assets/65a26758-2716-4e96-a7af-0609347bc28b)

gunzip backup.tar.gz
## OUTPUT

![Screenshot from 2025-03-09 20-42-04](https://github.com/user-attachments/assets/bc3148c7-f086-477c-964d-57826f62e85f)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-03-09 20-45-38](https://github.com/user-attachments/assets/658fd5ac-055e-405f-a97e-2ee7e3c325ae)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2025-03-09 20-47-27](https://github.com/user-attachments/assets/0e9eb1ba-5409-4f1a-9a5b-1398d9281a8b)

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
![Screenshot from 2025-04-10 08-38-34](https://github.com/user-attachments/assets/541d0b75-9157-4d40-ae27-56908dd3cc6f)

 
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
