---
title: "LCD Display with Arduino"
date: 2020-08-05T12:15:51-05:00
categories:
- Coding
- Arduino
tags:
- Coding
- Arduino
keywords:
- tech
- Coding
- Arduino
- Micro Controller
#thumbnailImage: //example.com/image.jpg
clearReading: true
thumbnailImage: /images/city.jpg
thumbnailImagePosition: left
metaAlignment: left
coverImage: /images/city.jpg
coverMeta: in
comments: true
showDate: true
showTags: true
showPagination: true
showSocial: true
showMeta: true
showActions: true
summary: "This article will show you how to use an LCD display with your Arduino."
---
In this article you will learn how to use an LCD Display to display things with your Arduino.

# Components
The components you will need for this project are:
- Arduino Uno R3
- LCD Display Module
- 10k Potentimeter
- Breadboard
- 16 male-to-male jumper wires

![Components](/images/Arduino.jpg)

------------------------------------

# LCD Display
Your LCD display should have 16 pins coming out from the bottom.

![LCD Pins](/images/LCDPins.jpg)

Each pin has different functions:
- VSS: Pin that connects to ground.
- VDD: Pin that connects to a 5v power supply.
- VO: Adjusts the contrast of the display.
- RS: A register selecting pin that controls where your writing data goes in the LCD's memory.
- R/W: Read/write pin.
- E: An enabling pin that, when supplied with low-level energy, causes the LCD module to carry out certain instructions.
- D0-D7: Pins that read or write data.
- A and K: Pins that control the LED backlight.

-------------------------------------------

# Connection Schematic

![Connection Schematic](/images/CS.jpg)

The LCD display needs 6 arduino pins, all set to be digital outputs. It also needs ground and 5v connections.

----------------------------------------

# Wiring Diagram
The wiring should look something like this.

![Wiring Diagram](/images/WD.jpg)

![Wiring Diagram](/images/WD2.jpg)

-------------------------------------------

# Code
To use this code you should download the [Arduino IDE](https://www.arduino.cc/en/main/software) so you can load it onto your Arduino Uno. You will also need the [Liquid Crystal](https://www.arduinolibraries.info/libraries/liquid-crystal) library to run this code.

```
  // Include the Liquid Crystal library.
  #include <LiquidCrystal.h>

  // Initialize the library with the numbers of the interface pins.
  LiquidCrystal lcd(7, 8, 9, 10, 11, 12);

  void setup() {
    // set up the LCD's number of columns and rows:
    lcd.begin(16, 2);

    // Print a message to the LCD. You can print whatever message you want.
    lcd.print("Hello, World!");
  }

    void loop() {
      // set the cursor to column 0, line 1
      // (note: line 1 is the second row, since counting begins with 0):
      // This is where the word or phrase will start.
      lcd.setCursor(0, 1);
  }
```

---------------------------------------------------
If you did everything properly this is what you should end up with.

![Finished Product](/images/Complete.jpg)






<!--more-->
