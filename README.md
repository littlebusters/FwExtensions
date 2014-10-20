Fireworks Extensions
====================

個人用として使ってるFireworksコマンドなどのバックアップ。公開にするにあたり、ある程度整理していますが、ソースが汚い・エラーが出る・英語が意味不明などは、スルーの方向で。

## selection_to_sublayer.jsf

選択範囲を新しく作成したサブレイヤーに移動させる。サブレイヤーは、現在のレイヤーのサブレイヤーとして作成される。表示されるダイアログにはサブレイヤー名を入力でき、キャンセルするとデフォルト名となる（e.g. レイヤー2）。

## increase_opacity.jsf / increase_opacity_L.jsf

選択範囲の不透明度を、_Lは10、Postfixなしは1ずつ上げる。

## reduce_opacity.jsf / reduce_opacity_L.jsf

選択範囲の不透明度を、_Lは10、Postfixなしは1ずつ下げる。

## set_opacity.jsf

選択範囲の不透明度を、ダイアログで入力した値に設定する。数値の前に四則演算子を入力した場合、各オブジェクトの不透明度を計算して設定する（e.g. 不透明度50のオブジェクトに対して、'/2'と入力した場合は25となる）。

## object_move.jsf

オブジェクトをダイヤログで入力した数値分移動させる。ダイヤログは'X[半角スペース]Y'の形式で入力する。どちらかの座標を移動させない場合は、0を入力すること（e.g. X座標を50px移動・Y座標を移動させない場合、'50 0'）。パスのアンカーポイントを選択している場合は、アンカーポイントが移動する。四則演算可能。

## object_move_coordinate.jsf

オブジェクトをダイヤログで入力した座標へ移動させる。ダイヤログは'X[半角スペース]Y'の形式で入力する。四則演算可能（座標は四捨五入）。パスのアンカーポイントを選択している場合は、アンカーポイントが移動する。

## set_fill_opacity.jsf / set_stroke_opacity.jsf

選択範囲の塗り（set_fill_opacity.jsf）/線（set_stroke_opacity.jsf）の不透明度を、ダイアログで入力した値に設定する。数値の前に四則演算子を入力した場合、各オブジェクトの塗りの不透明度を計算して設定する（e.g. 不透明度50の塗りに対して、'/2'と入力した場合は25となる）。グループ化されているオブジェクトには無効。

## fix_transformation_text.jsf

選択範囲のテキストオブジェクトの同じ場所で変形をリセットする。グループ化されていたりシンボル内のリセットはできないが、グループ内のテキストオブジェクトについては、ダイレクト選択ツールを使い直接選択することでリセット可能。

## set_bounds.jsf

左上を起点に、選択範囲のオブジェクトサイズを入力したサイズに変更する。ダイアログは'幅[半角スペース]高さ'で入力（初期値は選択範囲内で最上部にあるオブジェクトのサイズ）。複数選択可能で、すべて同じ大きさに変更される。

## set_font_size.jsf

フォントサイズを設定する。

## alpha_to_RGB.jsf

アルファを含むRGB値を通常のRGB値に変換する。塗りまたは線自体にアルファ値を設定している場合は、考慮しない。

## sort_by_coodinate.jsf

原点を起点に、スライスを Y座標 > X座標 でソートする。