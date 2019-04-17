### shc 在Linux上的安装

##### 1. 安装方法

```
mkdir /usr/local/man
mkdir /usr/local/man/man1

tar vxf shc-3.8.6.tgz && cd shc-3.8.6
make test
make strings
make install
yes

安装完成之后会有提示安装目录, 如果shc不在环境变量PATH下, 需要创建链接:
ln -s **** /usr/local/bin/shc
```

如果安装时出现: `install: 目标"/usr/local/man/man1/" 不是目录: 没有那个文件或目录`
`mkdir /usr/local/man/man1`

##### 2. 加密命令

```
shc -v -r -T -f shell脚本名称

#得到的以.sh.x结尾的就是加密后的脚本
```

