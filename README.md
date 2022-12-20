"HELLO WORLD" in Industrial Automation, Towards Industry 4.0

Hardware
- Power Supply: 1x Siemens PSU (In: 220VAC, Out: 24VDC)
- CPU: 1x Siemens PLC 1200 DC/DC/DC
- Input: 1x Start Push Button(NO), 1x STOP Push Button (NC)
- Output: 5x 24VDC Lamp, 1x 24VDC Buzzer with Lamp
- Cabling: All AWG 16 

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
- Utilize counter, compare instruction and memory bit
  Set a specific time (every 15 seconds) to energize the buzzer for 1 second




