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
