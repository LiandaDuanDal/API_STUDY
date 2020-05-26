[TOC]

# Study link:

[1] https://developer.cisco.com/learning/tracks/devnet-beginner/network-programmability/apic-em-basic/step/1

[2] https://developer.cisco.com/learning/labs/what-are-rest-apis/step/1

[3] https://developer.cisco.com/learning/modules/rest-api-fundamentals



# REST API Fundamentals

Learn concepts and terminology for REST APIs, how to get started with REST APIs, how to use POSTMAN to test APIs, and how to create scripts that can access a REST API.



### Clone and configure the APIC-EM Git repo

Create a working directory. For example:

```bash
mkdir \workingdir\
```

Clone the APIC-EM sample code to your working directory. For example:

```bash
cd \workingdir\
git clone https://github.com/CiscoDevNet/apicem-apis-with-python-sample-codes
```

After the `git clone` completes, you have the Python files used in the following labs.

By default, these files are configured to send API calls to the sandboxed Cisco APIC-EM controller, as shown here:

```
APICEM_IP = "sandboxapicem.cisco.com"
```

To use a different controller, locate the `apicem_config.py` configuration file. For example: `username/workingdir/apicem-apis-with-python-sample-codes/basic-labs/apicem_config.py`

Edit the `apicem_config.py` file and assign the URL or IP address of the APIC-EM controller you’ll be using to the `APICEM_IP` variable. If the controller is configured to listen on a specific port number, include the value of the port number in the URL or IP address.























# 将本地文件夹关联到远程仓库

1、（先进入项目文件夹）通过命令 git init 把这个目录变成git可以管理的仓库

```
git init
```

2、把文件添加到版本库中，使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点“.”，意为添加文件夹下的所有文件

```
git add .
```

3、用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明

```
git commit -m 'first commit'
```

4、关联到远程库

git remote add origin 你的远程库地址
如：

```
git remote add origin https://github.com/githubusername/demo.git
```

5、获取远程库与本地同步合并（如果远程库不为空必须做这一步，否则后面的提交会失败）

```bash
git pull --rebase origin master
```

# References

[1] https://developer.cisco.com/learning/tracks/devnet-beginner/network-programmability/apic-em-basic/step/1

[2] https://developer.cisco.com/learning/labs/what-are-rest-apis/step/1

[3] https://developer.cisco.com/learning/modules/rest-api-fundamentals

