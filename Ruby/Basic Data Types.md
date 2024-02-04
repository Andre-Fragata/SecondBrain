Numbers 
```ruby
# Addition
1 + 1   #=> 2

# Subtraction
2 - 1   #=> 1

# Multiplication
2 * 2   #=> 4

# Division
10 / 5  #=> 2

# Exponent
2 ** 2  #=> 4
3 ** 4  #=> 81

# Modulus (find the remainder of division)
8 % 2   #=> 0  (8 / 2 = 4; no remainder)
10 % 4  #=> 2  (10 / 4 = 2 with a remainder of 2)
```

Integers and Floats
```ruby
17 / 5    #=> 3, not 3.4

17 / 5.0  #=> 3.4
```

Converting Number Types
```ruby
# To convert an integer to a float:
13.to_f   #=> 13.0

# To convert a float to an integer:
13.0.to_i #=> 13
13.9.to_i #=> 13
```

Some useful number methods 
Theere are many useful methods for numbers build into Ruby. For example, 
```portuguese
Alguns métodos numéricos úteis

Existem muitos métodos úteis para números incorporados ao Ruby. Por exemplo
```

even?

```ruby
6.even? #=> true
7.even? #=> false
```

odd?

```ruby
6.odd? #=> false
7.odd? #=> true
```

Strings

At first glance, you might think that strings are just a bunch of characters that aren’t very useful beyond getting user input and outputting some information to the screen, but like Burt Reynolds passing up the chance to play Han Solo, you’d be wrong. Very wrong. What were you thinking, Burt?

```portuguese
À primeira vista, você pode pensar que strings são apenas um monte de caracteres que não são muito úteis além de obter a entrada do usuário e enviar algumas informações para a tela, mas como Burt Reynolds desperdiçando a chance de interpretar Han Solo, você estaria errado. Muito errado. O que você estava pensando, Burt?
```

Concatenation

In true Ruby style, there are plenty of ways to concatenate strings.

```portuguese
No verdadeiro estilo Ruby, existem muitas maneiras de concatenar strings.
```

```ruby
# With the plus operator:
"Welcome " + "to " + "Odin!"    #=> "Welcome to Odin!"

# With the shovel operator:
"Welcome " << "to " << "Odin!"  #=> "Welcome to Odin!"

# With the concat method:
"Welcome ".concat("to ").concat("Odin!")  #=> "Welcome to Odin!"
```

#### Substrings

You can access strings inside strings. Stringception! It’s super easy, too.
```portuguese
Você pode acessar strings dentro de strings. Stringcepção! Também é muito fácil.
```

```ruby
"hello"[0]      #=> "h"

"hello"[0..1]   #=> "he"

"hello"[0, 4]   #=> "hell"

"hello"[-1]     #=> "o"
```

