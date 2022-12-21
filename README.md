"HELLO WORLD" in Industrial Automation, Towards Industry 4.0

Hardware
- Power Supply: 
  * 1x External Siemens PSU (In: 220VAC 1 Phase, Out: 24VDC)
- CPU:
  * 1x Siemens Compact PLC 1200 DC/DC/DC
- Digital Input: 
  * 1x Start Push Button(NO) %I0.1
  * 1x STOP Push Button (NC) %I0.0
- Digital Output:
  * 5x 24VDC Lamps %Q0.0, %Q0.4, %Q0.5, %Q0.6, %Q0.7
  * 1x 24VDC Buzzer with Lamp %Q1.1
- Cabling:
  * AWG 16 with ferrules
- PLC Firmware level:
  * 4.6.0

Hardware Configuration change
- Utilize Realtime Clock (RTC)
  * enable (devices & network -> system & clock memory -> enable the use of clock memory byte
  * download to PLC (hardware configuration)

Connectivity
- Laptop to PLC:
  * RJ45
  * straight cable wiring as Siemens 1200 PLC has the capability to autocross on the ethernet cable

Application Software
- Siemens TIA Portal v17 on Windows 11

PLC Programming
- Ladder Diagram (LD) with Function Block (FB)
- Programming logic
  * If Start Push Button (NO) pressed -> Enabling Counter -> Passing Clock signal 1 Hz -> Lamps are energized (activated)
  * If Stop Push Button (NC) pressed -> Disabling Counter -> Blocking Clock signal 1 Hz -> Lamps are de-energized (deactivated)
  * Note that Stop Push Button is NO in the program, but NC in the hardware wiring for safety 
  * Utilize the counter, and compare instruction and memory bit while the Clock signal is passed to the counter
  * Note that every 15 seconds, the buzzer is energized for 1 second




