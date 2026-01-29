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
<img width="615" height="116" alt="image" src="https://github.com/user-attachments/assets/939013e3-e275-4333-9a80-8190bbec6bc0" />



cat < file2
## OUTPUT
<img width="601" height="130" alt="image" src="https://github.com/user-attachments/assets/311b485b-9ba4-4498-b46f-0273556dfa41" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="538" height="46" alt="image" src="https://github.com/user-attachments/assets/03007756-f3f3-4fcc-b984-695106859423" />
 
comm file1 file2
 ## OUTPUT
<img width="620" height="48" alt="image" src="https://github.com/user-attachments/assets/c2840e49-4e35-49a9-af14-2575182b18e1" />

 
diff file1 file2
## OUTPUT
<img width="507" height="216" alt="image" src="https://github.com/user-attachments/assets/b59257b8-d6f1-42b7-99db-ef9bc6df1176" />


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
<img width="509" height="56" alt="image" src="https://github.com/user-attachments/assets/b42f4dba-fd6a-423c-8506-23c690447b8c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="622" height="84" alt="image" src="https://github.com/user-attachments/assets/28377c96-7ec3-4832-923f-a02779b39508" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="573" height="89" alt="image" src="https://github.com/user-attachments/assets/9db0e173-74f0-44fb-9da4-bb58d191c9e7" />


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
<img width="501" height="72" alt="image" src="https://github.com/user-attachments/assets/c60cd48b-2eee-4846-9aa9-e72414728289" />



grep hello newfile 
## OUTPUT
<img width="462" height="46" alt="image" src="https://github.com/user-attachments/assets/f9fff259-9b17-4f7b-b99f-b23df127741d" />




grep -v hello newfile 
## OUTPUT
<img width="491" height="46" alt="image" src="https://github.com/user-attachments/assets/116c7872-ce69-418b-a719-7040265eb9e3" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="479" height="45" alt="image" src="https://github.com/user-attachments/assets/1f31de37-15d2-4c11-a011-60ab135e28f6" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="576" height="69" alt="image" src="https://github.com/user-attachments/assets/9b4cdfe8-59ac-43fd-9989-5bf98c92c950" />




grep -R ubuntu /etc
## OUTPUT
<img width="564" height="39" alt="image" src="https://github.com/user-attachments/assets/d8cfd058-ea48-4be1-b1ff-ed2683c7f1fb" />



grep -w -n world newfile   
## OUTPUT
<img width="736" height="374" alt="image" src="https://github.com/user-attachments/assets/02369915-7c88-4435-9f2e-fa598788078a" />


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
<img width="520" height="53" alt="image" src="https://github.com/user-attachments/assets/913ba11a-e06a-45fb-ad59-952125f09f1f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="599" height="107" alt="image" src="https://github.com/user-attachments/assets/f5aa19f3-eb55-4c9e-82b8-7b3b4ddca2f9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="544" height="55" alt="image" src="https://github.com/user-attachments/assets/3b030023-d978-413d-8430-6993079e5208" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="524" height="50" alt="image" src="https://github.com/user-attachments/assets/364fd9a2-43cc-4511-a305-345be860c8b8" />



egrep '(world$)' newfile 
## OUTPUT
<img width="536" height="41" alt="image" src="https://github.com/user-attachments/assets/f802cc8c-88e9-452d-b671-f59147836d94" />



egrep '(World$)' newfile 
## OUTPUT
<img width="497" height="60" alt="image" src="https://github.com/user-attachments/assets/ecbcb414-7368-4310-b403-144e5023278f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="527" height="70" alt="image" src="https://github.com/user-attachments/assets/b578ad68-e4e8-43aa-bfda-075004738e8f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="525" height="40" alt="image" src="https://github.com/user-attachments/assets/85d7520e-41a7-4e88-b1bf-6804edd3514b" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="557" height="37" alt="image" src="https://github.com/user-attachments/assets/f7e36647-9203-433a-bf14-5c88f1f0fe11" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="485" height="40" alt="image" src="https://github.com/user-attachments/assets/eb98174b-4d4f-40fe-96a6-bd24c25ae0b5" />


egrep l{2} newfile
## OUTPUT
<img width="501" height="60" alt="image" src="https://github.com/user-attachments/assets/099cd9ce-1ed2-4a70-acec-b863ccdc9c90" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="579" height="74" alt="image" src="https://github.com/user-attachments/assets/f359ce4e-d58b-4294-86ad-4c8b3551360a" />


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
<img width="571" height="36" alt="image" src="https://github.com/user-attachments/assets/5ca358ca-06b7-4098-9732-45ba3ab77e35" />



