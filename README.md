# Magnesis Rune の Tutorial をやってみる

## Tutorial

- https://www.youtube.com/watch?v=-3skkNbervM
- https://www.youtube.com/watch?v=O2mxqpSYHxs

## 出てきた問題

4.26 では問題なく Physics Handle での Grab Component がうま
くいったが、5.0 Preview 2 では、Grab した後に、一度オブジェクトにぶつかるなどして物理的な動作を起こさないと引っ張り回すことができなかった。

とりあえず、5.0 Preview 2 では、Add Force を Grab Component 後に実行し、動作を引き起こすことで回避している。

https://twitter.com/games_inu/status/1501246786580750343

上記の Tweet では Preview 2 になって Physics Handle は `tick physics async` (非同期ティック物理) 時には動作するとなっているが、今回はそれでもうまくいかなかった。

[非同期ティック物理の概要 | Unreal Engine ドキュメント](https://docs.unrealengine.com/5.0/ja/PhysicsFeatures/AsyncPhysics/)