In the above example we can access the individual characters of a string by referencing the index(es) of the character within the string using `[]`. For more information on the topic you can read the [method documentation](https://docs.ruby-lang.org/en/3.2/String.html#class-String-label-String+Slices).

```portuguese
No exemplo acima, podemos acessar os caracteres individuais de uma string referenciando o(s) índice(s) do caractere dentro da string usando []. Para mais informações sobre o tema você pode ler a documentação do método.
```


Escape Characters

Escape characters allow you to type in representations of whitespace characters and to include quotation marks inside your string without accidentally ending it. As a reminder, escape characters only work inside double quotation marks.

```portuguese
Os caracteres de escape permitem que você digite representações de caracteres de espaço em branco e inclua aspas dentro da string sem terminá-la acidentalmente. Como lembrete, os caracteres de escape só funcionam entre aspas duplas.
```

```ruby
\\  #=> Need a backslash in your string?
\b  #=> Backspace
\r  #=> Carriage return, for those of you that love typewriters
\n  #=> Newline. You'll likely use this one the most.
\s  #=> Space
\t  #=> Tab
\"  #=> Double quotation mark
\'  #=> Single quotation mark
```

```ruby
irb(main):001:0> puts "Hello \n\nHello"
Hello

Hello
=> nil
```

Interpolation

String interpolation allows you to evaluate a string that contains placeholder variables. This is a very useful and common technique, so you will likely find yourself using this often. Be sure to use double quotes so that string interpolation will work!

```portuguese 
A interpolação de string permite avaliar uma string que contém variáveis ​​de espaço reservado. Esta é uma técnica muito útil e comum, então provavelmente você a usará com frequência. Certifique-se de usar aspas duplas para que a interpolação de strings funcione!
```

```ruby
name = "Odin"

puts "Hello, #{name}" #=> "Hello, Odin"
puts 'Hello, #{name}' #=> "Hello, #{name}"
```

Common String Methods

There are many useful string methods that are built into Ruby. You need to capitalize a word? No problem! Reverse a string? Easy peasy. Extract the binary subatomic algorithm from any regex grep? We don’t know, but since this is Ruby, let’s go with YES.

```portuguese
Existem muitos métodos de string úteis incorporados ao Ruby. Você precisa colocar uma palavra em maiúscula? Sem problemas! Inverter uma string? Mole-mole. Extraia o algoritmo subatômico binário de qualquer regex grep? Não sabemos, mas como se trata de Ruby, vamos SIM.
```

Capitalize 
```ruby
"hello".capitalize #=> "Hello"
```

Include
```ruby
"hello".include?("lo")  #=> true

"hello".include?("z")   #=> false
```

Upcase
```ruby
"hello".upcase  #=> "HELLO"
```

Downcase
```ruby
"Hello".downcase  #=> "hello"
```

Empty?
```ruby
"hello".empty?  #=> false

"".empty?       #=> true
```

Lenght
```ruby
"hello".length  #=> 5
```

Reverse
```ruby
"hello".reverse  #=> "olleh"
```

Split
```ruby
"hello world".split  #=> ["hello", "world"]

"hello".split("")    #=> ["h", "e", "l", "l", "o"]
```

Strip
```ruby
" hello, world   ".strip  #=> "hello, world"
```

You’ll read more about these methods and others in the assignment. The examples below are just to get your creative juices flowing with some of the awesome ways you can modify strings.

```portuguese
Você lerá mais sobre esses métodos e outros na tarefa. Os exemplos abaixo são apenas para fazer fluir sua criatividade com algumas das maneiras incríveis de modificar cordas.
```

```ruby
"he77o".sub("7", "l")           #=> "hel7o"

"he77o".gsub("7", "l")          #=> "hello"

"hello".insert(-1, " dude")     #=> "hello dude"

"hello world".delete("l")       #=> "heo word"

"!".prepend("hello, ", "world") #=> "hello, world!"
```

The assignments will go much deeper, so go through them thoroughly and be sure to play around in a REPL as you read.

```portuguese
As tarefas serão muito mais profundas, portanto, analise-as minuciosamente e certifique-se de brincar com um REPL enquanto lê.
```

Converting other Objects to Strings

Using the to_s method, you can convert pretty much anything to a string. Here are some examples:

```portuguese
Usando o método to_s, você pode converter praticamente qualquer coisa em uma string. aqui estão alguns exemplos:
```

```ruby
5.to_s        #=> "5"

nil.to_s      #=> ""

:symbol.to_s  #=> "symbol"
```

Symbols

Symbols are an interesting twist on the idea of a string. The full explanation can be a bit long, but here’s the short version:

Strings can be changed, so every time a string is used, Ruby has to store it in memory even if an existing string with the same value already exists. Symbols, on the other hand, are stored in memory only once, making them faster in certain situations.

One common application where symbols are preferred over strings are the keys in hashes. We’ll cover this in detail in the hashes lesson later in the course.

You won’t need to use symbols much in the beginning, but it’s good to get familiar with what they are and what they look like so that you can recognize them.

```portuguese
Os símbolos são uma variação interessante da ideia de uma corda. A explicação completa pode ser um pouco longa, mas aqui está a versão resumida:

Strings podem ser alteradas, então toda vez que uma string é usada, Ruby tem que armazená-la na memória, mesmo que já exista uma string existente com o mesmo valor. Os símbolos, por outro lado, são armazenados na memória apenas uma vez, tornando-os mais rápidos em determinadas situações.

Uma aplicação comum onde os símbolos são preferidos às strings são as chaves em hashes. Abordaremos isso em detalhes na lição sobre hashes posteriormente neste curso.

Você não precisará usar muito símbolos no início, mas é bom se familiarizar com o que eles são e sua aparência para poder reconhecê-los.
```

Create a Symbol

To create a symbol, put a colon at the beginning of some text:

```portuguese
Para criar um símbolo, coloque dois pontos no início de algum texto:
```

```ruby
:my_symbol
```

Symbols vs. Strings

To get a better idea of how symbols are stored in memory, give this a whirl in irb or a REPL. The [`#object_id` method](https://docs.ruby-lang.org/en/3.2/Object.html#method-i-object_id) returns an integer identifier for an object. (And remember: in Ruby, _everything_ is an object!)

```portuguese
Para ter uma ideia melhor de como os símbolos são armazenados na memória, experimente irb ou REPL. O método #object_id retorna um identificador inteiro para um objeto. (E lembre-se: em Ruby, tudo é um objeto!)
```

```ruby
"string" == "string"  #=> true

"string".object_id == "string".object_id  #=> false

:symbol.object_id == :symbol.object_id    #=> true
```


Booleans

You will learn about these data types in more detail in the Conditional Logic lesson later in this course. The goal of this lesson is for you to get a basic understanding of what Booleans are.
True and false

The Boolean values true and false represent exactly what you think they do: true represents something that is true, and false represents something that is false.
Nil

In Ruby, nil represents “nothing”. Everything in Ruby has a return value. When a piece of code doesn’t have anything to return, it will return nil. This is pretty abstract, but it will make more sense as you learn and use Ruby more.

```portuguese
Booleanos

Você aprenderá sobre esses tipos de dados com mais detalhes na lição Lógica Condicional posteriormente neste curso. O objetivo desta lição é que você obtenha uma compreensão básica do que são booleanos.
Verdadeiro e falso

Os valores booleanos verdadeiro e falso representam exatamente o que você pensa que eles representam: verdadeiro representa algo que é verdadeiro e falso representa algo que é falso.
Nada

Em Ruby, nil representa “nada”. Tudo em Ruby tem um valor de retorno. Quando um trecho de código não tem nada para retornar, ele retornará nulo. Isso é bastante abstrato, mas fará mais sentido à medida que você aprender e usar mais Ruby.
```

### [Additional resources](https://www.theodinproject.com/lessons/ruby-basic-data-types#additional-resources)

This section contains helpful links to other content. It isn’t required, so consider it supplemental.

- If you want to go deeper into Ruby’s numbers and string data types, read these chapters from the _Bastards Book of Ruby_:
    - [Numbers](http://ruby.bastardsbook.com/chapters/numbers/)
    - [Strings](http://ruby.bastardsbook.com/chapters/strings/)
- Read through these Ruby Monstas sections about data types:
    - [Numbers](http://ruby-for-beginners.rubymonstas.org/built_in_classes/numbers.html)
    - [Strings](http://ruby-for-beginners.rubymonstas.org/built_in_classes/strings.html)
    - [Symbols](http://ruby-for-beginners.rubymonstas.org/built_in_classes/symbols.html)
    - [True, False, and Nil](http://ruby-for-beginners.rubymonstas.org/built_in_classes/true_false_nil.html)

Knowledge check
- Numbers
    - [What are the basic arithmetic operators you can use on numbers?](https://www.theodinproject.com/lessons/ruby-basic-data-types#numbers)
    - [What’s the difference between an integer and a float?](https://www.theodinproject.com/lessons/ruby-basic-data-types#integers-and-floats)
    - [What method would you use to convert a float to an integer?](https://www.theodinproject.com/lessons/ruby-basic-data-types#converting-number-types)
    - [What method would you use to convert an integer to a float?](https://www.theodinproject.com/lessons/ruby-basic-data-types#converting-number-types)
- Strings
    - [What is a string?](https://www.theodinproject.com/lessons/ruby-basic-data-types#strings)
    - [What are the differences between single and double quotes?](https://www.theodinproject.com/lessons/ruby-basic-data-types#double-and-single-quotation-marks)
    - [What is string interpolation?](https://www.theodinproject.com/lessons/ruby-basic-data-types#interpolation)
    - [How do you concatenate strings?](https://www.theodinproject.com/lessons/ruby-basic-data-types#concatenation)
    - [What method would you use to change all the characters in your string to upper case?](https://www.theodinproject.com/lessons/ruby-basic-data-types#upcase)
    - [What method would you use to split up strings into arrays?](https://www.theodinproject.com/lessons/ruby-basic-data-types#split)
    - [What are escape characters?](https://www.theodinproject.com/lessons/ruby-basic-data-types#escape-characters)
    - [How do you access a specific character or substring?](https://www.theodinproject.com/lessons/ruby-basic-data-types#substrings)
    - [How do you convert other data types into strings?](https://www.theodinproject.com/lessons/ruby-basic-data-types#converting-other-objects-to-strings)
- Symbols
    - [What is a symbol?](https://www.theodinproject.com/lessons/ruby-basic-data-types#symbols)
    - [How do you create a symbol?](https://www.theodinproject.com/lessons/ruby-basic-data-types#create-a-symbol)
    - [What’s the difference between a symbol and a string?](https://www.theodinproject.com/lessons/ruby-basic-data-types#symbols-vs-strings)
- Booleans
    - [What does `true` represent?](https://www.theodinproject.com/lessons/ruby-basic-data-types#true-and-false)
    - [What does `false` represent?](https://www.theodinproject.com/lessons/ruby-basic-data-types#true-and-false)
    - [What does `nil` represent?](https://www.theodinproject.com/lessons/ruby-basic-data-types#nil)