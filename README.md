# HSD-CIPHER-SM 
Chinese Cipher Algorithm


国密即国家密码局认定的国产密码算法，即商用密码。主要有SM1，SM2，SM3，SM4。密钥长度和分组长度均为128位。
SM1 为对称加密。其加密强度与AES相当。该算法不公开，调用该算法时，需要通过加密芯片的接口进行调用。
SM2为非对称加密，基于ECC。该算法已公开。由于该算法基于ECC，故其签名速度与秘钥生成速度都快于RSA。ECC 256位（SM2采用的就是ECC 256位的一种）安全强度比RSA 2048位高，但运算速度快于RSA。
SM3 消息摘要。可以用MD5作为对比理解。该算法已公开。校验结果为256位。
SM4 无线局域网标准的分组数据算法。对称加密，密钥长度和分组长度均为128位。
 
由于SM1、SM4加解密的分组大小为128bit，故对消息进行加解密时，若消息长度过长，需要进行分组，要消息长度不足，则要进行填充。


作为密码学算法，一定要公开接受行业的检验。



1. 对称算法：                                 （DES 3DES AES） --迁移-->   SM1 SM4

2. 非对称密码算法：                                      (RSA) --迁移-->   SM2(椭圆曲线密码)

3. 散列算法：  (HASH MD4、MD5 SHA-1、SHA-256、SHA-384、SHA512) --迁移-->   SM3
