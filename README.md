# ESP32 MAC Address Reader

## 📌 Description

This project demonstrates how to retrieve and display the **MAC (Media Access Control) address** of an ESP32 using the Arduino IDE.

The program configures the ESP32 in **Wi-Fi Station (STA) mode** and uses the ESP-IDF Wi-Fi API to read the device's unique MAC address.

## 🛠️ Components Required

* ESP32 Development Board
* USB Cable
* Arduino IDE

## 💻 Libraries Used

```cpp
#include <WiFi.h>
#include <esp_wifi.h>
```

## ⚙️ Working

1. The ESP32 is initialized using `Serial.begin(115200)`.
2. Wi-Fi is configured in **Station Mode** using `WIFI_STA`.
3. The `esp_wifi_get_mac()` function retrieves the MAC address of the ESP32.
4. The MAC address is converted into hexadecimal format.
5. The result is displayed on the Serial Monitor.

## 🔍 Important Function

```cpp
esp_wifi_get_mac(WIFI_IF_STA, mac);
```

This function reads the MAC address of the ESP32's Wi-Fi Station interface and stores it in a 6-byte array.

## 📟 Example Output

```text
ESP32 MAC: 24:6F:28:XX:XX:XX
```

> The MAC address will be different for every ESP32 device.

## 🎯 Applications

* Identifying individual ESP32 devices
* Device registration in IoT systems
* Network-based device identification
* MAC-based authentication
* IoT device management

## 🚀 Future Scope

The retrieved MAC address can be used as a unique device identifier in IoT projects, MQTT systems, cloud platforms, and ESP32-based device management systems.

## 📄 License

This project is created for educational and experimental purposes.