sed -n -e '$p' file23
## OUTPUT
<img width="476" height="42" alt="image" src="https://github.com/user-attachments/assets/9cedb69e-ccb5-41bc-9026-7e313b9a418e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="558" height="168" alt="image" src="https://github.com/user-attachments/assets/ddc66a2d-b9ca-4837-ba40-a219ed4baf86" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="513" height="164" alt="image" src="https://github.com/user-attachments/assets/6000fe29-11d2-4271-a7f2-87578f91fe3e" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="569" height="162" alt="image" src="https://github.com/user-attachments/assets/baf7dabf-5650-45fc-9c27-68a076082ab8" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="613" height="108" alt="image" src="https://github.com/user-attachments/assets/21db6f50-014f-4b9c-b17f-256226e33f48" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="640" height="83" alt="image" src="https://github.com/user-attachments/assets/dec1e162-9fe0-4b63-9b25-ca70fa96842c" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="598" height="56" alt="image" src="https://github.com/user-attachments/assets/ae0945a5-7331-4922-aa24-f21d189197ae" />



seq 10 
## OUTPUT
<img width="549" height="193" alt="image" src="https://github.com/user-attachments/assets/631eafc0-dab2-419c-b2b9-95810f776c9c" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="558" height="62" alt="image" src="https://github.com/user-attachments/assets/ea183d28-476a-4890-aec0-9b4d4324d209" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="538" height="83" alt="image" src="https://github.com/user-attachments/assets/d3dae7e0-f375-4c41-8365-94fccb3a9a35" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="508" height="92" alt="image" src="https://github.com/user-attachments/assets/1fade037-551b-414e-b507-c6a5da3a0674" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="496" height="74" alt="image" src="https://github.com/user-attachments/assets/a7acb509-984f-4846-b804-69199e1725fc" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="434" height="73" alt="image" src="https://github.com/user-attachments/assets/fbab0861-fcf4-4778-8140-3d5fbd5a59ac" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="485" height="72" alt="image" src="https://github.com/user-attachments/assets/cfecb0a3-2737-4ff5-a96a-5b0cc2032872" />



sed -n '2,4{s/$/*/;p}' file23

<img width="488" height="69" alt="image" src="https://github.com/user-attachments/assets/bdc1bbff-09c7-42bd-b4f1-49394c62f0af" />
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
<img width="459" height="107" alt="image" src="https://github.com/user-attachments/assets/a038bb00-9f10-44f8-af63-37d4ef689f72" />



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
<img width="521" height="118" alt="image" src="https://github.com/user-attachments/assets/9f1dea11-fc7d-4500-9fd8-b319270fee30" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="520" height="168" alt="image" src="https://github.com/user-attachments/assets/e5682c86-0524-4864-9368-4eab78618cda" />

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
<img width="569" height="73" alt="image" src="https://github.com/user-attachments/assets/3ccbfbc6-b39f-4401-bc0b-175a35211529" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="565" height="76" alt="image" src="https://github.com/user-attachments/assets/1fd22528-b6fd-4e9b-bd81-d93350976ba9" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="550" height="165" alt="image" src="https://github.com/user-attachments/assets/6282fd90-0004-4854-820e-d1cf31aaebc6" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="766" height="167" alt="image" src="https://github.com/user-attachments/assets/32aff0d8-a711-48aa-b2f3-cbee6283b5af" />


tar -xvf backup.tar
## OUTPUT
<img width="572" height="161" alt="image" src="https://github.com/user-attachments/assets/5c805212-112e-407c-bd31-ed61320388f8" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="548" height="44" alt="image" src="https://github.com/user-attachments/assets/f1faad18-6820-405f-b72f-80fc63efb57d" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="657" height="63" alt="image" src="https://github.com/user-attachments/assets/aef7f993-ae0e-44ef-af26-56f0b872df9f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="688" height="100" alt="image" src="https://github.com/user-attachments/assets/eca43ce1-1fa8-4b79-93cf-83e7e5cd325b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="575" height="71" alt="image" src="https://github.com/user-attachments/assets/f9fb741c-d8ff-47ad-8f09-cee72a63ce6a" />


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
<img width="654" height="504" alt="image" src="https://github.com/user-attachments/assets/7fda53c1-15c9-45c6-bb91-cd8051cf736a" />

 
ls file1
## OUTPUT
<img width="575" height="39" alt="image" src="https://github.com/user-attachments/assets/4edaf7b0-a99c-42bc-a60f-5efbd7e0fdbd" />

echo $?

