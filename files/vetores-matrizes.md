# Vetores e Matrizes

## 1. Conceito
- Estruturas de dados que armazenam **múltiplos valores** do mesmo tipo sob um único nome  
- Os dados são organizados por meio de **índices numéricos** sequenciais que sempre começam em 0  
- Permitem agrupar variáveis relacionadas, evitando a criação de muitos nomes diferentes no código  

---

## 2. Estrutura Básica
- Estruturas precisam ser declaradas com seus tamanhos definidos entre colchetes `[ ]`  

```portugol
// Estrutura de um Vetor (Unidimensional)
tipo_dado nome_vetor[tamanho]

// Estrutura de uma Matriz (Bidimensional)
tipo_dado nome_matriz[linhas][colunas]

// Estrutura Multidimensional (Tridimensional)
tipo_dado nome_multidimensional[profundidade][linhas][colunas]
```

### Exemplo de Declaração e Inicialização
```portugol
programa
{
    funcao inicio(){
        inteiro notas[3] = {8, 7, 9} 
        
        real tabela[2][2] = {
            {1.5, 4.2},
            {9.0, 3.7}
        }
    }
}
```

---

## 3. Vetores (1 Dimensão)

### O que é?
- Uma sequência linear de dados armazenados na memória, estendendo-se em apenas um eixo (horizontal)  
- Funciona como uma lista de compras ou uma fileira de armários numerados de 0 até o tamanho limite menos 1  

### Anatomia da Declaração
- No exemplo `real vetor[2] = {1.4, 2.5}`:
  - `real`: Define que os dados armazenados serão números decimais  
  - `vetor`: É o nome (identificador) que você escolheu para a sua lista  
  - `[2]`: Define o **tamanho obrigatório**, reservando exatamente 2 espaços na memória  
  - `= {1.4, 2.5}`: Guarda os valores imediatamente (o índice 0 recebe `1.4` e o índice 1 recebe `2.5`)  

### Exemplo de Uso
```portugol
programa
{
    funcao inicio(){
        cadeia nomes[3]
        
        nomes[0] = "Ana"
        nomes[1] = "Bruno"
        nomes[2] = "Carlos"
        
        para(inteiro i = 0; i < 3; i++){
            escreva("Posição ", i, ": ", nomes[i], "\n")
        }
    }
}
```

---

## 4. Matrizes (2 Dimensões)

### O que é?
- Uma estrutura de dados em formato de tabela organizada estritamente em dois eixos coordenados: **linhas e colunas**  
- Funciona cruzando duas informações distintas para localizar um dado específico, igual a uma planilha Excel  

### Como funciona o acesso?
- Para ler ou preencher uma matriz, você precisa indicar dois índices: primeiro a linha e depois a coluna `matriz[linha][coluna]`  
- Exige obrigatoriamente **dois laços de repetição aninhados** (um laço `para` dentro do outro) para varrer toda a tabela  

### Exemplo de Uso
```portugol
programa
{
    funcao inicio(){
        inteiro tabela[2][3]
        
        para(inteiro l = 0; l < 2; l++){
            para(inteiro c = 0; c < 3; c++){
                tabela[l][c] = l + c
            }
        }
    }
}
```

---

## 5. Estruturas Multidimensionais (3 ou mais Dimensões)

### O que é?
- Estruturas de dados que vão além das tabelas bidimensionais, adicionando novos eixos como **profundidade, páginas ou tempo**  
- Uma estrutura **3D** funciona como um **cubo** ou um bloco de notas formado por várias planilhas empilhadas  
- Uma estrutura **4D** funciona como uma **linha do tempo**, armazenando múltiplos cubos de dados que mudam a cada instante  

### Como funciona o acesso?
- Cada dimensão nova acrescenta uma coordenada que deve ser declarada com seu tamanho e mapeada por um colchete correspondente  
- Para varrer completamente uma estrutura multidimensional, você precisará de **um laço `para` para cada dimensão existente**  

### Exemplo de Uso (3 Dimensões)
```portugol
programa
{
    funcao inicio(){
        // Declaração com tamanhos definidos: [2 Lojas][3 Produtos][4 Cores]
        inteiro estoque[2][3][4] 
        
        // Atribuindo valor específico no estoque da Loja 0, Produto 1, Cor 3
        estoque[0][1][3] = 45 
        
        // Zerando sistematicamente todas as dimensões com 3 laços aninhados
        para(inteiro i = 0; i < 2; i++){
            para(inteiro j = 0; j < 3; j++){
                para(inteiro k = 0; k < 4; k++){
                    estoque[i][j][k] = 0
                }
            }
        }
    }
}
```

---

## 6. Tipos de Dados Suportados
- `inteiro`: Estruturas para idades, contadores ou índices numéricos
- `real`: Estruturas para notas, preços, salários ou pesos
- `cadeia`: Estruturas para armazenar listas de nomes, CPFs ou textos
- `caracter`: Estruturas para armazenar gabaritos (A, B, C) ou iniciais
- `logico`: Estruturas para controle de estados, como tabuleiros de jogos (verdadeiro/falso)

---

## 7. Exemplo Completo
```portugol
programa
{
    funcao inicio()
    {
        cadeia produtos[3] = {"Arroz", "Feijão", "Café"}
        real precos[3] = {25.50, 8.90, 14.30}
        real estoque_lojas[2][3] // 2 lojas e estoque dos 3 produtos
        
        // Cadastrando estoque da Loja 0
        estoque_lojas[0][0] = 100.0
        estoque_lojas[0][1] = 80.0
        estoque_lojas[0][2] = 50.0
        
        // Cadastrando estoque da Loja 1
        estoque_lojas[1][0] = 120.0
        estoque_lojas[1][1] = 65.0
        estoque_lojas[1][2] = 40.0
        
        // Exibindo relatório de estoque por loja
        para(inteiro loja = 0; loja < 2; loja++){
            escreva("--- LOJA ", loja, " ---\n")
            para(inteiro prod = 0; prod < 3; prod++){
                escreva(produtos[prod], " | Preço: R\$ ", precos[prod], " | Estoque: ", estoque_lojas[loja][prod], "\n")
            }
        }
    }
}
```

---

## 8. Diferença de Representação de Dimensões

| Dimensões | Nome Comum | Comportamento e Estrutura |
|---|---|---|
| 1 Dimensão | Vetor | Uma linha reta de elementos indexados sequencialmente |
| 2 Dimensões | Matriz | Uma grade bidimensional organizada em Linhas e Colunas |
| 3 Dimensões | Cubo / Volume | Uma pilha de matrizes, adicionando o conceito de Profundidade |

---

## 9. Boas Práticas
- Utilizar constantes para definir o tamanho das estruturas e evitar erros de índice inválido  
- Sempre inicializar os vetores e matrizes para limpar dados residuais da memória  
- Evitar criar estruturas com mais de 3 dimensões para não prejudicar a leitura do código  
- Usar nomes de variáveis descritivos nos laços (ex: `linha` e `coluna` em vez de `l` e `c`)  

---

## 10. Exercícios
1. Criar um vetor que armazene 5 números inteiros e exiba-os na ordem inversa da leitura
2. Criar um programa que preencha uma matriz 3x3 e exiba a soma de todos os seus elementos
3. Criar uma estrutura 3D (2x2x2) que armazene a nota de 2 alunos, em 2 disciplinas, durante 2 bimestres
4. Criar um vetor de 10 posições preenchido e contar quantos números pares existem dentro dele
5. Criar uma matriz 4x4 e preencher a sua diagonal principal com o número 1 e o restante com 0
