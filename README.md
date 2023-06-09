# Belajar Flutter 3 Navigation Bottom
![ss 2](https://github.com/ihsanunot/Flutter_Web_Satu_Nav/assets/127992374/8a8f5b54-00d8-4087-8f0e-355e4a5b504b)

Website News App

## Catatan

Cara Running:
```
flutter run -d chrome --web-renderer html
```
![ss 1](https://github.com/ihsanunot/Flutter_Web_Satu_Nav/assets/127992374/a72b277d-f5c4-4742-b590-c0dbebe066d5)

Class lain tidak bisa dimasukan ke dalam class lagi.

Contoh:

```
Class Home extends StatelessWidget{
    .....
    @override
    .....
    class Sidebar

    //Hasil nya Pasti Error
}
```

jadi perhatikan juga penempatan class nya dan import nya.

Kalau pas di jalanin Error
Berarti salah satu depencies nya harus di upgrade

Contoh :
```
flutter pub add google_fonts
```

Nah sekarang coba lagi **flutter run -d chrome --web-renderer html**

---

Flutter juga menyediakan library Cupertino yang merupakan tampilan widget untuk perangkat iOS.

Flutter dilengkapi dengan Flutter DevTools yang akan membantu kita dalam proses pengembangan aplikasi.

Beberapa hal yang dapat dilakukan dengan DevTools adalah:

Memeriksa layout UI dan state aplikasi Flutter.

Memeriksa isu performa di aplikasi Flutter.

CPU profiling untuk aplikasi Flutter atau Dart.

Network profiling untuk aplikasi Flutter.

Debugging sumber aplikasi Flutter atau Dart.

Debugging masalah memori di aplikasi Flutter atau Dart CLI.

Melihat log dan informasi diagnostik tentang aplikasi Flutter atau Dart CLI.

---

Widget buat dijalanin di Android :
```
Widget _buildAndroid(BuildContext context) {
  return Scaffold(
    appBar: AppBar(
      title: const Text('News App'),
    ),
    body: _buildList(context),
  );
}
```

Widget buat dijalanin di iOS:
```
Widget _buildIos(BuildContext context) {
  return CupertinoPageScaffold(
    navigationBar: CupertinoNavigationBar(
      middle: const Text('News App'),
    ),
    child: _buildList(context),
  );
}
```

Lalu PlatformWidget:
```
@override
Widget build(BuildContext context) {
  return PlatformWidget(
    androidBuilder: _buildAndroid,
    iosBuilder: _buildIos,
  );
}
```

yg widget PlatformWidget biasa nya ditaruh di bawah file.

--- Beberapa file nya di Refactoring biar lebih rapih

jadi di dalam lib nya main.dart, sisanya folder ui,folder common - isi nya styles.dart - folder ui - isi nya :
- article_list_page.dart
- detail_page.dart
- home_page.dart
- settings_page.dart



Terima Kasih.
