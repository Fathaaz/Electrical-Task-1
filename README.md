# Electrical-Task

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Fatharanni Faza   | ELC | Electrical Design |

## ELectrical Remote Control Diagram
### Electrical Diagram
![ELc drawio](https://github.com/user-attachments/assets/88c3058d-a142-4aeb-99b8-889ba25249a0)
### Communication Diagram
![Commu  drawio](https://github.com/user-attachments/assets/7052c500-6b4e-4505-b896-3969f69fbddd)

1. Battery: Sumber daya utama yang menyediakan energi untuk seluruh sistem.

2. Emergency Button : Memungkinkan pemutusan daya dalam keadaan darurat untuk mematikan seluruh sistem dengan cepat. Terhubung langsung ke baterai dengan menerima input dari STM32.

3. UBEC: Mengatur tegangan dari baterai dan mengirimkannya ke servo. Menerima daya dari baterai dan menyuplai tegangan stabil ke servo.

4. Servo: Mengendalikan arah kapal.Menerima tegangan dari UBEC dan sinyal kontrol dari microcontroller.

5. Buck Converter: Mengubah tegangan agar sesuai dengan receiver.

6. Receiver: Menerima sinyal kontrol dari Transmitter dan mengirimkannya ke STM32.

7. Buck Boost Converter: Mengatur tegangan dari baterai ke level yang sesuai untuk STM32.

8. STM32 : Memproses sinyal dari receiver dan mengirim perintah kontrol ke komponen lain seperti servo, ESC, dan emergency button.

9. ESC : Mengontrol kecepatan dan arah putaran thruster berdasarkan sinyal dari STM32 (dapat diprogram).
Menerima daya langsung dari baterai dan sinyal kontrol dari STM32 kemudian mengirimnya ke thruster.

10. Thruster: Motor pendorong yang menggerakkan kapal.

11. Cooling System: Sistem pendingin yang menjaga suhu komponen tetap stabil selama operasi.
Mencakup thermistor dan fan serta dapat juga water cooling yang terhubung ke STM32 kemudian tersambung dengan ESC.

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

13. Receiver: Menerima sinyal kontrol dari Transmitter dan mengirimkannya ke STM32.

14. Buck Boost Converter: Mengatur tegangan dari baterai ke level yang sesuai untuk STM32.

15. STM32 : Memproses sinyal dari receiver dan mengirim perintah kontrol ke komponen lain seperti throttle, cooling system, esc, dan servo.

16. ESC : Mengontrol kecepatan dan arah putaran thruster berdasarkan sinyal dari STM32 (dapat diprogram).
Menerima daya langsung dari baterai dan sinyal kontrol dari STM32 kemudian mengirimnya ke thruster.

17. Thruster: Motor pendorong yang menggerakkan kapal.

18. Cooling System: Sistem pendingin yang menjaga suhu komponen tetap stabil selama operasi.
Mencakup thermistor dan fan serta dapat juga water cooling yang terhubung ke STM32 kemudian tersambung dengan ESC dan engine.

19. Transmitter: Pemberi sinyal kontrol kepada receiver. Dalam hal ini Transmitternya adalah remote control.

## Boost Converter

![Screenshot 2024-11-29 070122](https://github.com/user-attachments/assets/4db406d0-5111-4935-b6f7-76c7493914bb)


Schematics diatas adalah schematics untuk boost converter. Boost converter digunakan untuk menaikkan tegangan, dimana output akan lebih besar daripada input. Dalam boost converter ini terdapat induktor untuk menyimpan energi ketika ic aktif dan akan melepaskannya ketika saklar pada ic tidak aktif. Capacitor digunakan untuk menyaring tegangan pada input dan output. Dioda digunakan untuk memastikan arus menuju output. Dalam boost converter ini digunakan IC LM2577. Di bawah ini adalah desain pcb beserta keterangan DRCnya.

![Screenshot 2024-11-29 221930](https://github.com/user-attachments/assets/144b84ff-9b56-43cd-b28f-f10e0fbcf68b)

![Screenshot 2024-11-29 213030](https://github.com/user-attachments/assets/ebe58e81-92db-4882-96d7-4328da8bb599)

Kemudian berikut ini adalah gambaran 3dnya.

![Screenshot 2024-11-29 221956](https://github.com/user-attachments/assets/fac39326-c1e0-4d4d-b480-1f2909e7e878)



