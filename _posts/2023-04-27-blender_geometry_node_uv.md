---
# Copyright (c) 2023 Windy Darian
# CC-BY-NC-SA-4.0
layout: post
title: Blender Geometry Nodes How to Output to Mesh UV
image: /assets/post_images/2023/2023-04-27-geonode.png
image_width: 256px
languages:
  - en
  - zh
  - zh-Hant
  - ja
---

tl;dr - Well not very long. Output to mesh UV with geometry map! 
<!--more-->

{:.ln-en lang="en"}
I haven't posted for... how long? And this is 2nd post after I switched to Jekyll??

{:.ln-en lang="en"}
Well. Anyway! Having fun with Geometry Nodes in Blender recently. I am trying to make a game and want to use geometry node to speed up some 3D asset creation. \  
However, was running into an issue where that there is no obvious output nodes that writes to mesh UV map. I could output to an attribute and use it for mesh UV, 
but would need extra work to pipe the attribute as UV in Godot (The game engine I am using).

{:.ln-en lang="en"}
After a bit of experimenting, I found that this will work - write to face corner 2d vector attribute "UVMap"! (see image)

{:.ln-en lang="en"}
Blender will use default "UVMap" for meshes, so unless it's manually changed, it should work for geometry node graphs that generate meshes.

{:.ln-zh lang="zh"}
我有多久没写博客了...? 而且这是第二篇？过了多少年？

{:.ln-zh lang="zh"}
嘛总之。最近在试着用Blender的Geometry Nodes 来加速自制游戏的3D内容。这个过程面临一个问题。。。要如何写入生成Mesh的UV坐标？ 似乎没有很明确的方式。虽然可以写入新的attribute, 但要作为UV坐标引入游戏引擎的话会比较艰难。

{:.ln-zh lang="zh"}
在一阵实验之后，发现一种可行的方案，直接按以2D向量的格式按Face Corner 写入“UVMap”！（如图）

{:.ln-zh lang="zh"}
因为Blender会默认生成"UVMap"作为默认UV，所以除非之前手动更改，对生成mesh的Geometry Node应该都有效

{:.ln-zh-Hant lang="zh-Hant"}
註：我使用了ChatGPT來翻譯這種語言

{:.ln-zh-Hant lang="zh-Hant"}
我有多久沒寫部落格了...? 而且這是我轉換到Jekyll之後的第二篇？

{:.ln-zh-Hant lang="zh-Hant"}
嗯，總之！最近在使用Blender的Geometry Nodes樂在其中。我試著製作一個遊戲並希望使用geometry node來加速一些3D資產的創建。\
然而，我遇到了一個問題，那就是沒有明顯的輸出節點可以寫入mesh UV map。我可以輸出到一個屬性並用它作為mesh UV，
但需要額外的工作來將該屬性作為UV在Godot（我正在使用的遊戲引擎）中使用。

{:.ln-zh-Hant lang="zh-Hant"}
經過一些實驗，我發現這種方法可以行得通 - 將資訊寫入面角2D向量屬性"UVMap"! (參見圖片)

{:.ln-zh-Hant lang="zh-Hant"}
Blender將使用默認的"UVMap"作為meshes UV，所以除非手動改變，它應該適用於生成meshes的geometry node圖表。

{:.ln-ja lang="ja"}
注：この言語への翻訳にはChatGPTを使用しました

{:.ln-ja lang="ja"}
どれくらいブログを書いていないだろう...？そして、これはJekyllに切り替えてから2回目の投稿？

{:.ln-ja lang="ja"}
まあ、とにかく！最近、BlenderのGeometry Nodesで楽しみながら、ゲームを作ろうとしています。ジオメトリノードを使って3Dアセットの作成を加速したいと思っています。\
しかし、メッシュUVマップに書き込む明確な出力ノードがないという問題に直面していました。アトリビュートに出力してメッシュUVに使用することは可能ですが、
それをGodot（使用中のゲームエンジン）のUVとしてパイプするのに追加の作業が必要になります。

{:.ln-ja lang="ja"}
少し実験した後、これが機能することがわかりました - フェースコーナー2Dベクターアトリビュート"UVMap"に書き込む！（画像参照）

{:.ln-ja lang="ja"}
Blenderは、メッシュに対してデフォルトの"UVMap"を使用するので、手動で変更しない限り、メッシュを生成するジオメトリノードグラフに対して機能するはずです。

[![the node]({{page.image}}){:width="256px"}]({{page.image}})