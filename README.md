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

<img width="997" height="417" alt="screen shot 1" src="https://github.com/user-attachments/assets/9916a1f1-6374-46f1-9509-46bda1439aa8" />


cat < file2
## OUTPUT

<img width="1012" height="502" alt="screenshot 2" src="https://github.com/user-attachments/assets/0bbb7b6a-a1dd-48a8-a7a1-2096a0386a8b" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1115" height="211" alt="screen shot 3" src="https://github.com/user-attachments/assets/30b5d27e-65e8-4624-8049-b43e45f0dd1f" />

comm file1 file2
 ## OUTPUT

<img width="1377" height="745" alt="screenshot 4" src="https://github.com/user-attachments/assets/b1cc277d-ffd5-4182-8117-4ebf911318f7" />

 
diff file1 file2
## OUTPUT
<img width="680" height="485" alt="screenshot 5" src="https://github.com/user-attachments/assets/87a06b55-bfba-40c0-af51-9f48dcb0d257" />

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

<img width="517" height="155" alt="screenshot 6" src="https://github.com/user-attachments/assets/9c057a03-50cb-46b8-9c2c-ef0672bd0e46" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="557" height="192" alt="screenshot 7" src="https://github.com/user-attachments/assets/b99c450f-9913-4bd7-a150-028bb019db7f" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="555" height="175" alt="screenshot 8" src="https://github.com/user-attachments/assets/0f4e5ea7-6bb2-4f2d-994b-5bf5780ccac9" />

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

<img width="570" height="125" alt="Screenshot 9" src="https://github.com/user-attachments/assets/a20f4753-3516-41f8-96ac-1afcc61731da" />


grep hello newfile 
## OUTPUT


<img width="545" height="105" alt="ss 10" src="https://github.com/user-attachments/assets/84f07783-0038-403c-bea5-dd92f312242b" />


grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT
<img width="567" height="142" alt="ss 11" src="https://github.com/user-attachments/assets/3c68faa9-2e82-4ed5-bc94-87c4dbcb564e" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="590" height="96" alt="ss 12" src="https://github.com/user-attachments/assets/0571bfe6-df2f-4aeb-870a-f54ffb098270" />



grep -R ubuntu /etc
## OUTPUT

<img width="807" height="552" alt="ss 13" src="https://github.com/user-attachments/assets/7bd4d119-fcd6-4a19-837b-38203ad6e996" />


grep -w -n world newfile   
## OUTPUT
<img width="455" height="146" alt="ss 14" src="https://github.com/user-attachments/assets/63e56f76-0744-4c9b-a97e-12a742da89f8" />


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

<img width="422" height="107" alt="ss 15" src="https://github.com/user-attachments/assets/fef9666e-bfe0-4280-b2bc-528dfaf028a5" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="432" height="105" alt="ss 16" src="https://github.com/user-attachments/assets/82f3420f-03ab-4fdc-8e06-7a24725a2e0b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="517" height="100" alt="ss 17" src="https://github.com/user-attachments/assets/09b24dba-f54f-460b-837a-b99f251d8dc1" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="352" height="72" alt="ss 18" src="https://github.com/user-attachments/assets/1786c72f-5e19-4cd8-8a21-a775b65819f3" />


egrep '(world$)' newfile 
## OUTPUT

<img width="407" height="127" alt="ss 19" src="https://github.com/user-attachments/assets/78679144-5e3f-4595-b381-58f7ee75a1f2" />


egrep '(World$)' newfile 
## OUTPUT

<img width="337" height="80" alt="ss 20" src="https://github.com/user-attachments/assets/3f33acf0-c56e-46fc-90e4-70c63d77cda6" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="366" height="127" alt="ss 21" src="https://github.com/user-attachments/assets/777c54ee-4da5-44bc-ac1d-e80dee31d300" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="307" height="87" alt="ss 22" src="https://github.com/user-attachments/assets/3bdd5f24-59f3-4867-bd20-3ded4ae834f5" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="417" height="67" alt="ss 23" src="https://github.com/user-attachments/assets/a375f52b-01cb-4ef6-93bb-b6653f0b787b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="355" height="76" alt="ss 24" src="https://github.com/user-attachments/assets/db918e7a-d48b-417a-81a0-aebfe82032e5" />

egrep l{2} newfile
## OUTPUT
<img width="351" height="97" alt="ss 25" src="https://github.com/user-attachments/assets/5d4acaf5-7458-451b-af79-de09d9ff0223" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="407" height="126" alt="ss 26" src="https://github.com/user-attachments/assets/e3f94d72-115d-41ea-ae14-271e3d707b68" />


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

<img width="465" height="82" alt="ss 27" src="https://github.com/user-attachments/assets/0f4175e9-5efa-4cdd-b0da-760f47f201f5" />


sed -n -e '$p' file23
## OUTPUT

