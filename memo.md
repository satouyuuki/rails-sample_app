generateの打ち消しコマンドdestory

このメソッドはいろんなところで使うな
  def setup
    @base_title = "Ruby on Rails Tutorial Sample App"
  end

基本的に文字列はダブルクオートを使おう。式が展開されないから

!!」(「バンバン (bang bang)」と読みます)初めて知った。二重否定だからどんなオブジェクトでも強制的に論理知になる。
false, nillはfalse
0はtrue

def string_message(str = '')
  if str.empty?
    "It's an empty string!"
  else
    "The string is nonempty."
  end
end

defで定義したものが
:string_messageみたいに先頭にコロンがつく

def palindrome_tester(s)
  if s == s.reverse
    puts "It's a palindrome!"
  else
    puts "It's not a palindrome."
  end
end

配列の最後はa.last とa[-1]で求められる

破壊的メソッドを使うにはメソッドの末尾に!をつける
使うときなさそう

範囲オブジェクトというオブジェクトがある

# ループ
{}で囲むかdo endでかく
(1..5).each{|i| puts 2 * i}

(1..5).each do |i|
  put 2 * i
end
数値が決まっていたら(1..5) も良いかも
3.timesもループ
mapはjavascriptとにてる

# ハッシュとシンボル
意味わかんないかも
ハッシュ＝連想配列
記法はjsの{}ポイ

ハッシュではシンボルをキーとして使うのが慣習
シンボルをjsのように後ろコロンにすることもできる
つまりjsのようにかける
{key: value}
{:key => value}

ハッシュ(object)はネストもできる

stylesheet_link_tag 'application', media: 'all',
'data-turbolinks-track': 'reload'

# メソッド呼び出しの丸カッコは省略可能。
stylesheet_link_tag('application', media: 'all',
'data-turbolinks-track': 'reload')
# 最後の引数がハッシュの場合、波カッコは省略可能。
stylesheet_link_tag 'application', { media: 'all',
'data-turbolinks-track': 'reload' }

# クラス
sはStringクラスのインスタンス変数
"foobar"は引数
暗黙のリテラルコンストラクタ
s = "foobar"
明示的にした場合
s = String.new("foobar")同等のこと

ハッシュ(Object)の場合は代入する値はデフォルトのシンボルのvalueになる
# 継承
String->Object->BasicObject

class Word
  def palindrome?(string)
    string == string.reverse
  end
end

class Word < String
  def palindrome?
    self == self.reverse
  end
end
String

# Q.組み込みクラスの変更できるの？
できるStringクラスを拡張できる

アクティブサポートでrailsはrubyを拡張している

エラスティックサーチ

8/9
パーシャルで肥大化したコードを分割することができる
<%= render 'layout/shim' %>

error 統合テスト時 add `gem 'rails-controller-testing'`