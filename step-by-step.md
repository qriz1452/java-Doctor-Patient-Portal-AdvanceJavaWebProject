Launching 3 servers :
Configuration :

Server 1,2,3  :
- Ubuntu 22.04
- Southeast asia
- 2 vcpu , 4 Gib Memory



All server passowrd set tp 1234@Qr
( Launched via acloudguru portal terraform and cfn script will add later )

------------------------
#  MANUALLY

SSH into VM 1 :
COMMANDS :
```
cloud_user@32270795f21c:~/ git --version : 
Git Version  2.34.1
cloud_user@32270795f21c:~/ git clone https://github.com/qriz1452/java-Doctor-Patient-Portal-AdvanceJavaWebProject.git
cloud_user@32270795f21c:~/ cd java-Doctor-Patient-Portal-AdvanceJavaWebProject/Doctor-Patient-Portal
cloud_user@32270795f21c:~/ sudo apt install maven -y

cloud_user@32270795f21c:~/java-Doctor-Patient-Portal-AdvanceJavaWebProject/Doctor-Patient-Portal$ mvn -v
Apache Maven 3.6.3
Maven home: /usr/share/maven
Java version: 11.0.21, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
Default locale: en, platform encoding: UTF-8
OS name: "linux", version: "6.2.0-1017-aws", arch: "amd64", family: "unix"
```



error :
```
cloud_user@32270795f21c:~/java-Doctor-Patient-Portal-AdvanceJavaWebProject/Doctor-Patient-Portal$ maven install
Command 'maven' not found, did you mean:
  command 'aven' from deb survex-aven (1.4.1-1)
Try: sudo apt install <deb name>
```

used `mvn install` and the error sorted.

COMMAND : `mvn install `

error : 
```
[ERROR] COMPILATION ERROR :
[INFO] -------------------------------------------------------------
[ERROR] Source option 5 is no longer supported. Use 6 or later.
[ERROR] Target option 1.5 is no longer supported. Use 1.6 or later.
[INFO] 2 errors
```

`nano pom.xml ` : updated pom and added maven compiler plugin
`git add .`
`git config --global user.email "you@example.com"    `
` git config --global user.name "quazi"`
` git commit -m "updated pom by adding maven compiler in properties and plugin"`
`cd target/`
` sudo apt install tomcat9 -y`
` sudo systemctl status tomcat9`
` sudo systemctl stop tomcat9`
` sudo systemctl status tomcat9`
` cd /var/lib/tomcat9/webapps/`
`sudo rm -rf ROOT` 
`  sudo cp /home/cloud_user/java-Doctor-Patient-Portal-AdvanceJavaWebProject/Doctor-Patient-Portal/target/Doctor-Patient-Portal.war .`
` sudo systemctl start tomcat9`
` sudo systemctl enable tomcat9`
` sudo systemctl status tomcat9`

`sudo tail -f /var/log/tomcat9/catalina.out`
` `
` `
` `
` `
` `
` `
