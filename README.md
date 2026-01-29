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



cat < file2
## OUTPUT
<img width="950" height="147" alt="image" src="https://github.com/user-attachments/assets/4de6051a-59b8-4de0-bb74-87a0e7e83b20" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="950" height="167" alt="image" src="https://github.com/user-attachments/assets/ff85d9eb-c405-46a2-b166-4d69d972962d" />

comm file1 file2
 ## OUTPUT
<img width="950" height="65" alt="image" src="https://github.com/user-attachments/assets/6cd96628-f3b9-47ed-9166-c2290feaee14" />

 
diff file1 file2
## OUTPUT
<img width="950" height="272" alt="image" src="https://github.com/user-attachments/assets/89960140-38b9-4154-a87e-9858fa396a87" />


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
<img width="950" height="85" alt="image" src="https://github.com/user-attachments/assets/1a61481b-2ce3-4da6-b514-b4d566823897" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="950" height="109" alt="image" src="https://github.com/user-attachments/assets/fbd1fa9c-a49c-4a99-be49-bf076cee82e1" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="950" height="109" alt="image" src="https://github.com/user-attachments/assets/42d6a13f-568c-4cfc-8697-8b34427857ab" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 <img width="950" height="83" alt="image" src="https://github.com/user-attachments/assets/8d0dabe1-2419-472e-9866-2c4cff7c3855" />

grep Hello newfile 
## OUTPUT
<img width="950" height="58" alt="540877881-10efc376-7711-483a-b350-2f2a9e2b85de" src="https://github.com/user-attachments/assets/0a4f3670-6787-42bc-b69a-304350362ae3" />



grep hello newfile 
## OUTPUT
<img width="950" height="58" alt="540878072-7f5ee12a-fe9b-41fe-af92-c9f860dfd573" src="https://github.com/user-attachments/assets/32a32371-d533-49e4-9bb2-fd1cfd18c8c6" />




grep -v hello newfile 
## OUTPUT
<img width="950" height="58" alt="540878113-db90ba52-e4e4-4c73-9640-2ee5c1193221" src="https://github.com/user-attachments/assets/59f15754-6935-468d-9e64-7bf8ef38d56c" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="950" height="83" alt="540878195-17697aba-5f71-4a2f-b7dc-e3ab81317837" src="https://github.com/user-attachments/assets/2c7c4521-7364-40db-951f-dcbbeca85723" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="950" height="56" alt="540878266-d06e4698-7d24-47a5-b88b-412c045fcc7e" src="https://github.com/user-attachments/assets/05abc79b-d104-4051-be67-0ee12c14a07f" />




grep -R ubuntu /etc
## OUTPUT
<img width="950" height="488" alt="540878732-4c8eecbd-f34d-438c-8997-9c1cfdb32421" src="https://github.com/user-attachments/assets/431deb55-b51d-40ea-b91e-8d6eb25ce7b1" />



grep -w -n world newfile   
## OUTPUT
<img width="950" height="69" alt="540878775-acb6d9bf-95b4-4f7a-a7ed-99c9e987e876" src="https://github.com/user-attachments/assets/1dd508bd-f88b-453f-81dc-2c28871815d2" />


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
<img width="950" height="136" alt="540878874-fb9f3963-f830-41d4-89da-674db2dc9014" src="https://github.com/user-attachments/assets/db9a8be2-97a0-4527-8fdb-1984be0ca3aa" />

egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="950" height="71" alt="540878945-5c759374-120e-4398-8cce-71422c83fcb4" src="https://github.com/user-attachments/assets/ce9a65bf-2a2e-477b-b8ef-ed18a94a5a87" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="950" height="71" alt="540878987-657f4c9c-0c6e-4520-ab71-f9ecaf6f22ac" src="https://github.com/user-attachments/assets/dc9abc25-e93c-4b3a-9376-d0799a2ef8e7" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="950" height="71" alt="540879038-7e08006f-4bdc-45be-8675-55d3d30d7002" src="https://github.com/user-attachments/assets/3561f70d-26ba-4aa6-a391-67353081ed58" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="950" height="50" alt="540879091-152e1326-58dc-49ab-af77-886fe8db38bd" src="https://github.com/user-attachments/assets/77b57909-2428-42d0-80e8-90f40e245632" />



