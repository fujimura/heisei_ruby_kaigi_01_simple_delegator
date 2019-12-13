---
title: "SimpleDelegator活用のご提案"
subtitle: "平成Ruby会議 01"
author: Daisuke Fujimura
date: 2019-12-13
---

# 自己紹介

藤村大介

- https://twitter.com/ffu_
- https://github.com/fujimura
- スタートアップ数社 ⇨ マチマチCTO ⇨ フリーランス
- 現在は数社で技術顧問のお仕事
- RubyとHaskellが好き
- [WEB+DB PRESS Vol.110 名前付け大全](https://gihyo.jp/magazine/wdpress/archive/2019/vol110)を書いた

# 今日のお話

SimpleDelegator活用のご提案

# 自己紹介
# SimpleDelegatorとは
# 基本的な使い方
# 主な使いみち

- アドホックにオブジェクトを拡張したいときに使う
- デコレータ
- 複合したオブジェクト

# 事例（１）アクセサを揃える

# Problem: APIのレスポンスとカラム名を揃えたい
- 微妙にインターフェイスが違うオブジェクトが返ってきてしまう
- APIのレスポンスとカラム名が違うなど

- デコレーター
- 継承でもいいんだけど気分の問題
`FeedReader::Entry`

# 事例（２）複合したオブジェクト

## Problem: 権限に応じてオブジェクトの値を変えたい

`PostPersonalizer::Result`

# 事例（３）バリデーションを追加

## Problem: HashやArrayを作るときに期待しない値があったら例外にしたい
`PlaceChange::PlaceSerializer`

# 事例（４）Hashの並べ替え

## Problem: Hashのソート順を変えたい
- デコレーター
`FeedItem::FeedItem`

# 事例（５）クエリオブジェクト

## Problem: クエリオブジェクト作るの面倒

`UpdateMailer::NewPostsInGroups`

- https://techracho.bpsinc.jp/hachi8833/2017_10_25/47287

# 補足

- 遅いってマジ？
- DelegateClassとの違いは？わからん！誰か教えてくれ！

