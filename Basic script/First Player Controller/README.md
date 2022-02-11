### **FPS (First person player)**

1. Create > Create empty > Rename: First person player
2. Add component > Character controller
3. Hit "F" , turn on "Gizmoz"
4. Set Radius=0.6 ,Height=3.8
5. Right click on First person player > Create 3D object > cylinder
6. Cylinder: Scale x=1.2 , y=1.8 , z=1.2
7. Remove capsule collider

Camera controll
8. Camera: Add C# script : MouseLook
>  _put Player body : FPS_
 Keyboard controll
9. FPS : Add C# script : PlayerMovement
>controller : FPS
>Stept offset =0.7
10.  Right click on First person player > Create empty >Rename: GroundCheck
>Move it to lower of FPS
11. FPS > Player movement 
>Ground Check: GroundCheck
>Ground Mask: Ground (you need to add Ground layer first)

Youtube: https://www.youtube.com/watch?v=_QajrabyTJc
___________________________________________________________________________________

**Problem**
- I cant't "Jump"... 
**แก้โดย** 

> if(Input.GetButtonDown("Jump"))

แต่มีปัญหาคือกระโดดกลางอากาศได้
