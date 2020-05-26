[TOC]

# Study link:

[1] https://developer.cisco.com/learning/tracks/devnet-beginner/network-programmability/apic-em-basic/step/1

[2] https://developer.cisco.com/learning/labs/what-are-rest-apis/step/1

[3] https://developer.cisco.com/learning/modules/rest-api-fundamentals



# REST API Fundamentals

Learn concepts and terminology for REST APIs, how to get started with REST APIs, how to use POSTMAN to test APIs, and how to create scripts that can access a REST API.

































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

