# SSRRNApp
React-Native demo app

React-Native Version 0.59.9

1. 引入插件
    新的版本中，对iOS的插件引入是通过Pod引入(如果iOS工程中使用CocoaPods)。
    比如引入 react-native-gesture-handler
      1. 1 `yarn add react-native-gesture-handler`
      1.2 `react-native link react-native-gesture-handler`
      第2步会自动在Podfile中添加
      `pod 'RNGestureHandler', :path => '../node_modules/react-native-gesture-handler'`
      1.3 cd ios && pod install 完成安装
