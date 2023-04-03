# flutter的状态管理

## 状态管理框架
- [Provider](https://pub.dev/packages/provider)

- [Redux](https://pub.dev/packages/redux)

- [MobX](https://pub.dev/packages/mobx)

- [BLoC](https://pub.dev/packages/bloc)

- [GetX](https://pub.dev/packages/get)

- [Riverpod](https://pub.dev/packages/riverpod)

- [StateNotifier](https://pub.dev/packages/state_notifier)

- [StateX](https://pub.dev/packages/statex)

### Provider
[Provider](https://pub.dev/packages/provider)是一个状态管理框架，它提供了一种简单的方式来管理应用程序的状态，同时还提供了一些小部件，这些小部件可以让我们在不使用`setState`的情况下更新UI。

#### Provider的使用
1. 在`pubspec.yaml`文件中添加依赖
```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^4.3.2+2
```

2. 在`main.dart`文件中导入`provider`包
```dart
import 'package:provider/provider.dart';
```

3. 在`main.dart`文件中使用`Provider`包裹`MyApp`类
```dart
void main() {
  runApp(
    Provider(
      create: (context) => Counter(),
      child: MyApp(),
    ),
  );
}
```

4. 在`main.dart`文件中创建`Counter`类
```dart
class Counter with ChangeNotifier {
  int _count = 0;

  int get count => _count;

  void increment() {
    _count++;
    notifyListeners();
  }
}
```

5. 在`main.dart`文件中创建`MyApp`类
```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}
```

6. 在`main.dart`文件中创建`MyHomePage`类
```dart
class MyHomePage extends StatelessWidget {
  MyHomePage({Key key, this.title}) : super(key: key);

  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have pushed the button this many times:',
            ),
            Consumer<Counter>(
              builder: (context, counter, child) {
                return Text(
                  '${counter.count}',
                  style: Theme.of(context).textTheme.headline4,
                );
              },
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          Provider.of<Counter>(context, listen: false).increment();
        },
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ),
    );
  }
}
```

### Redux
[Redux](https://pub.dev/packages/redux)是一个状态管理框架，它提供了一种简单的方式来管理应用程序的状态，同时还提供了一些小部件，这些小部件可以让我们在不使用`setState`的情况下更新UI。

#### Redux的使用
1. 在`pubspec.yaml`文件中添加依赖
```yaml
dependencies:
  flutter:
    sdk: flutter
  redux: ^4.0.0
```

2. 在`main.dart`文件中导入`redux`包
```dart
import 'package:redux/redux.dart';
```

3. 在`main.dart`文件中创建`Counter`类
```dart
class Counter {
  int count;

  Counter(this.count);
}
``` 

4. 在`main.dart`文件中创建`CounterReducer`类
```dart
class CounterReducer {
  static int reducer(int state, action) {
    if (action == 'increment') {
      return state + 1;
    } else if (action == 'decrement') {
      return state - 1;
    } else {
      return state;
    }
  }
}
```

5. 在`main.dart`文件中创建`MyApp`类
```dart
class MyApp extends StatelessWidget {
  final store = Store<int>(CounterReducer.reducer, initialState: 0);

  @override
  Widget build(BuildContext context) {
    return StoreProvider<int>(
      store: store,
      child: MaterialApp(
        title: 'Flutter Demo',
        theme: ThemeData(
          primarySwatch: Colors.blue,
        ),
        home: MyHomePage(title: 'Flutter Demo Home Page'),
      ),
    );
  }
}
```

6. 在`main.dart`文件中创建`MyHomePage`类
```dart
class MyHomePage extends StatelessWidget {
  MyHomePage({Key key, this.title}) : super(key: key);

  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have pushed the button this many times:',
            ),
            StoreConnector<int, String>(
              converter: (store) => store.state.toString(),
              builder: (context, count) {
                return Text(
                  count,
                  style: Theme.of(context).textTheme.headline4,
                );
              },
            ),
          ],
        ),
      ),
      floatingActionButton: StoreConnector<int, VoidCallback>(
        converter: (store) {
          return () => store.dispatch('increment');
        },
        builder: (context, callback) {
          return FloatingActionButton(
            onPressed: callback,
            tooltip: 'Increment',
            child: Icon(Icons.add),
          );
        },
      ),
    );
  }
}
```


