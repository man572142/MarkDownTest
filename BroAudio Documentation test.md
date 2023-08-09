# BroAudio

[UnityAudio特性研究](https://www.notion.so/UnityAudio-f7ebdf654f5346c1b152bd201a9aeab6?pvs=21)

[InstructionText](https://www.notion.so/InstructionText-d79b983799874e43a8875a5d7fd4cfa7?pvs=21)

[API Documentation](https://www.notion.so/API-Documentation-073e4d3c5f2141f7b63fa01d8a9554da?pvs=21)

[MainFeatures](https://www.notion.so/MainFeatures-09505c83aaa2402780f4b8ed4ac4d039?pvs=21)

[使用情境](https://www.notion.so/08139a4cb4504294a70a69b7bbb57b4b?pvs=21)

[設計困境](https://www.notion.so/991772f7243e45619080d0e4368c44c6?pvs=21)

[改Exclusive為Effect專用軌](https://www.notion.so/Exclusive-Effect-6fc777db2b2d44fd939f715c0830ce83?pvs=21)

[Demo](https://www.notion.so/Demo-0909989a00c7414292195423b16d09aa?pvs=21)

**NameSpace**

- ***MiProduction***
    - ***BroAudio***
        
        SoundSystem
        
        AudioExtension
        
        - Core
            
            MusicPlayer
            
            SoundPlayer
            
            SoundManager
            
        - Library
            
            AudioLibraryAsset
            
            AudioLibraryAssetEditor
            
            MusicLibrary
            
            MusicLibraryAsset
            
            SoundLibrary
            
            SoundLibraryAsset
            
        - SceneMusic
            
            SceneMusicConfig
            
            SceneMusicConfigEditor
            
            SceneMusic
            
            SceneMusicTrigger
            
    - ***Extension***
        
        EnumGenerator
        

### UnityVersion

已知版本不能低於2019.1 (因****AdvancedDropdown****)
不能低於 2018.3 (因****SettingsService****)

[Unity Editor Icon](https://www.notion.so/Unity-Editor-Icon-8bb6df74c6314c89b178a8966504dca9?pvs=21)

[EditedClip問題](https://www.notion.so/EditedClip-ee26cf7cfddf4cfda08c7a83da56e466?pvs=21)

[AudioPlayer ObjectPool策略](https://www.notion.so/AudioPlayer-ObjectPool-6503ed67779046f8a847abcecad3d2d3?pvs=21)

[AudioID管理策略](https://www.notion.so/AudioID-823e779caa7745fd872d84d17bc13709?pvs=21)

## ToDoList

- [x]  Fading、StartPosition 數值限制
- [x]  Fading以整段Clip為總長
- [x]  Fading、StartPosition 壓黑色塊
- [x]  PropertyDrawer播放/停止鍵
- [x]  Fading 縮小FloatField
- [x]  PropertyDrawer縱軸當作音量
- [x]  尚未更新Enum警告、隱藏Enum
- [x]  PropertyDrawer補各自額外的參數 (Delay , Loop)
- [x]  核心停止播放機制
- [x]  核心效果器機制
- [x]  Enum複寫與加入
- [x]  音量控制
- [x]  Duck
- [x]  StandOut
- [x]  分解Enums
- [x]  防止破音?
- [x]  如果其中一個Asset換了EnumPath，其他的怎麼辦? 應該要把這類的設定獨立出來
- [x]  如果直接刪掉Asset，要怎麼刪除Json與Enum裡的舊資料? (目前只能透過把Asset中的資料清除，然後再按Update來清資料)
- [x]  如果Asset改名了，GUID也會變怎麼辦…
- [x]  音樂軌音量改用總音量而不要用A跟B
- [x]  Fold c定義定義
- [x]  Library資料同名警告
- [x]  Window化
- [x]  自訂Library及Enum名稱
- [x]  enumName Validation
- [x]  刪掉Asset後會自動清除相關資料，但是如果那個Enum已經沒資料了，檔案還是會在
- [x]  拆掉SceneConfig
- [x]  EditorGUI.ProgressBar?
- [x]  更新Path的設計 (現在有點醜) ，也許獨立拉到一個Window
- [x]  ClipEdting還沒實作
- [x]  Preview應該依照position的設定播放
- [x]  GlobalSetting已建立，但大部份的設定都還沒加入
- [x]  Enum改const? 那Inspector怎麼辦
Enum的缺點是一旦Library被刪除，有用到的地方都會Error
用const 也會一樣，~~但應該可以想到辦法克服?~~
好像也不用克服，這是必須的結果。假設沒有這樣的話，當Library被刪除，使用者可能在不知情的情況下持續使用該ID，雖然不至於系統Crash，但也因此不容易發現錯誤。
- [x]  MusicLibrary改成class有個好處是可以用as 來cast，比較安全
- [x]  更新效果器及Track的Routing Design
- [x]  重設計ClipVolume與TrackVolume ?
不！在Ableton裡面也是Clip與Track分開，如果Clip 只有0.5，而設定Track 0.5的話就會是0.5再0.5
不過這樣計算結果是否相同? 應該是ok
- [x]  設計Transition
- [x]  effect只有暫時切換，還需要一個可以trigger進出ExclusiveMode的方法
- [x]  用完effect後paraName是否要回復
- [x]  IAutoResetWaitable
- [x]  Dynamic Boost
- [x]  新增Loop自動CrossFade (**Seamless Loop**)
- [x]  PlayackReference可以改Struct並用ref的方式?? 不行，仍需要物件的特性
- [x]  注意**Seamless Loop 與MusicPlayer互動的關係**
- [x]  當使用SeamlessLoop時，讓FadeInOut被Disable，並且SeamlessLoop的Transition必須>0
如果Transition == 0 就會變成跟一般Loop一樣。
- [x]  AudioPlayer的AudioMixer不需要serializedField
- [x]  audioVoice不夠時仍然可以播，可丟到Master? 讓他變成Virtual的
- [x]  拿掉Play的PreventTime
- [x]  檢查PlaybackPref變成Struct之後的問題
- [x]  檢查還有沒有地方對TransitionTime做限制 (要改成不限制)
- [x]  重新實作Seamless的Play at point
- [x]  支援Spatial
- [x]  新增Voices Global Settings warning
- [ ]  invader是否要被後續的SetEffect影響
- [x]  重新思考音量設計  還是要用AudioMixer，這樣才有順暢的Fading
- [ ]  如果使用者真的用了超多資料，會導致GetUniqueID很難找到可用的ID，因此需要有比用Random更安全的做法，能夠知道ID是否被用完
- [ ]  prioity
- [ ]  WebGL support
- [x]  提供增加Track的方法? 還是直接提供做好的?
直接用做好的可能會有版本問題，e.g Mixer有新的設計，但使用者還在舊版的
已提供自動新增track功能
- [x]  把switch 改成C#舊版寫法

## KnownIssue

- [x]  按多次停止播放會重複FadeOut
- [x]  音量重複設定問題
- [x]  音量控制在Build之後失效?
- [x]  按了Stop之後SoundPlayer無法再次播放(音量一直在-80)
- [x]  MultipleClips全部都共用?
- [x]  preview高度計算有問題 (在於DrawLine)
- [x]  clip properties還不能用(因為還沒弄到BroAudioClip上?)
- [x]  library更新問題是因為沒有執行OnEnable跟OnDisable
- [x]  playmode 自動切換失效，只有1個Clip時應該要自動切到single
- [x]  好像有因為GetWindow的關係多一個Window然後沒東西…?
- [x]  第一次開EditorWindow會lag
- [x]  剛創Library後第一次建的Set的高度會特別多(不清楚原因)
問題在property.CountInProperty()
但是刪掉再重新加Set就不會…Why
- [x]  自動設定音量到1的功能失效了
- [x]  clip 經常會抓不到
- [x]  即使一開始將volume設為0,播放時仍會先出一個聲音
只能先將所有音軌都預設為靜音(-80)
- [x]  EditorWindow有時沒有被正確刪除? 後來會越累積越多….會一直導致出現Error
5/17 沒再遇到
- [x]  Generate ID時，現有的不要再重新生成了，那會導致Inspector上設定的ID失效!!
- [x]  在刪Asset時出現index out of range bug
- [x]  ObjectPool似乎有問題，有Player的Script刪了但GameObject還在
- [x]  Sequence及Random無效
- [x]  聲音還是會破，而且Mixer抓不到
- [x]  音樂跟OneShot沒辦法播
因為不能從AudioPlayer轉到延伸的Player類別，要重新調整設計思路
方案一: 在ObjectPool時就生成指定的類別
方案二: 生成指定衍伸類別後，再把AudioPlayer複製過去
方案三: Decorate Pattern
方案四: 直接不轉了
問題：AudioPlayer是掛在GameObject上的Component，更加沒辦法轉
- [x]  觸發多次Exclusive後，最後Exclusive會一直重複SetFloat，原因在於本身ClipVolume的Coroutine仍然在跑。沒在一般Track發生是因為大家各自是不同Track，因次要阻止這行為就必須知道是否是以Exclusive方式播放。     已重新設計
- [x]  OverrideFade 失效，沒有設定到前一個Music
- [x]  設Transition 並override後，在首次播放沒有Transition時卻仍採用了Fading參數
- [x]  ****AdvancedDropdowny在超過3個時會變成Scroll****
- [x]  在LibraryManager內Preview播放要記得在關閉Editor時停止
- [x]  Master音量還沒正確實做，此外調整各別Type再調Master會有被重置的狀況，代表Master可能不應該用BroAudioType.All來用? **好像有修正，不確定是否已完成…**
- [x]  重選Clip會導致ClipProperties不見
- [x]  在音量手動輸入數值，有時會遇到float不準的問題
- [x]  第一次快速changeChannel會聽到一點點爆音?  目前的設計已減輕問題
- [ ]  SetEffect會被其他型態的Effect在結束時Reset? **好像有修正，不確定是否已完成…**
- [ ]  換到沒有指定AudioClip的clips element後，GetPropertyHeight不會更新(而且是完全不會call)
~~5/5 試試EditorWindow的Repaint? 沒用…~~
- [x]  有時候Player沒有被Recycle (音量沒有回-80f,AudioPlayer的Clip都還在) 
1. 要較短的Clip才會發生?? 
2. 無關Fade與PlaybackPosition
8/8 已解決！原因是因為AudioSource.time跑到EndTime的時候，Coroutine不一定剛好有刷新，而等到Coroutine刷新時，AudioSource已經播完了time變成0 ，導致WaitUntil永遠等不到(錯過)
- [x]  播一堆Audio後，有些AudioPlayer莫名其妙被設到Vector3.-1
- [ ]  超過VOICES上限後，把track 設null似乎不是個好方法，因為Seamless會一直去用到那個null的導致無法被音量控制

### 發布後再做

- [ ]  **AudioClipLoadType**
- [ ]  **ToolTips**
- [ ]  AnimationCurve
- [ ]  重新實作OneShot及PlayClipAtPoint
~~OneShot仍然需要AudioPlayer，因爲仍然可以控制AudioTrack，主要差別在好幾個相同id的OneShot都可使用同一個Player? 不行這樣就沒辦法Fade~~
OneShot必須犧牲AudioPlayer的Fading及其他功能，讓以使用者先以ClipEditor編輯好，與之換來的是效能的提升
- [ ]  Log要指向上一個code執行點
- [ ]  Sequencer 好像可以用IEnumerator實作[https://ithelp.ithome.com.tw/articles/10193586](https://ithelp.ithome.com.tw/articles/10193586)
- [ ]  Music及Ambience新增Stream的選項
- [ ]  SoundManager 一開始就要Load全部的Bank太耗效能了
可能可以分出Essenitial與Dynamic的Bank，依使用者需求優化
- [ ]  Seamless可能需要限制時長不超過Clip長度?
- [ ]  Builder Pattern 好像可以優化ChainingMethod?

## Design Decision

### ~~要不要獨立給StandOut 一個音軌?~~

目前想的到的需求好像不太需要，會用到的聲音類型要StandOut的時候都可以整個音軌一起動
主要會用到StandOut的情況：

1. 進入選單  ⇒ UI
2. 音樂(像死亡擱淺)  ⇒ Music
3. 對話 (像P5R) ⇒ VoiceOver

### GlobalSetting

- [x]  Asset Output Path
- [x]  Hass Effect
- [x]  GUISetting_Don’t show audioType label on AudioID
- [x]  change audioType label color
- [x]  Fading Ease
- [ ]  Pool Size
- [ ]  Show Optimization Tips
- [ ]  Advance Mode( audio voice)

### 定義

- **PreventPlayback** : 防止在指定時間內再次播放(預設0.1s)
- **ClipVolume** : 播放Clip的音量(0~1)，依不同的Clip有不同設定，而Fade In/Out也只作用在此值
- **TrackVolume** : 音軌的音量(0~1)，也可算是此Player的音量，作用相當於混音的Fader
- **MixerDecibelVolume** 實際在AudioMixer上的分貝數
- **MulticlipsPlayMode :** 挑選Clip的方式
- Bank  多個Library的集合
- Library/Asset 一個ScriptableObject、一個EnumType，
- Set 多個Clip以及各項參數
- **BroAudioClip** : 包含AudioClip及Playback參數等資訊

```csharp
using System;
using MiProduction.BroAudio.Data;

namespace MiProduction.BroAudio.Runtime
{
	public abstract class AudioPlayerDecorator : IAudioPlayer
	{
		protected AudioPlayer Player;

		public AudioPlayerDecorator() { }

		public AudioPlayerDecorator(AudioPlayer player)
		{
			Player = player;
		}
		
		public void Init(AudioPlayer player)
		{
			Player = player;
		}

		public event Action<AudioPlayer> OnRecycle
		{
			add => Player.OnRecycle += value;
			remove => Player.OnRecycle -= value;
		}

		public int ID => Player.ID;
		public bool IsPlaying => Player.IsPlaying;

		public IAudioPlayer DuckOthers(float othersVol, float fadeTime = 0.5f) => Player.DuckOthers(othersVol, fadeTime);
		public IAudioPlayer HighPassOthers(float freq, float fadeTime = 0.5f) => Player.HighPassOthers(freq, fadeTime);
		public IAudioPlayer LowPassOthers(float freq, float fadeTime = 0.5f) => Player.LowPassOthers(freq, fadeTime);
		public IAudioPlayer SetVolume(float vol, float fadeTime = 0.5f) => Player.SetVolume(vol, fadeTime);

		public virtual void Play(int id,BroAudioClip clip, PlaybackPreference pref,Action onFinishPlaying = null)
		{
			Player.Play(id,clip,pref,onFinishPlaying);
		}

		public virtual void Stop()
		{
			Player.Stop();
		}

		public virtual void Stop(Action onFinishStopping)
		{
			Player.Stop(onFinishStopping);
		}

	}
}
```