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
<img width="688" height="174" alt="image" src="https://github.com/user-attachments/assets/558d293c-af6b-4079-8b02-d47d08423729" />




cat < file2
## OUTPUT
<img width="698" height="202" alt="image" src="https://github.com/user-attachments/assets/7fd84499-38b0-41ec-904f-bbc82578420e" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="488" height="41" alt="image" src="https://github.com/user-attachments/assets/eb412549-716f-4b52-9ea8-34a2fdec1673" />

 
comm file1 file2
 ## OUTPUT
 <img width="646" height="300" alt="image" src="https://github.com/user-attachments/assets/124a8e27-50ed-495d-b666-c9abc945841e" />


 
diff file1 file2
## OUTPUT
<img width="648" height="301" alt="image" src="https://github.com/user-attachments/assets/0706650c-9b11-45a7-8949-c13dc26cc6ab" />



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
<img width="620" height="61" alt="image" src="https://github.com/user-attachments/assets/addf3e95-64c5-4fdc-8796-3f2da5d9a2d1" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="696" height="106" alt="image" src="https://github.com/user-attachments/assets/e2c49ba6-b606-4455-b4ff-879dbe4f9e60" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="700" height="109" alt="image" src="https://github.com/user-attachments/assets/ac2230e2-be30-4ba3-9147-2968c9d93ec1" />


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
<img width="657" height="62" alt="image" src="https://github.com/user-attachments/assets/bd9c1e31-f68c-4852-ba61-db2e1faa635b" />



grep hello newfile 
## OUTPUT
<img width="656" height="54" alt="image" src="https://github.com/user-attachments/assets/7d76b1c2-f91f-4b23-b6c0-76a48e13f1fb" />




grep -v hello newfile 
## OUTPUT
<img width="692" height="56" alt="image" src="https://github.com/user-attachments/assets/af3bab01-dac1-4548-b994-f6314d9b82cd" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="700" height="108" alt="image" src="https://github.com/user-attachments/assets/03c9c8c8-5382-4fd2-a865-e4add75d4bcc" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="702" height="107" alt="image" src="https://github.com/user-attachments/assets/609cb70d-5bfd-403e-be23-179a2a113913" />




grep -R ubuntu /etc
## OUTPUT
<img width="710" height="702" alt="image" src="https://github.com/user-attachments/assets/be7c1446-e3a3-46d4-8066-ae68c8ec20cb" />




grep -w -n world newfile   
## OUTPUT
<img width="708" height="105" alt="image" src="https://github.com/user-attachments/assets/43c88b93-dd9e-4c65-adf0-779f7a9c7370" />



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
<img width="702" height="103" alt="image" src="https://github.com/user-attachments/assets/3140b21e-a304-4bde-999d-3e00cc07d40d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="711" height="94" alt="image" src="https://github.com/user-attachments/assets/d1a7e83f-36ba-46d2-9542-c46e604c0acf" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="703" height="100" alt="image" src="https://github.com/user-attachments/assets/1e18b77a-d8e6-40eb-9219-2341093dd0b3" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="689" height="51" alt="image" src="https://github.com/user-attachments/assets/15bc80f1-178a-4e37-b211-b79dd1e0f2a9" />




egrep '(world$)' newfile 
## OUTPUT
<img width="699" height="90" alt="image" src="https://github.com/user-attachments/assets/617ea275-d834-446b-a403-e23cf48e2e02" />




egrep '(World$)' newfile 
## OUTPUT
<img width="725" height="53" alt="image" src="https://github.com/user-attachments/assets/14dae934-9160-4294-ac97-02d07d61aa28" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="746" height="146" alt="image" src="https://github.com/user-attachments/assets/240abba3-66b0-4bb7-b560-c620ad3c1287" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="716" height="62" alt="image" src="https://github.com/user-attachments/assets/5ab3df13-a5b1-4aff-a376-289a08e04e1a" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="734" height="95" alt="image" src="https://github.com/user-attachments/assets/c0eef368-ed10-416a-bdbd-c0f5fc98c046" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="746" height="88" alt="image" src="https://github.com/user-attachments/assets/59d8fc4a-1ca1-4145-8f57-2354b308b7b8" />


