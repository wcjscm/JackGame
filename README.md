# JackGame

--版本号修改
buildToolsVersion "26.0.1"

--查找替换
android-10 --> android-25

---------------------------------------------------------
--生成keystore
keytool -genkey -alias gamekey -keyalg RSA -validity 40000 -keystore gamekey.keystore

--打包
cocos compile --android-studio -p android -m release --compile-script 1 --lua-encrypt --lua-encrypt-key my_lua_encrypt_key --lua-encrypt-sign XXTEA

cocos compile --android-studio -p android -m release --compile-script 1