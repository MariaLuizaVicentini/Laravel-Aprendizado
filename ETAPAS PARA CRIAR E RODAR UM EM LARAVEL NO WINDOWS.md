
# 1 - Verificar se o ambiente esta pronto

O **Laravel** precisa de **três componentes essenciais** para funcionar corretamente:

- **PHP** – Linguagem principal utilizada pelo Laravel
    
- **Composer** – Gerenciador de dependências do PHP
    
- **Servidor local** – Pode ser o **embutido do PHP** ou o **Artisan**, que é o servidor próprio do Laravel

Abra o prompt de comando e digite:

```
php -v 

composer -v
```

- **php -v:**
    - Se o PHP estiver instalado, exibe a versão instalada.
        
    - Caso contrário, retorna um erro informando que o comando não foi encontrado.
        
- **composer -v:**
    - Se o Composer estiver instalado, exibe a versão.
        
    - Caso contrário, exibe uma mensagem indicando que o comando não foi reconhecido.

---
# 2 - Criar o projeto

- Entre dentro da pasta que queremos criar o projeto

```
cd nome-pasta
```

- Insira o comando abaixo para criar o projeto, baixar a estrutura do laravel e criar as pastas automaticamente 

```
composer create-project laravel/laravel nome-projeto
```

---

# 3 - Entrar no diretório e subir o servidor 

- Após a instalação, acesse a pasta do projeto através do CMD
```
cd nome-projeto
```

- Inicie o servidor local com o seguinte comando: 
```
php artisan serve
```

**O que é o Artisan:**
	
- Artisan é um arquivo executável em PHP, que fica na raiz seu projeto criado em laravel
	
- Ele é acessado através dos nossos comandos no CMD para interagir com o Laravel

**Explicação do código:**
	
- No começo do comando:
```
php artisan
```
-  estamos basicamente chamando o arquivo artisan e pedindo para que o php execute ele
	
- O comando seguinte:
```
serve
```
- É a ação (parte do script artisan) que queremos que o artisan execute. 

---
# 4 - Acessando o laravel no navegador 

- Após inicial o servidor embutido no PHP através do CMD com o artisan 
	
- O CMD vai retornar o endereço correto no navegador para acessar sua aplicação via web 
```
   INFO  Server running on [http://127.0.0.1:8000].
```