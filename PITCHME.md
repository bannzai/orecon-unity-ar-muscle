## [俺コン Vol.1 / Day. 2](https://orecon.connpass.com/event/64285/)
マッチョにUnityちゃんのアニメーションをつけた話

---

## 自己紹介
<img align="left" width="160px" src="https://avatars0.githubusercontent.com/u/10897361?v=4&s=400&u=f1cd0d99b3913476fe7bdcb6d4934105df2aa15f" />
<div align="left"> 
  名前: 廣瀬 雄大</br>
  あだ名: スター乞食
</div>

Swift製のライブラリを作って公開して発表して*スターください*と言っていたらこんな呼び名に

<div align="left"> 
  github:  [bannzai](https://github.com/bannzai/)</br>
  twitter: [@yhirose741](https://twitter.com/yhirose741/)
</div>

---

## [プロポーザル](https://iosdc.jp/2017/node/1418)
![image.png](https://qiita-image-store.s3.amazonaws.com/0/84459/70669659-4f9f-f62e-1bbd-700fc8e3b18c.png)

---


## 前置き

今回は`Unity`の使い方だったり特徴というものは一切話しません
大雑把に作ったものの紹介と 
肝となる `Unity<->ARKit` をブリッジングしているクラスとかを紹介し
参考になった記事等を紹介します

---

## 今回お話しすること

- マッチョのための開発環境の紹介
- 今回のマッチョ
- マッチョを配置
- マッチョを可愛くする
- マッチョ鑑賞 可愛いよマッチョ可愛いよ

---

## マッチョのための開発環境の紹介

**Unity ARKit plugin**に記載されている環境を準備

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

<img width="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/7340b6c5-2355-1408-a7ce-d572be6e660b.png" />

+++

<img width="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/58d033f0-3c7e-67ac-dca4-bb3e6418d33b.png" /> 

+++

`Scene`が変わってこうなる
<img width="400px" src="https://qiita-image-store.s3.amazonaws.com/0/84459/9c23bc73-ac1b-499e-5236-aba2de96fe46.png" />

---

## 今回のマッチョ
今回のマッチョは`Max`を使います
`Asset Store`で`Max`と検索して`import`しましょう

+++

<img width="400px" alt="スクリーンショット 2017-09-30 14.45.15.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/e45f7469-a852-e427-c1b0-6aee123c589d.png">

+++ 

`Assets`に`Max`が確認できればおKです
<img width="400px" alt="スクリーンショット 2017-09-30 14.45.15.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/c8721c66-1519-09a1-5dcf-55f051ae4a3b.png">

---

## マッチョを配置
`Mac` のディレクトリを展開して言って`prefab`に入っている`Max`を選択
`HitCubeParent`の下に選択した`Max`をドラッグ&ドロップする
もともとあった`HitCube`って素材は削除していいです

+++

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/11a20ef2-a74a-f046-34b7-e49f0db7885e.png">

+++

配置した`Max`に`Script`を追加します
`Unity AR Hit Test Example`がSampleにあるので今回はこれを使います

+++

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/cc913daa-9fcb-5aa3-9423-070e33ac39ad.png" />

---

## マッチョを可愛くする
ついにマッチョにUnityちゃんのアニメーションをつけるフェーズまで来ました
[UnityChan](https://assetstore.unity.com/packages/3d/characters/unity-chan-model-18705)
<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/8d7d62d3-11ff-5fce-4cd3-03c6b0f615ae.png" />

+++

[UnityChan](https://assetstore.unity.com/packages/3d/characters/unity-chan-model-18705)の`Asset`をプロジェクトに追加します(省略

+++

Animationをまず作って行きましょう
`Assets`右クリック
→ `Create`
→ `Animate Controller`
で`AnimateController`という名前で`Animation`を定義して行きます

+++

<img width="400px" alt="スクリーンショット 2017-10-02 2.30.32.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/3932ef82-0e7d-79ac-a748-3a10d45ff77b.png">


作った`AnimateController`をダブルクリックすると
`Animator`タブが画面上に表示されます
この画面で`Empty`の状態をとりあえず作成します

+++

<img width="400px" alt="スクリーンショット 2017-10-02 2.32.57.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/fbee4454-ea5f-caf9-5863-6c77e2c3c99d.png">

+++

作ったらこうなる
<img width="400px" alt="スクリーンショット 2017-10-02 2.34.21.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/bf0d66a0-6b19-5484-0737-0987376f35cb.png">

ここから`UnityChan/Animations`に入っている`WIN00`というアニメーションを
先ほど作った`Empty`のステートに定義していきます

+++

<img width="400px" alt="hoge.png" src="https://qiita-image-store.s3.amazonaws.com/0/84459/4dca2d63-1fbe-7b52-7886-e85812175c8d.png">

これでマッチョが可愛くアニメーションするようになりました。やったね

---

## マッチョ鑑賞 可愛いよマッチョ可愛いよ

<iframe width="400px" height="630px" src="https://www.youtube.com/embed/e-KPO3kzy-M" frameborder="0" allowfullscreen></iframe>

<h1></h1>
ワンモアマッチョ
<iframe  width="400px" height="630px"  src="https://www.youtube.com/embed/SDcD6hBul78" frameborder="0" allowfullscreen></iframe>

---
