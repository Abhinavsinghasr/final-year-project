⚙️ Auto Calibration Instructions

The system includes a built-in automatic calibration feature that adjusts the voltage and current calibration values to improve measurement accuracy.
Calibration is triggered using the CAL button connected to GPIO 4.

📌 When to Perform Calibration

Run calibration in the following cases:

♦ First time using the device
♦ After changing sensors or hardware
♦ If measured voltage/current is inaccurate
♦ After resetting EEPROM

🔧 Requirements Before Calibration

Before starting calibration, ensure the following:

♦ The energy meter is powered ON
♦ WiFi connection is optional but recommended
♦ A known voltage source (≈230V AC) is connected
♦ A known load (lamp, heater, etc.) is connected to draw measurable power
♦ Sensors are properly connected

Example load:

60W bulb
100W bulb
500W heater

Using a stable load improves calibration accuracy.

▶️ How to Start Auto Calibration

Follow these steps:

At first, change the voltage value in source code line number 196 and know power value in line number 197. After it has done, then:

1️⃣ Power ON the energy meter.
2️⃣ Wait until the system finishes startup.
3️⃣ Press and hold the CAL button for 3 seconds.
4️⃣ The LCD will display:

Calibrating...

5️⃣ The device will automatically measure voltage and power multiple times.
6️⃣ The system calculates new calibration values for:

Voltage calibration
Current calibration

7️⃣ The new values are stored in EEPROM.
8️⃣ The LCD will show:

System
Calibrated

Calibration is now complete.

📊 What Happens During Calibration

The system performs the following steps automatically:

Reads voltage and power 10 times
Calculates the average voltage
Calculates the average power
Adjusts calibration factors
Saves calibration values to EEPROM
Updates the measurement system

This ensures more accurate readings over time.

⚠️ Important Notes

♦ Do not press the button repeatedly during calibration
♦ Ensure the load remains stable during calibration
♦ Avoid calibrating with very small loads (<10W)
♦ Calibration only takes a few seconds

💡 Calibration Tips (For Best Accuracy)

For best results:

✔ Use a 60W–100W bulb
✔ Ensure stable mains voltage
✔ Avoid running heavy appliances during calibration

🔁 Recalibration

You can recalibrate anytime by simply:
Hold CAL button for 3 seconds

The system will automatically update the calibration again.
