# Tropfensensor
Mit einem Tropfensensor oder auch Flüssigkeitssensor kann man wie es der Name schon sagt eine Flüssigkeit detektieren. Dazu muss sich die Flüssigkeit direkt auf dem Sensor befinden. Es reicht bereits ein kleiner Tropfen aus, um einen eindeutigen Messwert zu erhalten.

Man kann den Sensor zum Beispiel als Regensensor verwenden. Sobald ein Tropfen auf den Sensor trifft, kann das Arduino-Board eine Aktion ausführen wie z.B. eine Markise einrollen, Jalousien schließen, einen Alarm auslösen oder einen Scheibenwischer betätigen.

Die Funktionsweise ist einfach. An den langen Kontaktstellen die den Sensor durchziehen liegt eine Spannung an (entweder + oder -). Sobald eine Flüssigkeit bspw. durch einen Tropfen zwei Kontakte verbindet, fließt ein kleiner Strom von einem Kontakt zum Anderen. Dieser Wert wird im Sensor elektronisch aufbereitet und in Form eines analogen Signals an einen analogen Eingang des Boards übermittelt. Da das Board, wie bereits in vorherigen Tutorials beschrieben, keine elektrische Spannung als solche messen kann, wandelt es die am analogen Pin anliegende Spannung in einen Zahlenwert um. 0 bis 5 Volt entspricht einem Zahlenwert von 0 bis 1023 (Das sind 1024 Zahlen, da die Null als erster Zahlenwert gezählt wird).

Bei dem Flüssigkeitssensor liegt der Wert im trockenen bei null „0“. Sobald ein Tropfen Wasser auf die Kontakte des Sensors trifft, liegt der Wer bei ca „480“. Je mehr Tropfen sich auf dem Sensor befinden, desto höher ist der Wert.

Im ersten Code geht es nur darum, den Sonsorwert mit dem Arduino-Board auszulesen und mit dem „serial monitor“ darzustellen.



Aufbau und Material

Material: Arduino Mikrocontrollerboard, Feuchtigkeitssensor, Jumperkabel

Verkabelung:
Tropfensensor am Funduino Mikrocontroller
+ an 5V
– an GND
S an A0

Hinweis zu Messungen:
Wir empfehlen, aufgrund der Elektrolyse durch das Wasser bzw. die Feuchtigkeit an den Sensoren, die Messungen nicht in einem Sekundenabstand durchzuführen. Aus Erfahrungen durch Tests direkt im Wasser, empfehlen wir einen Abstand von 15 Minuten zwischen jeder Messung. Bei Messungen im Sekundenbereich, bei direktem und durchgängigen Wasserkontakt, entstehen durch die Elektrolyse nach ca. 24 Stunden Schäden am Sensor.

Die Programmierung ist sehr einfach und ähnelt sehr stark dem Auslesen von Potentiometern oder dem Auslesen des Feuchtigkeitssensors, da einfach nur ein analoger Wert ausgelesen wird.





Erweiterung des Programms:
Nun soll ein Alarmsignal mit Hilfe eines Piezo-Speakers ertönen, sobald ein Regentropfen auf den Sensor trifft. Als Grenzwert wird in diesem Fall der Messwert 400 festgelegt, da bei einem Tropfen auf dem Sensor ein Messwert von ca. 480 zu erwarten ist.

Verkabelung:
Piezo an Funduino Mikrocontroller
+ an D6
– an GND


Weitere Infos: https://funduino.de/nr-17-tropfensensor
