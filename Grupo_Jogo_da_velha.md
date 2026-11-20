# 🎮 Análise Comparativa de Código Python — Jogo da Velha (v1 vs v2)

Este repositório documenta a evolução e a análise comparativa entre duas versões de um projeto de **Jogo da Velha** desenvolvido em Python, destacando a transição de um script procedural linear para uma arquitetura modularizada.

* **Arquivos analisados:** 
  * `verasao1_codigo_apresentado_em_sala.py` (Versão 1)
  * `versão2_codigo_apresentadado_em_sala.py` (Versão 2)

---

## 📋 Visão Geral

Na transição da **Versão 1** para a **Versão 2**, o programa deixou de ser um script linear e passou a adotar uma estrutura modularizada com funções. A atualização introduziu:
* Controle automático de turnos;
* Cadastro de dois jogadores em dicionário;
* Exibição formatada do tabuleiro;
* Mensagens de vitória personalizadas;
* Dois exercícios independentes de cálculo de médias ao final do arquivo.

---

## ✨ 1. O que foi adicionado na Versão 2

* **Modularização com funções:**
  * `exibir_tabuleiro(tabuleiro)`: imprime o tabuleiro formatado com separadores verticais (`" | ".join(linha)`) e linha divisória horizontal (`"-" * 15`).
  * `alternar_turno(jogador_atual)`: alterna automaticamente o símbolo do jogador entre `"X"` e `"O"`.
  * `jogar()`: encapsula toda a lógica principal do Jogo da Velha, sendo iniciada ao final do bloco com a chamada `jogar()`.
* **Cadastro de dois jogadores com dicionário:** Inclusão de duas entradas de dados (`nome_x` e `nome_o`) armazenadas no dicionário `jogadores = {"X": nome_x, "O": nome_o}`.
* **Controle automático de turno:** Criação da variável `jogador_atual = "X"`, que preenche o tabuleiro com o símbolo da vez e alterna o turno automaticamente após cada jogada válida.
* **Mensagem de vitória personalizada:** Ao detectar um vencedor em linhas, colunas ou diagonais, o código identifica quem ganhou por meio de `vencedor = alternar_turno(jogador_atual)` e exibe o nome correspondente (`f"Temos um vencedor! Parabéns, {jogadores[vencedor]}!"`), corrigindo também o erro de digitação `"vencendor"` presente na primeira versão.
* **Códigos extras de cálculo de médias (fora do jogo):** Adição de dois blocos de exercício independentes do Jogo da Velha ao final do arquivo:
  * Um laço `for` que percorre a matriz `notas` (`[[7.0, 9.0], [5.0, 6.0], [8.0, 8.0]]`) e calcula a média de cada estudante utilizando um contador (`numero_estudante`).
  * A função `calcular_media(notas)`, chamada separadamente para três listas (`lista_1`, `lista_2` e `lista_3`).

---

## 🗑️ 2. O que foi removido da Versão 1

* **Cadastro simples de um único nome:** Remoção da lista `nome = []`, da entrada `n = input("Digite seu n: ")` e da instrução `nome.append(n)`.
* **Escolha manual do símbolo a cada jogada:** Remoção da linha `escolha = input("Escolha X ou O: ").upper()` e do laço `while` que validava se o caractere digitado era `"X"` ou `"O"`, já que a troca de turno passou a ser automática.
* **Impressão bruta do tabuleiro:** Remoção do laço `for linha in Tabuleiro: print(linha)`, que exibia as listas com colchetes e aspas, substituído pela função `exibir_tabuleiro(Tabuleiro)`.
* **Mensagens genéricas de vitória:** Remoção das mensagens simples `"Temos um vencedor"` e `"Temos um vencendor"` em favor da exibição personalizada com o nome do vencedor.

---

## 📊 3. Quadro Comparativo Resumido

| Aspecto | Versão 1 | Versão 2 |
| :--- | :--- | :--- |
| **Estrutura** | Código linear executando diretamente no corpo do script. | Modularizado em funções (`exibir_tabuleiro`, `alternar_turno` e `jogar`). |
| **Jogadores** | Apenas um nome salvo na lista `nome`. | Dois nomes (`nome_x` e `nome_o`) associados aos símbolos no dicionário `jogadores`. |
| **Controle de turno** | Manual: pede `X` ou `O` a cada jogada com validação em `while`. | Automático: controlado por `jogador_atual` e pela função `alternar_turno`. |
| **Exibição do tabuleiro** | Impressão direta das listas (`print(linha)`). | Formatada com separadores `" | "` e linha `"-" * 15` via `exibir_tabuleiro`. |
| **Anúncio de vitória** | Mensagem fixa (`"Temos um vencedor"` / `"Temos um vencendor"`). | Mensagem personalizada exibindo o nome do jogador vencedor. |
| **Conteúdo extra** | Contém apenas o Jogo da Velha. | Inclui dois exercícios extras de cálculo de média com listas e função `calcular_media`. |

---

## 🤝 4. Membros do Grupo:

* ***Lídia Souza Vidal***
* ***Rafael Vinicius Viana***
* ***Thaís Pereira Cardoso***
* ***Gabriel Rocha Couto***
* ***Helena Dutra Braga***
* ***Paulo Eduardo Roma G. Júnior***
* ***Arthur Oliveira Antunes***
* ***Artur Carvalho Freires***
* ***Matteo da Silva Rodriguez***
