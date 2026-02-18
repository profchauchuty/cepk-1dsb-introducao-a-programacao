# Aula 1 – Introdução à Lógica de Programação

---

## Conceituação

### O computador e seu papel
Sem dúvida, o computador é uma das maiores invenções do ser humano e tem se mostrado uma ferramenta **versátil, rápida e segura** para a manipulação de informações.

Para muitos, essa invenção é responsável pela intensificação da mecanização e das descobertas científicas na vida moderna. Essa afirmação atribui ao computador um caráter **autônomo**, como se ele realizasse tudo sozinho.

> **Entretanto, cabe esclarecer que o computador não é criativo nem inteligente.**

Na realidade, ele apenas executa o que lhe é ordenado por meio de **programas de computador**, os quais são construídos para resolver problemas específicos. A solução adotada é sempre uma **solução lógica**.

Podemos compreender essa “solução lógica” como uma **receita de bolo**, utilizada para resolver um problema.

**A Lógica de Programação** é o **passo inicial** para a construção de qualquer programa de computador.

---

### Pensar logicamente
Para utilizar a lógica, é necessário desenvolver o pensamento e dominar a chamada **“Arte de pensar”**.

Alguns definem o raciocínio lógico como:

> Um conjunto de estudos que visa determinar os processos intelectuais que são as condições gerais do conhecimento verdadeiro.

Esse conceito é característico da tradição filosófica clássica **aristotélico-tomista**, também conhecida como **Lógica Formal**.

---

### Lógica Formal e Lógica Material

Em oposição ao conceito de **Lógica Formal**, surge a **Lógica Material**, que se dedica ao estudo do raciocínio considerando o seu **conteúdo ou matéria**.

Essa distinção permite compreender que:

- Pela **forma**, o raciocínio pode ser **correto ou incorreto** (válido ou inválido);  
- Pela **matéria**, a conclusão pode ser **verdadeira ou falsa**.

---

### Exemplo de raciocínio lógico

1. Nenhum homem sabe dançar;  
2. Este dançarino é homem;  
3. Este dançarino não sabe dançar.

O raciocínio apresentado é **formalmente correto**, pois a conclusão decorre logicamente das premissas.  
Entretanto, a conclusão é **falsa**, já que a primeira proposição é falsa.

> Temos, portanto, um raciocínio com **validade formal**, mas **sem validade material**.

Logo, conclui-se que o raciocínio é falso.

---

### Evolução histórica da lógica

Desde sua criação, a lógica passou por grandes avanços, especialmente a partir de meados do século XIX.

Tradicionalmente, sua evolução é dividida em três períodos:

- **Período Clássico**  
- **Período Moderno**  
- **Período Contemporâneo**

---

### Lógica Matemática ou Simbólica

A **Lógica Matemática ou Simbólica**, desenvolvida no Período Moderno:

- Representa o pensamento por meio de símbolos;  
- Defende que o raciocínio pode ser tratado como um **cálculo matemático**.

Essa vertente influenciou diretamente áreas como:

- Eletrônica  
- Cibernética  
- Informática  
- Inteligência Artificial  

---

### Lógica de Programação no contexto da informática

Apesar das diversas definições, a lógica pode ser compreendida como uma **ciência** que busca identificar as leis que o pensamento deve seguir para ser considerado válido.

No contexto da informática:

> **Lógica de Programação** é a técnica de encadear pensamentos de forma organizada para alcançar um objetivo previamente definido.

Ou seja, trata-se da técnica que define **o que deve ser feito** e **em que ordem**, para que uma solução seja obtida.

---

### Algoritmos: aplicabilidade da lógica no desenvolvimento de programas

A construção de **algoritmos** representa o primeiro passo no desenvolvimento de programas de computador. Embora seja uma das etapas mais complexas da programação, também é uma das mais desafiadoras e estimulantes.

O termo **algoritmo** não é exclusivo da computação. Sua origem vem do nome do matemático iraniano **Abu Abdullah Mohammad Ibn Musa al-Khawarizmi**, que viveu no século XVII. Sua contribuição foi fundamental para o desenvolvimento da matemática, astronomia e geografia.

Atualmente, algoritmos são utilizados em diversas áreas, como engenharia, administração e informática. Algumas definições comuns de algoritmo são:

- Uma sequência de passos para atingir um objetivo definido;  
- Um procedimento passo a passo para resolver um problema;  
- Uma sequência detalhada de ações para executar uma tarefa.

---

## Exemplo: Algoritmo para Fritar um Ovo

| Etapa          | Versão conceitual (cozinha)                              | Versão lógica / Pseudocódigo                                                                 |
|----------------|----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| **INÍCIO**     | Início do algoritmo / início da execução                 | INÍCIO                                                                                       |
| **ENTRADA**    | Coleta dos ingredientes e preferências (ponto da gema)   | ler ovo<br>ler oleo<br>ler sal<br>ler gemaDesejada                                           |
| **PROCESSAMENTO** | Preparar o ovo de acordo com o ponto desejado         | aquecerFrigideira()<br>adicionarOleo()<br>quebrarOvoNaFrigideira()<br>adicionarSal()<br><br>se gemaDesejada = "mole" então<br>&nbsp;&nbsp;fritarTempoCurto()<br>senão<br>&nbsp;&nbsp;fritarTempoMaior()<br>fimSe<br><br>enquanto claraNaoFirme()<br>&nbsp;&nbsp;fritar()<br>fimEnquanto |
| **SAÍDA**      | Ovo frito pronto para consumo                            | ovoFritoPronto                                                                               |
| **FIM**        | Fim do algoritmo / finalização                           | FIM                                                                                           |

---

### Referência

BATISTA, Rogério da Silva. *Lógica de Programação*. Teresina: Instituto Federal de Educação, Ciência e Tecnologia do Piauí, 2013.
