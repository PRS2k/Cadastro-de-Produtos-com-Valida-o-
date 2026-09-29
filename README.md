# Sistema de Cadastro de Produtos (PHP + MySQL)

Este projeto consiste em uma aplicação web simples desenvolvida em PHP e HTML, integrada a um banco de dados MySQL, destinada ao cadastramento de produtos com validação de dados tanto no lado do servidor quanto via JavaScript para mensagens temporárias.

---

## 🚀 Funcionalidades

- **Formulário de Cadastro:** Interface para inserção do nome e preço do produto.
- **Validação de Dados em PHP:**
  - Verifica se o nome do produto não está vazio.
  - Garante que o preço informado é um número válido e maior que zero.
- **Integração com Banco de Dados:** Conexão direta via `mysqli` para inserção de dados na tabela `produtos`.
- **Feedback Interativo:** Exibe mensagens de sucesso ou erro formatadas e utiliza JavaScript para ocultar a mensagem automaticamente após 5 segundos.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Estrutura da interface do usuário.
- **PHP 8.x:** Processamento de formulários, validação de regras de negócio e comunicação com o banco de dados.
- **MySQL:** Banco de dados relacional para armazenamento dos registros.
- **JavaScript:** Manipulação do DOM para temporizar o encerramento da exibição de mensagens.

---

## 🗄️ Estrutura do Banco de Dados

Para que o projeto funcione corretamente, certifique-se de criar o banco de dados e a tabela executando o seguinte script SQL no seu MySQL:

```sql
CREATE DATABASE IF NOT EXISTS exercicio;
USE exercicio;

CREATE TABLE IF NOT EXISTS produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    preco DECIMAL(10, 2) NOT NULL,
    criado_em TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
