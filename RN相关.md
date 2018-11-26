1. C:\Program Files (x86)\MuMu\emulator\nemu\vmonitor\bin

    adb_server.exe connect 127.0.0.1:7555 
      adb connect 127.0.0.1:7555

    mumu 模拟器链接
2. 设置Enable Live Reload
    需要先设置dev setting   ip 为自己电脑ip  端口号  8081

4. 手动使input失去焦点
    ```
        <ScrollView keyboardShouldPersistTaps="never">    //ScrollView      keyboardShouldPersistTaps
            <TouchableHighlight onPress = {this._onPress}>    //  refs.textInput1.blur()   antD RN  组件经过封装 需要多次向下找 才能找到blur()

            <InputItem
                    defaultValue=""
                    clear={true}
                    type="number"
                    ref="textInput1"

    ```
5. 开启原生动画  
   ```
        Animated.timing(                  // 随时间变化而执行动画
            this.state.top,            // 动画中的变量值
            {
            toValue: 0,                   // 透明度最终变为1，即完全不透明
            duration: 500,              // 让动画持续一段时间
            useNativeDriver: true,      //开启原生动画  只能用于布局属性
            }
        ).start();
   ```

- 返回数据量大的请求使用fetch
- KeyboardAvoidingView 
    behavior
    注意：Android 和 iOS 在此属性上表现并不一致。 Android 可能不指定此属性更好，而 iOS 可能相反。
    解决：
   ```
     if(Platform.OS==='ios'){
        behavior ={
          behavior:'padding'
        };
        SearchBarProps={
          value:''
        } 
      }  //然后将behavior值解构到KeyboardAvoidingView组件上
   ```
- SearchBar 
  ``` 
    if(Platform.OS==='ios'){
      behavior ={
        behavior:'padding'
      };
      SearchBarProps={
        value:''
      } 
    }
  ```
- rn上ios不支持中文输入，解决方法 , 改变inputItem值时，应避免多次setState

```
shouldComponentUpdate(nextProps: any) {
    return Platform.OS !== 'ios'
      || (this.props.value === nextProps.value && (nextProps.defaultValue == undefined || nextProps.defaultValue == ''))
      || (this.props.defaultValue === nextProps.defaultValue && (nextProps.value == undefined || nextProps.value == ''));
  }


```

- 增加 StyleSheet.createPlatformStyle 方法
- 可在style 增加 ios android 对象区分

```

StyleSheet.createPlatformStyle({
  wrap: {
    flex: 1,
    android:{
      backgroundColor:'#ffffff'
    },
    ios:{
       backgroundColor:'#000000'
    }
  },

```


- 在android中scrollview 使用 snapToInterval属性必须添加pagingEnabled

- 在jsx中是否显示组件 不要使用 ```aa&&(component) ```，应该使用```!!aa&&(component)```
