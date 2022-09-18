问题及解决



出现问题的原因是.sh文件是dos格式文件，但是linux的shell需要unix格式的文件，因此需要进行转换
sudo apt-get install dos2unix
dos2unix <filename>


创建以太坊的服务端
npm install -g ganache-cli
ganache-cli -i 1 -h 0.0.0.0 -p 8545




<build>
        <plugins>
            <plugin>
                <groupId>org.web3j</groupId>
                <artifactId>web3j-maven-plugin</artifactId>
                <version>4.8.7</version>
                <configuration>
                    <soliditySourceFiles/>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <configuration>
                    <excludes>
                        <exclude>
                            <groupId>org.projectlombok</groupId>
                            <artifactId>lombok</artifactId>
                        </exclude>
                    </excludes>
                </configuration>
            </plugin>
        </plugins>
    </build>



## 代理

正向代理

代理对客服端负责：科学上网，授权访问，跨网加速，缓存数据，隐藏访问者（肉鸡）

反向代理：保护服务器，负载均衡，认证负载均衡，跨域













**发送脚本**

```
#!/usr/bin/expect -f 


#用户名
set user ubuntu
#密码
set passwd 123456
#终端服务器IP
set host 123.123.123.123
#终端服务器端口
set port 22
#本地路径
set local_path /project/jenkins/opt/jenkins/data/workspace/hello-project/target/test.txt
#终端服务器路径
set remote_path /project/test/

spawn scp -r /project/jenkins/opt/jenkins/data/workspace/hello-project/target/tets.sh ubuntu@123.123.123.123:/project/test/
set timeout 5
expect {
"Connection refused" exit
"Name or service not know" exit 
#表示匹配到yer/no时就发送字符串yes\n到该进程里
"yes/no" { send "yes\n";exp_continue }
#匹配到password时就发送passwd\n到进程里
"*assword" { send "$passwd\n" }
 }
expect eof
```





