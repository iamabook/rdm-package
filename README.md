Package rdm for OS X

1. build with qt ( i used qt 5.11.1 )

2. make directories like this
```
	rdm.app		Contents	Frameworks  
					Info.plist
					MacOS
					Resources -- qml
					...
```
3. copy all files in source/bin/osx/Frameworks to Frameworks

4. copy libcrypto.1.0.0.dylib, libssl.1.0.0.dylib to Frameworks (they are in openssl)

5. copy all files in bin/osx/debug to MacOS

6. Info.plist - in source/src/resources/Info.plist

7. Resources - in source/src/resources folder.

8. Resources/qt.conf

```
[Paths]
Plugins = PlugIns
Imports = Resources/qml
Qml2Imports = Resources/qml
```

9. make directory Resources/qml

10. copy directories from YOUR_QT_BINARY/clang_64/qml/ [Qt, QtChars, QtGraphicalEffects, QtMultimedia, QtQml, QtQuick, QtQuick.2, QtTest] to Resources/qml

11. execute macdeployqt
