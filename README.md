# SSRRNApp
编译环境:

React-Native Version: 0.59.9

Xcode: 10.2.1

Swift : 5.0

##### 引入插件
新的版本中，对iOS的插件引入是通过Pod引入(如果iOS工程中使用CocoaPods)。
比如引入 react-native-gesture-handler

  1.  `yarn add react-native-gesture-handler. `
  2.  `react-native link react-native-gesture-handler`
  3.   第2步会自动在Podfile中添加
        `pod 'RNGestureHandler', :path => '../node_modules/react-native-gesture-handler'`
  4.   `cd ios && pod install` 完成安装



##### 问题汇总？

1. React-Native使用Pod不能自动打开控制台的bug
   通过在Xcode->Target->Build Phases -> Add Run Script解决

```shell
if nc -w 5 -z localhost 8081 ; then
if ! curl -s "http://localhost:8081/status" | grep -q "packager-status:running" ; then
echo "Port 8081 already in use, packager is either not running or not running correctly"
exit 2
fi
else
open "../node_modules/react-native/scripts/launchPackager.command" || echo "Can't start packager automatically"
fi
```