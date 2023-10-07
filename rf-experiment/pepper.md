This is the code accompanying the paper.

## Requirements

 - A Pepper robot running NAOqi-2.5.7
 - Ubuntu 20.04
 - The Choregraphe software [Installation](https://developer.softbankrobotics.com/pepper-naoqi-25/naoqi-developer-guide/getting-started/downloading-installing-softbank-robotics)

## Fix libz issue on Ubuntu 20.04

```
cd "/opt/Softbank Robotics/Choregraphe Suite 2.5/lib/"
mv libz.so.1 libz.so.1.old
ln -s /lib/x86_64-linux-gnu/libz.so.1
```

Reference: https://stackoverflow.com/questions/48306849/lib-x86-64-linux-gnu-libz-so-1-version-zlib-1-2-9-not-found
