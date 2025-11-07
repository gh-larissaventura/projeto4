# 🧩 UserForge API — Sistema de Padronização de Nomes e E-mails

Este é um projeto desenvolvido em **Python** com **FastAPI** e **SQLite**, que tem como objetivo **padronizar nomes e gerar e-mails corporativos automaticamente**, salvando os registros em um banco de dados.  

Foi construído como parte dos meus estudos de **desenvolvimento de APIs com FastAPI**

---

## ⚙️ Tecnologias utilizadas

- 🐍 **Python 3.14**
- ⚡ **FastAPI**
- 🧠 **Pydantic**
- 🧱 **SQLAlchemy**
- 💾 **SQLite**
- 🔍 **Regex (re)**
- 🧰 **Uvicorn**

---

## 📂 Estrutura do projeto

app/
├── main.py # Código principal da API
└── init.py # (opcional, pode ser criado depois)

requirements.txt # Dependências do projeto
usuarios.db # Banco de dados SQLite gerado automaticamente


---

## 🚀 Como rodar o projeto localmente

### 1️⃣ Clonar o repositório

```bash
git clone https://github.com/gh-larissaventura/userforge-api.git
cd userforge-api

2️⃣ **Criar ambiente virtual e ativar**
python -m venv .venv
.\.venv\Scripts\activate

3️⃣ **Instalar dependências**
pip install -r requirements.txt

4️⃣ **Rodar o servidor**
uvicorn app.main:app --reload

A API ficará disponível em:
👉 http://127.0.0.1:8000

E a documentação interativa (Swagger) em:
👉 http://127.0.0.1:8000/docs

🧮 **Funcionalidades**

✅ Padronização automática de nomes
✅ Geração automática de e-mails corporativos (@empresa.com.br)
✅ Armazenamento em banco de dados SQLite
✅ Validação de e-mail com Pydantic
✅ Endpoints RESTful com FastAPI

🧠** Exemplo de uso**
POST /usuarios/

Envia um nome e um e-mail (o e-mail é obrigatório apenas para validação, mas é substituído por um e-mail corporativo gerado automaticamente):

{
  "nome": "   MARIA   DAS   DORES   DE  SOUZA   ",
  "email": "teste@qualquercoisa.com"
  
**Resposta:**

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

**GET /usuarios/**

Retorna todos os usuários cadastrados no banco de dados.

💡**Próximos passos**

 Adicionar testes automatizados com pytest

 Criar interface web para visualização

 Permitir exportação dos usuários em .csv

 Implementar autenticação (JWT)

🏷️ Licença

Este projeto é de código aberto, sob a licença MIT.
