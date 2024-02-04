
Existem oito tipos básicos de dados em javascript

## [Número](https://javascript-info.translate.goog/types?_x_tr_sl=auto&_x_tr_tl=pt&_x_tr_hl=pt-BR#number)

```javascript
let n = 123;
n = 12.345;
```

O tipo number representa números inteiros e de ponto flutuante.

Existem muitas operações para números, por exemplo, multiplicação `*`, divisão `/`, adição `+`, subtração `-`e assim por diante.

Além dos números regulares, existem os chamados “valores numéricos especiais” que também pertencem a este tipo de dados `Infinity`:, `-Infinity`e `NaN`.

- `Infinity`representa o [infinito](https://translate.google.com/website?sl=auto&tl=pt&hl=pt-BR&u=https://en.wikipedia.org/wiki/Infinity) matemático ∞. É um valor especial maior que qualquer número.

	Podemos obtê-lo como resultado da divisão por zero:
```javascript
alert(1 / 0); // Infinity
```

Ou podemos apenas referencia-lo diretamente:
```javascript
alert( Infinity ); // Infinity
```

- `NaN`representa um erro computacional. É o resultado de uma operação matemática incorreta ou indefinida, por exemplo:
```javascript
alert( "not a number" / 2); // NaN, such division is erroneous
```

BigInt
Em Javascript, o tipo "número" não pode representar com segurança inteiros maiores (até), mas fora do intervalo seguro de números inteiros haverá um erro de precisão, por que nem todos os dígitos cabem no armazenamento fixo de 64 bits. Portando, um valor "aproximado" pode ser armazenado. `1.7976931348623157 * 10308``±(253-1)`

Por exemplo, estes dois números (logo acima da faixa segura) são iguais.

```javascript
console.log(9007199254740991 + 1); // 9007199254740992
console.log(9007199254740991 + 2); // 9007199254740992
```
Por assim dizer, todos os números inteiros ímpares maiores que não podem ser armazenados no tipo “número”.`(253-1)`

Para a maioria dos propósitos , o intervalo é suficiente, mas às vezes precisamos de todo o intervalo de números inteiros realmente grandes, por exemplo, para criptografia ou carimbos de data e hora com precisão de microssegundos.`±(253-1)`

`BigInt`type foi adicionado recentemente à linguagem para representar números inteiros de comprimento arbitrário.

Um `BigInt`valor é criado anexando `n`ao final de um número inteiro:

```javascript
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```
Como `BigInt`os números raramente são necessários, não os abordamos aqui, mas dedicamos a eles um capítulo separado [BigInt](https://javascript-info.translate.goog/bigint?_x_tr_sl=auto&_x_tr_tl=pt&_x_tr_hl=pt-BR) . Leia quando precisar de números tão grandes.




