**気付いた・検討した点**
1. 毎回APIでランキング情報を取得することでTOPページが重くなっているため、ランキング情報をキャッシュで保持することで2回目以降の動きを軽くする
1. アイコンの無駄な動きのせいで商品が見えにくい為、動きを止める
1. TOPページからMovieやMusicのTop10に行けない
1. POSTのパスワードが平文で送信されているため、暗号化する
1. accountページでaccount?id=xのxの値を変えれば他者のマイページに飛べる
1. ResiterページにLoginフォームが表示されるのは不要
1. Movie Musicのジャンル分けが細かすぎてわかりづらい
1. 映画のキャスト情報を表示させる
1. パスワードを数字だけで入力させるとセキュリティ面が弱くなるのでは
1. XSS対策
1. CSRF対策



**実装内容**
1. CSSファイルを変更し、アイコンの無駄な動きを止めた
1. ToPページのTOP MOVIESとTOP MUSICの文字にそれぞれMovieTop10とMovieTop10へのリンクを入れた
1. 送信時のパスワードを暗号化してから送信するように変更した
1. ResiterページのLoginフォームを削除
1. 入力検査でEmailフォームにEmail以外の値を入れられないようにした
1. Topページ中央付近のボックスにあった使用されていないリンクを削除
