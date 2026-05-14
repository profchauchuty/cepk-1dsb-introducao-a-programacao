# Estruturas de Repetição

## 1. Conceito
- Estruturas utilizadas para **repetir comandos**  
- Permitem executar um bloco de código várias vezes  
- A repetição ocorre enquanto uma condição for verdadeira ou até atingir um limite  

---

## 2. Estrutura `enquanto`
- Executa enquanto a condição for verdadeira  

```portugol
enquanto(condicao){
    // comandos
}
```

### Exemplo
```portugol
programa
{
    funcao inicio()
    {
        inteiro contador = 1

        enquanto(contador <= 5){
            escreva(contador)
            contador++ // contador = contador + 1
        }
    }
}
```

---

## 3. Estrutura `faca...enquanto`
- Executa o bloco primeiro e só depois verifica a condição  
- Garante pelo menos uma execução  

```portugol
faca{
    // comandos
} enquanto(condicao)
```

### Exemplo
```portugol
programa
{
    funcao inicio()
    {
        inteiro numero = 1

        faca{
            escreva(numero)
            numero++
        } enquanto(numero <= 5)
    }
}
```

---

## 4. Estrutura `para`
- Utilizada quando se sabe a quantidade de repetições  

```portugol
para(inicializacao ; condicao ; incremento){
    // comandos
}
```

### Exemplo
```portugol
programa
{
    funcao inicio()
    {
        inteiro i

        para(i = 1 ; i <= 10 ; i++){
            escreva(i)
        }
    }
}
```

---

## 5. Controle de Repetição

### `pare`
- Interrompe a repetição imediatamente  

### Exemplo
```portugol
programa
{
    funcao inicio()
    {
        inteiro i

        para(i = 1 ; i <= 10 ; i++){
            se(i == 5){
                pare
            }
            escreva(i)
        }
    }
}
```

---

## 6. Operadores Utilizados
- Relacionais: `=`, `<>`, `<`, `>`, `<=`, `>=`
- Lógicos: `e`, `ou`, `nao`
- Incremento: `++`
- Decremento: `--`

---

## 7. Exemplo Completo
```portugol
programa
{
    funcao inicio()
    {
        inteiro numero
        inteiro soma = 0

        para(numero = 1 ; numero <= 5 ; numero++){
            soma = soma + numero
        }

        escreva("Soma total: ", soma)
    }
}
```

---

## 8. Diferença Entre as Estruturas

| Estrutura | Uso Principal |
|---|---|
| `enquanto` | Quando não se sabe quantas repetições ocorrerão |
| `faca...enquanto` | Quando o bloco precisa executar ao menos uma vez |
| `para` | Quando a quantidade de repetições é conhecida |

---

## 9. Boas Práticas
- Evitar loops infinitos  
- Sempre garantir alteração da variável de controle  
- Utilizar identação adequada  
- Escolher a estrutura mais apropriada para cada situação  
- Evitar repetições desnecessárias  

---

## 10. Exercícios
1. Criar um programa que exiba os números de 1 até 10 usando `enquanto`
2. Criar um programa que conte de 10 até 1 usando decremento
2. Criar um programa que exiba os números pares de 0 até 20 usando `para`
3. Criar um programa que leia 5 números e mostre a soma total
5. Criar um programa que exiba a tabuada de um número informado pelo usuário
