# Algoritmos de Escalonamento de Processos

Trabalho da disciplina de **Sistemas Operacionais** — IFRS Campus Restinga
Curso: **Análise e Desenvolvimento de Sistemas — 3N**
Semestre: **2026/2**

## Sobre o projeto

Este projeto tem como objetivo desenvolver um simulador de 
**algoritmos de escalonamento de processos**, 
permitindo visualizar o funcionamento de diferentes estratégias 
utilizadas por sistemas operacionais.
Os algoritmos previstos para o projeto são:

* FCFS (First Come, First Served)
* SJF Preemptivo
* SJF Não Preemptivo
* Prioridade Preemptivo
* Prioridade Não Preemptivo
* Round Robin

O projeto está sendo desenvolvido gradualmente. O código atual possui o
 **FCFS implementado como referência**, enquanto os demais algoritmos serão 
 implementados nas próximas etapas.

---
## Tecnologias utilizadas

* **Python 3**
* Biblioteca padrão `random`
* Git
* GitHub
---

# Como executar o projeto

## 1. Pré-requisito: É necessário ter o **Python 3** instalado no computador.

Para verificar se o Python está instalado, abra o terminal e execute:
```bash
python --version
```
Caso esse comando não funcione, tente:
```bash
python3 --version
```
O terminal deverá apresentar uma versão do Python, por exemplo:
```text
Python 3.12.5
```

## 2. Clonar o repositório: No terminal, escolha uma pasta onde deseja armazenar 
o projeto e execute:

```bash
git clone https://github.com/dudavieiraoliveira/algoritmos_sis_operacionais.git
```

Depois entre na pasta do projeto:
```bash
cd algoritmos_sis_operacionais
```
---

## 3. Executar o programa

O projeto possui atualmente o arquivo principal:
```text
main.py
```
Para executá-lo:

### Windows
```bash
python main.py
```

### Linux / macOS
```bash
python3 main.py
```

---

# Utilizando o programa

Ao iniciar o programa, primeiro será solicitado:

```text
Sera aleatorio?:
```

Existem duas possibilidades.

### Opção 1 — Processos aleatórios

Digite:

```text
1
```

O programa irá gerar automaticamente os dados dos processos.

Atualmente são criados **3 processos**, com valores aleatórios para:

* Tempo de execução
* Tempo de chegada
* Prioridade

Exemplo:

```text
Processo[0]: tempo_execucao=5 tempo_restante=5 tempo_chegada=3 prioridade=8
Processo[1]: tempo_execucao=2 tempo_restante=2 tempo_chegada=1 prioridade=4
Processo[2]: tempo_execucao=7 tempo_restante=7 tempo_chegada=5 prioridade=12
```

### Opção 2 — Informar os processos manualmente

Digite qualquer valor diferente de `1`:

```text
Sera aleatorio?: 0
```

O programa solicitará os dados de cada processo:

```text
Digite o tempo de execucao do processo[0]:
Digite o tempo de chegada do processo[0]:
Digite a prioridade do processo[0]:
```

Esse procedimento será repetido para os 3 processos.

---

# Menu principal

Depois que os processos forem definidos, será apresentado o menu:

```text
Escolha o algoritmo?:

[1=FCFS
 2=SJF Preemptivo
 3=SJF Nao Preemptivo
 4=Prioridade Preemptivo
 5=Prioridade Nao Preemptivo
 6=Round_Robin
 7=Imprime lista de processos
 8=Popular processos novamente
 9=Sair]
```

## 1 — FCFS

Executa o algoritmo **First Come, First Served**.

O FCFS já está implementado no código atual e serve como referência para o desenvolvimento dos demais algoritmos.

---

## 2 — SJF Preemptivo

Executará o algoritmo **Shortest Job First Preemptivo**.

Nesta modalidade, o processo em execução pode ser interrompido caso outro processo disponível possua menor tempo de execução restante.

**Status atual:** em desenvolvimento.

---

## 3 — SJF Não Preemptivo

Executará o algoritmo **Shortest Job First Não Preemptivo**.

Após um processo começar a executar, ele permanece em execução até sua conclusão.

**Status atual:** em desenvolvimento.

---

## 4 — Prioridade Preemptivo

Executará o algoritmo de escalonamento baseado em prioridade, permitindo interrupções durante a execução.

**Status atual:** em desenvolvimento.

---

## 5 — Prioridade Não Preemptivo

Executará o algoritmo de prioridade sem interrupção do processo que estiver executando.

**Status atual:** em desenvolvimento.

---

## 6 — Round Robin

Executará o algoritmo **Round Robin**, baseado na utilização de um intervalo de tempo (*quantum*) para alternar entre os processos.

**Status atual:** em desenvolvimento.

---

## 7 — Imprimir processos

Exibe novamente os dados atuais dos processos:

```text
Processo[0]: tempo_execucao=...
Processo[1]: tempo_execucao=...
Processo[2]: tempo_execucao=...
```

---

## 8 — Popular processos novamente

Permite gerar uma nova lista de processos.

Ao selecionar essa opção, o programa perguntará novamente:

```text
Sera aleatorio?:
```

Assim, é possível criar outro conjunto de processos sem precisar 
reiniciar o programa.

---

## 9 — Sair: Encerra a execução do programa.
---

# Informações utilizadas pelos processos

Cada processo possui atualmente as seguintes informações:

| Informação       | Descrição                                               |
| ---------------- | ------------------------------------------------------- |
| `tempo_execucao` | Tempo total necessário para executar o processo         |
| `tempo_restante` | Tempo que ainda falta para concluir o processo          |
| `tempo_chegada`  | Momento em que o processo chega ao sistema              |
| `prioridade`     | Prioridade atribuída ao processo                        |
| `tempo_espera`   | Tempo que o processo permanece aguardando para executar |

Os dados são armazenados utilizando **listas paralelas**, seguindo a estrutura definida no código-base fornecido para o trabalho.

---