<img width="402" height="102" alt="ss 28" src="https://github.com/user-attachments/assets/7595183b-8857-45bf-8612-2a52502140cc" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1132" height="602" alt="ss 29" src="https://github.com/user-attachments/assets/e41baded-9dc0-4a69-bf2a-00a76a8cb209" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1217" height="592" alt="ss 30" src="https://github.com/user-attachments/assets/993431cb-318d-42b3-ae6e-25b681341d1e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1342" height="595" alt="ss 31" src="https://github.com/user-attachments/assets/7f113a45-1834-44a2-bc44-3e2f2220138b" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1132" height="602" alt="ss 29" src="https://github.com/user-attachments/assets/6fb66f28-9d38-4a6c-a358-f559107e6ad5" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Uploading ss 30.png…]()



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1342" height="595" alt="ss 31" src="https://github.com/user-attachments/assets/94674a78-6687-42d8-84e7-2b336f4aa103" />


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



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
<img width="946" height="450" alt="ss 32" src="https://github.com/user-attachments/assets/f520d848-a197-427f-9d99-04520f62b99f" />


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

<img width="927" height="557" alt="ss 33" src="https://github.com/user-attachments/assets/101dd79b-be2f-464b-ae8d-fdec14ed4f79" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="840" height="357" alt="ss 34" src="https://github.com/user-attachments/assets/54ba36b6-e7ff-4d99-8164-c9684208c5eb" />

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


 <img width="825" height="345" alt="ss 35" src="https://github.com/user-attachments/assets/832bd217-f094-40d0-8f62-b3de43cb076a" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="945" height="792" alt="ss 36" src="https://github.com/user-attachments/assets/8d8b4248-1155-4d7b-95be-5303cd1d534f" />

tar -xvf backup.tar
## OUTPUT

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
<img width="496" height="391" alt="ss 37" src="https://github.com/user-attachments/assets/b2287da2-79f6-49ee-bebc-7c46804a6ddf" />


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

 <img width="720" height="657" alt="ss 38" src="https://github.com/user-attachments/assets/bc20070c-64c3-475f-a261-8f38e3b84b1d" />

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
<img width="811" height="552" alt="ss 39" src="https://github.com/user-attachments/assets/49ce9b06-95dd-4c65-a2f3-ac042c13cc87" />


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
<img width="806" height="555" alt="ss 41" src="https://github.com/user-attachments/assets/b6e929e1-d502-4197-bbb7-2e1a00cf0142" />

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

<img width="646" height="552" alt="ss 42" src="https://github.com/user-attachments/assets/5d2f13e2-25ab-4171-be8c-dee2c0e620ff" />


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
<img width="801" height="502" alt="ss 43" src="https://github.com/user-attachments/assets/fe55da9d-683e-4ff1-a0c7-85824543ce6f" />

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
<img width="800" height="752" alt="ss 44" src="https://github.com/user-attachments/assets/4eb31549-8e3e-44f9-b720-7eb452725c1e" />

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
<img width="797" height="660" alt="ss 45" src="https://github.com/user-attachments/assets/c6654489-df31-41b8-b1c1-4982a6beb9a4" />


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
<img width="806" height="322" alt="ss 46" src="https://github.com/user-attachments/assets/f442f91e-fc27-4d1c-815a-5100d5124923" />

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
<img width="802" height="446" alt="ss 47" src="https://github.com/user-attachments/assets/fc9458dd-2548-4262-8122-e6b5f75a83b0" />
<img width="802" height="515" alt="ss 48" src="https://github.com/user-attachments/assets/61ccb5df-c391-46e7-937b-7014b699a072" />

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

<img width="810" height="367" alt="ss 49" src="https://github.com/user-attachments/assets/e5aa1c1f-022a-42b4-a3cf-9b78415316a1" />

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
<img width="537" height="272" alt="ss 50" src="https://github.com/user-attachments/assets/5f5d57e9-e5b8-40b1-8e05-d39b5d58f676" />

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
<img width="807" height="656" alt="ss 51" src="https://github.com/user-attachments/assets/9c78383c-a0aa-477e-b01e-f71ef935c969" />

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

 <img width="807" height="656" alt="ss 51" src="https://github.com/user-attachments/assets/ca3bd34e-75c9-447c-a404-5a6dc6eabb84" />

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
<img width="807" height="450" alt="ss 52" src="https://github.com/user-attachments/assets/4839cf63-b6b1-42ae-be53-f2d30891fabb" />

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
 <img width="622" height="280" alt="ss 53" src="https://github.com/user-attachments/assets/4ccf95e0-b9c4-4011-a3ae-a230a7bc204b" />

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

<img width="687" height="222" alt="ss 54" src="https://github.com/user-attachments/assets/45738631-ca89-4bd8-84cd-03a3e64616a4" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="687" height="222" alt="ss 54" src="https://github.com/user-attachments/assets/dc62f881-b817-4e92-8d81-c7a8dd671fae" />


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

 <img width="830" height="451" alt="ss 55" src="https://github.com/user-attachments/assets/8bfd4230-8d24-4904-937a-c7a94b6bfc89" />

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
 <img width="612" height="327" alt="ss 56" src="https://github.com/user-attachments/assets/4c247dc4-5676-4a2e-b89a-a3c5f9366a70" />

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
 ![Uploading ss 57.png…]()

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
 
 <img width="822" height="657" alt="ss 58" src="https://github.com/user-attachments/assets/7d492ae0-5082-4fca-80a5-fca37f3e6077" />

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
 <img width="822" height="671" alt="ss 59" src="https://github.com/user-attachments/assets/a8ceae7a-9164-4c49-b262-4570e1d93007" />

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
