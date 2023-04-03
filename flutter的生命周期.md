## flutter的生命周期

#### 1. Flutter的生命周期

Flutter的生命周期分为三个阶段：**初始化阶段**、**运行阶段**、**销毁阶段**。

###### 1.1 初始化阶段

初始化阶段主要是Flutter引擎的初始化，包括Dart VM的初始化、Flutter引擎的初始化、Flutter引擎的启动、Dart isolate的初始化、Dart isolate的启动、Dart
isolate的运行、Flutter引擎的运行等。

- Dart VM的初始化
    * Dart VM的初始化是Flutter引擎的初始化的前置条件，Flutter引擎的初始化需要Dart VM的支持。
- Flutter引擎的初始化
    * Flutter引擎的初始化是Flutter引擎的启动的前置条件，Flutter引擎的启动需要Flutter引擎的支持。
    * Flutter引擎的初始化主要是初始化Flutter引擎的一些属性，比如：Dart VM的引用、Dart isolate的引用、Dart isolate的入口函数、Dart
      isolate的入口函数的参数等。
    * Flutter引擎的初始化主要是通过`FlutterEngine`类的`run`方法来完成的。
    * `FlutterEngine`类的`run`方法主要是通过`FlutterEngine`类的`runWithEntrypoint`方法来完成的。
    * `FlutterEngine`类的`runWithEntrypoint`方法主要是通过`FlutterEngine`类的`runWithEntrypointAndLibraryUri`
      方法来完成的。
    * `FlutterEngine`类的`runWithEntrypointAndLibraryUri`方法主要是通过`FlutterEngine`
      类的`runWithEntrypointAndLibraryUri`方法来完成的。

- Flutter引擎的启动

- Dart isolate的初始化
    * Dart isolate的初始化是Dart isolate的启动的前置条件，Dart isolate的启动需要Dart isolate的支持。
    * Dart isolate的初始化主要是初始化Dart isolate的一些属性，比如：Dart isolate的入口函数、Dart isolate的入口函数的参数等。
    * Dart isolate的初始化主要是通过`DartIsolate`类的`run`方法来完成的。
    * `DartIsolate`类的`run`方法主要是通过`DartIsolate`类的`runWithEntrypoint`方法来完成的。
- Dart isolate的启动
    * Dart isolate的启动是Dart isolate的运行的前置条件，Dart isolate的运行需要Dart isolate的支持。
    * Dart isolate的启动主要是通过`DartIsolate`类的`run`方法来完成的。
    * `DartIsolate`类的`run`方法主要是通过`DartIsolate`类的`runWithEntrypoint`方法来完成的。
    * `DartIsolate`类的`runWithEntrypoint`方法主要是通过`DartIsolate`类的`runWithEntrypointAndLibraryUri`
      方法来完成的。
    * `DartIsolate`类的`runWithEntrypointAndLibraryUri`方法主要是通过`DartIsolate`
      类的`runWithEntrypointAndLibraryUri`方法来完成的。
- Dart isolate的运行
    * Dart isolate的运行是Flutter引擎的运行的前置条件，Flutter引擎的运行需要Dart isolate的支持。
    * Dart isolate的运行主要是通过`DartIsolate`类的`run`方法来完成的。
- Flutter引擎的运行
    * Flutter引擎的运行是Flutter应用的运行的前置条件，Flutter应用的运行需要Flutter引擎的支持。

###### 1.2 运行阶段

运行阶段主要是Flutter应用的运行，包括Flutter应用的启动、Flutter应用的运行、Flutter应用的销毁等。

- flutter应用的启动
    * flutter应用的启动是flutter应用的运行的前置条件，flutter应用的运行需要flutter应用的支持。
    * flutter应用的启动主要是通过`FlutterActivity`类的`onCreate`方法来完成的。
    * `FlutterActivity`类的`onCreate`方法主要是通过`FlutterActivityAndFragmentDelegate`类的`onCreate`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`onCreate`方法主要是通过`FlutterActivityAndFragmentDelegate`
      类的`onCreateView`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`onCreateView`
      方法主要是通过`FlutterActivityAndFragmentDelegate`类的`createFlutterView`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`createFlutterView`
      方法主要是通过`FlutterActivityAndFragmentDelegate`类的`createFlutterSurfaceView`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`createFlutterSurfaceView`
      方法主要是通过`FlutterActivityAndFragmentDelegate`类的`createFlutterTextureView`方法来完成的。

- flutter应用的运行
    * flutter应用的运行是flutter应用的销毁的前置条件，flutter应用的销毁需要flutter应用的支持。
    * flutter应用的运行主要是通过`FlutterActivity`类的`onResume`方法来完成的。
    * `FlutterActivity`类的`onResume`方法主要是通过`FlutterActivityAndFragmentDelegate`类的`onResume`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`onResume`方法主要是通过`FlutterActivityAndFragmentDelegate`
      类的`onPostResume`方法来完成的。

- flutter应用的销毁
    * flutter应用的销毁是flutter应用的销毁的前置条件，flutter应用的销毁需要flutter应用的支持。
    * flutter应用的销毁主要是通过`FlutterActivity`类的`onDestroy`方法来完成的。
    * `FlutterActivity`类的`onDestroy`方法主要是通过`FlutterActivityAndFragmentDelegate`类的`onDestroy`方法来完成的。
    * `FlutterActivityAndFragmentDelegate`类的`onDestroy`方法主要是通过`FlutterActivityAndFragmentDelegate`
      类的`onDetach`方法来完成的。

###### 1.3 销毁阶段

销毁阶段主要是Flutter引擎的销毁，包括Flutter引擎的销毁、Dart isolate的销毁、Dart VM的销毁等。

- Flutter引擎的销毁
    * Flutter引擎的销毁是Flutter引擎的销毁的前置条件，Flutter引擎的销毁需要Flutter引擎的支持。
    * Flutter引擎的销毁主要是通过`FlutterEngine`类的`destroy`方法来完成的。

- Dart isolate的销毁
    * Dart isolate的销毁是Dart isolate的销毁的前置条件，Dart isolate的销毁需要Dart isolate的支持。
    * Dart isolate的销毁主要是通过`DartIsolate`类的`destroy`方法来完成的。

- Dart VM的销毁
    * Dart VM的销毁是Dart VM的销毁的前置条件，Dart VM的销毁需要Dart VM的支持。
    * Dart VM的销毁主要是通过`DartVM`类的`destroy`方法来完成的。

###### 1.4 总结

Flutter应用的启动、运行、销毁主要是通过Flutter引擎的启动、运行、销毁来完成的，Flutter引擎的启动、运行、销毁主要是通过Dart isolate的启动、运行、销毁来完成的，Dart
isolate的启动、运行、销毁主要是通过Dart VM的启动、运行、销毁来完成的。