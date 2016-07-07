
please change the username and password before run it
```
SVN_USER=username
SVN_PWD=password

yum install svn -y
svn checkout https://github.com/lhcpig/dockers/trunk/svn-server
cd svn-server && docker build -t svn . && echo -e "[users]\n$SVN_USER=$SVN_PWD" > passwd
docker run -p 3690:3690 -d -v /data/svn:/svn svn
```
