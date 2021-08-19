# วิธีการ Setup และ Run Program
## ติดตั้ง Visual Studio Code
### ติดตั้ง Extensions 
* Dart
* Flutter
## ติดตั้ง Emulator
* Genymotion
### Run Program
* Run Emulator
* เปิด Terminal และใช้คำสั่ง flutter run เพื่อ Run Program
## วิธีออกแบบโปรแกรม
มีการออกแบบ UI ไว้ 3 หน้า
* หน้าแรกจะเป็นหน้าหลักเพื่อรับขนาดของเกมส์ Tic Tac Toe 
* หน้าที่สองเป็นหน้าของเกมส์ที่มีขนาดของ Row และ Column เท่ากับค่าที่รับเข้ามา
* หน้าที่สามเป็นหน้าเก็บประวัติคนที่ชนะ
## Algorithm ที่ใช้
กำหนดให้ matrix = List Array 2D, n = จำนวนที่รับเข้ามา ,win = n ,col = 0, row = 0, ii = 0, rii = 0 , x และ y คือค่า
สร้าง matrix โดยมีขนาด Row และ Column = จำนวนที่รับค่าเข้ามา แล้วทำการ set ค่า = ' '  <br>
ตัวอย่างของ matrix ที่มีขนาด n = 3

| | | |
|-|-|-|
| | | |
| | | |

Player ทำการเลือกตำแหน่งที่ x,y เช่น 0,0 
ถ้า ในตำแหน่งที่ x,y มีค่า ='' จะมีเงื่อนไขเช็คดังนี้<br>
ถ้า lastMove == X ให้ newValue = O แล้วให้ lastMove = newValue และในตำแหน่งที่ x,y = newValue <br>
ถ้า lastMove != X ให้ newValue = X แล้วให้ lastMove = newValue และในตำแหน่งที่ x,y = newValue <br>

ถ้า มีการส่งค่า x และ y ให้วนลูปเพื่อทำการเก็บค่า X หรือ O ลงใน matrix ในตำแหน่งที่ x,y โดยลูปจะทำไปเรื่อยๆโดยเริ่มตั้งแต่ 0 แต่น้อยกว่า n <br>
* ถ้า column ใดใน matrix ในตำแหน่งที่ x,i มีการเก็บค่า X หรือ O ที่มีค่าเดียวกันอย่างใดอย่างนึงเท่านั้นจึงจะทำการเก็บค่า col+1
* ถ้า row ใดใน matrix ในตำแหน่งที่ i,y มีการเก็บค่า X หรือ O ที่มีค่าเดียวกันอย่างใดอย่างนึงเท่านั้นจึงจะทำการเก็บค่า row+1
* ถ้า แนวทแยง matrix ในตำแหน่งที่ i,i มีการเก็บค่า X หรือ O ที่มีค่าเดียวกันอย่างใดอย่างนึงเท่านั้นจึงจะทำการเก็บค่า ii+1
* ถ้า แนวทแยง matrix ในตำแหน่งที่ x,n-i-1 มีการเก็บค่า X หรือ O ที่มีค่าเดียวกันอย่างใดอย่างนึงเท่านั้นจึงจะทำการเก็บค่า rii+1

เงื่อนไขเช็คผู้ชนะ ถ้า Player X หรือ O มีจำนวนนับของ col หรือ row หรือ ii หรือ rii มีค่า = ค่าที่รับเข้ามาก่อน Player คนนั้นจะเป็นผู้ชนะ แล้วทำการบันทึกข้อมูล Player ที่ชนะลงฐานข้อมูล<br>  

แล้วถ้า matrix ไม่มีค่าใด ='' ให้เพิ่ม Draw ลงให้ฐานข้อมูล และแสดงผลเป็น Draw <br>






