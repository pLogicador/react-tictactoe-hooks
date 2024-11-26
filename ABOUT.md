# React Tic Tac Toe (Hooks)
## Descrição
Este é um jogo da velha (Tic Tac Toe) interativo desenvolvido com **React**. Ele utiliza **React Hooks** e o **React Context API** para gerenciar o estado da aplicação e garantir que o jogo funcione de forma eficiente e escalável. O jogo permite que dois jogadores joguem, mostre o histórico de jogadas e declare um vencedor.

## Tecnologias Utilizadas
- **React**: Biblioteca para construção da interface.
- **React Hooks**: Utilizado para gerenciar o estado local e o ciclo de vida dos componentes (ex. `useState`, `useEffect`).
- **React Context API**: Para gerenciamento de estado global (ex. estado do tabuleiro, jogador atual, vencedor, histórico).
- **PropTypes**: Para validação das propriedades dos componentes.
- **UUID**: Para garantir que cada item renderizado tenha uma chave única.
- 
## Funcionalidades
- **Tabuleiro interativo**: O usuário pode clicar nas células para jogar, alternando entre '`X`' e '`O`'.
- **Verificação de vencedor**: Após cada jogada, o sistema verifica se houve um vencedor ou empate.
- **Histórico de jogadas**: O usuário pode navegar pelas jogadas anteriores e retornar a um movimento específico.
- **Reset do jogo**: É possível reiniciar o jogo com um clique no botão de reset.
- **Indicação do jogador**: Mostra qual jogador está ativo ('`X`' ou '`O`').

## Estrutura do Projeto
- `src/`
  - `components/` - Contém os componentes principais da interface.
    - `Board.js`: O componente principal que renderiza o tabuleiro e as células.
    - `Square.js`: Representa cada célula do tabuleiro.
    - `Player.js`: Exibe o jogador atual ('X' ou 'O').
    - `Reset.js`: Componente para reiniciar o jogo.
    - `Winner.js`: Exibe o vencedor quando o jogo termina.
    - `History.js`: Permite visualizar e voltar a movimentos anteriores no histórico do jogo.
  - `contexts/`
    - `GameContext.js`: Contexto que fornece o estado global do jogo, incluindo tabuleiro, jogador, vencedor e histórico de jogadas.
  - `pages/`
    - `Home.js`: Página principal do aplicativo, que contém o `GameContextProvider` e o componente `Board`.
  - `utils/`
    - `calculateWinner.js`: Função que calcula o vencedor com base no estado atual do tabuleiro.
- `index.js`: Arquivo de entrada da aplicação, que inicializa o componente `Home`.
- `index.css`: Estilos globais da aplicação (não é necessário para o README, mas importante para a apresentação visual).

## Como Executar

1. Clone o repositório:
````bash
git clone https://github.com/pLogicador/react-tictactoe-hooks
````
2. Instale as dependências:
````bash
npm install
````
3. Inicie o servidor de desenvolvimento:
````bash
npm start
````
4. Abra o navegador em http://localhost:3000.

## Como Funciona
1. **Tabuleiro**: O tabuleiro é composto por 9 células (botões), que alternam entre 'X' e 'O' conforme o jogador joga. As jogadas são salvas no histórico.
2. **Histórico**: O histórico registra cada jogada, permitindo que o jogador volte a qualquer ponto do jogo.
3. **Vencedor**: O jogo verifica as condições de vitória a cada jogada e exibe o vencedor ou um empate no final.
4. **Reset**: Após o término de um jogo, o jogador pode reiniciar o jogo com o botão de reset.

## Contribuição
Sinta-se à vontade para abrir **issues** ou enviar **pull requests**!
