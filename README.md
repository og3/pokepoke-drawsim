# やりたいこと
- 「大会で高シェアかつ高勝率のデッキに勝ちやすいデッキ」＝ランクマッチでメタとして刺さるデッキとし、それを特定すること。
- さらに特定したデッキの盤面構築安定率を「一人回し」にて確認する。（フェーズ２）

# 環境メタデッキ
- シェア率TOP7のデッキに対して平均勝率が50％以上のデッキ

# フロー
1, [ポケポケ大会勝敗結果データベース](https://play.limitlesstcg.com/decks?game=POCKET)から上位7件を取得し、以下の「シェア率と勝率の出力イメージ」の形で、かつ、yyyy-mm-dd＋share_and_win_rateのファイル名でcsv保存する。
2, csvの内のすべての「matchups」のページに遷移し、その値を取得する。
3, countが50以上のレコードを「出力データイメージ」の形で保存する。ファイル名はyyyy-mm-dd＋win_rate。

## シェア率と勝率の出力イメージ
デッキ名 | シェア率 | 勝率 | matchups
-- | -- | -- | -- 
シルヴァディ・ラムパルド| 13.4% | 52.81% |  https://play.limitlesstcg.com/decks/silvally-a3a-rampardos-a2/matchups?game=POCKET&format=standard&set=A3a
ソルガレオex・マシェード| 9.10% | 51.92% |  https://play.limitlesstcg.com/decks/solgaleo-ex-a3-shiinotic-a3a/matchups?game=POCKET&format=standard&set=A3a

## 出力データイメージ
　これがきれいに出せたらあとはソートすればtop7に対して勝率が優秀なデッキがわかる。
vsデッキ名 | 自デッキ名 | 自デッキの勝率 | 対戦数
-- | -- | -- | -- 
シルヴァディ・ラムパルド|  マッシブーンex・テッカグヤ | 60.8% | 296
ソルガレオex・マシェード|  マッシブーンex・テッカグヤ | 35.77% | 246

# データ参照元
https://play.limitlesstcg.com/decks?game=POCKET
