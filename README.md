# Electrical-Task-1
## ELectrical Remote Control Diagram
### Electrical Diagram
![ERC Electrical DIagram drawio](https://github.com/user-attachments/assets/433cfb13-507a-4e3e-a6d1-05902e83d572)
### Communication Diagram
![ERC Communication DIagram drawio](https://github.com/user-attachments/assets/0e14e198-1859-407f-acb7-bf3df2223aa5)
```
1. Battery: Sumber daya utama yang menyediakan energi untuk seluruh sistem.

2. Emergency Button (Tombol Darurat): Memungkinkan pemutusan daya dalam keadaan darurat untuk mematikan seluruh sistem dengan cepat.
Koneksi: Terhubung langsung ke baterai.

3. UBEC (Universal Battery Elimination Circuit): Mengatur tegangan dari baterai dan mengirimkannya ke servo.
Koneksi: Menerima daya dari baterai dan menyuplai tegangan stabil ke servo.

4. Servo: Mengendalikan arah kapal.
Koneksi: Menerima tegangan dari UBEC dan sinyal kontrol dari microcontroller.

5. Buck Converter: Mengubah tegangan agar sesuai dengan receiver.

6. Receiver: Menerima sinyal kontrol dari Transmitter dan mengirimkannya ke mikrokontroler (STM32).

7. Buck Boost Converter: Mengatur tegangan dari baterai ke level yang sesuai untuk STM32.

8. STM32 (Mikrokontroler): Memproses sinyal dari receiver dan mengirim perintah kontrol ke komponen lain seperti servo dan ESC.

9. ESC (Electronic Speed Controller): Mengontrol kecepatan dan arah putaran thruster berdasarkan sinyal dari STM32 (dapat diprogram).
Koneksi: Menerima daya langsung dari baterai dan sinyal kontrol dari STM32 kemudian mengirimnya ke thruster

10. Thruster: Motor pendorong yang menggerakkan kapal.

11. Cooling System: Sistem pendingin yang menjaga suhu komponen tetap stabil selama operasi.
Mecakup thermistor dan fan serta dapat juga water cooling yang terhubung ke STM32 kemudian tersambung dengan ESC.

12. Transmitter: Pemberi sinyal kontrol kepada receiver. Dalam hal ini Transmitternya adalah remote control
