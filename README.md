# Splash Screen

* A small Splash Screen used for an intro for any flutter application easily using

## For iOS And Android 

* It 's Now Very Simple And Easy To Use 
* Coming Soon Will Add A Greater Functions 
* For Any information Send Message To Me On => monkey4gamesmmm@gmail.com


### ScreenShot
![screenshot description (alt)](screenshot.png)

## Usage

[Example](https://github.com/KarimMohamed2005/SplashScreenFlutterPackage/blob/master/example/example.dart)

To use this package :

* add the dependency to your [pubspec.yaml](https://github.com/KarimMohamed2005/SplashScreenFlutterPackage/blob/master/pubspec.yaml) file.

```yaml
  dependencies:
    flutter:
      sdk: flutter
    splashscreen:
```

### How to use

As time based...

``` dart
      new SplashScreen(
      seconds: 14,
      navigateAfterSeconds: new AfterSplash(),
      title: new Text('Welcome In SplashScreen'),
      image: new Image.asset('screenshot.png'),
      backgroundColor: Colors.white,
      styleTextUnderTheLoader: new TextStyle(),
      photoSize: 100.0,
      loaderColor: Colors.red
    );
```

As futured based...

``` dart
      new SplashScreen(
      navigateAfterFuture: stateClass.loadProfile(),
      title: new Text('Welcome In SplashScreen'),
      image: new Image.asset('screenshot.png'),
      backgroundColor: Colors.white,
      styleTextUnderTheLoader: new TextStyle(),
      photoSize: 100.0,
      loaderColor: Colors.red
    );
```


## Example

As time based...

``` dart

import 'package:flutter/material.dart';
import 'package:splashscreen/splashscreen.dart';
void main(){
  runApp(new MaterialApp(
    home: new MyApp(),
  ));
}


class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => new _MyAppState();
}

class _MyAppState extends State<MyApp> {
  @override
  Widget build(BuildContext context) {
    return new SplashScreen(
      seconds: 14,
      navigateAfterSeconds: new AfterSplash(),
      title: new Text('Welcome In SplashScreen',
      style: new TextStyle(
        fontWeight: FontWeight.bold,
        fontSize: 20.0
      ),),
      image: new Image.network('https://i.imgur.com/TyCSG9A.png'),
      backgroundColor: Colors.white,
      styleTextUnderTheLoader: new TextStyle(),
      photoSize: 100.0,
      onClick: ()=>print("Flutter Egypt"),
      loaderColor: Colors.red
    );
  }
}

class AfterSplash extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new Scaffold(
      appBar: new AppBar(
      title: new Text("Welcome In SplashScreen Package"),
      automaticallyImplyLeading: false
      ),
      body: new Center(
        child: new Text("Done!",
        style: new TextStyle(
          fontWeight: FontWeight.bold,
          fontSize: 30.0
        ),),

      ),
    );
  }
}
```

As future based...

``` dart

import 'package:flutter/material.dart';
import 'package:splashscreen/splashscreen.dart';
void main(){
  runApp(new MaterialApp(
    home: new MyApp(),
  ));
}


class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => new _MyAppState();
}

class _MyAppState extends State<MyApp> {

  Future<Widget> loadFromFuture() async {
  
  <fetch some data from server. ex. login>
  
     return Future.value(new AfterSplash());
  }

  @override
  Widget build(BuildContext context) {
    return new SplashScreen(
      navigateAfterFuture: loadFromFuture(),
      title: new Text('Welcome In SplashScreen',
      style: new TextStyle(
        fontWeight: FontWeight.bold,
        fontSize: 20.0
      ),),
      image: new Image.network('https://i.imgur.com/TyCSG9A.png'),
      backgroundColor: Colors.white,
      styleTextUnderTheLoader: new TextStyle(),
      photoSize: 100.0,
      onClick: ()=>print("Flutter Egypt"),
      loaderColor: Colors.red
    );
  }
}

class AfterSplash extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new Scaffold(
      appBar: new AppBar(
      title: new Text("Welcome In SplashScreen Package"),
      automaticallyImplyLeading: false
      ),
      body: new Center(
        child: new Text("Done!",
        style: new TextStyle(
          fontWeight: FontWeight.bold,
          fontSize: 30.0
        ),),

      ),
    );
  }
}
```
