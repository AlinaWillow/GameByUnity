 - Make a "multi-person" dialogue system
  - In case anyone is still looking, I made an adaptation to the script so it fits two or more people in the conversation: https://repl.it/@Felipe_ThiagoTh/BrackeysDialogueUpdate
  - @Felipe Costa  I see yours and raise you one: https://repl.it/repls/KnowingLawfulGravity (I'm too lazy to create an account so I just left an anonymous repl). I tried to keep the initial classes as designed, keep the original Dialogue class but modified, use DialogueTrigger for the conversations, and access it from DialogueManager.+++
- @Felipe Costa  I see yours and raise you one: https://repl.it/repls/KnowingLawfulGravity (I'm too lazy to create an account so I just left an anonymous repl). I tried to keep the initial classes as designed, keep the original Dialogue class but modified, use DialogueTrigger for the conversations, and access it from DialogueManager.
- @Useless  It's not only the script, somehow the object in Unity is connected to the script. They work in unison. To see exactly where the problem is, try to debug it. Print a message with your conversations size ( Debug.Log("conversations size: " + conversations.Length) ) and at every step and see where things go wrong. I've changed the dialogue a lot since I started. I'm using ScriptableObject(s) now. The error suggests you are trying to access an element in the array although it doesn't have the size of the requested index. Something like: conversations has length 3 and you try to get conversations[3]  (the three elements being at indexes 0,1 and 2).

- Actually I've found the best way to do it
Just make dialogs array in the trigger
And make queue of dialogs in manager, not phrases
Fix some errors
And that should do it :)
You should make Dialog class like class with one phrase (not array) and one name
- Nvm i fixed it, i was using FindObjectOfType to find the trigger now i’m using collision.gameObject.GetComponent and it works, also you can but sounds in the foreach statement and i makes a sound every time they talk and also the speed they talk, i controll this using strings
