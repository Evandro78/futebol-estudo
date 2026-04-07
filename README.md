#  Projeto Django - Sistema de Times de Futebol

##  Descrição

Este projeto é uma aplicação web desenvolvida com o framework **Django**, com o objetivo de cadastrar evisualizar informações sobre times de futebol.

A aplicação permite que o usuário administre os dados através do painel administrativo do Django e visualize os times cadastrados em uma página web.

---

##  Funcionalidades

* Cadastro de times de futebol
* Visualização dos times em uma página web
* Interface administrativa para gerenciamento dos dados
* Exibição de informações como:

  * Nome do time
  * Cidade
  * Estádio
  * Ano de fundação

---

##  Tecnologias utilizadas

* Python
* Django
* SQLite (banco de dados padrão do Django)
* HTML + CSS

---

##  Como o sistema funciona

###  1. Model (Banco de Dados)

O sistema possui um model chamado **Time**, responsável por armazenar os dados:

* nome
* cidade
* estádio
* fundação

Esses dados são salvos automaticamente no banco de dados SQLite.

---

###  2. Admin (Painel de Controle)

O Django possui um painel administrativo onde é possível:

* Adicionar novos times
* Editar times existentes
* Remover registros

Acesse em:

```
http://127.0.0.1:8000/admin
```

---

###  3. View (Lógica)

A view busca todos os times cadastrados no banco:

```python
times = Time.objects.all()
```

E envia esses dados para o template HTML.

---

###  4. Template (Interface)

Os dados são exibidos na página utilizando Django Template:

```html
{% for time in times %}
```

Cada time é mostrado com suas informações.

---

##  Como executar o projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/Evandro78/futebol-estudo.git
cd futebol-estudo
```
 2. Criar ambiente virtual

```bash
python -m venv venv
venv\Scripts\activate
```

3. Instalar dependências

```bash
pip install -r requirements.txt
```

### 4. Aplicar migrações

```bash
python manage.py migrate
```

### 5. Criar superusuário

```bash
python manage.py createsuperuser
```

---

### 6. Rodar o servidor

```bash
python manage.py runserver
```

---

### 7. Acessar o sistema

* Página principal:

```
http://127.0.0.1:8000/
```

* Admin:

```
http://127.0.0.1:8000/admin
```

---

##  Estrutura do projeto

```
futebol-estudo/
│
├── futebol_proj/     # Configurações do projeto
├── times/            # Aplicação principal
├── manage.py
├── db.sqlite3
└── README.md
```

---

##  Controle de versão (Git)

Para salvar alterações no repositório:

```bash
git add .
git commit -m "Atualização do projeto"
git push
```

