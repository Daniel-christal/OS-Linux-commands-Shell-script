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
![image](https://github.com/user-attachments/assets/08402428-e54f-4cc8-bd48-472c33d3b138)


## OUTPUT
![image](https://github.com/user-attachments/assets/67193d61-8a15-4235-93e7-9948e2c8e0a1)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/58ae4dfa-ba38-4140-988d-b4ace7495a3d)

 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/1a5d4c1e-95df-4681-a492-d9fa6e95911d)

## OUTPUT
![image](https://github.com/user-attachments/assets/b4f95526-1f59-4f27-9040-10b390a79f86)


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
![image](https://github.com/user-attachments/assets/495a0f4c-05c1-4e8a-a1d7-a6119f32067a)


cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/b33f0a33-0e12-4622-a914-8b5148c4993f)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/1b3d29dc-eb45-4b15-a0e1-5119f118b5e7)


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
![image](https://github.com/user-attachments/assets/18fed6e1-c8f1-43a3-9059-93cb6d994f96)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/43e15053-3d30-4142-95ec-e909e8e26a22)


grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7a1de95c-946e-4960-842e-a3f9aeda9baf)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/2ca553a6-ebfd-45da-b64b-5ef7bae7d5d6)


cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/a247a4a0-b45d-4cfa-8a21-0421aeae78b9)


grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT


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
![image](https://github.com/user-attachments/assets/877bc707-3963-4c4b-9869-ddf588c274ea)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/29bd6c69-75f8-4efa-9663-734afbb31e5c)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/80c80b80-368f-4499-8565-5fcd8529faa3)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c9482271-7e66-4db1-8df1-1f659ecf4849)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/13726181-d0c5-4c21-90d0-958fb6f444f9)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d274bd03-ed30-4aa5-a00d-9683f973ff0b)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ac40d1d8-a95d-4444-ac4a-cffb881f4292)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9dfc6d04-d1e1-4228-902f-2b656ccf8621)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c54991c2-683d-46f9-9d97-50254dabff03)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d1fb60ae-eb46-4da7-981f-0105177bc0c8)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/33ce21d9-a6b3-45b1-a26e-a1af2a98dfbf)



egrep 's{1,2}' newfile
## OUTPUT 


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

![image](https://github.com/user-attachments/assets/2c4d6701-90cf-4044-8e0a-9c47bc529f5b)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/a5aacd71-f6f7-4428-86bc-01904c2e0ac4)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/1b51d49b-e817-4b0b-a824-47444e4e6413)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f9c77f55-73ce-4c2a-88ae-a0dca7e56a72)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/deb119b8-778b-4fa0-875b-0ac45fe70bd3)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/78562ac1-bc1c-4fcd-bc6f-80b4d3f6f606)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/40be8494-0ea8-4790-9635-4665ac48c490)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1ae4c4a9-5396-48c1-8dc2-57469326d186)



seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/6f9931b5-00ea-4be4-bf00-74f773ef1bec)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/8f5314e2-9dd4-4bf7-8f86-a43f7eea8945)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/771e099f-5eb0-45b6-b87b-3151ea7b49c8)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/85f23438-a6f4-40f6-bf3f-681415d8e012)

seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/95ca0ded-9d12-428a-8b23-b928455ad3e5)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/aa692d07-6908-447a-98c9-dfdfa39495f2)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5d5520ac-a397-4888-876a-6f7236ef041c)



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
![image](https://github.com/user-attachments/assets/a242df26-b623-43ba-8452-fcfb36d06201)


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

![image](https://github.com/user-attachments/assets/3cc52142-b358-495b-92b8-d7b43d471169)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/278573ad-e3da-4796-93e1-61c066c1ce12)

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

![image](https://github.com/user-attachments/assets/c01b90ef-356d-4e75-9a4e-ca9123f387bf)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/08dadbc0-f620-4514-9e94-18f312c3c930)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/72a3e25a-9138-40ea-8556-cf33ad5e17f2)


mkdir backupdir
 

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/fcb040f3-8213-479b-8f52-ae6697593dbd)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/589bfe6e-eb2c-4983-a7a9-32b407838559)


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
![image](https://github.com/user-attachments/assets/92ca568f-e02b-4671-bb8c-2fbb30a18125)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/3dc94a00-c13d-4270-977e-f3544fa22acf)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/389a052f-9ed3-483f-b559-25b1166192b0)

./one
bash: ./one: Permission denied
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/bc206200-f2a5-46d4-b826-b9addd31448c)

 
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

![image](https://github.com/user-attachments/assets/71ce2456-f18d-4eeb-9717-b7a02651fa25)


chmod 755 strcomp.sh
 
./strcomp.sh 

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
![image](https://github.com/user-attachments/assets/65dad7f0-61d5-4ba4-8ffe-9641bd101adc)



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
![image](https://github.com/user-attachments/assets/79ee5d5b-11da-4362-8743-aba73ff071e4)


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
![image](https://github.com/user-attachments/assets/bbcc5ed1-0631-495d-a242-c8c906680122)

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
![image](https://github.com/user-attachments/assets/f76af194-b9ed-4b30-91b1-f429611bc3b2)


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
![image](https://github.com/user-attachments/assets/6ebb0fbb-fe8b-46a6-8d4f-c31c7f72ed36)


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
![image](https://github.com/user-attachments/assets/95200232-b288-44f9-88dd-b41126dfba7c)

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
![image](https://github.com/user-attachments/assets/8e889791-c183-4531-a046-ef4af5ce6b7b)

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
![image](https://github.com/user-attachments/assets/9e60d3e8-75d6-4cdf-b739-72f8014135ea)

 
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
![image](https://github.com/user-attachments/assets/01d0661a-0dc6-45e2-babe-22bfe0addf29)

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
 ![image](https://github.com/user-attachments/assets/c1780f41-4cdb-4448-8326-fe83bb577f7f)

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
![image](https://github.com/user-attachments/assets/3ba4a9db-eb23-4d9a-8d44-a84bde803c43)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/5fffd4ac-4cb4-4b2a-af11-9692adeb6b66)



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
![image](https://github.com/user-attachments/assets/4186e03d-6686-40f1-96d3-826876774216)

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
![image](https://github.com/user-attachments/assets/4bdb0d7b-347a-4275-ba41-bfb65f97aad7)

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
 ![image](https://github.com/user-attachments/assets/ca733c1a-9d86-4f66-aa55-36ae1ffb9f7b)

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
![image](https://github.com/user-attachments/assets/857d479e-a2b1-4f5a-b195-bff8bd319679)


# RESULT:
The Commands are executed successfully.