egrep l{2} newfile
## OUTPUT
<img width="663" height="85" alt="image" src="https://github.com/user-attachments/assets/291e3102-1a5e-4342-85f2-36ebd0c32337" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="713" height="114" alt="image" src="https://github.com/user-attachments/assets/a2081c96-6073-4715-972a-b8ba7914a211" />


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
<img width="688" height="56" alt="image" src="https://github.com/user-attachments/assets/979d30e4-a091-4750-9055-3107654f76b2" />




sed -n -e '$p' file23
## OUTPUT
<img width="693" height="61" alt="image" src="https://github.com/user-attachments/assets/16a9a1e5-5bb2-4894-976f-009deb4d8632" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="751" height="278" alt="image" src="https://github.com/user-attachments/assets/3d706f59-6ecd-4a9a-bc3d-03aba33ee347" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="750" height="277" alt="image" src="https://github.com/user-attachments/assets/4451ff8d-6ecb-475f-b528-7266a0903dda" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="740" height="285" alt="image" src="https://github.com/user-attachments/assets/a9a5fe84-8343-4c99-94c6-95f4be2b08b3" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="711" height="174" alt="image" src="https://github.com/user-attachments/assets/d0e4f53a-cf5b-4a6f-b2a7-dd1e2bd21b03" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="745" height="143" alt="image" src="https://github.com/user-attachments/assets/ab5adef5-d19a-4444-82eb-0bab74da0d1c" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="739" height="112" alt="image" src="https://github.com/user-attachments/assets/743c0cba-0644-4a0f-ae94-d882962d9ebb" />




seq 10 
## OUTPUT
<img width="506" height="313" alt="image" src="https://github.com/user-attachments/assets/786fe2f3-7575-47b8-91ee-0195c4414820" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="692" height="100" alt="image" src="https://github.com/user-attachments/assets/7a063bf5-0be1-47ab-93fe-9818fcd98f40" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="709" height="110" alt="image" src="https://github.com/user-attachments/assets/c8bc9523-6672-41ee-aaad-f5cfd53ee95f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="700" height="133" alt="image" src="https://github.com/user-attachments/assets/ca6d9e8b-ce00-4328-8931-667c3e805441" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="702" height="107" alt="image" src="https://github.com/user-attachments/assets/807ca3c2-07aa-4d85-9dbd-3c785f88dbd7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="732" height="118" alt="image" src="https://github.com/user-attachments/assets/fea35d85-3acf-4323-900c-b41726d76eb0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="744" height="138" alt="image" src="https://github.com/user-attachments/assets/46272333-fcae-4699-9714-3e2d92726bdf" />



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
<img width="567" height="167" alt="image" src="https://github.com/user-attachments/assets/e08bc912-ab97-4f7b-8a1b-3c20241687c7" />


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
<img width="572" height="171" alt="image" src="https://github.com/user-attachments/assets/9d289637-88ec-4e62-9bba-44d7f18cf121" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="748" height="274" alt="image" src="https://github.com/user-attachments/assets/9ba508e3-53b1-4acf-b13e-d7002f631b2b" />


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
<img width="737" height="140" alt="image" src="https://github.com/user-attachments/assets/e7755ef0-c1f8-430c-9b3e-1c63ff7c7c57" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="719" height="144" alt="image" src="https://github.com/user-attachments/assets/a911d8c0-d7a5-473a-ba37-0a0b6537006f" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="696" height="255" alt="image" src="https://github.com/user-attachments/assets/6cbc6faa-1a5d-48e4-b3a1-39fc114c632e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="752" height="290" alt="image" src="https://github.com/user-attachments/assets/c9f71e30-80a7-440e-9575-56a06b95d2a9" />


