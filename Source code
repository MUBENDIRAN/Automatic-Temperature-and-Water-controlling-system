#include <Wire.h>
#include <LiquidCrystal_I2C.h>
#include <Servo.h>

LiquidCrystal_I2C lcd1(0x27, 16, 2);
LiquidCrystal_I2C lcd2(0x24, 16, 2);

const int tempPin = A0;
const int ledPin = 13;
const int servoPin = 11;

const float tempThreshold = 30.0;

Servo myServo;

void setup() {
    lcd1.init();
    lcd1.backlight();
    
    lcd2.init();
    lcd2.backlight();

    Serial.begin(9600);

    pinMode(ledPin, OUTPUT);
    myServo.attach(servoPin);
}

void loop() {
    int analogValue = analogRead(tempPin);
    float voltage = (analogValue * 5.0) / 1023.0;
    float temperatureC = (voltage - 0.5) * 100.0;

    lcd1.clear();
    lcd1.setCursor(0, 0);
    lcd1.print("Temperature: ");
    lcd1.print(temperatureC);
    lcd1.print(" C");

    if (temperatureC > tempThreshold) {
        digitalWrite(ledPin, HIGH);

        lcd1.setCursor(0, 1);
        lcd1.print("Cooling: ON");

        myServo.write(90);

        lcd2.clear();
        lcd2.setCursor(0, 0);
        lcd2.print("Water Flow: ON");
    } else {
        digitalWrite(ledPin, LOW);

        lcd1.setCursor(0, 1);
        lcd1.print("Cooling: OFF");

        myServo.write(0);

        lcd2.clear();
        lcd2.setCursor(0, 0);
        lcd2.print("Water Flow: OFF");
    }

    delay(1000);
}
