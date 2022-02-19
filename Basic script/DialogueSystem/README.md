Dialogue
Youtube : https://www.youtube.com/watch?v=_nRzoTzeyxU

Show hide panel
Toutube : https://www.youtube.com/watch?v=e0feEWLRSYI

That's great! But if you need diferent characters talking... I supose that we need to do  transform the variable "Dialogue" (from DialogueTrigger script) in a Array (like this "Dialogue [ ]" ).
But... How can we do for Start the next Dialogue? I supose we must create a function in DialogueManager script, but I don't know what to do... :'(


- Leandro Libarona
4 ปีที่แล้ว (แก้ไขแล้ว)
Great as always! maybe a choice system (with a node editor) could be nice!!
I was thinking something along the lines of the following structure:

Dialogue:{
Character {Name,  picture, tone}
Text
Choices[{name, () => enabled? , Dialogue, () => effect}]
}

If Choices is null or empty, then it means it's the end of conversation.
If there is only one choice, then it works similar to the list you use in your system.

enabled -> boolean function meant to check conditions by which you can access this part of conversation (quest completed? enough lv? etc)
effect -> void function which makes it possible for the Dialogue choice to affect the game world (for example () => character.evil++)

picture -> for example, face of the talking character.
tone -> could be an enum, which sets the style of the text

- Ziying Tan
2 ปีที่แล้ว
For those who want to trigger the dialogue when you open the scene, use Awake(). Here are the details how to do that (million thanks to @Foggzie) https://stackoverflow.com/questions/54481993/brackeys-dialogue-without-start-buttonunity/59224401#59224401 Check your order of Start() and Awake() method, and make sure if you change the name of scripts, do the same to <>tag. 
Again, thank you Brackeys for this brilliant tutorial!

- You can make it with a Trigger! You need an emty Game Object with a Box Collider 2D and make sure, the "is Trigger" checkbox is checked! Then you place this object wherever you want! It's important that your player have a tag, for example: "Player". And in your script, you write:

void OnTriggerEnter2D(Collider2D other)
    {
        if (other.tag == "Player")
        {
            FindObjectOfType<DialogueManager>().StartDialogue(dialogue);
        }
    }

Place the "Dialogue Trigger" script to the empty Game Object with the Collider! ;)
  
  - It's possible to use OnSceneLoaded() which gets called before Start(), when it's hooked onto the SceneManager.sceneLoaded delegate. More/better details in the docs: https://docs.unity3d.com/ScriptReference/SceneManagement.SceneManager-sceneLoaded.html. As RPGtogether said below, you can use Start(), which is probably easier, unless you have some specific need to run code before that. 

Also, I'd consider timing as experienced from the user perspective. Maybe give them a couple seconds in the scene, or set the context with an image/cutscene animation first. Depends largely on what you're wanting to accomplish though.
  
  - I had issues with implementing this code for multiple NPCs. I would get a NullReferenceExeption and only one NPC  at a time would show the text. What I did to solve that issue, was create a public DialogueManager dialogeManager and then assign the dialogManager like this in the code:
dialogeManager.StartDialogue(dialogue); in the TriggerDialogue() function.
In the Inspector I would drag the DialogManager in the DialogTrigger Script panel.
In case anybody runs agains that issue, too.
  
 
