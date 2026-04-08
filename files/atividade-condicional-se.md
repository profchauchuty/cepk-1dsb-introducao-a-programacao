# Exercícios de Portugol: Estrutura Condicional (SE)

## Objetivo
Criar programas simples em Portugol utilizando a estrutura de decisão `SE`.

---

## Exercícios com SE

### 1. Número Positivo ou Negativo
- Solicitar ao usuário um número.
- Verificar:
  - Se for maior que 0 → "Número positivo".
  - Senão → "Número negativo ou zero".
- Exibir o resultado.

---

### 2. Par ou Ímpar
- Solicitar um número inteiro.
- Verificar:
  - Se `n % 2 == 0` → "Par".
  - Senão → "Ímpar".
- Exibir o resultado.

---

### 3. Maior de Idade
- Solicitar a idade do usuário.
- Verificar:
  - Se idade ≥ 18 → "Maior de idade".
  - Senão → "Menor de idade".
- Exibir o resultado.

---

### 4. Maior entre Dois Números
- Solicitar dois números.
- Verificar:
  - Se o primeiro for maior → mostrar ele.
  - Senão → mostrar o segundo.
- Exibir o resultado.

---

### 5. Aprovado ou Reprovado
- Solicitar a nota do aluno.
- Verificar:
  - Se nota ≥ 7 → "Aprovado".
  - Senão → "Reprovado".
- Exibir o resultado.

---

### 6. Desconto Progressivo (1 Aninhamento)
- Solicitar o valor da compra.
- Verificar:
  - Se valor ≥ 100:
    - Se valor ≥ 200 → aplicar 20% de desconto.
    - Senão → aplicar 10% de desconto.
  - Senão:
    - Sem desconto.
- Exibir o valor final.

---

### 7. Classificação de Idade (2 Aninhamentos)
- Solicitar a idade do usuário.
- Verificar:
  - Se idade ≥ 0:
    - Se idade < 12 → "Criança".
    - Senão:
      - Se idade < 18 → "Adolescente".
      - Senão:
        - Se idade < 60 → "Adulto".
        - Senão → "Idoso".
  - Senão:
    - "Idade inválida".
- Exibir o resultado.

---

### 8. Sistema de Login Completo (3 Aninhamentos)
- Solicitar usuário, senha e código de verificação.
- Verificar:
  - Se usuário for "admin":
    - Se senha for "1234":
      - Se código for "9999" → "Acesso total permitido".
      - Senão → "Código de verificação incorreto".
    - Senão:
      - Se senha estiver vazia → "Senha não informada".
      - Senão → "Senha incorreta".
  - Senão:
    - "Usuário não encontrado".
- Exibir o resultado.

---

**Observações:**  
- Crie **um programa separado** para cada exercício.  
- Use comandos `Leia` e `Escreva`.  
- Utilize a estrutura `SE ... SENAO`.  
