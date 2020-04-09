## タイトル
* Ticket404 111111111111111111

## 関連URL

* Redmine ticket URL
* 他の関連URL


## 概要

* topページのレスポンスが遅い為sqlの構文をチェックする
* インデックスが効いてなかったのでインデックスを追加した
* 見られる効果はresponse_time 2.9ms ->0.3msにアップ

## 見て欲しいとこと及び手順

* ローカル環境でテストして欲しい
* indexが追加した前後のresponse timeの比較
* 影響範囲の確認

## 影響範囲

* 影響範囲はテープルm_joblist,textxxxxを使用してる所です。

## UIに対する変更はスクリンショットをとる（or redmine）

* 今回はUIの変更なし

## Git以外の変更

変更ある時の例
下記の小タイトルの変更は場合により自分で定義
* SQL textxxxxテープル indexの変更があり (変更前、変更後)
    * 変更前 : インデックスが4つありました。
    * 変更後 : idx_active_flagが追加された

* 実装詳細
   * ADD : ALTER TABLE textxxxx ADD INDEX idx_active_flag(clume_name);  
   * DROP : ALTER TABLE textxxxx DROP INDEX idx_active_flag;
* #変更ない時の例
* 特にない

## レビュー優先度
* [x] 最速でお願いしたい
* [ ] ありがたい期日(今週のx曜日まで)
* [ ] なるべく早く(なるはや)
* [ ] お時間あるときでOK

## 確認ポイントのチェック

* [ ] redmineのURL記入済
* [ ] labelsを追加した
* [ ] レビューアを追加した
