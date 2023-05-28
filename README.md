# Belajar Flutter 3

Website News App

## Catatan

Cara Running:
```
flutter run -d chrome --web-renderer html
```

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

Terima Kasih.