# Smart Home – Sistem de securitate smart home cu monitorizare remote
Acest proiect reprezintă un sistem complet funcțional de casă inteligentă, realizat în cadrul disciplinei **Automatizarea clădirilor**, fiind un proiect de echipă. Platforma combină funcționalitățile de monitorizare, securitate și control la distanță, utilizând microcontrolerele Arduino Mega 2560 și ESP32, integrate cu senzori diverși și o interfață web.

---

## Funcționalități
Permiterea accesului în funcție de distanță (<150 cm) – afișarea opțiunii de login doar în apropierea ușii

Modalități multiple de autentificare: prin tastatură fizică (PIN), tag RFID sau direct din browser

Dashboard senzori: temperatură, umiditate, gaz, flacără, distanță, cameră video

Streaming video în timp real (ESP32-CAM) integrat în interfața web

Feedback sonor (buzzer) pentru accesul permis sau respins

Afișaj local pe LCD I2C pentru mesajele și stările sistemului

Interfață web responsive pentru control și monitorizare

Transmisie de date serială între Arduino Mega și ESP32

---

## Componente utilizate
Arduino Mega 2560 – colectează datele de la senzori și gestionează autentificarea

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

## Autentificare
Keypad – cod presetat (ex. 0000)

Browser PIN – form online

RFID – autentificare pe bază de UID

## Dashboard
Permite accesul la datele citite în timp real de senzori

Streaming video live prin iframe

Mesaje dinamice și actualizări automate

## Transmiterea datelor
Realizarea legăturilor fizice între componente, conform schemei Fritzing

Încărcarea codurilor în Arduino Mega și ESP32

Setare rețelei Wi-Fi în codul ESP32 (SSID + parolă)

Accesarea interfeței web din browser, folosind IP-ul afișat de ESP32

Arduino trimite periodic informații către ESP32 prin Serial1

ESP32 actualizează pagina web la fiecare 5 secunde

---

## Capturi

![fritzing](https://github.com/user-attachments/assets/646f588b-4d35-483b-994a-760de7bb2d2f)

Schema Fritzing a montajului

![IMG-20250529-WA0006](https://github.com/user-attachments/assets/81f64fd6-d36c-42c1-b81c-480f87ef3d47)
![IMG-20250529-WA0011](https://github.com/user-attachments/assets/e18ce6e9-aaad-4ea9-8916-0845a5aa3e6e)

Detectarea distanței față de persoana din fața ușii

![IMG-20250529-WA0027](https://github.com/user-attachments/assets/40f6454c-a7d9-42c0-9f96-e8c65c0d7059)

Prezentarea generală a casei

![IMG-20250529-WA0064](https://github.com/user-attachments/assets/0f5a831c-e488-4923-a1df-bbdaf233f878)

Pagina de login

![IMG-20250529-WA0041](https://github.com/user-attachments/assets/0977cf1f-0892-477a-9cce-814be6edbab4)

Afișarea mesajului de întâmpinare

![WhatsApp Image 2025-06-14 at 12 24 55_7609e469](https://github.com/user-attachments/assets/17964355-c624-4d25-9516-250c0f9e4f90)

Alegerea modalității de acces

![IMG-20250529-WA0017](https://github.com/user-attachments/assets/eb004b72-1e4b-4ff2-93d1-fcb2085d62e6)
![IMG-20250529-WA0034](https://github.com/user-attachments/assets/54d8e326-db5e-4e62-9f0e-6b583f631af0)

Modalitatea de login prin keypad

![IMG-20250529-WA0014](https://github.com/user-attachments/assets/fef2d041-8462-4d68-aeaa-96214ea6f8f3)
![IMG-20250529-WA0033](https://github.com/user-attachments/assets/a14376d8-154b-4181-8e89-3d0969df0573)

Modalitatea de login prin RFID

![IMG-20250529-WA0053](https://github.com/user-attachments/assets/9426d0e4-d195-44b2-9156-abf81ae4ad6a)

Panoul de control al casei

![IMG-20250529-WA0049](https://github.com/user-attachments/assets/e67f2fae-2433-44df-ab85-44e4f00381ea)

Afișarea valorilor citite de senzori

![IMG-20250529-WA0063](https://github.com/user-attachments/assets/9601a8a1-39c7-44c6-acf7-3bc4f7a41a6c)

Afișarea valorii temperaturii

![IMG-20250529-WA0065](https://github.com/user-attachments/assets/62b04703-cf9e-482f-ba0c-4687680ea5b1)
![IMG-20250529-WA0056](https://github.com/user-attachments/assets/eb03a51a-c585-4e31-96bb-e9fb639630d3)

Stările senzorului de gaz

![IMG-20250529-WA0047](https://github.com/user-attachments/assets/37d14e5d-b341-4845-a577-c6851baddf15)

Exemplificarea funcționării senzorului de gaz, G: DA

![IMG-20250529-WA0020](https://github.com/user-attachments/assets/97044a37-6d84-48b8-bcb6-8c34a428bb44)

Afișarea valorii citite de senzorul de umiditate

![IMG-20250529-WA0022](https://github.com/user-attachments/assets/47c0ad95-ede9-45d2-8c6f-c465e5bc68ac)
![IMG-20250529-WA0023](https://github.com/user-attachments/assets/c2b96cd3-f6e6-4345-99e8-9b85b773efbd)

Stările de funcționare ale senzorului de flacără

![IMG-20250529-WA0052](https://github.com/user-attachments/assets/45cdbd79-cbc9-40ee-b4ec-f7fe02d64142)

Exemplificarea funcționării senzorului de flacără, F: DA

![IMG-20250529-WA0066](https://github.com/user-attachments/assets/c5b2caa8-d3a3-431b-ad4e-e1bc11a8b3f1)

Exemplificarea modului de funcționare a camerei video

---

## Realizat de
Proiect realizat de [bogdanch7](https://github.com/bogdanch7)

An universitar 2024–2025

---

## Licență
Acest proiect este creat pentru uz educațional.
