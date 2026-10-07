### Os Quatro Pilares da POO

| Pilar | Descrição |
|-------|-----------|
| Herança | Reutilização de características e comportamentos entre classes |
| Encapsulamento | Proteção e controle dos dados internos do objeto |
| Polimorfismo | Diferentes comportamentos para uma mesma operação |
| Abstração | Representação apenas das características relevantes |

---

### 1. Herança

Permite que uma classe (**subclasse**) reaproveite atributos e métodos de outra (**superclasse**), podendo também sobrescrever comportamentos.

**TypeScript**
```typescript
class Pessoa {

    constructor(public nome: string) {}

    apresentar(): void {
        console.log(`Meu nome é ${this.nome}`);
    }

}

class Aluno extends Pessoa {

    constructor(nome: string, public nota: number) {
        super(nome);
    }

    override apresentar(): void {
        console.log(`Aluno: ${this.nome}`);
    }

}

const aluno = new Aluno("Maria", 8);
aluno.apresentar();
```

**PHP**
```php
<?php

class Pessoa {

    public function __construct(public string $nome) {}

    public function apresentar(): void {
        echo "Meu nome é {$this->nome}\n";
    }

}

class Aluno extends Pessoa {

    public function __construct(string $nome, public float $nota) {
        parent::__construct($nome);
    }

    public function apresentar(): void {
        echo "Aluno: {$this->nome}\n";
    }

}

$aluno = new Aluno("Maria", 8);
$aluno->apresentar();
```

**Python**
```python
class Pessoa:

    def __init__(self, nome):
        self.nome = nome

    def apresentar(self):
        print(f"Meu nome é {self.nome}")


class Aluno(Pessoa):

    def __init__(self, nome, nota):
        super().__init__(nome)
        self.nota = nota

    def apresentar(self):
        print(f"Aluno: {self.nome}")


aluno = Aluno("Maria", 8)
aluno.apresentar()
```

---

### 2. Encapsulamento

Protege os dados internos do objeto, controlando como eles podem ser acessados ou modificados — geralmente por meio de métodos.

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

const conta = new Conta();
conta.depositar(500);
console.log(conta.consultarSaldo());
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

$conta = new Conta();
$conta->depositar(500);
echo $conta->consultarSaldo();
```

**Python**
```python
class Conta:

    def __init__(self):
        self.__saldo = 0

    def depositar(self, valor):
        if valor > 0:
            self.__saldo += valor

    def consultar_saldo(self):
        return self.__saldo


conta = Conta()
conta.depositar(500)
print(conta.consultar_saldo())
```

---

### 3. Polimorfismo

Objetos diferentes podem responder de maneiras diferentes ao mesmo método.

**TypeScript**
```typescript
class Animal {
    emitirSom(): void {
        console.log("Som");
    }
}

class Cachorro extends Animal {
    override emitirSom(): void {
        console.log("Au Au");
    }
}

class Gato extends Animal {
    override emitirSom(): void {
        console.log("Miau");
    }
}

const animais: Animal[] = [new Cachorro(), new Gato()];
for (const animal of animais) {
    animal.emitirSom();
}
```

**PHP**
```php
<?php

class Animal {
    public function emitirSom(): void {
        echo "Som\n";
    }
}

class Cachorro extends Animal {
    public function emitirSom(): void {
        echo "Au Au\n";
    }
}

class Gato extends Animal {
    public function emitirSom(): void {
        echo "Miau\n";
    }
}

$animais = [new Cachorro(), new Gato()];
foreach ($animais as $animal) {
    $animal->emitirSom();
}
```

**Python**
```python
class Animal:
    def emitir_som(self):
        print("Som")


class Cachorro(Animal):
    def emitir_som(self):
        print("Au Au")


class Gato(Animal):
    def emitir_som(self):
        print("Miau")


animais = [Cachorro(), Gato()]
for animal in animais:
    animal.emitir_som()
```

---

### 4. Abstração

Representa apenas as características relevantes de algo, ocultando detalhes de implementação. Costuma ser expressa por meio de **classes abstratas** ou **interfaces**, que definem métodos que as classes filhas são obrigadas a implementar.

**TypeScript**
```typescript
abstract class Forma {
    abstract calcularArea(): number;
}

class Retangulo extends Forma {

    constructor(private largura: number, private altura: number) {
        super();
    }

    calcularArea(): number {
        return this.largura * this.altura;
    }

}

const retangulo = new Retangulo(4, 5);
console.log(retangulo.calcularArea());
```

**PHP**
```php
<?php

abstract class Forma {
    abstract public function calcularArea(): float;
}

class Retangulo extends Forma {

    public function __construct(
        private float $largura,
        private float $altura
    ) {}

    public function calcularArea(): float {
        return $this->largura * $this->altura;
    }

}

$retangulo = new Retangulo(4, 5);
echo $retangulo->calcularArea();
```

**Python**
```python
from abc import ABC, abstractmethod


class Forma(ABC):

    @abstractmethod
    def calcular_area(self):
        pass


class Retangulo(Forma):

    def __init__(self, largura, altura):
        self.largura = largura
        self.altura = altura

    def calcular_area(self):
        return self.largura * self.altura


retangulo = Retangulo(4, 5)
print(retangulo.calcular_area())
```

> No Python não existe a palavra-chave `interface`; o conceito é representado com classes abstratas (`ABC` + `@abstractmethod`).

---

**1. Herança**
Crie uma classe `Pessoa` com o atributo `nome`. Depois crie as classes `Aluno` e `Professor`, que devem herdar de `Pessoa`.

**2. Encapsulamento**
Crie uma classe `ContaBancaria` com o saldo protegido. Implemente os métodos `depositar(valor)`, `sacar(valor)` e `consultarSaldo()`, impedindo o acesso direto ao saldo.

**3. Polimorfismo**
Crie uma classe `Animal` com o método `emitirSom()`. Depois crie as classes `Cachorro` e `Gato`, cada uma implementando o método de forma diferente.

**4. Abstração**
Crie uma classe abstrata `Forma` com o método `calcularArea()`. Depois crie as classes `Retangulo` e `Circulo`, cada uma implementando seu próprio cálculo de área.

**5. Projeto integrando os quatro pilares**
Desenvolva um pequeno sistema com as classes `Pessoa`, `Aluno` e `Professor`, aplicando:
- Herança (`Aluno` e `Professor` herdando de `Pessoa`);
- Encapsulamento (algum atributo privado/protegido com métodos de acesso);
- Polimorfismo (um método sobrescrito de forma diferente em `Aluno` e `Professor`);
- Abstração (uma classe abstrata ou interface definindo um contrato comum).