egrep '(world$)' newfile 
## OUTPUT
<img width="950" height="72" alt="540879136-1d5dba85-73a2-495c-83fd-355a7a456bbe" src="https://github.com/user-attachments/assets/fa6bcbb7-1ecf-4d8f-913e-7ff9d17413e7" />



egrep '(World$)' newfile 
## OUTPUT

<img width="950" height="51" alt="540879183-0206a2bc-ab65-4481-94de-641dc0983a45" src="https://github.com/user-attachments/assets/2597fe8c-1aad-4982-a1d2-987a31f8edeb" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="950" height="95" alt="540879241-8bdf15e5-289f-4712-95c1-d18b9853350c" src="https://github.com/user-attachments/assets/930118de-6e19-4702-8a4a-9c6d0917b35d" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="950" height="49" alt="540879319-c34f861e-f525-4f76-9eb8-869c1c77be21" src="https://github.com/user-attachments/assets/e9a61b95-bcd1-443b-83c6-8a34a4d84ac9" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="950" height="49" alt="540879366-7a0b0b08-d74e-4cf6-807d-1b6857360c58" src="https://github.com/user-attachments/assets/122ab9ac-19dd-4058-8026-8ab9464467ee" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="950" height="49" alt="540879448-ee8b42b3-75b7-4ec6-9b44-c47b5a94afc2" src="https://github.com/user-attachments/assets/85a47784-cd73-4fd1-a5c9-7bf5d9ad8d44" />


egrep l{2} newfile
## OUTPUT

<img width="950" height="70" alt="540879475-d33628d8-fb05-4ac6-ac52-b194733298f1" src="https://github.com/user-attachments/assets/de1ebedb-17d7-4bb8-9fb9-77e45d439d6a" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="950" height="92" alt="540879502-42be619e-845a-40e0-9014-2e8c5db7cf24" src="https://github.com/user-attachments/assets/964aadb5-0598-4251-a5be-7f6787b1d956" />


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
<img width="950" height="47" alt="540879575-d850bcc0-8390-4802-be89-3e5a11effdb7" src="https://github.com/user-attachments/assets/9f5a20b6-e2c2-4347-b7a3-acca35e9684c" />



sed -n -e '$p' file23
## OUTPUT

<img width="950" height="47" alt="540879638-dd99a269-d71f-40e4-ba95-c24112ffea7f" src="https://github.com/user-attachments/assets/31d7902e-0c11-4993-9e88-bde83b218598" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="950" height="202" alt="540879674-058c607e-acaa-430a-b91f-6ae2ab7c0476" src="https://github.com/user-attachments/assets/de1ebfb2-af23-479f-83e4-ad518367accf" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="950" height="202" alt="540879712-a3f6f9af-4cc0-426b-b137-fa13ad1de73a" src="https://github.com/user-attachments/assets/0ffda5e4-6133-4f37-a6c3-acc5bd252cca" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="950" height="202" alt="540879767-1223274f-7973-40c0-8c2d-ba51e9804861" src="https://github.com/user-attachments/assets/416633eb-8414-4294-b59e-f047b35e2c93" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="950" height="138" alt="540879808-2ac84b56-4fb2-4c5c-bf18-dc51126e2752" src="https://github.com/user-attachments/assets/d9cad6e2-6a33-41d8-a421-4a3ad3e6d143" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="950" height="93" alt="540879861-dbb98e7a-e1f7-4404-914f-e14ee2c8c2b1" src="https://github.com/user-attachments/assets/1f5f0ffa-5246-4f98-b944-18399f6514fb" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="950" height="74" alt="540879949-75c32a6f-fcf1-4ecb-aa41-90c6135704fc" src="https://github.com/user-attachments/assets/5ecde9bd-fae6-4b93-8db1-23bf4c87e4a4" />


seq 10 
## OUTPUT

