---
title: "Nano Banana Proで解法を図解する"
emoji: "🍌"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["kaggle"]
published: false
---

## はじめに
先日開催された関西Kaggler会にて以下のように解法を図解する技術について発表しました。
https://www.docswell.com/s/kuto1963222/ZX6772-2025-11-14-170808#p1
![](/images/5cdcd1b274abc8/slide.png)

この発表をした1週間後にNano Banana Proという画像生成AIがGoogleから発表されました。
その性能は非常に高く、以下の記事でさまざまな生成事例が紹介されています。
https://note.com/google_gemini/n/n064d03afe2c0

今まで人力でやっていた解法の図解ですが、いよいよAIでできるのでは？という期待が自分の中で高まったので、この記事ではNano Banana Proを用いて、解法の図解を試してみたのでその結果と感想を共有します。

## 実験条件
現在私はAIMO3というコンペに参加しているので、その過去コンペであるAIMO2の1位解法を図解の題材として利用したいと思います。
https://www.kaggle.com/competitions/ai-mathematical-olympiad-progress-prize-2/writeups/nemoskills-1st-place-solution-nemoskills

今回は以下の方法で画像生成を試すことにします。
- 解法のみ
- 解法+過去の図解画像
- 解法+指示テキスト

生成される解法画像は実行のたびに異なる結果となるため、複数回生成したものからピックアップして紹介します。(他の生成結果も貼ってるので見比べるとブレや傾向がわかるかと思います.)

## 結果
### 1.解法のみ
まずは、生成画像のベースラインを確認するために、解法テキストのみを入力として生成を試みてみましょう。

:::details プロンプト
```markdown
下記のテキストはkaggleで開催されていた`AI Mathematical Olympiad - Progress Prize 2`の1位解法です。
この解法を図解した画像を作成してください。

---
<解法テキスト>
---
```
:::

![](/images/5cdcd1b274abc8/sample7.png)
![](/images/5cdcd1b274abc8/sample5.png)
![](/images/5cdcd1b274abc8/sample6.png)

### 2.解法+過去の図解画像
解法に加えて、過去に私が作成した他コンペの図解画像を入力に事例として追加し生成したのがこちらです。

:::details プロンプト
```markdown
下記のテキストはkaggleで開催されていた`AI Mathematical Olympiad - Progress Prize 2`の1位解法です。
この解法を元に添付画像のフォーマットに従って、図解した画像を作成してください。

---
<解法テキスト>
---

<過去の図解画像を複数添付>
```
:::

:::details 添付画像
![](/images/5cdcd1b274abc8/eedi.png)
![](/images/5cdcd1b274abc8/handm.png)
![](/images/5cdcd1b274abc8/luxais3.png)
:::

生成結果
![](/images/5cdcd1b274abc8/sample2.png)
![](/images/5cdcd1b274abc8/sample1.png)
![](/images/5cdcd1b274abc8/sample3.png)
<!-- ![](/images/5cdcd1b274abc8/sample4.png) -->


### 3.解法+指示テキスト



## 感想
