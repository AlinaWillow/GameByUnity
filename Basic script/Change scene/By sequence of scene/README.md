### **Change scene by sequence**

เป็นการเปลี่ยนจากลำดับการวาง scene 
เหมาะกับการเปลี่ยน scene แบบ level 1,2,...

ไป scene ถัดไป
1. Create > 3D object > Cube > Rename: DoorNext

> Box collider > ติ๊ก Is Trigger

2. Add C# script : NextScene

ไป scene ก่อนหน้า
3. Create > 3D object > Cube > Rename: DoorPrev
> Box collider > ติ๊ก Is Trigger
4. Add C# script : PrevScene

5.File > Build setting > Add open scene > เลือก scene อันแรก (0),(1),(2).....
6. Put DoorNext และ DoorPrev into folder Prefab (เพื่อให้เรียกใช้ได้หลายฉาก)
7. ซ่อนกล่อง: ติ๊กออกจาก Mesh Renderer

Youtube: https://www.youtube.com/watch?v=_sDXZcvDXCU
