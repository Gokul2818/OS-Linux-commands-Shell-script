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
// git add-h
// git commit
// git origin

### Display the content of the files
cat < file1



## OUTPUT
![Screenshot from 2025-03-16 14-10-10](https://github.com/user-attachments/assets/7f564263-6fc2-4105-b533-4899d77f3cb3)


cat < file2
## OUTPUT
![Screenshot from 2025-03-16 14-10-34](https://github.com/user-attachments/assets/275d0cba-a4d4-4162-9a88-1186062cb55b)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-16 14-11-17](https://github.com/user-attachments/assets/d7884b7d-cac8-40a8-b058-a578224d8204)


 
comm file1 file2
 ## OUTPUT
![Screenshot from 2025-03-16 14-12-26](https://github.com/user-attachments/assets/8a7071b9-d9c5-49d3-a570-dd95926d3edc)



 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-16 14-13-40](https://github.com/user-attachments/assets/8870cda8-18c7-4fc2-8fa3-a3cd36fc6046)



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
![Screenshot from 2025-03-16 14-17-33](https://github.com/user-attachments/assets/dbb05641-c6c8-4a9e-b239-517618da5b34)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-16 14-18-04](https://github.com/user-attachments/assets/ac8f266c-5724-4d21-b8a6-8ee4422b4e56)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-16 14-18-29](https://github.com/user-attachments/assets/7b9b6072-7544-49d7-aef7-721f7f80f839)



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
![Screenshot from 2025-03-16 14-30-02](https://github.com/user-attachments/assets/7f2572af-62f4-4382-a664-00789889e132)




grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-16 14-30-29](https://github.com/user-attachments/assets/0ef6d32c-5609-48d6-bdbd-59bacb82a6c2)





grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-16 14-30-50](https://github.com/user-attachments/assets/af909fd8-e3f7-4dd5-beea-d16906223a99)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-16 14-31-37](https://github.com/user-attachments/assets/34777722-dc8c-4a6f-a45e-f8572f8f764b)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-16 16-47-59](https://github.com/user-attachments/assets/cc0e07df-3080-4f61-9212-581e07a57a38)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-16 16-57-02](https://github.com/user-attachments/assets/66af7ea1-acbf-4155-a058-2d966f6c2c8d)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-16 17-06-59](https://github.com/user-attachments/assets/236df39e-c8f8-4b45-a120-1ce6c9b23098)


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
![Screenshot from 2025-03-16 17-08-42](https://github.com/user-attachments/assets/492e8cdb-825c-4b92-b68d-37ed12e38f81)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-09-01](https://github.com/user-attachments/assets/a4cbb36f-072f-4d46-847b-830d3349d195)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-09-17](https://github.com/user-attachments/assets/5d1af7dc-4f79-4577-8eef-7605553100dd)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-09-39](https://github.com/user-attachments/assets/2fbed084-b02b-4b4c-b49a-edf9ed6b5f4e)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-10-01](https://github.com/user-attachments/assets/a64a64f3-d16c-4f8c-82ad-5e63a6590e57)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-10-23](https://github.com/user-attachments/assets/9c22e515-3650-4e16-b22f-54b32fd13e52)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-12-21](https://github.com/user-attachments/assets/18ff54af-dd93-46d8-acad-603316e33823)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-12-45](https://github.com/user-attachments/assets/a004cdbc-fc4a-4a10-8de4-de2e15fe06eb)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-13-13](https://github.com/user-attachments/assets/073afd8a-1144-43bd-9780-be251a558592)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-16 17-13-29](https://github.com/user-attachments/assets/56154c71-c8a8-4c28-9ce7-6b1910b0d577)



egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-16 17-13-46](https://github.com/user-attachments/assets/50b49016-f0d1-40e9-b502-44b7c3552083)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-16 17-14-05](https://github.com/user-attachments/assets/6e6416d0-ace3-4b52-8c96-d26e349c1fc9)


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
![Screenshot from 2025-03-16 17-15-02](https://github.com/user-attachments/assets/fde7e7a2-d40c-45ef-a26c-67597dfd606f)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-16 17-15-19](https://github.com/user-attachments/assets/53474dcc-9973-4832-901e-6113f2c8626c)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-16 17-15-36](https://github.com/user-attachments/assets/f4b5d72a-4d79-4807-8dab-5c40351688f2)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-16 17-16-03](https://github.com/user-attachments/assets/1ef18d29-ef1e-4b41-8ed0-18d079d9a72d)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-03-16 17-16-26](https://github.com/user-attachments/assets/b0741f3e-a038-4488-8cd9-64ec9b9b0433)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-03-16 17-16-48](https://github.com/user-attachments/assets/5f99caa2-29f3-416a-9747-2c8b6ab2aca5)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-16 17-16-48](https://github.com/user-attachments/assets/4939ed39-2e52-4c4f-b836-5200262a3b4e)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-16 17-17-08](https://github.com/user-attachments/assets/3e973172-c836-48f1-8c94-71797ff4688a)



seq 10 
## OUTPUT
![Screenshot from 2025-04-16 20-56-17](https://github.com/user-attachments/assets/203d46fc-2293-4b4e-b46d-6e0858bccff4)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-16 17-18-20](https://github.com/user-attachments/assets/205ca7a2-238c-44bf-8790-da3611b9b0f8)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-16 17-18-41](https://github.com/user-attachments/assets/1fb7f1a6-276b-47ab-8c15-586ec17aa7e9)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-16 17-19-07](https://github.com/user-attachments/assets/117b4bea-ca4e-45fa-a888-ae257db1b7e6)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-16 17-19-26](https://github.com/user-attachments/assets/a5b2895e-a411-4ee3-ba1c-6201939b2fac)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-16 17-19-36](https://github.com/user-attachments/assets/c7b488e2-01b9-4ca0-8fcb-e56405f93e40)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-16 17-19-55](https://github.com/user-attachments/assets/8562cf70-0b99-463a-90ff-c60efac182e1)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-03-16 17-20-09](https://github.com/user-attachments/assets/c8b9bb0f-a90c-49a3-8058-eef8872d9373)


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
![Screenshot from 2025-03-16 17-21-10](https://github.com/user-attachments/assets/f907038d-a0ab-4256-b68a-00794974c2d8)


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
![Screenshot from 2025-03-16 17-22-04](https://github.com/user-attachments/assets/e573a376-111e-48c3-bfcc-c2e421083573)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-03-16 17-22-35](https://github.com/user-attachments/assets/65917aea-396c-4513-ba02-b028f7bd5159)

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
![Screenshot from 2025-03-16 17-24-34](https://github.com/user-attachments/assets/1648f7ad-d1a6-4131-bb63-744255803eeb)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-03-16 17-24-54](https://github.com/user-attachments/assets/5a992df1-8ec7-4100-a6ad-9b5cf26042ba)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-16 17-27-04](https://github.com/user-attachments/assets/12c3ec94-23c5-406b-abc9-76108ce820aa)


mkdir backupdir
 
mv backup.tar backupdir
 
## OUTPUT
![Screenshot from 2025-03-16 17-28-43](https://github.com/user-attachments/assets/ac5899bb-8946-4308-a7f5-314f2c5a6872)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-16 17-29-52](https://github.com/user-attachments/assets/33d4f0f8-5394-4517-81e2-c52c7325137d)


gzip backup.tar

ls .gz
## OUTPUT
![Screenshot from 2025-03-20 09-52-57](https://github.com/user-attachments/assets/b65d5eac-461f-4f23-bfa3-52fdaecef512)



gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2025-03-24 08-07-08](https://github.com/user-attachments/assets/f6f3ff6d-f27b-4dc1-bcd4-5ad59579afb9)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-03-24 09-27-22](https://github.com/user-attachments/assets/c954c354-549a-4d55-932c-f4a36c1e055f)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-03-24 09-31-28](https://github.com/user-attachments/assets/925c0a0c-3fa6-40f2-89a0-6326dced453f)


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
![Screenshot from 2025-03-24 09-33-24](https://github.com/user-attachments/assets/3d5a6e05-a7ab-420e-ab3f-442d26a64372)

 
ls file1
## OUTPUT
![Screenshot from 2025-03-24 09-34-46](https://github.com/user-attachments/assets/e1547b06-e69d-4d47-8cce-064859846f42)


echo $?
## OUTPUT 
![Screenshot from 2025-03-24 09-34-56](https://github.com/user-attachments/assets/2a4781cc-945f-40a4-a80a-fceee543810f)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot from 2025-03-24 09-35-10](https://github.com/user-attachments/assets/bd3a0199-0274-4fd6-a76a-a6147f6d0d58)


abcd
 
echo $?
## OUTPUT
![Screenshot from 2025-03-24 09-35-43](https://github.com/user-attachments/assets/b00cd5a4-bb2c-44d0-8688-500fb201014d)


 
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
![Screenshot from 2025-03-24 09-37-21](https://github.com/user-attachments/assets/43127506-9997-4c4e-93a2-59d547e6a69a)



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

![Screenshot from 2025-03-24 09-41-13](https://github.com/user-attachments/assets/d153774f-9994-4394-a822-4ad80705291c)

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
![Screenshot from 2025-03-24 09-42-53](https://github.com/user-attachments/assets/115985f7-9407-49ec-a11e-94abca9c861e)



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
![Screenshot from 2025-03-24 09-44-33](https://github.com/user-attachments/assets/2b755a0e-6bc1-4cf8-9058-528238edc80c)


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
![Screenshot from 2025-03-24 09-45-48](https://github.com/user-attachments/assets/b6378e88-9ffa-4579-acd6-3be5d8c6bbed)


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
![Screenshot from 2025-03-24 09-47-39](https://github.com/user-attachments/assets/d4766311-5af8-4993-9c69-ec1f17329261)


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
![Screenshot from 2025-03-24 09-48-58](https://github.com/user-attachments/assets/7a5e9dec-82e3-4f5f-a2e4-6c5a909ed1ef)


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
![Screenshot from 2025-03-24 09-49-48](https://github.com/user-attachments/assets/b8266a4c-25e5-446c-aaa6-31f959862d82)


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
![Screenshot from 2025-03-24 09-54-08](https://github.com/user-attachments/assets/09559719-3a5d-4a5c-a295-3d3a10d0a458)

 
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
![Screenshot from 2025-03-26 21-04-09](https://github.com/user-attachments/assets/1d45ac07-7185-4422-8d3a-3a76c92a3a7a)

 
 
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
![Screenshot from 2025-03-26 21-05-49](https://github.com/user-attachments/assets/03fea6ca-f5af-41d1-9aa2-9dfaf5dd9edf)

 
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
![Screenshot from 2025-03-26 21-10-01](https://github.com/user-attachments/assets/6e22285c-d248-474e-aff5-8d6c1cce83b6)

 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT
![Screenshot from 2025-03-26 21-11-30](https://github.com/user-attachments/assets/97e0b239-805e-4568-8283-5ddef4316685)

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

cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

$ chmod 777 forinfile.sh
$./forinfile.sh
## OUTPUT
![Screenshot from 2025-04-16 21-25-21](https://github.com/user-attachments/assets/4c4c7b55-352f-4e2a-a407-8553670b5bcd)



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
![Screenshot from 2025-03-27 08-17-25](https://github.com/user-attachments/assets/324d66ea-62d0-4446-99c0-c03d07022b2b)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
![Screenshot from 2025-04-10 08-20-28](https://github.com/user-attachments/assets/a6d0be7d-5ac7-4077-bdfb-f8d765b91f15)

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
![Screenshot from 2025-04-10 08-22-19](https://github.com/user-attachments/assets/0bd93cc3-ae2f-4dcc-a74c-3b7784259645)

 
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
![Screenshot from 2025-04-10 08-23-13](https://github.com/user-attachments/assets/f561fa23-6e9f-4639-893d-5fbae71d1354)

 
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
echo "The for loop is completed"
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![Screenshot from 2025-04-10 08-23-53](https://github.com/user-attachments/assets/e036d541-7d51-49da-ab07-767c0236ab89)


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
![Screenshot from 2025-04-10 08-25-01](https://github.com/user-attachments/assets/215d0174-75a8-4eed-9b94-5ec6d1d57e0f)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
![Screenshot from 2025-04-10 08-25-01](https://github.com/user-attachments/assets/0f90952e-25e4-45f0-b76c-3e2843d8e00e)




 
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

![Screenshot from 2025-04-16 20-22-38](https://github.com/user-attachments/assets/dee272f8-357a-4950-82a3-bf9c62cffba7)

 
 ./funcex.sh 1 2

![Screenshot from 2025-04-16 20-23-01](https://github.com/user-attachments/assets/954c5412-fcbb-4cc0-971b-2dc69a1d3eeb)

 
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

![Screenshot from 2025-04-16 20-24-14](https://github.com/user-attachments/assets/7f58b660-3237-462c-a5cc-f3dc3917bf58)




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
$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3

![Screenshot from 2025-04-16 20-25-01](https://github.com/user-attachments/assets/11ebe20a-8043-4219-a29e-7f67816ceb33)


cat argshift3.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +xch
```
## OUTPUT
 ./argshift3.sh 1 2 3

![Screenshot from 2025-04-16 20-25-58](https://github.com/user-attachments/assets/b8e03972-fb40-452b-bb70-15c33aa44226)

 
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

![Screenshot from 2025-04-16 20-27-09](https://github.com/user-attachments/assets/2bfc5fec-2b50-407c-ae38-87d648cff891)

 
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

![Screenshot from 2025-04-16 20-28-21](https://github.com/user-attachments/assets/46a29976-aed7-4e11-88e9-a09843f5babb)


# RESULT:
The Commands are executed successfully.
