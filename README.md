<h1 align="center">🧩 UserForge API</h1>

<p align="center">
  <b>Sistema de Padronização de Nomes e E-mails</b><br>
  <i>Primeiro projeto do meu portfólio — desenvolvido com FastAPI, SQLite e SQLAlchemy</i> 🚀
</p>

---

## 🧠 Sobre o projeto

O **UserForge API** é uma aplicação em **Python (FastAPI)** que realiza a **padronização automática de nomes** e a **geração de e-mails corporativos** no formato `<nome.sobrenome@empresa.com.br>`.  
Além disso, os registros são armazenados em um banco de dados **SQLite**, com toda a validação feita por **Pydantic**.

Este foi meu **primeiro projeto de portfólio**, construído passo a passo para consolidar conceitos de backend, APIs REST e persistência de dados. 💡

---

## ⚙️ Tecnologias utilizadas

| Tecnologia | Descrição |
|-------------|------------|
| 🐍 **Python 3.14** | Linguagem principal do projeto |
| ⚡ **FastAPI** | Framework moderno para criação de APIs |
| 🧱 **SQLAlchemy** | ORM para comunicação com o banco de dados |
| 💾 **SQLite** | Banco de dados local simples e leve |
| 🧠 **Pydantic** | Validação de dados com tipagem rigorosa |
| 🔍 **Regex (re)** | Limpeza e normalização de textos |
| 🧰 **Uvicorn** | Servidor ASGI para rodar a API |

---

## 🗂️ Estrutura do projeto

app/
├── main.py # Código principal da API
└── init.py # (opcional)

requirements.txt # Lista de dependências
usuarios.db # Banco de dados SQLite gerado automaticamente

yaml
Copiar código

---

## 🚀 Como rodar o projeto localmente

### 🔹 1. Clonar o repositório

```bash
git clone https://github.com/gh-larissaventura/userforge-api.git
cd userforge-api
🔹 2. Criar e ativar o ambiente virtual
bash
Copiar código
python -m venv .venv
.\.venv\Scripts\activate
🔹 3. Instalar dependências
bash
Copiar código
pip install -r requirements.txt
🔹 4. Rodar o servidor
bash
Copiar código
uvicorn app.main:app --reload
🔗 Acesse a API: http://127.0.0.1:8000
📘 Documentação interativa (Swagger): http://127.0.0.1:8000/docs

🧮 Funcionalidades
✨ Padroniza nomes automaticamente
✨ Gera e-mails corporativos válidos
✨ Armazena usuários no banco de dados
✨ Valida campos com Pydantic e Regex
✨ API REST completa com rotas de criação e listagem

🧠 Exemplos de uso
🔸 POST /usuarios/
Entrada:

json
Copiar código
{
  "nome": "   MARIA   DAS   DORES   DE  SOUZA   ",
  "email": "teste@qualquercoisa.com"
}
Saída:

json
Copiar código
{
  "id": 1,
  "nome": "Maria das Dores de Souza",
  "email": "maria.das.dores.de.souza@empresa.com.br",
  "detalhes": {
    "nome_original": "   MARIA   DAS   DORES   DE  SOUZA   ",
    "nome_padronizado": "Maria das Dores de Souza",
    "email_gerado": "maria.das.dores.de.souza@empresa.com.br"
  }
}
🔸 GET /usuarios/
Saída:

json
Copiar código
[
  {
    "id": 1,
    "nome": "Maria das Dores de Souza",
    "email": "maria.das.dores.de.souza@empresa.com.br"
  }
]
💡 Próximos passos
 Adicionar testes automatizados com pytest

 Criar uma interface web simples para visualização dos usuários

 Adicionar exportação de dados para .csv

 Implementar autenticação com JWT

👩‍💻 Autora
Larissa Ventura
💼 Diretora Financeira no Instituto Farol na Quebrada
📊 Estudante de Ciência de Dados, apaixonada por tecnologia e impacto social.
🌐 LinkedIn • GitHub

🏷️ Licença
Distribuído sob a licença MIT.
Sinta-se à vontade para usar, modificar e compartilhar! 💙
