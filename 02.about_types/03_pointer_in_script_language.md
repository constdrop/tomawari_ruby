## 3. スクリプト言語におけるポインタ

スクリプト言語では、C言語などのコンパイル言語と異なり、ポインタを直接扱うことはできません。しかし、多くのスクリプト言語では、オブジェクト参照と呼ばれる仕組みによって、間接的にデータへのアクセスや操作を行うことができます。

### Rubyでのオブジェクト参照とは
Rubyにおいて、オブジェクト参照はオブジェクトへのポインタのようなものです。オブジェクト参照を使用すると、オブジェクトのプロパティやメソッドにアクセスしたり、オブジェクトの値を変更したりすることができます。オブジェクト参照は、オブジェクトを直接操作するのではなく、間接的に操作する方法を提供します。

### オブジェクト参照の利点
オブジェクト参照を使用する主な利点は、以下のとおりです。

* **安全性**: オブジェクト参照は、メモリ管理を自動的に行うため、C言語などの言語におけるポインタのようなメモリリークなどの問題が発生する可能性が低くなります。
* **使いやすさ**: オブジェクト参照は、C言語などの言語におけるポインタよりも使いやすく、初心者でも比較的簡単に理解できます。
* **柔軟性**: オブジェクト参照は、オブジェクトを共有したり、オブジェクト間で関係を構築したりするのに役立ちます。

### オブジェクトの作成と参照

```Ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end

  def name
    @name
  end

  def age
    @age
  end
end

person = Person.new("John Doe", 30)

# オブジェクト参照を使用してプロパティにアクセス
person.name # "John Doe"
person.age # 30
```

この例では、Person クラスの新しいインスタンスを作成し、person という名前の変数に格納します。その後、person オブジェクト参照を使用して、name と age プロパティにアクセスしています。

### オブジェクト参照の代入と変更

```Ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end

  def name
    @name
  end

  def name=(new_name)
    @name = new_name
  end

  def age
    @age
  end

  def age=(new_age)
    @age = new_age
  end
end

person = Person.new("John Doe", 30)

# オブジェクト参照を使用してプロパティの値を変更
person.name = "Jane Doe"
person.age = 31

# 変更後のプロパティの値を確認
person.name # "Jane Doe"
person.age # 31
```

この例では、Person クラスの新しいインスタンスを作成し、person という名前の変数に格納します。その後、person オブジェクト参照を使用して、name と age プロパティの値を変更しています。最後に、変更後のプロパティの値を確認しています。

### メソッドの呼び出し

```Ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end

  def name
    @name
  end

  def age
    @age
  end

  def introduce
    puts "私の名前は #{@name} です。年齢は #{@age} 歳です。"
  end
end

person = Person.new("John Doe", 30)

# オブジェクト参照を使用してメソッドを呼び出す
person.introduce # 私の名前は John Doe です。年齢は 30 歳です。
```

この例では、Person クラスの新しいインスタンスを作成し、person という名前の変数に格納します。その後、person オブジェクト参照を使用して、introduce メソッドを呼び出しています。introduce メソッドは、オブジェクトの名前と年齢を出力します。
