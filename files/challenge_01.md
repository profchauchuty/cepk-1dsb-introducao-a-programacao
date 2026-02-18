# Atividade - 🍰 Bolo Mestre 3000 🤖

Em uma confeitaria automatizada, foi criada a Bolo Mestre 3000, uma máquina inteligente responsável por preparar bolos personalizados de forma totalmente automática. A máquina recebe as escolhas da pessoa, como sabor do bolo, nível de doçura, se deseja cobertura e outras preferências. A partir desses dados, a Bolo Mestre 3000 seleciona os ingredientes, prepara a massa, assa o bolo e, quando necessário, adiciona cobertura ou ..., até deixá-lo pronto para consumo.
O desafio é desenvolver um algoritmo simples que represente o funcionamento da Bolo Mestre 3000, desde a entrada das preferências até a finalização do bolo.

> **Observação:** escolha **apenas uma** resposta em cada questão.

# Algoritmo - Bolo Mestre 3000

---

```text
# ENTRADA
LER saborBolo          = _________________  # Opções: Chocolate / Morango / Cenoura
LER etapa              = _________________  # Opções: Inicial / Massa Pronta / Assado / Pronto
LER hasCobertura       = _________________  # Opções: Verdadeiro / Falso
LER _________________  = _________________  # Opções: Sim / Não
mensagemFinal          = _____________________________________________________________________

# PROCESSAMENTO
selecionarIngredientes(saborBolo)

etapa = prepararMassa()

SE etapa = _________________ ENTÃO
    mostrarMensagem("Massa pronta para assar")
SENÃO
    mostrarMensagem("Erro no preparo da massa")
    _________________
FIMSE

etapa = assarBolo()

# SAÍDA
```

```text
INÍCIO

# ENTRADA
LER saborBolo          = _________________  # Opções: Chocolate / Morango / Cenoura
LER comCobertura       = _________________  # Opções: Verdadeiro / Falso
LER nivelDocura        = _________________  # Opções: Pouco doce / Médio / Bem doce
LER etapa              = "Inicial"          # Opções: Inicial / Massa Pronta / Assado / _________________
LER _________________  = _________________  # Opções: Sim / Não
mensagemFinal          = _____________________________________________________________________

# PROCESSAMENTO
selecionarIngredientes(saborBolo, nivelDocura)

etapa = prepararMassa()

SE etapa = _________________ ENTÃO
    mostrarMensagem("Massa pronta para assar")
SENÃO
    mostrarMensagem("Ocorreu um erro no preparo da massa")
    _________________
FIMSE

etapa = assarBolo()

SE etapa = _________________ ENTÃO
    mostrarMensagem("Bolo assado com sucesso!")
SENÃO
    mostrarMensagem("Ocorreu um erro ao assar a massa")
    _________________
FIMSE

SE comCobertura = "Verdadeiro" ENTÃO
       _____________________()
FIMSE

SE _________________ = "Sim" ENTÃO
       _____________________()
FIMSE

etapa = _________________

SE etapa = _________________ ENTÃO
       mostrarMensagem(_____________________________________________________________________)
       mostrarMensagme(mensagemFinal)
FIMSE

SAÍDA
Descrição do Bolo:
" Bolo de _________________ com _________________, no nível de doce _________________,  cobertura: _________________, _________________: _________________.

FIM
```
---
