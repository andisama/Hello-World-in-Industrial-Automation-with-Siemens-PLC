"HELLO WORLD" in Industrial Automation, Towards Industry 4.0

Hardware
- Power Supply: 
  * 1x Siemens PSU (In: 220VAC, Out: 24VDC)
- CPU:
  * 1x Siemens Compact PLC 1200 DC/DC/DC
- Input: 
  * 1x Start Push Button(NO) %I0.1
  * 1x STOP Push Button (NC) %I0.0
- Output:
  * 5x 24VDC Lamps %Q0.0, %Q0.4, %Q0.5, %Q0.6, %Q0.7
  * 1x 24VDC Buzzer with Lamp %Q1.1
- Cabling: AWG 16 with ferrules

Connectivity
- PC to PLC: RJ45, Straight cable wiring
  as Siemens 1200 PLC has the capability to autocross on the ethernet cable

Software
- Siemens TIA Portal v17 on Windows 11

Programming
- Ladder Diagram (LD) with Function Block (FB)
- Utilize Realtime Clock (RTC)
  * enable (devices & network -> system & clock memory -> enable the use of clock memory byte
  * download to PLC (hardware configuration)
- Start Push Button (NO) ON -> Enabling Timer -> Passing Clock signal 1 Hz -> Lamps are energized (activated)
- Stop Push Button (NC) ON -> Disabling Timer -> Blocking Clock signal 1 Hz -> Lamps are de-energized (deactivated)
  * Note that Stop Push Button is NO in the program, but NC in the hardware wiring
- Utilize counter, compare instruction and memory bit
  While the Clock signal is passed to the counter
  * Every 15 seconds, the buzzer is energized for 1 second




