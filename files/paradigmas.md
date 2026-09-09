# Paradigmas de Programação

## 1. O que é um Paradigma de Programação?

Um paradigma de programação é uma **forma de organizar e estruturar** a solução de um problema utilizando código.

Cada paradigma possui características próprias e uma **maneira diferente de pensar** o desenvolvimento de software.

Os três paradigmas mais conhecidos são:

- Programação Estruturada
- Programação Funcional
- Programação Orientada a Objetos

Atualmente, muitas linguagens suportam mais de um paradigma ao mesmo tempo, como JavaScript/Typescript, Python e PHP.

---

## 2. Programação Estruturada

A Programação Estruturada **organiza o programa como uma sequência de instruções executadas passo a passo**.

Seu foco está na definição de algoritmos utilizando estruturas de controle como:

- Sequência
- Decisão (`if` e `else`)
- Repetição (`for`, `while`, `do while`)
- Funções e procedimentos

Nesse paradigma, os dados e as funções normalmente ficam separados.

### Exemplo

```javascript
function calcularMedia(n1, n2) {
    return (n1 + n2) / 2;
}

let media = calcularMedia(8, 6);

if (media >= 6) {
    console.log("Aprovado");
} else {
    console.log("Reprovado");
}
```

### Características

- Simples de aprender.
- Fácil para programas pequenos.
- Utiliza funções para organizar o código.
- Baseada em algoritmos e fluxo de execução.
- Pode se tornar difícil de manter em sistemas muito grandes.

### Como o problema é visto?

O programador pensa:

> "Quais passos preciso executar para resolver o problema?"

---

## 3. Programação Funcional

A Programação Funcional trata o **programa como uma combinação de funções matemáticas**.

Nesse paradigma, as funções recebem dados de entrada e retornam resultados, **evitando alterar variáveis externas sempre que possível**.

Uma função idealmente deve produzir sempre o mesmo resultado para a mesma entrada.

### Exemplo

```javascript
function quadrado(numero) {
    return numero * numero;
}

console.log(quadrado(5));
```

Resultado:

```text
25
```

### Características

- Prioriza funções.
- Evita alterar dados existentes.
- Favorece reutilização de código.
- Facilita testes.
- Muito utilizada em Ciência de Dados e Inteligência Artificial.

### Exemplo com vetor

```javascript
const numeros = [1, 2, 3, 4, 5];

const dobrados = numeros.map(numero => numero * 2);

console.log(dobrados);
```

Resultado:

```text
[2, 4, 6, 8, 10]
```

### Como o problema é visto?

O programador pensa:

> "Quais transformações devem ser aplicadas aos dados?"

---

## 4. Programação Orientada a Objetos

A Programação Orientada a Objetos (POO) **organiza o sistema em objetos**.

Um objeto representa algo do mundo real e possui:

- Atributos (dados)
- Métodos (ações)

Os objetos interagem entre si para realizar tarefas.

### Exemplo

```javascript
class Aluno {

    constructor(nome, nota) {
        this.nome = nome;
        this.nota = nota;
    }

    aprovado() {
        return this.nota >= 6;
    }

}

const aluno = new Aluno("Maria", 8);

console.log(aluno.aprovado());
```

Resultado:

```text
true
```

### Características

- Organiza dados e comportamentos juntos.
- Facilita manutenção de sistemas grandes.
- Permite reutilização de código.
- Aproxima o código de situações do mundo real.
- Muito utilizada em sistemas corporativos.

### Como o problema é visto?

O programador pensa:

> "Quais objetos existem no sistema e como eles interagem?"

---

## 5. Comparação entre os Paradigmas

| Aspecto | Estruturada | Funcional | Orientada a Objetos |
|----------|------------|-----------|---------------------|
| Organização | Funções e algoritmos | Funções | Objetos |
| Foco | Passos da solução | Transformação de dados | Modelagem do mundo real |
| Estado dos dados | Variáveis modificáveis | Preferência por dados imutáveis | Objetos possuem estado |
| Reutilização | Funções | Composição de funções | Classes e objetos |
| Facilidade para iniciantes | Alta | Média | Média |
| Sistemas grandes | Limitada | Boa | Excelente |

---

## 6. Exemplos

Imagine que precisamos representar um aluno.

### Estruturada

```javascript
let nome = "Maria";
let nota = 8;

function aprovado(nota) {
    return nota >= 6;
}
```

### Funcional

```javascript
function aprovado(nota) {
    return nota >= 6;
}

console.log(aprovado(8));
```

### Orientada a Objetos

```javascript
class Aluno {

    constructor(nome, nota) {
        this.nome = nome;
        this.nota = nota;
    }

    aprovado() {
        return this.nota >= 6;
    }

}
```

Observe que o problema é o mesmo, mas cada paradigma o organiza de maneira diferente.

---

## 7. Linguagens e Paradigmas

| Linguagem | Estruturada | Funcional | POO |
|------------|------------|------------|------|
| C | Sim | Não | Não |
| JavaScript | Sim | Sim | Sim |
| Typescript | Sim | Sim | Sim |
| Java | Parcial | Parcial | Sim |
| C# | Sim | Parcial | Sim |
| Python | Sim | Sim | Sim |
| PHP | Sim | Parcial | Sim |

Muitas linguagens modernas são multiparadigma, permitindo combinar diferentes estilos de programação.

---

## 8. Conclusão

Os paradigmas de programação representam diferentes maneiras de organizar e resolver problemas computacionais.

- A Programação Estruturada foca nos passos necessários para resolver um problema.
- A Programação Funcional foca na transformação de dados através de funções.
- A Programação Orientada a Objetos foca na modelagem de objetos e suas interações.

Não existe um paradigma melhor para todas as situações. Cada um possui vantagens e é mais adequado para determinados tipos de aplicações.

---

# Exercícios

1. Explique com suas palavras a principal diferença entre Programação Estruturada, Programação Funcional e Programação Orientada a Objetos.

---

2. Analise o código abaixo e indique a qual paradigma ele mais se aproxima.

```javascript
function soma(a, b) {
    return a + b;
}

console.log(soma(5, 3));
```

---

3. Analise o código abaixo e indique a qual paradigma ele mais se aproxima.

```javascript
class Produto {

    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
    }

}
```

---

4. Crie um exemplo simples de função que receba um número e retorne seu dobro.

Explique por que esse exemplo pode ser associado à Programação Funcional.

---

5. Uma escola deseja desenvolver um sistema para cadastrar alunos, professores, turmas e notas.

Qual paradigma seria mais adequado para esse sistema?
