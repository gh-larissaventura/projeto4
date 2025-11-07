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

## 📂 Estrutura do projeto

```text
app/
 ├── main.py           # Código principal da API
 └── __init__.py       # (opcional)

requirements.txt       # Lista de dependências
usuarios.db            # Banco de dados SQLite gerado automaticamente
