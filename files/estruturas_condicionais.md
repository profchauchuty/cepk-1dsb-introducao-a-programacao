# Estruturas Condicionais

## 1. Conceito
- Estruturas que permitem que o programa **tome decisões**  
- Executam comandos **condicionalmente**, dependendo de uma expressão lógica  

## 2. Estrutura `se`
```portugol
se (condicao) entao
    // comandos se verdadeiro
fimse
```

## 3. Estrutura `se...senao`
```portugol
se (condicao) entao
    // comandos se verdadeiro
senao
    // comandos se falso
fimse
```

## 4. Estruturas Encadeadas (Aninhadas)
```portugol
se (condicao1) entao
    // comandos 1
senao
    se (condicao2) entao
        // comandos 2
    senao
        // comandos 3
    fimse
fimse
```

## 5. Estrutura `escolha/caso`
```portugol
escolha (variavel)
    caso valor1:
        // comandos caso valor1
    caso valor2:
        // comandos caso valor2
    caso contrario:
        // comandos se nenhum caso for verdadeiro
fimescolha
```

## 6. Operadores Relacionais e Lógicos
- Relacionais: `=`, `<>`, `<`, `>`, `<=`, `>=`  
- Lógicos: `e`, `ou`, `nao`  

**Exemplo:**
```portugol
programa
{
    funcao inicio()
    {
        inteiro nota
        escreva("Digite a nota: ")
        leia(nota)

        se (nota >= 7) entao
            escreval("Aprovado")
        senao
            escreval("Reprovado")
        fimse
    }
}
```

## 7. Boas Práticas
- Sempre usar identação adequada  
- Evitar muitas estruturas encadeadas profundas  
- Comentar decisões importantes  
- Garantir que todas as condições possíveis sejam tratadas  

## 8. Exercícios
1. Criar programa que verifique se um número é positivo, negativo ou zero  
2. Criar programa que receba a idade e informe se é menor ou maior de idade  
3. Criar programa que leia três notas e informe se o aluno foi aprovado ou reprovado (média >= 7)