<img width="950" height="245" alt="540879980-19ac168d-83ed-4625-a3f6-21b1e9afcb89" src="https://github.com/user-attachments/assets/943d9fec-3249-4a1b-a91d-54c4736982f5" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="950" height="94" alt="540880009-43cac0f4-1dd7-4d79-bb99-6a9768624531" src="https://github.com/user-attachments/assets/84044549-0419-4fcc-afc9-516a608d05d7" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="950" height="94" alt="540880034-9ba76297-34c4-4c4b-910f-f617ce267abd" src="https://github.com/user-attachments/assets/44c346ff-a8f8-46e9-9d82-0b370f5b2844" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="950" height="117" alt="540880064-d9c9c23c-b058-445b-a60e-e5694be1fd18" src="https://github.com/user-attachments/assets/690f60aa-e54e-47c9-a40f-f52c74f16a40" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="950" height="90" alt="540880124-4591f396-6c05-48a6-8bc8-f09e9b5c50e9" src="https://github.com/user-attachments/assets/1dcd5a5a-5d76-4c1e-a567-c57339146d8b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="950" height="90" alt="540880152-ad40dec1-668c-43a1-9bb2-54ad60d57634" src="https://github.com/user-attachments/assets/efe2df66-a3b6-46bb-a885-1ee1a9f99247" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="950" height="90" alt="540880191-377dd6e5-506a-45c8-86c4-6df30b9cc661" src="https://github.com/user-attachments/assets/4c8ecd57-1633-4f61-bea7-8b6f78e952f9" />



sed -n '2,4{s/$/*/;p}' file23
<img width="950" height="90" alt="540880251-a64184c1-641f-4a41-b37a-ecd0109cfd89" src="https://github.com/user-attachments/assets/f3670bee-d3b1-46ad-b140-447a50016a41" />


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
<img width="950" height="136" alt="540880318-33029524-6755-4061-8b6e-ab36ad6ecab0" src="https://github.com/user-attachments/assets/01dad662-e29c-4a89-9b04-1cd87ad5df3f" />


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
<img width="950" height="136" alt="540880376-fa1ab0ab-e7da-4123-931d-50dddabb5e3e" src="https://github.com/user-attachments/assets/d6e76114-5850-4676-a165-65cc0488317d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="950" height="204" alt="540880439-5e219d10-3a0a-4c05-b426-1ef4523b03f6" src="https://github.com/user-attachments/assets/f9e82d6a-e348-43e3-874d-c50449b1d87f" />

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
<img width="950" height="95" alt="540880489-50feec44-65d9-43cb-bc1f-db810c02b3e7" src="https://github.com/user-attachments/assets/1a47eb41-57a7-47ab-adcd-936c93afa7e2" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="950" height="95" alt="540880529-ee0a3ade-79d8-4db6-84a2-7eb8337b7a6c" src="https://github.com/user-attachments/assets/66922339-588a-4dd2-84f3-27c643d2ce72" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="950" height="202" alt="540880569-fadb54ab-52d3-41a7-b3d3-6b524a345f2f" src="https://github.com/user-attachments/assets/f70b20e5-7f68-4b1a-a188-b4983ef0937f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="950" height="202" alt="540880673-09905422-d71c-4ebc-a26a-074f113ddd5e" src="https://github.com/user-attachments/assets/6b46cf94-eef7-4231-968b-07f955eec2a7" />


tar -xvf backup.tar
## OUTPUT
<img width="950" height="202" alt="540880733-c0d060dc-2ae6-4ce3-b654-deda30e97987" src="https://github.com/user-attachments/assets/163bc9a2-9eb0-4292-9e6f-7afe691c752b" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="950" height="55" alt="540880834-24749cac-abdc-430a-92a6-f2ca5d924149" src="https://github.com/user-attachments/assets/11e6b3d9-dff0-4aa3-b560-ce810dbd2ba7" />

