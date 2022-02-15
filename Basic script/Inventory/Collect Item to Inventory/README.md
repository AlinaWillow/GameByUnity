ใน PlayerController ให้เพิ่ม
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
