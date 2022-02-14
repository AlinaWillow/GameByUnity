### **InventoryUI**

1. Create > UI > Canvas > Rename : HUD
> Reference resolution : x=1920 ,y=1080 
2. [RC] HUD > Panel >Rename: Inventory

> alignment bottom
> w=910 , H=100
3. [RC] Inventory > UI > Image > Rename : Slot
> aligement left middle
> w=80, H=80
4. [RC] Slot > UI > Image > Rename : Border
> w=80 , H= 80
5. [RC] Border > UI > Image > ItemImage
> W=80 ,H=80
> Convert image of Item to : Sprite(2D and UI)
> put image into Source image : _________
> ปรับ size
6. Border > Add component : Button
> Highlight color : _______ (Blue?)
7. Inventory > Add component : horizontal Layout group
> Child Aligement : Middle center
> Child force : ติ๊ก Width , ติ๊ก Height
8. Dupicate Slot!

**Youtube** : https://www.youtube.com/watch?v=-xB4xEmGtCY
