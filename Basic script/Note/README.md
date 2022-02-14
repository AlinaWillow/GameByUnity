การใส่ aniamtion ตัวละคร
### **PROBLEM**
1. It all went fine till animation part, in preview and solo they run fine, but in blend tree, 
idle works, but walk and run get stuck in a single frame after half of the animation is played,
 it goes back to idle when button is no longer pressed.

-Even when previewing blend tree in preview it works as intended, its just ingame it doesn't

**Solution** Fixed it by setting both walk and cycle to loop pose.