gunzip backup.tar.gz
## OUTPUT
<img width="950" height="76" alt="540880898-c934f596-2e77-4ba3-b117-47caed7c868a" src="https://github.com/user-attachments/assets/4c3f4d34-366e-4ae2-9c49-3a05d13a6b08" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="950" height="118" alt="540881020-0cbb6969-42cf-40ad-80f7-8cc921418de8" src="https://github.com/user-attachments/assets/bdf58863-34ab-4db3-a58a-97208c3f6dbe" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="950" height="96" alt="540881173-f6933f92-ad99-4aa2-a3b1-5e9246714f8c" src="https://github.com/user-attachments/assets/a19a2bf2-fbd0-4af0-a859-f019fe8aac41" />

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
<img width="950" height="621" alt="540881350-102f5fd3-9f63-4b89-956c-01c95d4c7ddf" src="https://github.com/user-attachments/assets/d6452a04-bb58-4c35-a01b-6465f36bd569" />

 
ls file1
## OUTPUT
<img width="950" height="50" alt="540881407-917a0533-151d-4bb7-a565-75b87420043a" src="https://github.com/user-attachments/assets/79791a4b-5cc3-44b9-968f-a707957ae485" />

echo $?
## OUTPUT 
<img width="950" height="50" alt="540881545-600f1854-a8ef-4daa-831a-a85f76a94321" src="https://github.com/user-attachments/assets/42440c2e-2499-468b-95df-139060e7401f" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="950" height="50" alt="540881663-45f6d1c9-4253-4340-b2fb-1594fa18d6e6" src="https://github.com/user-attachments/assets/2c395bd7-0d39-4fd7-b20a-7024b3dbf5b9" />

abcd
 
echo $?
 ## OUTPUT

<img width="950" height="226" alt="540881719-284c419a-70aa-4cb5-84fc-2d710ef86f1f" src="https://github.com/user-attachments/assets/0f026cb8-0725-4407-b423-e8bbde78b21d" />

 
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

<img width="950" height="225" alt="540882129-be29cba4-d15e-4e93-bc50-64d499331859" src="https://github.com/user-attachments/assets/2dd0c3c1-90bd-42cd-935e-715484bd8f23" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="950" height="92" alt="540882062-5add6c56-43bc-4f69-ae42-23cf1ef15a2e" src="https://github.com/user-attachments/assets/edc8a517-85a8-4d4f-82fb-63909ddec7a9" />


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
<img width="950" height="92" alt="540882062-5add6c56-43bc-4f69-ae42-23cf1ef15a2e" src="https://github.com/user-attachments/assets/9799ebf0-210d-4c4b-aeeb-bc062468d09c" />

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
<img width="950" height="130" alt="540882376-524dcadc-e133-4fb3-a6e2-1d48e6d12fd1" src="https://github.com/user-attachments/assets/04680f6a-0146-42a0-bc87-181f1e621d87" />



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
<img width="950" height="98" alt="540882444-12ef5fe8-99f9-4729-b181-badc898c5d6c" src="https://github.com/user-attachments/assets/7cd577a4-261a-4dc2-80ff-be414aea00df" />

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
<img width="950" height="114" alt="540882498-35ada94e-f5ea-4631-a647-49d8b22858f3" src="https://github.com/user-attachments/assets/3a6273b6-1497-4bc0-b7ce-2bcf01a04054" />

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
<img width="950" height="77" alt="540882573-87920638-f6eb-40e2-b64a-dfe06c89cca8" src="https://github.com/user-attachments/assets/f97c1ed2-7a5e-4441-84b8-fa8fc9d5e916" />


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
<img width="950" height="77" alt="540882651-ea35930c-bfe4-44bf-a84a-1fe4e24d8e98" src="https://github.com/user-attachments/assets/d76bc5d6-30e7-4a79-b29e-f6a27364daad" />

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
 <img width="950" height="77" alt="540882781-7ab1d69d-6995-4cd5-84fc-97760aa7a989" src="https://github.com/user-attachments/assets/43328485-821d-4a21-a14e-310d8b5413c5" />

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
 <img width="950" height="273" alt="540883111-78c03d60-8062-4ee9-93dd-41ffd2fda643" src="https://github.com/user-attachments/assets/e9730097-06d0-4d64-a55d-c2fbd3d8ab31" />

 
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
 
 <img width="950" height="161" alt="540883249-5a2ad133-1617-42bb-8a23-ae6a52c09922" src="https://github.com/user-attachments/assets/ac79e991-799d-47d6-8918-80f221ef1707" />

 
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
 
 <img width="950" height="204" alt="540883439-a6c983a4-e4c5-418e-b3c4-964e0d28c2c2" src="https://github.com/user-attachments/assets/9a49236f-56be-4b8e-a75b-5e4f25fc8d2c" />

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
 <img width="950" height="142" alt="540884740-1700a3d5-b356-4435-b125-61cba38036c6" src="https://github.com/user-attachments/assets/878d4d6e-4dd6-4fb2-83c5-37b42f428707" />

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
 <img width="950" height="142" alt="540884740-1700a3d5-b356-4435-b125-61cba38036c6" src="https://github.com/user-attachments/assets/deec5fa6-1e11-4817-9256-2949487b9fbf" />

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
<img width="950" height="181" alt="540884845-09a961b5-6617-42ad-a5ae-25e2046a4f33" src="https://github.com/user-attachments/assets/ef4dfbfb-8dc2-4ed4-a8db-e0cdf3e5a415" />

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

