
---

## 🧱 2️⃣ Estrutura de pastas do Laravel — visão geral

O Laravel é baseado no **padrão MVC (Model-View-Controller)**, e as pastas refletem exatamente essa separação.

Vamos revisar com base nas suas anotações e corrigir o que precisa 👇

---

### 📂 `app/`
	
> **Contém a lógica da aplicação, incluindo a manipulação de dados**
	
Aqui ficam os **Models**, **Controllers**, **Policies**, **Middlewares**, etc.  
Exemplo:
	
```
app/
 ├── Http/
 │   ├── Controllers/
 │   │   └── UserController.php
 │   ├── Middleware/
 │   └── Kernel.php
 ├── Models/
 │   └── User.php

```

👉 Tudo que envolve **lógica de negócio e manipulação de dados**.

---

### ⚙️ `config/`

> **Arquivos de configuração**
	
Cada arquivo dentro dessa pasta controla uma parte do comportamento do framework.
	
Exemplo:

- `config/app.php` — nome, timezone, idioma
    
- `config/database.php` — conexão com o banco
    
- `config/mail.php` — envio de e-mails
    

---

### 🗂️ `database/`

> **Manipulação do banco de dados**

```
project>database
```

Aqui ficam:

- **Migrations** (versões das tabelas)
    
- **Seeders** (dados de exemplo)
    
- **Factories** (geradores de dados fake)
    

📘 Exemplo:

```
database/
 ├── migrations/
 ├── seeders/
 └── factories/

```

---

### 🎨 `resources/`

> **Arquivos exibidos ao cliente (views, assets)**, Tudo o que o usuário **vê** está aqui.

Contém:

- `views/` → arquivos Blade (`.blade.php`)
    
- `css/`, `js/`, `images/` (opcionalmente)
    
- `lang/` → arquivos de tradução
    

📘 Exemplo:

```
resources/
 ├── views/
 │   └── welcome.blade.php
 ├── css/
 └── js/

```

---

### 🌐 `routes/`

> **Definição das rotas**

```
project>routes

```
Dentro dela:

- `web.php` → rotas de páginas normais (navegador)
    
- `api.php` → rotas de APIs
    
- `console.php` → comandos do terminal
    
- `channels.php` → eventos/broadcast
    

📘 Exemplo:

```php
// routes/web.php
Route::get('/ola', function () {
    return 'Olá Mundo!';
});

```

---

### 🧩 MVC na prática

O fluxo é assim:

```
[ Navegador ] → [ Rota ] → [ Controller ] → [ Model ] → [ Banco de Dados ] →
→ [ View ] → [ Resposta ao Usuário ]

```
🔹 **Model** → representa os dados e regras de negócio  
🔹 **View** → exibe a informação (HTML, Blade)  
🔹 **Controller** → faz a ponte entre rota, model e view

---

## 🧠 3️⃣ Dica extra — Entendendo o papel do `artisan`

O **Artisan** é a ferramenta de linha de comando do Laravel.  
Alguns comandos úteis:

|Comando|Função|
|---|---|
|`php artisan serve`|Sobe o servidor local|
|`php artisan make:controller NomeController`|Cria um controller|
|`php artisan make:model NomeModel -m`|Cria um model e migration|
|`php artisan migrate`|Executa migrations (cria tabelas)|
|`php artisan route:list`|Lista todas as rotas do sistema|

---

