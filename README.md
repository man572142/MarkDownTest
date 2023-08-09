# GMTK_RoleReverse

[發想](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/%E7%99%BC%E6%83%B3%20cb8299ca08934933a3022d7d3984d6cc.md)

[Assets Credits](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Assets%20Credits%208d9ef702e5fb4c12b7c551ae2b1d02f5.md)

[問題備註](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/%E5%95%8F%E9%A1%8C%E5%82%99%E8%A8%BB%201d7bea07eb1644dc9fcf89f1bdbbd1b4.md)

[美術素材共享夾](https://drive.google.com/drive/folders/182huklRhOWVby0zjDRUfyVQQVgQstDLZ?usp=sharing)

[I’m not a robot 劇情](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/I%E2%80%99m%20not%20a%20robot%20%E5%8A%87%E6%83%85%20b96bcdac5447437e83049a6583e873a2.md)

1. CutSceneManager.Instance.Play(PuzzleType.EndScene, OnCutSceneFinished);
2. ***July 9, 2023 9:29 AM*July 9, 2023 9:29 AM*July 9, 2023 9:29 AM***
    
    OnCutSceneFinished是callback 用來接Load下一個scene
    

Check Point 晚上10十點

[https://discord.com/channels/1040997245299986432/1122511072339955833/1127044478973255761](https://discord.com/channels/1040997245299986432/1122511072339955833/1127044478973255761)

```csharp
//CutSceneManager, 關卡成功通過的話

//第一個parameter PuzzleType 隨puzzel類型調整
GMTK.CutSceneManager.Instance.Play(PuzzleType.TrolleyProblem, () =>
{
    if (_loadSceneHelper)
    {
        _loadSceneHelper.LoadNextScene();
    }
});
```

願望清單

- [ ]  滑鼠UI特製
- [ ]  User Agreement
- [x]  拼圖 : 機器人頭像
- [ ]  場景轉換顯示舊謎題
- [x]  puzzle 選取不明顯
- [x]  Bad End Countdown

尚未完成的

謎題一

- [x]  Are you a robot? 的小對話框 & 彈出事件串接
- [x]  畫面全黑並出現字幕 I doubt it… 幾秒後出現Try solve this !接下一個謎題 ⇒ UI事件串接

### 謎題二~五任選 (共跑三道題)

- [x]  若有在時限內解完題目，電腦會有以下幾種回覆 ⇒ 每個題目的Scene解完題要串UI事件
1. You must be cheating … 
2. No Way!
3. That’s insane

### 最終謎題

**下一步按鈕文字統一為：Verify**

# 名稱 I’m not a Robot

CAPTCHA

[https://www.cloudflare.com/zh-tw/learning/bots/how-captchas-work/](https://www.cloudflare.com/zh-tw/learning/bots/how-captchas-work/)

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled.png)

最簡單CAPTCHA

難道你是機器人

藉由CAPTCHA找同伴

**劇情最後的反轉**

走到最後其實機器人還是說，你才不是機器人，機器人才不會做這些事

玩家玩到最後面，為了避免玩家誤會走到Bad End，可以加上「恭喜你玩到最後，但我們知道你還是人類」然後秀出Credit名單

### 謎題一 (開啟遊戲直接進入, AHan))

僅有I’m not a robot的選項，打勾了遊戲就結束，必須等待幾秒都不按才能讓它繼續下去

出現新的按鈕

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%201.png)

### 謎題二(AHan)

超難數學算式，玩家要用超快的速度輸入，以證明自己是機器人
Key的內容：

![0709_樣板更新-02.jpg](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/0709_%25E6%25A8%25A3%25E6%259D%25BF%25E6%259B%25B4%25E6%2596%25B0-02.jpg)

玩家可以暫停來找額外工具計算

遊戲結束 : 時間到OR給錯誤答案

Qualifying question

Just to prove you are a human, please answer the following math challenge.

Q: Calculate

A:

~~Note: If you do not know the answer to this question, reload the page and you’ll get another question.~~

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%202.png)

### 謎題三 (Will)

選圖片的，可能是很多類似的圖片(例如: 胡瓜vs 阿信, 吉娃娃 vs 司康 , 炸雞 vs 貴賓犬)

Select all squares with clouds.

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%203.png)

//Todo: 1跟2機制上不一致，可能讓玩家無所適從。處理方式 : 先把題目做出來再決定要怎麼做。

1) 選反的

~~2) 選「機器人不會做的事」 (人類黑歷史)~~

~~-猶太大屠殺~~

~~-64天安門~~

~~-盧安達大屠殺~~

先做一般的

3)選一堆相似的圖片 → 還不確定要怎麼解(假裝機器人)

### 謎題四(阿咪)

給歪曲圖片，並輸入文字

Match the characters in the picture

To continue, type the characters you see in the picture.

The picture contains n characters.

Characters

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%204.png)

成功**：**

1. 不斷重新整理
2. 不斷打錯並按確定，等同於重新整理

重新整理幾次 3-5次

要呈現哪些文字?

1) 隨機文字 3個

2) Human is Good

3) You Idiot

**失敗：**

如果輸入正確，就結束遊戲

### 謎題五 (Will)

電車難題(附迷因圖片) 

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%205.png)

題目 : 我在範本

A鐵軌上有一個人

B鐵軌上有五個機器人

你應該選偏向哪個? 

**失敗：**

如果選擇救人，遊戲就結束

### 謎題六 (發條)

移動拼圖

**成功：**拚到白色空缺

**失敗：**像平常一樣對到空缺

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%206.png)

![Untitled](GMTK_RoleReverse%2066c1fd21c36e4efb8f7ee2c3df2e5592/Untitled%207.png)

## Bad End 畫面 (Willard)

Oh you are not a robot ;( 

## Good End 畫面 (Willard)

ScrollRect的機制

結尾生英文

動畫

企劃 WillardPeng, WengShan, Neji Yuri, A_HAN, Riri

音效 WengShan

程式 WillardPeng, WengShan, Neji Yuri, A_HAN

美術 Riri

## [Itch.io](http://Itch.io)

排版

文字 

## 音效

## 個別負責的UI

圖片上上去

## TMPro 匯入