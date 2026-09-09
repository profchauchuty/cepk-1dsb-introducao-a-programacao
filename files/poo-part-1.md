# Programação Orientada a Objetos (POO)

## Elementos da POO

### 1. O que é Programação Orientada a Objetos?

A **POO** é um paradigma que organiza o código em **objetos**, que possuem:

- **Atributos:** características ou dados.
- **Métodos:** ações ou comportamentos.

Exemplo: em um sistema escolar, um `Aluno` pode ter os atributos `nome`, `idade`, `nota` e os métodos `calcularMedia()`, `aprovado()`, `exibirDados()`.

A ideia central da POO é **agrupar dados e comportamentos relacionados**.

---

### 2. Classe

Uma **classe** é o molde usado para criar objetos. Ela ainda não representa nada específico — apenas define o modelo.

**TypeScript**
```typescript
class Aluno {

}
```

**PHP**
```php
<?php

class Aluno {

}
```

**Python**
```python
class Aluno:
    pass
```

---

### 3. Objeto

Um **objeto** é uma instância de uma classe. A partir de uma classe podemos criar vários objetos, cada um com existência própria.

**TypeScript**
```typescript
const aluno1 = new Aluno();
const aluno2 = new Aluno();
```

**PHP**
```php
$aluno1 = new Aluno();
$aluno2 = new Aluno();
```

**Python**
```python
aluno1 = Aluno()
aluno2 = Aluno()
```

---

### 4. Atributos e Construtor

**Atributos** são as características de um objeto (ex: `nome`, `idade`, `nota`).

O **construtor** é um método especial, executado automaticamente ao criar o objeto, usado para inicializar os atributos.

| Linguagem | Construtor |
|-----------|------------|
| TypeScript | `constructor()` |
| PHP | `__construct()` |
| Python | `__init__()` |

**TypeScript**
```typescript
class Aluno {

    nome: string;
    idade: number;
    nota: number;

    constructor(nome: string, idade: number, nota: number) {
        this.nome = nome;
        this.idade = idade;
        this.nota = nota;
    }

}

const aluno = new Aluno("Maria", 16, 8.5);
console.log(aluno.nome);
```

**PHP**
```php
<?php

class Aluno {

    public string $nome;
    public int $idade;
    public float $nota;

    public function __construct(string $nome, int $idade, float $nota) {
        $this->nome = $nome;
        $this->idade = $idade;
        $this->nota = $nota;
    }

}

$aluno = new Aluno("Maria", 16, 8.5);
echo $aluno->nome;
```

**Python**
```python
class Aluno:

    def __init__(self, nome, idade, nota):
        self.nome = nome
        self.idade = idade
        self.nota = nota


aluno = Aluno("Maria", 16, 8.5)
print(aluno.nome)
```

---

### 5. Métodos

**Métodos** são funções pertencentes a uma classe, representando comportamentos do objeto.

**TypeScript**
```typescript
class Aluno {

    nota: number;

    constructor(nota: number) {
        this.nota = nota;
    }

    aprovado(): boolean {
        return this.nota >= 6;
    }

}

const aluno = new Aluno(8);
console.log(aluno.aprovado());
```

**PHP**
```php
<?php

class Aluno {

    public float $nota;

    public function __construct(float $nota) {
        $this->nota = $nota;
    }

    public function aprovado(): bool {
        return $this->nota >= 6;
    }

}

$aluno = new Aluno(8);
echo $aluno->aprovado();
```

**Python**
```python
class Aluno:

    def __init__(self, nota):
        self.nota = nota

    def aprovado(self):
        return self.nota >= 6


aluno = Aluno(8)
print(aluno.aprovado())
```

---

### 6. `this` e `self`

Dentro da classe, usamos uma referência ao próprio objeto para acessar seus atributos:

| Linguagem | Referência ao próprio objeto |
|-----------|------------------------------|
| TypeScript | `this` |
| PHP | `$this` |
| Python | `self` |

---

### 7. Modificadores de acesso: `public`, `private`, `protected`

- **`public`**: pode ser acessado de fora da classe.
- **`private`**: só pode ser acessado dentro da própria classe.
- **`protected`**: pode ser acessado pela própria classe e por suas subclasses.

**TypeScript**
```typescript
class Conta {

    private saldo: number = 0;

    depositar(valor: number): void {
        if (valor > 0) this.saldo += valor;
    }

    consultarSaldo(): number {
        return this.saldo;
    }

}
```

**PHP**
```php
<?php

class Conta {

    private float $saldo = 0;

    public function depositar(float $valor): void {
        if ($valor > 0) $this->saldo += $valor;
    }

    public function consultarSaldo(): float {
        return $this->saldo;
    }

}
```

**Python**
```python
class Conta:

    def __init__(self):
        self.__saldo = 0  # convenção de "privado"

    def depositar(self, valor):
        if valor > 0:
            self.__saldo += valor

    def consultar_saldo(self):
        return self.__saldo
```

---

# Exercícios

## PARTE 1 — Elementos da POO

**1. Classe e Objeto**
Crie uma classe `Pessoa` com os atributos `nome` e `idade`. Crie um objeto e exiba seus atributos.

**2. Construtor**
Crie uma classe `Produto` com os atributos `nome`, `preco` e `estoque`, inicializados por um construtor. Crie dois produtos diferentes e exiba seus dados.

**3. Métodos**
Crie uma classe `Aluno` com os atributos `nome` e `nota`. Implemente o método `aprovado()`, que deve retornar `true` quando a nota for maior ou igual a 6.

**4. `this` / `self`**
Crie uma classe `Retangulo` com os atributos `largura` e `altura`. Utilize `this` (ou `self`) para inicializá-los no construtor e implemente um método `calcularPerimetro()`.

**5. Modificadores de acesso**
Crie uma classe `ContaBancaria` com o atributo `saldo` como **privado**. Implemente os métodos `depositar(valor)` e `consultarSaldo()`, sem permitir que o saldo seja alterado diretamente.
