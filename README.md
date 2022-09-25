# snsアプリケーション

## 機能

##

##

##　苦戦したポイント
中間テーブルに苦戦した。favarite機能と同じようなことをしたため、モデルのbelongsToManyを設定する際に最初
return $this->belongsToMany(Tweet::class)->withTimestamps();としていたためにbad機能を使う際にfavarite機能と連動してしまうといことがおきた。それを防ぐために、モデルのツイートのusersとbaduserのbelongsToManyの引数を（第一引数に相手側のモデル名、第二引数に中間テーブル名、第三引数に接続元モデルID (中間テーブルで使われる名称)、第四引数に接続先モデルID (中間テーブルで使われる名称)）に帰ることで解決したが、行き着くのに苦戦した。
