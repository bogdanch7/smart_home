# Smart Home – Sistem casă inteligentă cu monitorizare și control
Acest proiect reprezintă un sistem complet funcțional de casă inteligentă, realizat în cadrul disciplinei **Automatizarea clădirilor**. Platforma combină funcționalitățile de monitorizare, securitate și control la distanță, utilizând microcontrolerele Arduino Mega 2560 și ESP32, integrate cu senzori diverși și o interfață web.

---

## Funcționalități
Detecție acces în funcție de distanță (<150 cm) – afișare opțiune login doar în apropierea ușii
Autentificare multiplă: prin tastatură fizică (PIN), tag RFID sau direct din browser
Dashboard senzori: temperatură, umiditate, gaz, flacără, distanță, cameră video
Streaming video în timp real (ESP32-CAM) integrat în interfața web
Feedback sonor (buzzer) pentru acțiuni reușite sau eșuate
Afișaj local pe LCD I2C pentru mesaje și stări sistem
Interfață web responsive pentru control și monitorizare
Transmisie de date serială între Arduino Mega și ESP32

---

## Componente utilizate
Arduino Mega 2560 – colectează date de la senzori și gestionează autentificarea
ESP32 – server web + comunicare cu Arduino + integrare cameră
Senzori:
DHT11 – temperatură și umiditate
MQ-2 – detecție gaze
HC-SR04 – măsurare distanță
Senzor IR flacără
Tastatură 4x4 – introducere cod PIN
Modul RFID RC522 – autentificare cu tag-uri RFID
Buzzer – notificări sonore
LCD 16x2 cu I2C – afișare locală a stărilor sistemului
Cameră OV2640 (ESP32-CAM) – streaming video integrat

---

## Biblioteci utilizate

SPI.h, MFRC522.h, Keypad.h, DHT.h, Wire.h, LiquidCrystal_I2C.h, WiFi.h, WebServer.h

---

## Modul de funcționare
Accesul inițial: activat doar dacă senzorul detectează prezența la <150 cm

## Autentificare:
Keypad – cod presetat (ex. 0000)
Browser PIN – form online
RFID – autentificare pe bază de UID

## Dashboard:
Acces la date în timp real de la senzori
Streaming video live prin iframe
Mesaje dinamice și actualizări automate

## Transmiterea datelor:
Arduino trimite periodic informații către ESP32 prin Serial1
ESP32 actualizează pagina web la fiecare câteva secunde
Rulare & configurare
Montare hardware pe breadboard, conform schemei Fritzing
Încărcare coduri în Arduino Mega și ESP32
Setare rețelei Wi-Fi în codul ESP32 (SSID + parolă)
Accesare interfață web din browser, folosind IP-ul afișat de ESP32

---

## Capturi

(Capturile pot include imagini precum: pagina de login, acces permis/respins, dashboard senzori, valori senzor, flux video etc.)
![image](https://github.com/user-attachments/assets/202beb63-b97a-48a2-9021-af4b537dc553)



---

## Realizat de

Proiect realizat de [bogdanch7](https://github.com/bogdanch7)
An universitar 2024–2025

---

## Licență

Acest proiect este creat pentru uz educațional.
