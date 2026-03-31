# ESP32-C3 WS2812 RGB LED Strip - Red Light

Simple Arduino sketch to control a WS2812 (NeoPixel) RGB LED strip using ESP32-C3, lighting it up in red.

## Hardware Requirements

- **ESP32-C3** DevKit or compatible board
- **WS2812** RGB LED Strip (NeoPixel compatible)
- **Power Supply** (5V for LED strip, USB for ESP32-C3)
- **Jumper Wires**

## Wiring Diagram

```
ESP32-C3          WS2812 LED Strip
--------          ----------------
GPIO8     ------> Data In (DIN)
5V        ------> VCC (if using 5V strip)
GND       ------> GND
```

**Note:** ESP32-C3 uses 3.3V logic. Some WS2812 strips may need a level shifter (e.g., 74HCT245) for reliable operation at 5V. However, many strips work fine with 3.3V directly.

## Software Requirements

- **Arduino IDE** (version 1.8.x or 2.x)
- **ESP32 Board Package** (by Espressif Systems)
- **Adafruit NeoPixel Library**

### Installing Libraries

1. Open Arduino IDE
2. Go to **Sketch** → **Include Library** → **Manage Libraries**
3. Search for "Adafruit NeoPixel"
4. Install "Adafruit NeoPixel by Adafruit"

### ESP32 Board Setup

1. Go to **File** → **Preferences**
2. Add to "Additional Board Manager URLs":
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
3. Go to **Tools** → **Board** → **Board Manager**
4. Search for "ESP32" and install "ESP32 by Espressif Systems"
5. Select **Tools** → **Board** → **ESP32C3 Dev Module**

## Configuration

Edit these values in the code as needed:

```cpp
#define LED_PIN     8       // GPIO pin for WS2812 data
#define NUM_LEDS    30      // Number of LEDs in your strip
#define BRIGHTNESS  128     // Brightness (0-255)
```

## Upload Instructions

1. Connect ESP32-C3 to computer via USB
2. Select correct **Port** in Arduino IDE (Tools → Port)
3. Select **ESP32C3 Dev Module** as board
4. Click **Upload** button
5. Wait for "Done uploading" message

## Functions Available

- `setAllRed()` - Set all LEDs to solid red
- `blinkRed(delayMs)` - Blink all LEDs red
- `setStripBrightness(brightness)` - Change brightness (0-255)
- `redGradient()` - Gradient from dark to bright red
- `redChase(wait)` - Chase animation with red LEDs

## Troubleshooting

### LEDs not lighting up
- Check wiring (Data, VCC, GND)
- Verify correct GPIO pin in code
- Ensure adequate power supply (5V, sufficient current)

### Flickering or wrong colors
- Add a 470Ω resistor between GPIO and LED data pin
- Add a 1000µF capacitor across LED strip power
- Try using a level shifter if strip requires 5V logic

### Upload fails
- Hold BOOT button while clicking Upload
- Release BOOT after "Connecting..." appears
- Try different USB cable or port

## License

MIT License - Feel free to use and modify!

---

*Created by Friday* 🤖
