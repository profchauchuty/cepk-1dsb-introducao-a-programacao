# Funções

## 1. Conceito
- Blocos de código que realizam uma **tarefa específica**  
- Permitem reaproveitar código sem precisar reescrevê-lo  
- Ajudam a organizar o programa em partes menores e mais fáceis de entender  

---

## 2. Estrutura Básica
- Uma função precisa ser declarada e pode ser chamada em qualquer parte do programa  

```portugol
funcao tipo_retorno nome_da_funcao(parametros){
    // comandos
    retorne valor
}
```

### Exemplo sem Retorno (Vazia)
```portugol
programa
{
    funcao inicio(){
        mensagemBoasVindas() // Chamada da função
    }

    funcao mensagemBoasVindas(){
        escreva("Bem-vindo ao sistema!")
    }
}
```

---

## 3. Funções com Parâmetros
- Dados enviados para dentro da função para serem processados  

### Exemplo
```portugol
programa
{
    funcao inicio(){
        exibirIdade(25) // O valor 25 é passado como parâmetro
    }

    funcao exibirIdade(inteiro idade){
        escreva("Você tem ", idade, " anos.")
    }
}
```

---

## 4. Funções com Retorno
- Utilizadas quando a função precisa devolver um resultado para quem a chamou  
- Obrigatório o uso do comando `retorne`  

### Exemplo
```portugol
programa
{
    funcao inicio(){
        inteiro resultado
        
        resultado = somar(10, 5) // Armazena o valor retornado
        escreva("O resultado é: ", resultado)
    }

    funcao inteiro somar(inteiro a, inteiro b){
        retorne a + b // Devolve o valor calculado
    }
}
```

---

## 5. Escopo de Variáveis

### Variáveis Locais
- Declaradas dentro de uma função  
- Só existem e podem ser usadas dentro daquela própria função  

### Variáveis Globais
- Declaradas no início do programa, fora de qualquer função  
- Podem ser acessadas por todas as funções do código  

### Exemplo
```portugol
programa
{
    inteiro global = 100 // Variável Global

    funcao inicio(){
        inteiro local = 10 // Variável Local
        escreva(local, " e ", global)
    }

    funcao outra_funcao(){
        // escreva(local) -> Erro! Esta função não conhece a variável local
        escreva(global) // Funciona!
    }
}
```

---

## 6. Tipos de Retorno Suportados
- `vazio`: Quando a função não devolve nenhum valor
- `inteiro`: Retorna números inteiros
- `real`: Retorna números decimais
- `cadeia`: Retorna textos
- `caracter`: Retorna um único caractere
- `logico`: Retorna `verdadeiro` ou `falso`

---

## 7. Exemplo Completo
```portugol
programa
{
    funcao inicio()
    {
        real nota1 = 7.5
        real nota2 = 8.0
        real media_final
        logico aprovado

        media_final = calcularMedia(nota1, nota2)
        aprovado = verificarAprovacao(media_final)

        escreva("Média: ", media_final, "\n")
        
        se(aprovado){
            escreva("Status: Aluno Aprovado!")
        } senao {
            escreva("Status: Aluno Reprovado!")
        }
    }

    funcao real calcularMedia(real n1, real n2){
        retorne (n1 + n2) / 2
    }

    funcao logico verificarAprovacao(real media){
        se(media >= 6.0){
            retorne verdadeiro
        } senao {
            retorne falso
        }
    }
}
```

---

## 8. Diferença de Passagem de Parâmetros


| Tipo de Passagem | Comportamento |
|---|---|
| Por Valor | Envia uma cópia da variável; a original não muda |
| Por Referência (Pesquisar!) | Envia o endereço da variável; se mudar na função, altera a original (usa o símbolo `&`)  |

---

## 9. Boas Práticas
- Dar nomes que indiquem ações (ex: `calcularTotal`, `exibirMenu`)  
- Criar funções pequenas e focadas em apenas uma tarefa  
- Evitar o uso excessivo de variáveis globais  
- Declarar o tipo correto de retorno para cada situação  

---

## 10. Exercícios
1. Criar uma função que receba um número e exiba se ele é par ou ímpar
2. Criar uma função que receba o ano de nascimento de uma pessoa e retorne a idade dela
3. Criar um programa que utilize uma função para converter uma temperatura de Celsius para Fahrenheit
4. Criar uma função que receba dois números e retorne o maior deles
5. Criar uma função chamada `calcularFatorial` que receba um número inteiro e retorne o seu fatorial
