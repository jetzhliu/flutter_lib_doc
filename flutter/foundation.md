## annotations

用于生成文档的注解，没啥用

- Category
- DocumentationIcon
- Summary

```dart
@Category(const <String>['Animals', 'Cats'])
@Category(const <String>['Cute', 'Pets'])
@DocumentationIcon('https://www.examples.net/docs/images/icons/pillar.jpeg')
@Summary('A famous three-legged cat.')
class Pillar extends Cat {
  // ...code...
}
```

## assertions

- void debugPrintStack({ String label, int maxFrames }) 打印当前堆栈

其他没啥用

## basic_types

一些基本的类型定义，很少直接使用

## binding

用于定义单例的服务

- abstract class BindingBase

## change_notifier

定义监听器

- abstract class Listenable
- abstract class ValueListenable<T> extends Listenable
- class ChangeNotifier extends Listenable
- class ValueNotifier<T> extends ChangeNotifier

## collections

集合和数组的相等比较

- bool setEquals<T>(Set<T> a, Set<T> b)
- bool listEquals<T>(List<T> a, List<T> b)

## consolidate_response

http请求返回处理

- Future<Uint8List> consolidateHttpClientResponseBytes(HttpClientResponse response)

把response的内容以Uint8List形式一次性返回（response是Stream接口，这个方法转成Future接口）

## debug

没啥用

## diagnostics

UI诊断，用于打印组件树

## isolates

多任务，类似于开线程执行耗时任务

## key

用于判断两个`Widget`，`Element`或`SemanticsNode`是否为同一个，类似`react.js`中的key

- abstract class Key
- abstract class LocalKey extends Key
- class ValueKey<T> extends LocalKey

## licenses

没啥用

## node

太基础

## observer_list

用于频繁判断元素是否在列表中的优化实现（内部维护一个HashSet）

- class ObserverList<T> extends Iterable<T>

## platform

用于判断平台

- enum TargetPlatform { android, fuchsia, iOS }
- TargetPlatform get defaultTargetPlatform

```dart
bool isIos = defaultTargetPlatform == TargetPlatform.iOS ? true : false;
```

## print

调试输出，很少直接用

## profile

没啥用

## serialization

二进制序列化，太基础很少直接用

## synchronous_future

把一个值转成resolve该值的future，类似js的Promise.resolve

## unicode

