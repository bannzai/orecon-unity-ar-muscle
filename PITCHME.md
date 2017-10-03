## [俺コン Vol.1 / Day. 2](https://orecon.connpass.com/event/64285/)
マッチョにUnityちゃんのアニメーションをつけた話

---

## 自己紹介
<img align="left" width="160px" src="https://avatars0.githubusercontent.com/u/10897361?v=4&s=400&u=f1cd0d99b3913476fe7bdcb6d4934105df2aa15f" />
<div align="left"> 
  <br>
  <p>&nbsp;&nbsp;名前: 廣瀬 雄大</br></p>
  <p>&nbsp;&nbsp;あだ名: スター乞食</p>
</div>

<p aligh="left">&nbsp;Swift製のライブラリを作って公開して発表して<br>**スターください**と言っていたらこんなあだ名に</p>

<div align="left"> 
  <p>&nbsp;github:  [bannzai](https://github.com/bannzai/)</br> </p>
  <p>&nbsp;twitter: [@yhirose741](https://twitter.com/yhirose741/) </p>
</div>

---

## プロポーザル
![image.png](https://qiita-image-store.s3.amazonaws.com/0/84459/70669659-4f9f-f62e-1bbd-700fc8e3b18c.png)

---


## 前置き1 今回のお話について
<p align="left">今回は`Unity`の使い方だったり特徴というものは詳細にはお話ししません  </p>
<p align="left">作った時の流れをざっくり紹介します  </p>
<p align="left">作ったものは繰り返しになりますが`Unity`で`マッチョ`に`Unityちゃん`</p>
<p align="left">のアニメーションをつけた話になります</p>
<p align="left">最後に参考になった記事等を最後紹介します</p>  

---

## 前置き2 Unityちゃん

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/8d7d62d3-11ff-5fce-4cd3-03c6b0f615ae.png" />

+++

### 可愛いですね！

---

## 前置き3 マッチョについて

<p align="left">筋肉質の男です<br> </p>
<p align="left"> この後発表する筋肉エンジニアの`K-BOY`さんとは一切関係ないです<br></p>


---

## 今回お話しすること
<p align="left">- マッチョ開発環境 </p>
<p align="left">- 今回のマッチョ</p>
<p align="left">- マッチョを配置</p>
<p align="left">- マッチョを可愛くする</p>
<p align="left">- マッチョ鑑賞</p>
<p align="left">- まとめ</p>


---

## マッチョ開発環境

+++

### Unity ARKit plugin**に記載されている環境を準備 

<img width="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/e6b5c364-23ab-9f0c-53ec-745b8bede413.png" />

+++

## 今回は以下の環境で開発

- [Unity ARKit plugin](https://assetstore.unity.com/packages/essentials/tutorial-projects/unity-arkit-plugin-92515) 1.0.9
- macOS Sierra 10.12.6
- Unity 5.6.3p2
- iPhone7 iOS 11.0
- Xcode 9.0

+++ 

## ARKit plugin のサンプルのシーンを使おう
`Unity ARKit Plugin`にはいくつかの`Scene`が含まれています。`Open Scene`から
`$HOME/YourProject/Assets/UnityARKitPlugin/Examples/UnityARKitScene/UnityARKitScene.unity`を開きます

+++

<img height="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/7340b6c5-2355-1408-a7ce-d572be6e660b.png" />

+++

<img height="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/58d033f0-3c7e-67ac-dca4-bb3e6418d33b.png" /> 

+++

`Scene`が変わってこうなる<br>

<img align="bottom" height="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/9c23bc73-ac1b-499e-5236-aba2de96fe46.png" />

---

## 今回のマッチョ
今回のマッチョは`Max`を使います
`Asset Store`で`Max`と検索して`import`しましょう

+++

<img width="600px" alt="スクリーンショット 2017-09-30 14.45.15.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/e45f7469-a852-e427-c1b0-6aee123c589d.png">

+++ 

`Assets`に`Max`が確認できればおKです <br>

<img width="400px" alt="スクリーンショット 2017-09-30 14.45.15.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/c8721c66-1519-09a1-5dcf-55f051ae4a3b.png">

---

## マッチョを配置
`Mac` のディレクトリを展開して言って`prefab`に入っている`Max`を選択<br>
`HitCubeParent`の下に選択した`Max`をドラッグ&ドロップする<br>
もともとあった`HitCube`って素材は削除していいです

+++

<img width="600px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/11a20ef2-a74a-f046-34b7-e49f0db7885e.png">

+++

配置した`Max`に`Script`を追加します<br>
`Unity AR Hit Test Example`がSampleにあるので今回はこれを使います

+++

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/cc913daa-9fcb-5aa3-9423-070e33ac39ad.png" />

---

## マッチョを可愛くする
ついにマッチョにUnityちゃんのアニメーションをつけるフェーズまで来ました<br>
[UnityChan](https://assetstore.unity.com/packages/3d/characters/unity-chan-model-18705)<br>


+++

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/8d7d62d3-11ff-5fce-4cd3-03c6b0f615ae.png" />

[UnityChan](https://assetstore.unity.com/packages/3d/characters/unity-chan-model-18705)の`Asset`をプロジェクトに追加します
`Asset Store`から探して`import`しましょう

+++

Animationをまず作って行きましょう<br>
`Assets`右クリック<br>
→ `Create`<br>
→ `Animate Controller`<br>
で`AnimateController`という名前で`Animation`を定義して行きます<br>

+++

<img width="400px" alt="スクリーンショット 2017-10-02 2.30.32.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/3932ef82-0e7d-79ac-a748-3a10d45ff77b.png">


作った`AnimateController`をダブルクリックすると
`Animator`タブが画面上に表示されます
この画面で新しく`State`を追加しましょう

+++

<img width="600px" alt="スクリーンショット 2017-10-02 2.32.57.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/fbee4454-ea5f-caf9-5863-6c77e2c3c99d.png">

+++

作ったらこうなる<br>
<img width="600px" alt="スクリーンショット 2017-10-02 2.34.21.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/bf0d66a0-6b19-5484-0737-0987376f35cb.png">

+++

ここから`UnityChan/Animations`に入っている`WIN00`というアニメーションを
先ほど作った`Empty`のステートに定義していきます

+++

<img width="600px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/4dca2d63-1fbe-7b52-7886-e85812175c8d.png">

<p style="font-size: 17px; align=left;">これでマッチョが可愛くアニメーションするようになりました。やったね <br></p>
<p style="font-size: 17px; align=left;">あとは光の当たり方とかマッチョの向きとかを適当に調整して完成です</p>

---

## マッチョ鑑賞

---

というわけで

---

僕が作った可愛いマッチョを鑑賞しましょう

---

![](https://www.youtube.com/embed/e-KPO3kzy-M)

---
ワンモアマッチョ
![](https://www.youtube.com/embed/SDcD6hBul78)

---

### まとめ
(ちょっと長い)


---
### 作る際に参考にしたURL
- Unityで「ARKit」を使ってみよう
https://creator.game.cyberagent.co.jp/?p=4158

- Unityで筋肉質な男性に女子っぽい動きをするアニメーションを付けてみる
http://llcc.hatenablog.com/entry/2016/01/29/000518

- ARKitでユニティちゃんを踊らせてみた
https://qiita.com/bathtimefish/items/15764799cbf1e2ea2041

---

### どのくらい大変だったかとか
<p align="left">ここまでググりながらの制作日数はだいたい1日くらいです</p> 
<p align="left">Unity歴もそんな長くなくて累計で100時間くらいだと思います</p> 
<p align="left">驚くくらい簡単に3Dオブジェクトの配置とアニメーションをつけることができました</p> 

---

### ネイティブと比べて
- Pros
<p align="left"> 素材は多いだろうなと予想</p>
<p align="left"> 複雑なアニメーションを繋げる時にもGUIでぽちぽちアニメーションできるのはちょっと感動</p>
<p align="left"> SceneKitに比べると資料も多い</p>

- Cons
<p align="left"> 慣れ親しんだ言語ではない(Swiftじゃない)</p>
<p align="left"> Unityは良くも悪くも高機能で文化になれるのにも少し時間がかかるかな</p>
<p align="left"> 実機で確認して直すのは少し手間。Unity→Xcodeの更新となるのがちょっと億劫</p>

---

## 資料について
<p align="left">今回の発表資料は`GitPitch`で作成しました</p>
<p align="left">CSSにも慣れてなくてレイアウト等が崩れている部分がある状態で発表してしまいました。。。(申し訳ない</p>

+++

`GitPitch`なので崩れている部分については`PR`とかあげてくれないかなとちょっとだけ期待してます

+++

`GitPitch`なので`GitHub`のリポジトリにこの資料があります<br>
そう、みなさんこの資料にはなんと**スターをつけることができるのです**


+++

というわけで

+++

# スターください！

---



### おしまい
---
