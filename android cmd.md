```keytool -list -printcert -jarfile``` 查看证书

```select * from instanceof android.app.Activity``` 内存泄露

```adb logcat -v time | grep ActivityManager``` 页面启动时间

```adb logcat -v time | grep AndroidRuntime``` crash log

```adb logcat -v time | grep "D\/Dalvik"```

```adb logcat -v time | grep "I\/art"```

```adb shell "kill -s SIGUSR1 12345"``` 手动gc

```Log.getStackTraceString(new Throwable())```

```NDK_ROOT/toolchains/arm-linux-androideabi-4.9/.../arm-linux-androideabi-readelf -Ws xxx.so```

```NDK_ROOT/toolchains/arm-linux-androideabi-4.9/.../arm-linux-androideabi-nm -gC xxx.so```

<br>

```android list sdk --extended --proxy-host test.com --proxy-port 1234```

```android update sdk --no-ui -t 1,2,3 --proxy-host test.com --proxy-port 1234```


```gradle -Dhttp.proxyHost=test.com -Dhttp.proxyPort=1234 -Dhttps.proxyHost=test.com -Dhttps.proxyPort=1234```
<br>

######备用
```android list sdk --all --extended --proxy-host test.com --proxy-port 1234```

```android update sdk --no-ui --all --filter build-tools-23.0.3 --proxy-host test.com --proxy-port 1234```

```adb shell monkey -p your.app.package.name -c android.intent.category.LAUNCHER 1```

<br>

```setprop ctl.start [cmd]```  setprop ctl.start bootanim/bugreport

```bugreport  miui:*#*#284#*#*```     (bugreport->dumpstate->dumpsys)

```gradle -Dorg.gradle.jvmargs="-Xmx8192m -XX:MaxPermSize=6144m"```