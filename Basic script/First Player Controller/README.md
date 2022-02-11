- But I cant't "Jump"... 

**แก้โดย** 
if(Input.GetButtonDown("Jump"))
        {
            velocity.y = Mathf.Sqrt(jumpHeight * -2f * gravity);
        }
แต่มีปัญหาคือกระโดดกลางอากาศได้
