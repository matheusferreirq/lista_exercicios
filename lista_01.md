# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
**a) A saída será undefined seguido de erro** 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

**RESPOSTA:** Alternativa A.
**JUSTIFICATIVA:** No primeiro "console.log", o "var" faz com que a variável possa ser chamada em qualquer parte do código. Entretanto, seu valor só é atribuído após a execução das linhas de código, o que resulta em "undefined". Já no segundo "console.log", o "let" permite que a variável seja acessada apenas no escopo em que é definida. Nesse caso, ela não é atribuída no escolo do "console.log" e, por isso, resulta em erro.



**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

**a) Substituir if (a || b === 0) por if (a === 0 || b === 0)**

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

**RESPOSTA:** Alternativa A.
**JUSTIFICATIVA:** Nesse caso, nenhum operador lógico de comparação é utilizado com "a", tornando sua condição sempre verdadeira independente do valor (que não seja 0, NaN, undefined ou null). Assim, é verificado apenas se "b" é igual a 0 que, nesse situação, é também verdadeira, resultando em "Erro: número inválido.". Para resolver, deve-se adicionar o mesmo operador lógico para verificar se a condição "a === 0" para que o erro seja realmente válido.

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

**b) O código imprime 200.**

c) O código imprime 50.

d) O código gera um erro.

**RESPOSTA:** Alternativa B.
**JUSTIFICATIVA:** O valor impresso será 200 pois, no código, ainda que o tipo requisitado tenha sido "eletrônico", seu case não possui a condição de "break" caso seja verdadeiro, fazendo com que o código continue a rodar até o break do tipo "vestuário", que possui o "preco" 200.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

**d) 24**

**RESPOSTA:** Alternativa D.
**JUSTIFICATIVA:** Primeiramente,a função ```numeros.map(x => x * 2)``` cria um novo array onde todos os seus elementos são multiplicados por 2, resultando em ``` numeros = [2, 4, 6, 8, 10] ```. Após isso, a função ```filter(x => x > 5)``` filtra os números que atendem a condição x > 5, resultando em ``` numeros = [6, 8, 10] ```. Em seguida, a função ```.reduce((a, b) => a + b, 0)``` soma todos os elementos do array e, portanto, 6 + 8 + 10 = 24
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

**c) ["banana", "abacaxi", "manga", "laranja"]**

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

**RESPOSTA:** Alternativa C.
**JUSTIFICATIVA:** A função ```lista.splice(1, 2, "abacaxi", "manga");``` substitui os valores do array nas posições "1" e "2", pelo valores "abacaxi" e "manga" respectivamente. Assim, o array é impresso como na alternativa C.
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


**a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.**

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

**RESPOSTA:** Alternativa A.
**JUSTIFICATIVA:** Ambas as alternativas são corretas. A herança de classes possibilita que uma classe herde métodos e atributos de outra, reduzindo as linhas de código necessárias. Para isso, utiliza-se a palavra-chave 'extends' para sua implementação
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

**a) I e II são verdadeiras.**

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

**RESPOSTA:** Alternativa A.
**JUSTIFICATIVA:** A opção I é verdadeira pois a palavra-chave ```extends``` + a classe Pessoa ao declarar a classe funcionário explicita a herança e pode acessar os atributos nome e idade diretamente a partir do método ```super()```. A opção II é também verdadeira pois realmente sobrepõe o método ```apresentar()``` herdando o método da classe pai.
______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

**b) A asserção é verdadeira e a razão é falsa.**

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

**RESPOSTA:** Alternativa B.
**JUSTIFICATIVA:** A asserção sobre o conceito de polimorfismo é verdadeira, o qual realmente permite objetos de diferentes tipos responderem à mesma mensagem de maneiras diferentes. Já a razão está incorreta, já que o JavaScript não suporta sobrecarga de métodos em uma classe. Isso ocorre por meio de substituição de métodos.
______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

**RESPOSTA:**
```
var numeros = [];

function somaArray(numeros) {
    var soma = 0
    for (i = 0; i < numeros.length; i++) {
        soma += numeros[i];
    }
    return soma * 2;
}
console.log(somaArray([1, 2, 3, 4]));
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

**RESPOSTA:**
```
/*10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.*/

class Produto {
    constructor(nome, preco) {
        this.nome = nome
        this.preco = preco
    }

    calcularDesconto() {
        var desconto = this.preco * 0.1
        var valorFinal = this.preco - desconto
        console.log("O produto '" + this.nome + "' possui um desconto de " + desconto.toFixed(1) + "% e, portanto, custa R$" + valorFinal.toFixed(2));
    }
}

class Livro extends Produto {
    constructor(nome, preco) {
        super(nome, preco);
    }

    calcularDescontoDoLivro() {
        var descontoLivro = this.preco * 0.2
        var valorFinalLivro = this.preco - descontoLivro
        console.log("O livro '" + this.nome + "' possui desconto de " + descontoLivro.toFixed(1) + "% e, portanto, custa R$" + valorFinalLivro.toFixed(2))
    }
}

var product = new Produto("Copo", 50);
product.calcularDesconto();

var book = new Livro("As Crônicas de Narnia", 100)
book.calcularDescontoDoLivro()

var product2 = new Produto ("Colher", 11.50)
product2.calcularDesconto()
```
