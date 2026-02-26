# Variáveis e Tipos de Dados

## 1. Conceito de Variável
- Variável é um espaço de memória que armazena valores temporários  
- Cada variável tem um **nome** e um **tipo**  
- Pode receber e alterar valores durante a execução do programa  

## 2. Regras para Identificadores
- Nomes significativos, claros e descritivos  
- Não podem começar com números  
- Não usar palavras reservadas da linguagem  
- Evitar caracteres especiais e espaços  

## 3. Tipos de Dados
- **Inteiro**: números sem vírgula (ex: 5, 10, -3)  
- **Real**: números com vírgula ou ponto decimal (ex: 3.14, -2.5)  
- **Caractere**: letra ou símbolo único (ex: 'A', 'b', '!')  
- **Cadeia de caracteres**: texto (ex: "Olá Mundo")  
- **Lógico**: verdadeiro ou falso (true/false)  

## 4. Declaração de Variáveis
```portugol
programa
{
    funcao inicio()
    {
        inteiro idade
        real altura
        caractere inicial
        cadeia nome
        logico aprovado
    }
}
```

## 5. Atribuição de Valores
```portugol
programa
{
    funcao inicio()
    {
        inteiro idade
        idade <- 16

        real altura
        altura <- 1.75

        caractere inicial
        inicial <- 'C'

        cadeia nome
        nome <- "Cesar"

        logico aprovado
        aprovado <- true
    }
}
```
- `<-` → operador de atribuição  
- Valor à direita é armazenado na variável à esquerda  

## 6. Entrada de Dados
```portugol
programa
{
    funcao inicio()
    {
        inteiro idade
        escreva("Digite sua idade: ")
        leia(idade)
        escreval("Sua idade é: ", idade)
    }
}
```
- `leia()` → recebe dados do usuário e armazena na variável  

## 7. Operações com Variáveis
- Aritméticas: `+`, `-`, `*`, `/`, `%`  
- Relacionais: `=`, `<>`, `<`, `>`, `<=`, `>=`  
- Lógicas: `e`, `ou`, `nao`  

**Exemplo:**
```portugol
programa
{
    funcao inicio()
    {
        inteiro a, b, soma
        escreva("Digite a: ")
        leia(a)
        escreva("Digite b: ")
        leia(b)
        soma <- a + b
        escreval("Soma: ", soma)
    }
}
```

## 8. Boas Práticas
- Nomes de variáveis claros  
- Evitar abreviações confusas  
- Declarar variáveis antes de usar  
- Testar entradas do usuário  

## 9. Exercícios
1. Criar um programa que peça o nome e a idade do usuário e mostre na tela  
2. Criar um programa que leia dois números e mostre a soma, subtração, multiplicação e divisão  
3. Criar um programa que leia a altura e peso do usuário e calcule o IMC  
