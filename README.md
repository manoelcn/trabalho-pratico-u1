# Projeto: Somador de 3 Bits com Registrador e Display

Este projeto consiste em um sistema digital que realiza a soma de dois números binários de 3 bits, armazena o resultado de forma sincronizada e o exibe em um display de 7 segmentos.

## 👥 Autores
* **Manoel Candido Neto**
* **Kaua Vinicius Ramos Campos**

## 🛠️ Tecnologias Utilizadas
* **Logisim-evolution (v4.0.0):** Software utilizado para a modelagem e simulação do circuito.
* **Lógica Digital:** Implementação de somadores, registradores e decodificadores.

## 📂 Estrutura do Projeto
O arquivo `TrabalhoPraticoU1.circ` está estruturado de forma modular com os seguintes circuitos:

### 1. Circuito `main` (Principal)
Integra todos os módulos do sistema para garantir o fluxo de dados entre entrada, processamento e saída.
* **Entradas:** Dois conjuntos de pinos (A0-A2 e B0-B2) que representam os números binários de 3 bits.
* **Display:** Componente de 7 segmentos que apresenta o resultado final de forma visual.
* **Clock:** Componente que sincroniza a gravação dos dados no registrador.

### 2. Circuito `Somador3Bits`
Realiza a operação aritmética do sistema.
* **Lógica:** Utiliza portas **XOR**, **AND** e **OR** para calcular a soma bit a bit e gerenciar o transporte (*carry*).
* **Saídas:** Fornece os bits de soma (S0, S1, S2) e o bit de *carry* final (C2).

### 3. Circuito `Registrador3Bits`
Responsável pela persistência e sincronização dos dados.
* **Componentes:** Composto por três **Flip-Flops tipo D**.
* **Sincronização:** Todos os Flip-Flops compartilham o mesmo sinal de clock (CLK), garantindo que as saídas (Q0, Q1, Q2) sejam atualizadas simultaneamente.

### 4. Circuito `Conversor7Segmentos`
Atua como um decodificador para a interface visual.
* **Funcionamento:** Transforma a entrada de 3 bits (In0, In1, In2) em sinais lógicos para os segmentos de 'a' a 'g' do display.
* **Mapeamento:** Utiliza uma rede de portas **NOT**, **AND** e **OR** para converter as combinações binárias na representação correta.
