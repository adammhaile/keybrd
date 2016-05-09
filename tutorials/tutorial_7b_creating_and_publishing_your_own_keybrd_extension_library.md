Tutorial 7b - creating and publishing your own keybrd extension library
=======================================================================
Listing your keybrd extension library allows others to find and install your library.
The keybrd extension library name should start with "keybrd_" so that it is easy for people to find.
The directory structure of the library depends on where it will be listed.

## Publishing anywhere with listing on Arduino Playground LibraryList
Arduino Playground LibraryList can list a library with any directory structure.
The directory structure of your keybrd extension library can be as simple as:

    keybrd_MyKeyboard/
        class1.cpp
        class1.h
        class2.cpp
        class2.h
        ..
        instantiations_codes.h
        instantiations_ports.h
        instantiations_matrix.h
        doc/
            keybrd_MyKeyboard_guide
        examples/
            keybrd_MyKeyboard1/
                keybrd_MyKeyboard1.ino
            keybrd_MyKeyboard2/
                keybrd_MyKeyboard2.ino

[Arduino playground](http://playground.arduino.cc/) is a wiki.
Instructions for listing a library on the Arduino playgound LibraryList are at:
    http://playground.arduino.cc/Code/Library#Sharing

Add your keybrd library to the Keyboard/Keypads sublist:
    http://playground.arduino.cc/Main/InterfacingWithHardware#keyb

## Publishing on GitHub with listing on Arduino Library-Manager and Arduino Playground LibraryList
The advantage of using GitHub is that users can submit pull requests.
The advantage of using Arduino Library-Manager is that users can install your library through the Arduino IDE.

Arduino Library-Manager is particular about directory structures it accepts.
The directory structure of your keybrd extension library to look like this:

    keybrd_MyKeyboard/
        library.properties
        doc/
            keybrd_MyKeyboard_guide
        examples/
            keybrd_MyKeyboard1/
                keybrd_MyKeyboard1.ino
            keybrd_MyKeyboard2/
                keybrd_MyKeyboard2.ino
        src/
            class1.cpp
            class1.h
            class2.cpp
            class2.h
            ..
            instantiations_codes.h
            instantiations_ports.h
            instantiations_matrix.h

The library.properties file is described in
    https://github.com/arduino/Arduino/wiki/Arduino-IDE-1.5:-Library-specification
Example library.properties file:
    name=keybrd_MyKeyboard
    version=1.2.3
    author=Me
    maintainer=Me
    sentence=An extension to the keybrd library for the My keyboard.
    paragraph=This library demonstrates my feature.
    category=Device Control
    url=https://github.com/Me/keybrd_MyKeyboard
    architectures=Teensy LC

Instructions for listing a library on Arduino Library Manager are at:
    https://github.com/arduino/Arduino/wiki/Library-Manager-FAQ

After it has been accepted into the Arduino IDE Library Manager, add your library to the Arduino Playground LibraryList.
[Arduino playground](http://playground.arduino.cc/) is a wiki.
Sign in at http://playground.arduino.cc/Main/LibraryList and add keybrd libraries to Keyboard/Keypads sublist:
    http://playground.arduino.cc/Main/InterfacingWithHardware#keyb