## OUTPUT
<img width="630" height="42" alt="image" src="https://github.com/user-attachments/assets/7f39d00e-e958-43dc-866a-40a08f7625b0" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="529" height="38" alt="image" src="https://github.com/user-attachments/assets/a4d9f65f-0224-4602-b370-6db7a09bb210" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="573" height="178" alt="image" src="https://github.com/user-attachments/assets/3cf8f9be-736c-47f6-bde8-da321383771c" />


 
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
<img width="635" height="190" alt="image" src="https://github.com/user-attachments/assets/86a6c215-3afb-49b0-959d-60dec7423bc6" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="730" height="72" alt="image" src="https://github.com/user-attachments/assets/56aa4e04-0a7c-41f2-ab36-5459e7d503d2" />


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
<img width="603" height="67" alt="image" src="https://github.com/user-attachments/assets/b8f2dd18-7ef4-42c7-81a5-a96f68492f30" />

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
<img width="581" height="105" alt="image" src="https://github.com/user-attachments/assets/eff72c54-7163-43cb-abe1-462d49e4ee2b" />



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
<img width="505" height="76" alt="image" src="https://github.com/user-attachments/assets/255d110d-b450-4fd9-ab07-62820c420928" />

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
<img width="646" height="91" alt="image" src="https://github.com/user-attachments/assets/b986f73b-02ca-45f9-b14d-41369ceda37e" />

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
<img width="499" height="58" alt="image" src="https://github.com/user-attachments/assets/f2d74fda-fe99-4b29-a9a6-1b1ac5f4be25" />


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
<img width="576" height="65" alt="image" src="https://github.com/user-attachments/assets/655b07c4-f9ea-47b6-96d3-852b55aa30c9" />

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
<img width="554" height="55" alt="image" src="https://github.com/user-attachments/assets/9078bb07-f436-4e08-9f28-7286b7a5eb5f" />
 
$ ./whiletest.sh
 
<img width="669" height="227" alt="image" src="https://github.com/user-attachments/assets/ad59a736-3392-4f9d-b13d-2095fd73b3eb" />
 
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
 
 
<img width="655" height="131" alt="image" src="https://github.com/user-attachments/assets/09f07798-2f57-4f12-90ee-949913e7dbc4" />
 
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
 
<img width="595" height="158" alt="image" src="https://github.com/user-attachments/assets/3f9ab9b1-155f-42e9-8c66-11f21f82c088" />
 
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
<img width="635" height="116" alt="image" src="https://github.com/user-attachments/assets/0232ff90-bd20-47c2-ad1e-04ea4b710c0b" />
 
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
<img width="571" height="143" alt="image" src="https://github.com/user-attachments/assets/8dc71c2f-fc4d-47f5-8987-8ba375c139de" />

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
<img width="641" height="257" alt="image" src="https://github.com/user-attachments/assets/9c5cd5ae-7f77-4847-b396-1eb1912d9ab8" />


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
<img width="574" height="129" alt="image" src="https://github.com/user-attachments/assets/821672ed-f3ce-4fb2-951d-6edf8ed0e74d" />

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
<img width="569" height="125" alt="image" src="https://github.com/user-attachments/assets/95ec57a2-9f39-4997-9833-9a8e5cc19f67" />

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
<img width="529" height="124" alt="image" src="https://github.com/user-attachments/assets/d0dabf1b-75f6-4f10-a3b2-9c4d081e3c05" />

 
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
<img width="576" height="252" alt="image" src="https://github.com/user-attachments/assets/52e5bff8-62e4-4fe3-ac08-86a65b7203bf" />

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
 <img width="588" height="91" alt="image" src="https://github.com/user-attachments/assets/f9fa1b3b-7365-42d3-a9d8-68189011aa29" />

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
<img width="511" height="118" alt="image" src="https://github.com/user-attachments/assets/4e3f017b-c568-42c2-afe6-d38ea9ae4ff6" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="586" height="74" alt="image" src="https://github.com/user-attachments/assets/40cb13f4-8f3c-4c0d-8cc2-ee4c05b32dac" />



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
<img width="569" height="50" alt="image" src="https://github.com/user-attachments/assets/03acec2f-9341-40d5-8522-857d4817949e" />

 ./funcex.sh 
<img width="596" height="31" alt="image" src="https://github.com/user-attachments/assets/840fd184-3276-4afd-9a14-a6854e2eedcf" />

 
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
<img width="588" height="95" alt="image" src="https://github.com/user-attachments/assets/418ec41e-a1e4-40b5-b7ee-9f1297c6fc6d" />

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
<img width="586" height="100" alt="image" src="https://github.com/user-attachments/assets/8ad6849e-e262-47f2-bd26-dee3a27c9fe3" />

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
<img width="685" height="290" alt="image" src="https://github.com/user-attachments/assets/1fcdc6e3-0537-4518-9dd5-a1c5dfd1f63e" />

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
<img width="617" height="260" alt="image" src="https://github.com/user-attachments/assets/33e416e2-7f15-4195-a12f-2e30d8138cda" />
 
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
<img width="621" height="267" alt="image" src="https://github.com/user-attachments/assets/5674731b-dcc1-47c0-93bf-5245595917f1" />


# RESULT:
The Commands are executed successfully.
