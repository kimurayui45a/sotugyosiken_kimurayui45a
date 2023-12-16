
■サービス概要
どんなサービスなのかを３行で説明してください。

  自分が所持しているものやよくなくすものを記録して、
  欲しい時に検索できたりそれに該当する記憶を管理するアプリ
  もの探しや断捨離アプリとして使用できる


■ このサービスへの思い・作りたい理由
このサービスの題材となるものに関してのエピソードがあれば詳しく教えてください。
このサービスを思いつくにあたって元となる思いがあれば詳しく教えてください。

  ものとは記憶や自己と強く結びついた存在です。
  手放すことを含めこれを管理することで現在の自己の存在が左右され、
  いかに自己が掴みどころがなく不確かな存在かを認識できます。
  その手助けとなるようなアプリを作成したいです。
  またものを探す経験が多いため作ってみたいと思いました。


■ ユーザー層について
決めたユーザー層についてどうしてその層を対象にしたのかそれぞれ理由を教えてください。

  よくものを探す経験のある人や、自己の幻覚に囚われる人が対象です。

  表面的にはただの「もの探しアプリ」なので「よくものを探す経験のある人」が対象の主軸です。
  でもそれだけでは味気ないため、該当のものにエピソードも記録できるようにし、自己の記録を目視できる機能もつけたいと思いました。
  それによってものの有無による自己の揺らぎをユーザーに提供できたら幸いです。


■サービスの利用イメージ
ユーザーがこのサービスをどのように利用できて、それによってどんな価値を得られるかを簡単に説明してください。

  Bluetoothトラッカーなどを使用せずに、コストをかけずに探しものを見つける手助けができます。
  また探しものが見つからない場合、記録を元に「掲示板」に投稿し他ユーザーと推理することも可能です。
  しかし、ユーザー間の争いを生むような「フォロー・フレンド・ユーザー詳細の閲覧」機能は実装しません。


■ ユーザーの獲得について
想定したユーザー層に対してそれぞれどのようにサービスを届けるのか現状考えていることがあれば教えてください。

  snsに詳しくないため、とりあえずgoogle検索で考えています。


■ サービスの差別化ポイント・推しポイント
似たようなサービスが存在する場合、そのサービスとの明確な差別化ポイントとその差別化ポイントのどこが優れているのか教えてください。
独自性の強いサービスの場合、このサービスの推しとなるポイントを教えてください。

  Bluetoothトラッカーなどを使用せずに、コストをかけずに探しものを見つける手助けができます。
  また、断捨離アプリもよくありますが、それを捨てたことによってなぜスッキリするのかなどが提示されていないように思います。なので、ものとエピソードを関連付けることにしました。
  ものとエピソードを結びつけることで「捨てたいエピソードから関連するものを捨てる」という逆のアプローチも可能です。


■ 機能候補
現状作ろうと思っている機能、案段階の機能をしっかりと固まっていなくても構わないのでMVPリリース時に作っていたいもの、本リリースまでに作っていたいものをそれぞれ分けて教えてください。

  ＜入力した自分の行動に合わせてポイントが上下する機能＞
  例えば…「楽しいことがあった場合はポイントが一時的に上昇し、数時間後に上昇したポイント＋α低下」します。
  これはポジティブなことがあると裏でネガティブなことが働いている人間の脳の仕組みです。
  このように現在の自身の行動が少し未来の自身の肉体に物理的にどのような影響を与えるかをポイントという形で目視できる状態で提示します。
  いかに波を立てない状況（無に近いもの）が穏やかな状況であるかをユーザーに提供することが目的です
  本当はこちらを主軸にしたかったのですが、いろいろ調べたところ、多くのデータが必要になるため、簡単なミニ機能での実装を考えています。
  いかにデータを入力できるかでクオリティが左右されると考えています。


■ 機能の実装方針予定
一般的なCRUD以外の実装予定の機能についてそれぞれどのようなイメージ(使用するAPIや)で実装する予定なのか現状考えているもので良いので教えて下さい。

  Rails7で制作します。データベースはPostgreSqlを使います。
  esbuildを使用するためimportmap-railsは使用しません。

  ・pg：PostgreSQLを使用するため
  ・devise：外部認証を含めたログイン機能の実装とユーザー管理用
  ・MeCab：日本語の分解や検索を手助けするために導入
  ・Natto：MeCabと同じく、日本語の分解や検索を手助けするために導入
  ・bootstrap：フロントエンドのデザインのため
  ・esbuild：JavaScriptアプリケーションのビルドを高速化するため
  ・rails-i18n：国際化(i18n)を導入するため

  ＜下記は類似で他にいい物があったら変更する可能性があります＞
  ・carrierwave：ファイルアップロード機能のため
  ・kaminari：ページネーション
  ・ransack：検索フォームを作成するため
  ・Paper.js：まだ実装検討中の段階ですが、ユーザーの部屋の地図を作成できるようにし、探しものを記述できるようにする
  ・fabric.js：こちらはPaper.jsとCanvas要素の関係でうまく共存できない可能性があるようなので、検討中です…
  ・Twitter（X）API：一応SNSと連携できる機能を持たせるため…
  ・その他SNSのAPI：SNSに詳しくないためこちらは検討中です…
  ・メルカリAPI：可能なら不要なものをすぐ売れる機能をつけたいため、検討中です…

  ＜デバッグ用＞
  better_errors：デフォルトのエラー画面をわかりやすく整形するため	binding_of_caller：better_errorsと一緒に入れるといいもの
  byebug：希望の場所に「byebug」を入力し、変数の値を確認できるようにするため
  pry：プログラムが動いている途中で希望の場所で止められるようにするため
    ※pryの拡張機能として以下も導入
    pry-byebug
    pry-doc
    pry-rails
  listen：ファイルシステムの変更を監視するため
  rack-mini-profiler：画面が表示されるまでに実行されたメソッドとその処理時間を計測するため
  bullet：N+1クエリなどのパフォーマンス問題を検出するため