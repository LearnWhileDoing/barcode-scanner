# Hybrid apps

## One app/one platform: fast

Most popular apps that you know run on iPhones and Android phones. But is it really the same "app" that is running on both systems? In most cases, the answer is no.

Typically, when an app developer wants to make an app, they have to code **a different app for each platform.** That means one app for iOS, another app for Android, another app for macOS, etc. etc. That is a lot of work, especially if you are making an app by yourself or with a small team. For example, if you have a great idea for an app and you want as many people as possible to use your app, you would have to code multiple apps for each platform. That's a big hassle, and is why some apps in the past like HQ have chosen to just start off on iOS.

## One app/all platforms: slow

But what if you could write a SINGLE app that runs on all platforms? Some frameworks have attempted to solve this problem, like Apache Cordova, Ionic, or Monaca. However, these platforms are often very slow. Why is that?

These frameworks add an extra layer on top of the native operating system because they use runtime environments. That means that the code is actively being "understood" by the runtime environment, which then sends information to the operating system. That makes these apps much slower when compared to native apps because their code is compiled before-hand, and the operating system is able to make its own instructions.

Can we have the best of both worlds?

## One app/all platforms: fast

With new hybrid platforms like Flutter, React Native, and NativeScript, you are able to make one app for all platforms that run as if they are native apps. [Sometimes](https://medium.com/swlh/flutter-vs-react-native-vs-native-deep-performance-comparison-990b90c11433), hybrid apps are able to even perform better than native apps because they use only the most efficient code for each platform.

One of the many reasons Flutter chose Dart to be it's programming language is that it can compile down to machine code with Dart's native compilers. This lets the app be run directly by the operating system, whether it is iOS, Android, macOS, Windows, or Linux. 

## Why is performance important?

Have you ever played a game that got very glitchy? Or used an app that seemed to stutter when you are scrolling or swiping? This is a sign of an app with bad performance issues. Often times like with intense games, this is unpreventable. But when you are simply making apps without a lot of graphics, your app should look as polished as possible.

