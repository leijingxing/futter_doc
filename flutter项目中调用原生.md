# flutter项目调用原生
## 1. flutter项目调用原生
#### flutter项目调用原生主要分为三个部分：**原生项目**、**flutter项目**

#### flutter调用原生的方法
- flutter调用原生的方法主要是通过`MethodChannel`类来完成的。
- `MethodChannel`类主要是指方法通道类，方法通道类主要是用来调用原生的方法的。
- `MethodChannel`类主要有两个参数：**name**、**binaryMessenger**。
- name参数主要是指方法通道的名称，方法通道的名称主要是用来标识方法通道的。
- binaryMessenger参数主要是指方法通道的二进制消息，方法通道的二进制消息主要是用来传递方法通道的二进制消息的。
- `MethodChannel`类主要有两个方法：**invokeMethod**、**setMethodCallHandler**。
- invokeMethod方法主要是指调用方法，调用方法主要是用来调用原生的方法的。
- setMethodCallHandler方法主要是指设置方法调用处理器，设置方法调用处理器主要是用来设置方法调用处理器的。
- `MethodChannel`类主要有两个属性：**name**、**binaryMessenger**。
- name属性主要是指方法通道的名称，方法通道的名称主要是用来标识方法通道的。
- binaryMessenger属性主要是指方法通道的二进制消息，方法通道的二进制消息主要是用来传递方法通道的二进制消息的。
- `MethodChannel`类主要有两个回调：**MethodCallHandler**、**MethodCall**。
- MethodCallHandler回调主要是指方法调用处理器，方法调用处理器主要是用来处理方法调用的。
- MethodCall回调主要是指方法调用，方法调用主要是用来调用原生的方法的。
- MethodCall回调主要有两个属性：**method**、**arguments**。
- method属性主要是指方法，方法主要是用来标识方法的。
- arguments属性主要是指参数，参数主要是用来传递参数的。
- MethodCall回调主要有两个方法：**arguments**、**hasArgument**。
- arguments方法主要是指参数，参数主要是用来传递参数的。
- hasArgument方法主要是指是否有参数，是否有参数主要是用来判断是否有参数的。
- MethodCall回调主要有两个属性：**method**、**arguments**。
- method属性主要是指方法，方法主要是用来标识方法的。
- arguments属性主要是指参数，参数主要是用来传递参数的。

#### flutter调用原生的流
- flutter调用原生的流主要是通过`EventChannel`类来完成的。
- `EventChannel`类主要是指事件通道类，事件通道类主要是用来调用原生的事件的。
- `EventChannel`类主要有两个参数：**name**、**binaryMessenger**。
- name参数主要是指事件通道的名称，事件通道的名称主要是用来标识事件通道的。

