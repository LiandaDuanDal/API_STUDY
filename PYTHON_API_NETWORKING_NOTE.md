[TOC]

# Study link:

[1] https://developer.cisco.com/learning/tracks/devnet-beginner/network-programmability/apic-em-basic/step/1

[2] https://developer.cisco.com/learning/labs/what-are-rest-apis/step/1

[3] https://developer.cisco.com/learning/modules/rest-api-fundamentals

# 基本的数据操作

## JSON

```python
import json
with open("./json/json_example.json") as jj:
    json_read = jj.read()
    print(type(json_read))
    
    <class 'str'>
```

此时你拿到的是一个json_read 字符串

将执行read拿到的字符串编程dic的话需要用jason.loads()

```python
		json_dic = json.loads(json_read)
  
    print(type(json_dic))
    print(json_dic)
    
<class 'dict'>

{'interface': {'name': 'GigabitEthernet2', 'description': 'Wide Area Network', 'enabled': True, 'ipv4': {'address': [{'ip': '172.16.0.2', 'netmask': '255.255.255.0'}]}}}
```



## CSV

同样地用with open操作，这个操作的好处在于他对read操作进行缩进

所以结束读取后会自动执行close

```python
import csv
with open("./csv/csv_example.csv") as f:
    read_csv = f.read()
    
    
print(read_csv)

>>
"router1","10.1.0.1","New York"
"router2","10.2.0.1","Denver"
"router3","10.3.0.1","Austin" 
```

这个时候，由于每一行的数据的结构非常明显，有一种想法是将这个东西的每一行变成列表：

需要用到：

```python
import csv
with open("./csv/csv_example.csv") as f:
    csv_obj = csv.reader(f)
```

这个时候注意的是这个csv.reader接受的东西并不是read返回的那一大堆乱七八糟的字符串，

而是with open返回出来的对象 f。

```python
# print(type(csv_obj))
with open("./csv/csv_example.csv") as f:
    csv_obj = csv.reader(f)
    
    for line in csv_obj:
        
        print("router: {router}, network: {network}, location: {location}".format(router = line[0],
                                                                                 network= line[1],
                                                                                 location = line[2]),end = '\n')
```















# Cisco SDN Model with APIC-EM



1. Always on, public instance

2. - For all DevNet users
   - **https://SandBoxAPICEM.cisco.com**
   - **User**: *devnetuser* **PW**: *Cisco123!*

# representational state transfer (REST).









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

