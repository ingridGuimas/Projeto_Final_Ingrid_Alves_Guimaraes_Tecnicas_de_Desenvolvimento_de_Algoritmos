# Sistema de Biblioteca

Este projeto é um sistema simples de gerenciamento de biblioteca desenvolvido em PHP com MySQL, utilizando Bootstrap para a interface.
O objetivo principal é aplicar os conceitos da disciplina de Programação Web e os fundamentos de algoritmos, incluindo pseudocódigo, fluxograma e lógica algorítmica.

---

## Sobre o Projeto

O sistema permite gerenciar:

- Usuários
- Livros
- Reservas

Cada módulo possui operações **CRUD**

- Cadastrar
- Listar
- Editar
- Excluir

O projeto foi desenvolvido com foco no aprendizado de:

- lógica de programação
- criação de fluxos e rotas
- manipulação de banco de dados
- divisão modular de código
- construção de interfaces simples

---

## Tela Inicial

![Tela inicial do sistema](https://github.com/ingridGuimas/Projeto_Final_Programcao_Web_Biblioteca/blob/main/tela_inicial_biblioteca.png)

---

## Tecnologias Utilizadas
- PHP
- MySQL
- HTML5
- CSS3
- Bootstrap

---

## Como Executar o Projeto

1. Coloque o projeto em uma pasta dentro do **XAMPP** ou **WAMP**  
   Exemplo: htdocs/biblioteca/
   
3. Importe o banco de dados que está na pasta **/database/biblioteca_2122n.sql**.

4. Inicie os serviços **Apache** e **MySQL**.

5. Acesse o sistema pelo navegador: http://localhost/biblioteca/

---

## Lógica Algorítmica 

O sistema funciona por meio de um controlador simples baseado em URLs.
O arquivo index.php interpreta o parâmetro ?page= e carrega a página correspondente.

O fluxo geral funciona assim: 

1. O usuário acessa o sistema.

2. O menu principal permite escolher entre Usuários, Livros e Reservas.

3. Cada ação do CRUD é mapeada por uma rota, como:
   - ?page=usuario-cadastrar
   - ?page=livro-listar
   - ?page=reserva-editar
   
4. O arquivo correspondente é carregado dinamicamente.
   
5. Ao enviar um formulário, os dados são enviados via POST para um arquivo “salvar”, que:
   - recebe os dados
   - valida
   - insere/edita/remove no banco
   - retorna mensagem
   - redireciona para a listagem
   
Esse modelo permite um fluxo simples, modular e fácil de manter.

---

## Fluxograma Geral do Sistema

![Fluxograma Geral](https://github.com/ingridGuimas/Projeto_Final_Ingrid_Alves_Guimaraes_Tecnicas_de_Desenvolvimento_de_Algoritmos/blob/main/fluxograma_geral.png)

---

## Pseudocódigo dos Principais CRUDs

### Cadastrar Usuário

INÍCIO
- Receber nome, email, telefone, endereço e data de nascimento
- Conectar ao banco de dados
- Executar INSERT na tabela usuario
- SE operação bem-sucedida
      - Exibir mensagem de sucesso
  SENÃO
      Exibir mensagem de erro

FIM

### Editar Usuário

INÍCIO
- Receber o ID do usuário
- Receber dados atualizados
- Executar UPDATE na tabela usuario
- SE operação bem-sucedida
      Exibir mensagem de sucesso
  SENÃO
      Exibir mensagem de erro
 FIM

### Excluir Usuário
INÍCIO
- Receber o ID do usuário
- Executar DELETE na tabela usuario
- SE operação bem-sucedida
      Exibir mensagem de sucesso
  SENÃO
      Exibir mensagem de erro

FIM

### Cadastrar Livro

INÍCIO
- Receber título, ano e gênero
- Conectar ao banco
- Executar INSERT na tabela livro
- Mostrar mensagem para o usuário
FIM

### Cadastrar Reserva

INÍCIO

- Receber id_usuario e id_livro
- Verificar se o livro está disponível
- SE disponível
      - Inserir reserva na tabela reserva
      - Exibir sucesso
  SENÃO
      - Informar indisponibilidade

  FIM

---

## Estrutura de Pastas

- biblioteca/
- usuario/
- livro/
- reserva/
- css/
- js/
- database/
- index.php
- config.php
- README.md

---

## Autora

**Ingrid Guimarães**  