tar -xvf backup.tar
## OUTPUT
<img width="734" height="279" alt="image" src="https://github.com/user-attachments/assets/44723f66-ac3f-4e96-9f47-b0c0348f0118" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="669" height="63" alt="image" src="https://github.com/user-attachments/assets/b437389e-0159-441e-9aac-575ae30161ac" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="761" height="147" alt="image" src="https://github.com/user-attachments/assets/47d6c42b-be63-4276-b403-28658e8d1034" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="742" height="112" alt="image" src="https://github.com/user-attachments/assets/0c8e6c35-1a8e-4ccd-abcd-24c25186659e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="656" height="119" alt="image" src="https://github.com/user-attachments/assets/8d943bd4-5c46-49b6-b116-8a96b796a6b2" />


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
<img width="742" height="446" alt="image" src="https://github.com/user-attachments/assets/ad62a7f9-727f-4471-bc70-2240e603881c" />

 
ls file1
## OUTPUT
<img width="536" height="62" alt="image" src="https://github.com/user-attachments/assets/bc606c05-44ee-4985-b264-610389121c99" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="520" height="53" alt="image" src="https://github.com/user-attachments/assets/980b9b25-dcb2-4104-a7b7-7f94e1bb3880" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="521" height="50" alt="image" src="https://github.com/user-attachments/assets/f6d6ba8a-806a-4e9c-9aab-751de2f7cac3" />


 
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
<img width="685" height="112" alt="image" src="https://github.com/user-attachments/assets/d17a789e-d3b5-4e2d-8f1e-fba10ee7599a" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="714" height="120" alt="image" src="https://github.com/user-attachments/assets/cc538a68-a053-48bc-a731-d7a0bbb615f3" />




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
<img width="705" height="119" alt="image" src="https://github.com/user-attachments/assets/56bf2c47-5095-45c1-8731-92e0a29336d2" />

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
<img width="764" height="169" alt="image" src="https://github.com/user-attachments/assets/7b4746d5-aa1c-43db-af84-2f68d52fc28e" />



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
<img width="670" height="137" alt="image" src="https://github.com/user-attachments/assets/408be499-811f-4f71-babc-4d1ebacc1d9d" />

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

<img width="695" height="165" alt="image" src="https://github.com/user-attachments/assets/962fffb8-a250-4a5b-b512-fbabf98eb05e" />

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
<img width="702" height="116" alt="image" src="https://github.com/user-attachments/assets/4d05c415-75af-4e7b-a76d-3654616b795e" />


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
<img width="699" height="107" alt="image" src="https://github.com/user-attachments/assets/ad642f30-7675-4a76-a97c-c25e840edd63" />

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
<img width="654" height="245" alt="image" src="https://github.com/user-attachments/assets/e4fa2306-27f3-4d41-8264-ebed157d08fc" />

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
<img width="731" height="270" alt="image" src="https://github.com/user-attachments/assets/95ab2815-302a-48ec-98a8-87bf5a2450e0" />


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
<img width="683" height="193" alt="image" src="https://github.com/user-attachments/assets/2b95de6d-441b-4909-bf36-4b3561acd208" />

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
<img width="688" height="187" alt="image" src="https://github.com/user-attachments/assets/97965c6c-d20f-4a71-a019-1172e89113ba" />

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
<img width="706" height="379" alt="image" src="https://github.com/user-attachments/assets/4659d82f-bf4f-4fc8-b2fb-9b6efc56ff27" />

 
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
<img width="729" height="225" alt="image" src="https://github.com/user-attachments/assets/a0f104f9-b623-433b-ba81-e0cbd4e4e0bb" />


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
<img width="681" height="123" alt="image" src="https://github.com/user-attachments/assets/d08262ca-cccf-445c-b30c-0288e9a061d0" />
 
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
<img width="684" height="111" alt="image" src="https://github.com/user-attachments/assets/6acbe6a6-ddd1-46c1-a3fc-4de50f53a3b7" />



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
<img width="687" height="83" alt="image" src="https://github.com/user-attachments/assets/e6b17c4a-1f49-45b2-ad8c-86eaeccf8d76" />

 
 ./funcex.sh 1 2
<img width="630" height="56" alt="image" src="https://github.com/user-attachments/assets/7617f302-dcd8-4e04-8f5b-82f82a51d8de" />

 
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
<img width="714" height="119" alt="image" src="https://github.com/user-attachments/assets/c72a0ed1-d4f5-4385-a4a8-b717f5c58f24" />

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
<img width="700" height="133" alt="image" src="https://github.com/user-attachments/assets/59603a0c-bb77-44d0-95b7-3b474cbaffa3" />

 
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
<img width="717" height="411" alt="image" src="https://github.com/user-attachments/assets/933140bc-db11-46b3-88be-d496fcebfa3b" />
 
 
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
<img width="693" height="400" alt="image" src="https://github.com/user-attachments/assets/23c0f09e-8bf3-4bd7-b3db-37d9694b10ce" />
 
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
<img width="700" height="149" alt="image" src="https://github.com/user-attachments/assets/690509db-b3f6-40d3-b6d7-00100ef168c5" />

# RESULT:
The Commands are executed successfully.
