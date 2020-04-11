# ManagaKey
真中あお 身份验证体系

在这里放出我的两个公钥，用于身份验证和信息加密。

注意：以下代码基于openssl，Windows用户请安装Ubuntu（x）

<br/><br/>

### 发送加密消息给我

使用文件 `Manaka_Message_Pub.key`

指令 `openssl rsautl -encrypt -in INPUT_FILE_NAME -inkey Manaka_Message_Pub.key -pubin -out OUTPUT_FILE_NAME`

<br/><br/>

### 使用公钥验证我的身份信息

使用文件 `Manaka_Identity_Pub.key`

指令 `123`



<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
### MEMO

#### 传输加密消息

密钥生成 `openssl genrsa -out Manaka_Message.key 4096`

公钥生成 `openssl rsa -in Manaka_Message.key -pubout -out Manaka_Message_Pub.key`

本地消息的解密 `openssl rsautl -decrypt -in INPUT_FILE_NAME -inkey Manaka_Message.key -out OUTPUT_FILE_NAME`

#### 身份验证



身份消息的加密 ``


