
---

## 🧩 O que é o padrão MVC
	
O **MVC (Model-View-Controller)** é um **padrão de arquitetura de software** que organiza o código de uma aplicação em **três camadas principais**, separando responsabilidades.  
Ele é como uma **estrutura base (planta)** que orienta o desenvolvimento, tornando o sistema **mais limpo, organizado e fácil de manter**.
	
 Ele divide a aplicação em três CAMADAS principais:
	
|Camada|Função principal|O que faz no Laravel|Caminho padrão|
|---|---|---|---|
|**Model (Modelo)**|Representa a **lógica da aplicação** e **regras de negócio**. É responsável por se **comunicar com o banco de dados**.|Utiliza o **Eloquent ORM** para buscar, salvar e manipular dados.|`app/Models`|
|**View (Visão)**|Define o que o **usuário vê** — a interface visual da aplicação.|Exibe páginas HTML, geralmente com o **Blade Template**.|`resources/views`|
|**Controller (Controlador)**|Atua como um **intermediário** entre o Model e a View.|Recebe as requisições, chama o Model e envia os dados para a View.|`app/Http/Controllers`|

---

## **3. Fluxo de funcionamento do MVC no Laravel**

1. **O usuário faz uma requisição** (exemplo: acessa `/usuarios`).
    
2. O Laravel **verifica a rota** em `routes/web.php`.
    
3. A rota **chama o método** de um **Controller** (ex: `UsuarioController@index`).
    
4. O **Controller** solicita dados ao **Model**.
    
5. O **Model** busca os dados no banco de dados e os retorna ao Controller.
    
6. O **Controller** envia esses dados para uma **View**.
    
7. A **View** exibe as informações para o usuário na tela.
    

**Fluxo resumido:**  
`Rota → Controller → Model → Controller → View`

---

## **4. Importância do MVC**

- **Organização:** separa responsabilidades, deixando o código mais limpo.
    
- **Facilidade de manutenção:** é mais fácil localizar e corrigir problemas.
    
- **Reuso de código:** cada parte pode ser reaproveitada em outros pontos da aplicação.
    
- **Trabalho em equipe:** vários desenvolvedores podem atuar em camadas diferentes sem se atrapalhar.