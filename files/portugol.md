# Conhecendo o Portugol

## 1. O que é Portugol
- Linguagem de pseudocódigo em português  
- Facilita o aprendizado de lógica de programação  
- Foco na lógica antes de linguagens formais como Java, C ou Python  
- Ambiente utilizado: https://portugol.dev/

## 2. Estrutura Básica de um Programa
```portugol
programa
{
    funcao inicio()
    {
        // comandos do programa
    }
}
```
- `programa` → define o início do algoritmo  
- `{ }` → delimitam blocos de código  
- `funcao inicio()` → ponto inicial da execução  
- `//` → comentário, não executado  

## 3. Comandos de Saída
- `escreva()` → exibe texto sem pular linha  
- `escreval()` → exibe texto e pula linha  

**Exemplo:**
```portugol
programa
{
    funcao inicio()
    {
        escreval("Linha 1")
        escreval("Linha 2")
    }
}
```

## 4. Comentários
- Comentários servem para documentar o código  
- Não são executados  
- Sintaxe de uma linha: `// comentário`  

**Exemplo:**
```portugol
programa
{
    funcao inicio()
    {
        // Exibe mensagem inicial
        escreva("Bem-vindo ao curso de Algoritmos")
    }
}
```

## 5. Primeiro Programa
```portugol
programa
{
    funcao inicio()
    {
        escreva("Olá, mundo!")
    }
}
```
- `escreva()` exibe texto na tela  
- O texto deve estar entre aspas  
- Programa executa a partir da função `inicio()`  

## 6. Boas Práticas
- Usar indentação adequada  
- Comentar partes importantes  
- Testar programas após alterações  

## 7. Exercícios
- Criar um programa que mostre seu nome e idade  
- Criar um programa que escreva três frases diferentes, cada uma em uma linha  
- Adicionar comentários explicando cada linha do código  
