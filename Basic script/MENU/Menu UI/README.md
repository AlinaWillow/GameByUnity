### **MENU UI**
1.Create > UI > Panel > Rename: Background
2. Choose image

> Texture typr : Sprite (2D&UI)

3. Camera > UI > Text
4. Import package : TextMeshPro
5. [RC] Canvas > UI > TextMeshPro > Rename : PLAY

> Font size : _______
> Align center
> Font Asset : ______
> Underlay : _______(create shadow)
> ติ๊ก Coloer Gradient
6. Create > TextMeshPro > ColorGradient > Rename : Gold ------>> (Add color)
7. Drag Gold into TextMeshPro > Gradient(Present) : ________
8. [RC] Canvas > UI > Button >Rename : PayButton
> Color 
> ไม่ติ๊ก Image(Script)
> delete text under button
> replace play under button > Rename : Text
> Hold down all Click (Center)
> ติ๊ก Image --->> Change color
9. Duplicate and Rename othe button

**Youtube** : https://www.youtube.com/watch?v=zc8ac_qUXQY&list=RDCMUCYbK_tjZ2OrIZFBvU6CCMiA&start_radio=1
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
### **สร้าง Main MENU**
1. [RC] Canvas > create empty > Rename : MainMenu
2. Drag All (Play Button ,Option Button , Quit Button) to MainMenu
3. Duplicate MainMenu > Rename : Option Menu
> จัดเรียงให้เหลือแต่ Text Option
4. [RC] OptionMenu > UI > Slider > Handle slide area > Handle > ไม่ติ๊ก Image
5. MainMenu > Add c# script : MainMenu
6. PlayButton > On Click() > (+) > ไม่ติ๊ก_________(MainMenu) > function : PlayGame()
7. QuitButton > OnClick() > (+) > ไม่ติ๊ก_________(MainMenu) > Function : QuitGame()
>  ติ๊ก__________(OptionMune) > Function : GameObject
> ไม่ติ๊ก________(MainMenu) ---->> Set Active (bond)
8. BackButton > OnClick() > (+) > ติ๊ก ________(MainMenu) > ---->> Set Active(bond)
> ไม่ติ๊ก _______(OptionMenu)
