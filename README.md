# winscppassword
encrypt and decrypt winscp password

解密winscp密码使用方法： 

1.首先找到WinSCP.ini文件，在WinSCP安装目录下，如果没有的话打开winscp然后保存生成

2.主函数修改为如下形式： 
if name == 'main': 
    # encrypt_password为WinSCP.ini中Password后面的
    # 为避免密码泄露，我的这个是随便写的密码 
    encrypt_password = 'A029asfasdfasdgasdgrgasfghqergh39' 
    # 输出打印 
    # 'gmdong'为WinSCP.ini中UserName，'192.168.1.1'为WinSCP.ini中的HostName 
    print(decrypt_password(encrypt_password, 'gmdong'+'192.168.1.1'))

3.命令行中cd到代码所在目录，然后运行python代码
