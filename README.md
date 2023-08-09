# BroAudio Readme

# Library Setup

1. **Open LibraryManager window**
    
    ![1_LibraryManagerWindow.png](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/1_LibraryManagerWindow.png)
    
2. **Create a library**
click [+] to create a Library 
    
    ![2_CreateLibrary.png](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/2_CreateLibrary.png)
    
3. Choose an AudioType
    
    ![3_ChooseAudioType.png](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/3_ChooseAudioType.png)
    
    - Music
    - UI
    - Ambience
    - SFX
    - VoiceOver
4. **Type a name for this new library**
The name will be its enum name . So it has to follow the c# naming rules.
**Click [OK] to create the library, It will generate a Scriptable Object asset in LibraryPath** 
    
    ![4_Type a name.png](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/4_Type_a_name.png)
    
5. **Add audio set to the Sets list and name it welln**
Every library has a list of sets where they can store a bunch of audio set
an audio set represent a kind of sound , music or voice which can be play(call) via enum
ex. Play(Cat.Meow)   ⇒ play the sound in the [Meow] audio set with its setting 
    
    ![5_Add a Set.png](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/5_Add_a_Set.png)
    
    ![6_Many Set in the list.PNG](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/6_Many_Set_in_the_list.png)
    
6. **Add one clip for single sound trigger ,or add multiple clips to have more variety** 
(more details in below)
    
    ![7_AddClip.PNG](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/7_AddClip.png)
    
7. **Click [Update] , and let Bro take care for you !
If there is a new AudioSet hasn’t updated to the system . The [Update] button will show and you need to press it ! otherwise , it can’t be used.**

What the update button will do under the hood :
It will use [Name] field’s string as the value of current library’s enum ,and also generate an ID.
8. **Add clips and set any values as you need !**

# AudioSet’s Properties Setup

![7_MultiClips.PNG](BroAudio%20Readme%209313b0d4dd9347e58d3fe3aee15e3a60/7_MultiClips.png)

### BaseProperties

1. **Name** : name of the sound , and also the Enum value.
2. **Delay**(Sound,UI,VoiceOver only) : plays audio with a delay specified in seconds.
3. **Loop**(Music,Ambience only) : tick to enable looping.
4. **Clips :** list of clips 
if there is only one single clip , it will always play that clip (obviously...)
but if there is more than one , PlayMode option will show up!
then each time you play ,a different clip will be picked by the mode as follow  
- Sequence Mode
clip will be picked by index.
- Random Mode
clip will be picked randomly. 
You can set weight to control the probability , or keep all in zero to pick equally.

### ClipProperties

According to the clip you selected in the clips list

1. **ClipName**(in green) : let you know which clip is currently selected .
2. **Volume** : the volume that the clip will be played.
3. **Playback Position** : defines the clip’s Start and End position in seconds.
4. **Fade :** defines how long it will take to arrive at maximum volume after it starts, and how long it will take to arrive at minimum volume before it ends.
5. **Preview** (foldable option) : It shows the clip’s waveform ,visualizes playback position and Fade In/Out . Not to mention the most important function : Play and Stop button as audible preview.