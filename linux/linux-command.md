# Linux command
show dns entry of the given url
```
dig www.google.de
```
sed tutorial

https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/

https://www.gnu.org/software/sed/manual/sed.html

awk tutorial

https://www.baeldung.com/linux/awk-nawk-gawk-mawk-difference

https://www.gnu.org/software/gawk/

execute commands in arbitary intervals
```
watch -n 1 "kubectl get pods | grep dev"
```
find all files in directory and print the number of founded files
```
find /etc -type f -name '*.sh' | wc -l
```
find files from specific folder which matching regex by using grep
```
find fcp/ -type f -exec grep -l "TARGET" {} \;

find . -type f -exec grep -l "ekl-backend-blackbox" {} \;
```
add user to group vboxsf
```
sudo usermod -a -G vboxsf tim
```
#### SSH host key verification failed, remove the old host key from the known_hosts file
```
ssh-keygen -R <hostname>
```

#### SCP
copy a directory from remote server
```
scp -r tim@192.168.178.48:/etc/bind/ config/
```

copy a single file from remote server
```
scp tim@192.168.179.48:/etc/bind/named.conf config/
```
copy a directory to remote server
```
scp ./workspaces-k8s/ tim@ekl-jenkins.ponyworld:/home/tim/
```

#### Get release of current OS
```
cat /etc/os-release
```

#### Set hostname
```
sudo hostnamectl hostname primary.ponyworld.io
```

#### Show hostmane
```
hostnamectl hostname
```

#### read free disk space
```
df -h --total
```

#### Find Listening Ports
```
netstat -tulpn|grep LISTEN 
```