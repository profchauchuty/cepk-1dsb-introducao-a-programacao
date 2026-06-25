# Exercícios: Vetores e Matrizes

## Objetivo
Criar programas simples em Portugol utilizando **VETORES** e **MATRIZES** para armazenar, organizar e manipular conjuntos de dados estruturados.

---

# Exercícios com Vetores e Matrizes

## 1. Armazenar e Exibir Nomes
- Criar um vetor chamado `nomes` com capacidade para 5 posições.
- O programa deve ler os 5 nomes informados pelo usuário.
- Exibir ao final:
  - A lista com todos os nomes na ordem em que foram digitados.

---

## 2. Soma de Elementos em um Vetor
- Criar um vetor chamado `numeros` para armazenar 6 números inteiros.
- Preencher o vetor com dados informados pelo usuário.
- Somar apenas os números armazenados que forem ímpares.
- Exibir o resultado da soma no programa principal.

---

## 3. Lista de Produtos e Preços
- Criar dois vetores paralelos com capacidade para 4 posições:
  - `produtos` (tipo cadeia).
  - `precos` (tipo real).
- Ler o nome e o preço de cada produto.
- Exibir ao final uma listagem formatada de cada item com seu respectivo valor.

Exemplo:

```text
Produto 1: Caderno - R$ 15.50
Produto 2: Caneta - R$ 2.50
```

---

## 4. Multiplicação de Vetor (Cópia)
- Criar um vetor chamado `original` com 5 números inteiros fornecidos pelo usuário.
- Criar automaticamente um segundo vetor chamado `resultado`.
- Armazenar no vetor `resultado` cada valor do vetor original multiplicado por 3.
- Exibir os valores do vetor `resultado`.

---

## 5. Média da Turma e Notas Acima da Média
- Criar um vetor chamado `notas` para armazenar as notas de 8 alunos.
- Calcular a média geral da turma.
- Descobrir quantos alunos obtiveram nota estritamente maior que a média calculada.
- Exibir a média da turma e a quantidade de alunos acima dela.

---

## 6. Diagonal Principal de uma Matriz
- Criar uma matriz chamada `matrizQuad` de tamanho 3x3 (tipo inteiro).
- Preencher a matriz com números digitados pelo usuário.
- Somar todos os valores que estão localizados na diagonal principal (onde linha é igual a coluna).
- Exibir o valor total da soma.

---

## 7. Controle de Consumo de Energia
- Criar uma matriz chamada `consumo` de tamanho 4x2 (4 eletrodomésticos e 2 meses).
- Ler os gastos de energia de cada aparelho nos dois meses.
- Calcular o total consumido por cada um dos 4 aparelhos ao longo do bimestre.
- Exibir o consumo acumulado de cada eletrodoméstico.

---

## 8. Compactador de Linhas de Matriz
- Criar uma matriz 3x3 de números inteiros preenchida pelo usuário.
- Criar um vetor chamado `somasLinhas` com capacidade para 3 posições.
- Guardar em cada posição do vetor a soma correspondente dos elementos de cada linha da matriz.
- Exibir os valores resultantes contidos no vetor.

---

## 9. Caça ao Tesouro no Tabuleiro
- Criar uma matriz 4x4 do tipo cadeia para representar um mapa, preenchida com "Água".
- Definir estaticamente uma posição secreta com o texto "Tesouro".
- Pedir para o usuário digitar uma linha e uma coluna para dar um "palpite".
- Exibir:
  - "Parabéns, você encontrou o tesouro!" se ele acertar a coordenada.
  - "Água! Tente novamente." caso contrário.

---

## 10. Sistema de Análise de Matrizes

- Criar um sistema interativo para analisar dados em uma matriz 3x3 de números inteiros.

Menu:

```text
1 - Preencher Matriz
2 - Procurar Maior Valor
3 - Exibir Matriz Completa
4 - Contar Números Pares
5 - Sair
```

Regras:
- Enquanto o usuário não escolher a opção `5`:
  - Mostrar o menu.
  - Ler a opção escolhida.

### Opção 1 — Preencher Matriz
- Permitir que o usuário digite novos valores para todas as 9 posições da matriz.

### Opção 2 — Procurar Maior Valor
- Percorrer a matriz atual e identificar qual é o maior número armazenado.
- Exibir o maior valor encontrado e as suas coordenadas exatas (Linha e Coluna).

### Opção 3 — Exibir Matriz Completa
- Mostrar a matriz formatada na tela em formato de grade (linhas e colunas alinhadas).

### Opção 4 — Contar Números Pares
- Percorrer a matriz e contar quantos números armazenados são divisíveis por 2.
- Exibir a quantidade total encontrada.

### Opção 5 — Sair
- Mostrar:
  - "Sistema encerrado".

### Qualquer Outra Opção
- Mostrar:
  - "Opção inválida".

---

- Utilizar:
  - `PARA`
  - `SE`
  - `SENAO`
  - `ESCOLHA` (opcional)
- Organizar o código com indentação.

# Observações
- Crie **um programa separado** para cada exercício.
- Utilize:
  - `Leia`
  - `Escreva`
- Utilize:
  - Vetores `[tamanho]` e Matrizes `[linhas][colunas]`
- Organize o código com indentação.