<img width="950" height="314" alt="540885026-59cea591-c576-453a-baad-740b8298f6de" src="https://github.com/user-attachments/assets/d3dad662-5b7b-4084-a5c3-045d5660c195" />

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
<img width="950" height="156" alt="540885227-87c85a27-bc8d-4157-bd7f-1e470ea4de8e" src="https://github.com/user-attachments/assets/c4bd15aa-7457-418a-89dd-aef5935f24e9" />

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
<img width="950" height="156" alt="540885303-5ea60882-86ec-459c-8333-6cce1c9de47f" src="https://github.com/user-attachments/assets/1f9d81ae-107d-490b-b252-4789f652af46" />
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

 <img width="950" height="315" alt="540885394-fcb3d651-8dcd-42b9-8389-032401bfb7af" src="https://github.com/user-attachments/assets/8581c907-268f-4da8-a248-6fbadaa9e067" />

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
<img width="950" height="116" alt="540885604-100ead1b-8c51-4964-aa6c-d65f3611307b" src="https://github.com/user-attachments/assets/3e89825e-4fb4-4113-ab5c-a665b2859bff" />

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
 <img width="950" height="154" alt="540885696-21791bde-2af6-4cad-bb3d-9adb932cc7bf" src="https://github.com/user-attachments/assets/0a5d08cd-f9ca-494b-b260-4278fec8a9f9" />

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

<img width="950" height="94" alt="540885818-2a2b5b10-0a66-49dd-bcc7-84667090a7c1" src="https://github.com/user-attachments/assets/502bd2ca-095c-4578-a050-b9d54faa3112" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="950" height="94" alt="540885896-eb4b4176-5f34-476b-bb87-42b912601ee9" src="https://github.com/user-attachments/assets/cb0e80d8-f2bc-44a1-8125-c1d343c30058" />


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
<img width="950" height="71" alt="image" src="https://github.com/user-attachments/assets/5ee027c9-dacf-4ff5-87c5-174849ac7310" />

 
 ./funcex.sh 1 2
<img width="950" height="55" alt="540886815-c2f5ecba-1aaa-4419-b3c1-106463cb54e5" src="https://github.com/user-attachments/assets/85e8a575-53fa-4935-a44b-e243019930f8" />

 
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
 <img width="950" height="119" alt="image" src="https://github.com/user-attachments/assets/da3f0dc9-1f27-4588-afff-e0948c6df118" />

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
 <img width="950" height="119" alt="image" src="https://github.com/user-attachments/assets/f17ebb96-3f73-44bf-b5be-ddae113d55b6" />

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
 <img width="950" height="361" alt="image" src="https://github.com/user-attachments/assets/8d735c4c-74c6-4513-8ac9-2dd9f2b57902" />

 
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
 <img width="950" height="320" alt="image" src="https://github.com/user-attachments/assets/f3f11920-c114-42cd-8936-3e0f4a59fb03" />

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
<img width="950" height="335" alt="image" src="https://github.com/user-attachments/assets/ca823ede-fd69-44e6-9d09-35a8fe6eaa2d" />


# RESULT:
The Commands are executed successfully.
