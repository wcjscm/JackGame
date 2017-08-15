# JackGame

cocos new JackGame -p com.jackgame.chesscards -l lua -d ../NewGame

set buildToolsVersion "26.0.1"

AppActivity.java add code: import android.os.Bundle;

---------------------------------------------------------
--生成keystore
keytool -genkey -alias gamekey -keyalg RSA -validity 40000 -keystore gamekey.keystore

--打包
cocos compile --android-studio -p android -j 8 -m release --compile-script 1 --lua-encrypt --lua-encrypt-key my_lua_encrypt_key --lua-encrypt-sign XXTEA

cocos run --android-studio -p android -j 8 -m release --compile-script 1
