# EVP-Symmetric-Encryption-and-Decryption
OpenSSL中的libcrypto库提供了在各种算法和模式下执行对称加密和解密操作的功能。可以通过该程序实现DES，AES等各种加密算法，还 可以选择ebc，cbc等操作模式。
# 程序运行截图<br/>
![image](https://github.com/Ruipeng-LI/EVP-Sym
metric-Encryption-and-Decryption/blob/master/image/%E6%90%9C%E7%8B%97%E6%88%AA%E5%9B%BE20190128222546.png)


# 程序流程说明
1、首先生成一个随机数作为盐值salt<br/>
2、通过EVP_BytesToKey函数来生成加密秘钥和加密向量<br/>
3、将盐值写入文件，解密时读取出来在生成加密向量和加密码秘钥来进行解密。<br/>


# 修改加密算法

if (1 != EVP_EncryptInit_ex(ctx, EVP_des_cbc(), NULL, key, iv)<br/>
修改EVP_des_cbc()来变换不同的算法
