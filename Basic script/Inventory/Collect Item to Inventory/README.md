### **Collet item to UI inventory**
ทำให้เก็บไอเท็มใส่ในช่องเก็บไอเท็มได้

1. Create C# script IInventoryItem
2. [C] Inventory > Add c# script : Inventory
3. [C] FPS > PlayerMovement > Inventory:____________<Inventory(obj)>
4. [C] Axe (your item!) > Add c# script: Axe > put Image:__________ 
> Don't forget to change your image into Sprite (2D & UI)
> add component : Box collider 
5. [C] HUD > Add c# script: HUD > Inventory:________<Inventory(obj)>
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
### **Character**
ใน PlayerMovement ให้เพิ่ม
` public Inventory inventory;`

ใน void update()
{
    `private void OnControllerColliderHit(ControllerColliderHit hit)
        {
            IInventoryItem item = hit.collider.GetComponent<IInventoryItem>();
            if(item != null)
            {
                inventory.AddItem(item);
            }
        }`
}



**Youtube** : https://www.youtube.com/watch?v=Hj7AZkyojdo&list=PLOyj0nn-asmaqBZ_hGoCh-PBlraNaHLyA&index=3

-----------------------------------------------------------------------------------
### **Problem**

- HELLO EVERYONE!
If you're still having issues with your items not showing up in your hotbar even though you followed all the steps outlined in the comments:
> MAKE SHURE THAT YOUR ItemImage IN UNITY IS DISABLED!!!
> If the little box next to 'Image' is ticked, the HUD script wont be able to replace it with your actual ItemImage.

- i got all the scripts to be in their perfect spots,but whenever i collide with the item,the item disappears but it doesn't show the image on the ui inventory panel...

> Transform inventoryPanel = transform.Find("Inventory");    // Inventory is a child of HUD
