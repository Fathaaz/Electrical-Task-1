# Electrical-Task-1
## ELectrical Remote Control Diagram
### Electrical Diagram
![ERC Electrical DIagram drawio](https://github.com/user-attachments/assets/433cfb13-507a-4e3e-a6d1-05902e83d572)
### Communication Diagram
![ERC Communication DIagram drawio](https://github.com/user-attachments/assets/0e14e198-1859-407f-acb7-bf3df2223aa5)

1. Battery: Sumber daya utama yang menyediakan energi untuk seluruh sistem.

2. Emergency Button : Memungkinkan pemutusan daya dalam keadaan darurat untuk mematikan seluruh sistem dengan cepat. Terhubung langsung ke baterai dengan menerima input dari STM32.

3. UBEC: Mengatur tegangan dari baterai dan mengirimkannya ke servo. Menerima daya dari baterai dan menyuplai tegangan stabil ke servo.

4. Servo: Mengendalikan arah kapal.Menerima tegangan dari UBEC dan sinyal kontrol dari microcontroller.

5. Buck Converter: Mengubah tegangan agar sesuai dengan receiver.

6. Receiver: Menerima sinyal kontrol dari Transmitter dan mengirimkannya ke mikrokontroler (STM32).

7. Buck Boost Converter: Mengatur tegangan dari baterai ke level yang sesuai untuk STM32.

8. STM32 : Memproses sinyal dari receiver dan mengirim perintah kontrol ke komponen lain seperti servo, ESC, dan emergency button.

9. ESC : Mengontrol kecepatan dan arah putaran thruster berdasarkan sinyal dari STM32 (dapat diprogram).
Menerima daya langsung dari baterai dan sinyal kontrol dari STM32 kemudian mengirimnya ke thruster.

10. Thruster: Motor pendorong yang menggerakkan kapal.

11. Cooling System: Sistem pendingin yang menjaga suhu komponen tetap stabil selama operasi.
Mecakup thermistor dan fan serta dapat juga water cooling yang terhubung ke STM32 kemudian tersambung dengan ESC.

12. Transmitter: Pemberi sinyal kontrol kepada receiver. Dalam hal ini Transmitternya adalah remote control.

## Fuel Engine Remote Control Diagram
### Electrical Diagram
![FERC Electrical Diagram drawio](https://github.com/user-attachments/assets/6e45734b-9e71-4c4e-80f1-aff560ab3e63)
### Communication Diagram
![FERC Communication DIagram drawio](https://github.com/user-attachments/assets/d8974c97-9d6c-440a-847b-9740d89abc3b)

1. Throttle: Mengatur jumlah bahan bakar yang masuk ke mesin untuk mengontrol kecepatan dan tenaga yang dihasilkan. Throttle dikenadilkan melalui STM32.

2. Fuel Tank: Menyimpan bahan bakar yang akan digunakan oleh mesin. Bahan bakar dari fuel tank bercampur dengan oil tank yang akan mengalir ke engine.

3. Oil Tank: Menyimpan oli yang dicampurkan dengan bahan bakar untuk pelumasan mesin, dan pembakaran itu sendiri.

4. Fuel Engine : Membakar campuran bahan bakar dan oli untuk menghasilkan tenaga mekanis. Campuran bahan bakar dan oli dibakar di dalam mesin, menghasilkan tenaga mekanis yang digunakan untuk alternator.

5. Exhaust: Mengeluarkan gas buang hasil pembakaran dari mesin.

6. Alternator: Mengubah tenaga mekanis dari mesin menjadi listrik. Menghasilkan listrik dalam bentuk arus AC.

7. Rectifier: Mengubah arus AC dari alternator menjadi arus DC.

8. Buck-Boost Converter: Mengatur tegangan arus DC yang dihasilkan oleh rectifier agar sesuai dengan kebutuhan baterai.

9. Battery: Menyimpan energi listrik yang dihasilkan oleh alternator dan diatur oleh buck-boost converter kemudian mengirim daya ke seluruh sistem

10. Emergency Button : Memungkinkan pemutusan daya dalam keadaan darurat untuk mematikan seluruh sistem dengan cepat. Terhubung langsung ke baterai dengan menerima input dari STM32

11. UBEC: Mengatur tegangan dari baterai dan mengirimkannya ke servo. Menerima daya dari baterai dan menyuplai tegangan stabil ke rudder. Menerima sinyal dari STM32

12. Buck Converter: Mengubah tegangan agar sesuai dengan receiver.

13. Receiver: Menerima sinyal kontrol dari Transmitter dan mengirimkannya ke mikrokontroler (STM32).

14. Buck Boost Converter: Mengatur tegangan dari baterai ke level yang sesuai untuk STM32.

15. STM32 : Memproses sinyal dari receiver dan mengirim perintah kontrol ke komponen lain seperti throttle, cooling system, esc, dan servo.

16. ESC : Mengontrol kecepatan dan arah putaran thruster berdasarkan sinyal dari STM32 (dapat diprogram).
Menerima daya langsung dari baterai dan sinyal kontrol dari STM32 kemudian mengirimnya ke thruster.

17. Thruster: Motor pendorong yang menggerakkan kapal.

18. Cooling System: Sistem pendingin yang menjaga suhu komponen tetap stabil selama operasi.
Mecakup thermistor dan fan serta dapat juga water cooling yang terhubung ke STM32 kemudian tersambung dengan ESC.

19. Transmitter: Pemberi sinyal kontrol kepada receiver. Dalam hal ini Transmitternya adalah remote control.
