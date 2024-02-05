Variables are a way of assigning data to names in your programs. You can think of a variable as a box with a label on it: it stores something and has a name so that you know what’s inside. This is an imperfect metaphor as you’ll see by the end of this lesson, but it should help with understanding variables for now.

```portuguese
Variáveis ​​são uma forma de atribuir dados a nomes em seus programas. Você pode pensar em uma variável como uma caixa com um rótulo: ela armazena algo e tem um nome para que você saiba o que há dentro dela. Esta é uma metáfora imperfeita, como você verá no final desta lição, mas deve ajudar na compreensão das variáveis ​​por enquanto.
```


Declaring a Variable

This is how to create a variable in Ruby.
```portuguese
Veja como criar uma variável em Ruby
```

```ruby
age = 18 #=> 18
```

You can also assign the result of an expression to a variable
```portuguese
Você também pode atribuir o resultado de uma expressão a uma variável.
```

```ruby
age = 18 + 5 #=> 23
```

Variable names are reusable, so you can assign a new value to a variable at any point in your program. Naturally, doing so will override the original value.

```portuguese
Os nomes das variáveis ​​são reutilizáveis, portanto você pode atribuir um novo valor a uma variável em qualquer ponto do seu programa. Naturalmente, isso substituirá o valor original.
```

```ruby
age = 18
age #=> 18
age = 33
age #=> 33
```

There will often be scenarios where you want to perform an operation on the original value of a variable and then reassign the result of that operation to the same variable.

```portuguese
Frequentemente, haverá cenários em que você deseja executar uma operação no valor original de uma variável e, em seguida, reatribuir o resultado dessa operação à mesma variável.
```

```ruby
age = 18
age #=> 18
age = age + 4
age #=> 22
```

Because this is a common scenario, Ruby provides a nice shorthand assignment operator for doing this: +=.

```portuguese
Como esse é um cenário comum, Ruby fornece um ótimo operador de atribuição abreviado para fazer isso: +=.
```

```ruby
age = 18
age += 4 #=> 22
```

There are similar assignment operators for all the common math operators:

```portuguese
Existem operadores de atribuição semelhantes para todos os operadores matemáticos comuns:
```

```ruby
age = 18
age -= 2  #=> 16

cash = 10
cash *= 2 #=> 20

temperature = 40
temperature /= 10 #=> 4
```

How to name variables

Ruby is a language that aims to be natural to read and easy to write. Remember this when you’re naming your variables. The name should, as clearly as possible, describe what the value of the variable represents.

Naming variables clearly will pay dividends when you review your code months after you’ve written it, when you can no longer remember what that variable was designed to store. From now on, when naming your variables, remember the following quote by John Woods:

> Always code as if the person who ends up maintaining your code will be a violent psychopath who knows where you live.

The most basic thing you can do to write clean, maintainable code is to name your variables properly. So get into this habit early to avoid psychopath programmers coming after you.

Variable names should always be lowercase, and multiple words that make up a variable name should be split by an underscore. This is known as **snake_case**.

```portuguese
Ruby é uma linguagem que pretende ser natural de ler e fácil de escrever. Lembre-se disso ao nomear suas variáveis. O nome deve descrever, da forma mais clara possível, o que o valor da variável representa.

Nomear variáveis ​​claramente renderá dividendos quando você revisar seu código meses depois de escrevê-lo, quando você não conseguir mais lembrar o que aquela variável foi projetada para armazenar. De agora em diante, ao nomear suas variáveis, lembre-se da seguinte citação de John Woods:

Sempre codifique como se a pessoa que acabaria mantendo seu código fosse um psicopata violento que sabe onde você mora.

A coisa mais básica que você pode fazer para escrever um código limpo e de fácil manutenção é nomear suas variáveis ​​corretamente. Portanto, adquira esse hábito cedo para evitar que programadores psicopatas venham atrás de você.

Os nomes das variáveis ​​devem sempre estar em letras minúsculas e as múltiplas palavras que compõem um nome de variável devem ser divididas por um sublinhado. Isso é conhecido como Snake_case.
```

```ruby
# bad
a = 19
string = "John"

# good
age = 19
name = "John"
can_swim = false
```

Variables are references

The information you name with a variable is stored in memory on your computer, so a variable is effectively a reference or a pointer to that address in memory. This is important to know as it can sometimes be the cause of unexpected behavior from your code.

Let’s look at an example of this unexpected behavior, with two variables: desired_location, which is assigned to the string “Barcelona”, and johns_location, which is assigned to the desired_location variable. Both variables are pointing to where “Barcelona” is stored in memory.

```portuguese
Variáveis ​​são referências

As informações que você nomeia com uma variável são armazenadas na memória do seu computador, portanto, uma variável é efetivamente uma referência ou um ponteiro para esse endereço na memória. É importante saber disso, pois às vezes pode ser a causa de um comportamento inesperado do seu código.

Vejamos um exemplo desse comportamento inesperado, com duas variáveis: local_desejado, que é atribuído à string “Barcelona”, e local_de_johns, que é atribuído à variável local_desejado. Ambas as variáveis ​​apontam para onde “Barcelona” está armazenado na memória.
```

```ruby
desired_location = "Barcelona"
johns_location = desired_location

desired_location  #=> "Barcelona"
johns_location    #=> "Barcelona"
```

Unexpected behavior happens if the string “Barcelona” that is stored in memory is modified. One way to modify a string is to use the `upcase!` method, instead of the safe `upcase` method. If the string is modified using `johns_location.upcase!` then `desired_location` will also reflect that change:

```portuguese
Comportamento inesperado acontece se a string “Barcelona” que está armazenada na memória for modificada. Uma maneira de modificar uma string é usar maiúsculas! método, em vez do método upcase seguro. Se a string for modificada usando johns_location.upcase! então o local desejado também refletirá essa alteração:
```

```ruby
johns_location.upcase!  #=> "BARCELONA"

desired_location        #=> "BARCELONA"
johns_location          #=> "BARCELONA"
```

### [Additional resources](https://www.theodinproject.com/lessons/ruby-variables#additional-resources)

This section contains helpful links to other content. It isn’t required, so consider it supplemental.

- Read the full [Variables](http://ruby.bastardsbook.com/chapters/variables) chapter from _The Bastards Book of Ruby_ if you can’t get enough about variables.
- To dive deeper into how variables point to memory locations on your computer, go through these short sections:
    - [Variables as Pointers](https://launchschool.com/books/ruby/read/more_stuff#variables_as_pointers), from LaunchSchool’s _Introduction to Programming With Ruby_.
    - [A visual guide to variables](http://ruby.bastardsbook.com/chapters/variables/#visual-guide) from the [Variables](http://ruby.bastardsbook.com/chapters/variables) chapter of _The Bastards Book of Ruby_
- If you want to know more about Ruby’s naming conventions, check out the [Ruby Style Guide](https://github.com/rubocop-hq/ruby-style-guide). Don’t get too deep into it; just know that it’s there.