# Estruturas Condicionais

## 1. Conceito
- Estruturas que permitem que o programa **tome decisões**  
- Executam comandos **condicionalmente**, dependendo de uma expressão lógica  

## 2. Estrutura `se`
```portugol
se (condicao){
    // comandos se verdadeiro
}
```

## 3. Estrutura `se...senao`
```portugol
se (condicao){
    // comandos se verdadeiro
} senao {
    // comandos se falso
}
```

## 4. Estruturas Encadeadas (Aninhadas)
```portugol
se(condicao){
    // comandos 1
} senao {
    se (condicao2){
        // comandos 2
    } senao {
        // comandos 3
    }
}
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

        se (nota >= 7){
            escreval("Aprovado")
        } senao {
            escreval("Reprovado")
        }
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
4. Criar programa que identifique se o número é PAR ou ÍMPAR (usar %)
