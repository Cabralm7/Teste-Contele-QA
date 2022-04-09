![header](https://capsule-render.vercel.app/api?type=waving&color=auto&height=300&section=header&text=Contele&fontSize=90&animation=fadeIn&fontAlignY=38&desc=%20%20%20%20%20%20%20&descAlignY=100&descAlign=62)


# Teste-Contele-QA
A proposta do desafio deve conter a criação de uma conta e utilizando a documentação disponibilizada no site https://dummyapi.io realizar validação dos 4 endpoints disponiveis (User Controller, Post Controller, Comment Controller, Tag Controller)


<aside>
💡 Crie uma conta e utilizando a documentação disponibilizada no site [https://dummyapi.io](https://dummyapi.io/)
 realize a validação dos 4 Endpoints disponiveis (User Controller, Post Controller, Comment Controller, Tag Controller)

</aside>

# Requisitos

<aside>
💡 Executar do começo ao fim e documentar a validação dos 4 Endpoints disponiveis (User Controller, Post Controller, Comment Controller, Tag Controller)

</aside>

# Documentação

<aside>
💡 Todos os modelos de requisição e Endpoints se encontram nesse link: [https://dummyapi.io/docs](https://dummyapi.io/docs)
  Github do projeto de testes: [https://github.com/contele/contele-vagas/tree/master/QA](https://github.com/contele/contele-vagas/tree/master/QA)
  Notion da Documentação completa: https://boom-spectrum-9c0.notion.site/Teste-Contele-14b3a22a0e9f4e57a238a8e97df2c582

</aside>

# Test Cases

## **User Controller**

### Generico

Passo genérico que deve ser seguido para todas as requests.

![Untitled](https://user-images.githubusercontent.com/91293456/162552040-c28ebd76-9eaa-4dba-933c-4f495fb21e31.png)


---

# **Create User**

Criar um novo usuário, retornar data de usuário criada

**Body:** User Create (firstName, lastName, email are required)

### Critérios de Aceite

1. Rodar o Endpoint de `/create`.
2. Formatar o Body de acordo com as necessidades especificadas “firstName, lastName e email” e adicionar os dados.
3. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Screenshot_1](https://user-images.githubusercontent.com/91293456/162552092-c3a45443-7d0e-40ce-8bc6-7cd8c62bc9c0.png)


---

### Critério de negação

Foram executados testes onde devem apresentar erros.

1. Executado os testes sem firstname, lastname, email, sem os três dados, sem String, sem formatação correta de email e com o mesmo exemplo de email que um usuário já cadastrado. Todos os testes apresentaram o Status Code 400 “Bad Request” Body invalido.

![Untitled](https://user-images.githubusercontent.com/91293456/162552114-509c558f-ab32-4329-8039-bae8a64de4d5.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552132-d443c0ef-9a5e-4cf8-a1ea-c08647c8db69.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552140-2e7d3874-9725-428f-aae5-67dfa3094810.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552156-4660b2a7-bb3a-4c47-b762-db3193752a6e.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552163-8a5a846a-427d-4c4e-abb0-fff2837c2d93.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552173-e7ded066-41df-4679-924d-287c866bd49e.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552180-aa930bb7-fa25-4637-b6c4-19ab6df9b8fd.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552185-bd48709d-3f5e-4cd4-bf90-71d4b9306802.png)

---

# **Get List**

Cria uma lista de usuários ordenada, a partir da data de registro.

### Criterio de aceite

1. Rodar o Endpoint `/user`.
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552220-e5a5d0eb-ec78-4db5-8d26-898f31037465.png)

---

# **Get User by id**

Retorna o cadastro do usuário completo a partir do ID gerado.

### Criterio de aceite

1. Rodar o Endpoint `/user/:id`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552235-095f9672-ad8b-4a99-9daf-9be74224dcb7.png)

### Critério de negação

1. Executado o teste com o ID incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552241-a0fc1a3e-1b9f-4cde-9fd8-0c33496dfe14.png)

---

# **Update User**

Atualiza os dados do usuário a partir do ID.

### Criterio de aceite

1. Rodar o Endpoint PUT `/user/id`.
2. Colocar o ID de usuário cadastrado.
3. Informe os dados atualizados dos campos “firstname” e “lastname”.
4. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled(1)](https://user-images.githubusercontent.com/91293456/162552251-de03fa7b-9b3a-437a-8b2a-5db00f16183e.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552265-d694321a-087f-4011-9e3d-6fad69861145.png)

### Critérios de negação

Foram encontrados diversos Bugs onde foram relatados no final do documento. “[Bugs](https://www.notion.so/Teste-Contele-14b3a22a0e9f4e57a238a8e97df2c582)”

---

# **Delete User**

Deletar o usuário a partir do ID

### Criterio de Aceite

1. Rodar o Endpoint DELETE `/user/id`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.
3. Verificar no Getlist e no Getlist By ID se o usuário foi devidamente deletado.

![Untitled](https://user-images.githubusercontent.com/91293456/162552290-33878b04-2063-4421-8697-2634f4a4fe0f.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552301-620d269a-6a74-40ba-bdc3-afd358946607.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552312-c11555ab-ffbd-4a6f-a7d3-79956baf34d4.png)

---

# Ações de Melhoria

### Getlist

Aumentar o limite de users.

![Untitled](https://user-images.githubusercontent.com/91293456/162552320-8bde4d8d-7c2e-4aba-a9a5-592d2b5503fa.png)

---

### Delete user

Apresentar no Body uma mensagem informando que o Usuário foi devidamente deletado.

![Untitled](https://user-images.githubusercontent.com/91293456/162552334-95cf98f2-95bb-43e8-8f61-36914fd05048.png)

---

# Bugs

### **Update User**

O campo “email” é proibido a alteração, porém a API não repassa um Status da impossibilidade da mudança.

![Untitled](https://user-images.githubusercontent.com/91293456/162552338-1abe4a0d-9397-40b6-b8cc-f7909f3fa9d1.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552362-f0caeb55-67ab-4e48-979b-0f71443282d4.png)

---

### **Update User**

A API permite que os campos “firstname” e “lastname” sejam atualizados sem informações.

![Untitled(1)](https://user-images.githubusercontent.com/91293456/162552381-929df6ac-622b-4080-a919-6367ad53b219.png)

---

### **Update User**

Após o teste de negação do Update User, ao remover o “firstname” e “lastname” de dentro das Strings, retorna o Status Code 400 (o que era de se esperar), porém a Response retorna um HTML de erro.

![Untitled](https://user-images.githubusercontent.com/91293456/162552395-592b7eec-b98c-40be-b071-ec4fc81ab423.png)

---

### Create User

Após o teste de negação do Create User, ao remover o “firstname”, “lastname” e “email” de dentro das Strings, retorna o Status Code 400 (o que era de se esperar), porém a Response retorna um HTML de erro.

![Untitled](https://user-images.githubusercontent.com/91293456/162552404-46b3f4d3-8527-412c-b0e4-7fdc00947c4d.png)

---

# **Tag Controller**

# Get List

Retorna uma lista das Tags.

### Criterio de Aceite

1. Rodar o Endpoint DELETE `/tag`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552409-ee10b47c-b468-4485-ba5b-ca8c16b3b13d.png)

---

# Create Post

Cria um Post para um determinado Usuário a partir do ID

### Criterio de aceite

1. Rodar o Endpoint de `/post/create`.
2. Formatar o Body de acordo com as necessidades especificadas “likes”, “tags” “text” e “owner” e adicionar os dados necessários.
3. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled(1)](https://user-images.githubusercontent.com/91293456/162552412-56d0762e-6804-4554-9e5a-b81704b46c7e.png)

---

### Critério de negação

Foram executados testes onde devem apresentar erros.

1. Executado o teste  do campo “owner” sem os três dados, sem String. Todos os testes apresentaram o Status Code 400 “Bad Request” Body invalido e Erro HTML.

![Untitled](https://user-images.githubusercontent.com/91293456/162552422-d6a9d447-d7a8-4922-b127-00b3e93ebb59.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552425-4c7f980e-89a6-4d7f-bdad-31a7b11a17d0.png)

---

# **Get List**

Cria uma lista dos posts ordenada, a partir da data de registro.

### Criterio de aceite

1. Rodar o Endpoint `/post`.
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552431-4ef9cfd3-36fe-4cd7-9293-ece0bcd70b4e.png)

---

# **Get Post by id**

Retorna o post a partir do próprio ID do post.

### Criterio de aceite

1. Rodar o Endpoint `/post/:id`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552442-0800af1c-eecc-4a50-92d4-95bd2c1c897f.png)

---

### Critério de negação

1. Executado o teste com o ID incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552467-295a8058-576a-41d8-8b28-4f02a3e5e420.png)

---

# **Get List by User**

Retorna todos os posts do usuário a partir do ID do mesmo.

### Criterio de aceite

1. Rodar o Endpoint `/user/:id/post`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552486-48ccb44c-4156-4343-9613-b79d4ef6ce51.png)

---

### Critério de negação

1. Executado o teste com o ID do usuário incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552492-fa107b1c-557d-495b-9c36-08d6680cf34a.png)

---

# **Get List by User**

Retorna uma lista de posts para uma tag específica a partir da data de criação.

### Criterio de aceite

1. Rodar o Endpoint `/tag/:id/post`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.
    
![Untitled](https://user-images.githubusercontent.com/91293456/162552511-b60eafb5-2a6e-446f-9b2f-992c9dbb68d7.png)

---

# **Update Post**

Atualiza os dados do post a partir do ID.

### Critério de aceite

1. Rodar o Endpoint `/post/:id`
2. Colocar o ID do Post .
3. Informe os dados atualizados dos campos necessários.
4. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552517-66bcd19d-cfcd-4cf7-a21e-2a6f497956a6.png)

---

### Critério de negação

1. Executado o teste com o ID do Post incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552528-e8a3016e-8028-4470-98d7-e4fc634af44b.png)

---

# **Delete Post**

Deletar o post a partir do ID

### Criterio de Aceite

1. Rodar o Endpoint DELETE `/post/id`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.
3. Verificar no Getlist e no Getlist By ID se o usuário foi devidamente deletado.

![Untitled](https://user-images.githubusercontent.com/91293456/162552536-e7f08007-2d0b-4bcc-a857-9eaa7c15483e.png)

---

### Critério de negação

1. Executado o teste com o ID do Post incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552542-23059f5a-969f-4d0d-9493-a075067aca80.png)

---

# Bugs

### Create Post

Permite o envio de um post sem os dados dos campos, e o campo “likes” caso não seja preenchido apresenta um erro de HTML

![Untitled](https://user-images.githubusercontent.com/91293456/162552547-36436d04-503c-4c88-845a-218cf04e5f29.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552561-02d1cd25-ebd1-4660-bb7b-daab482ffbb8.png)

---

### Get List by Tag

A mesma após executada, retorna o Status Code 200, porém no Body não apresenta conteúdo nenhum.

![Untitled](https://user-images.githubusercontent.com/91293456/162552571-52088aa6-b943-4c53-b13f-1f6bf36685ac.png)

---

### Get List by Tag

Caso o ID do Post estejá incorreto, o Status Code 200 permanece OK!

![Untitled](https://user-images.githubusercontent.com/91293456/162552577-827be471-ed90-4f05-803c-908175904313.png)

---

# Comment **Controller**

# Create Comment

Cria um novo comentário.

### Criterio de aceite

1. Rodar o Endpoint de `/comment/create`.
2. Formatar o Body de acordo com as necessidades especificadas "message”, "post” e “owner” e adicionar os dados necessários.
3. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552587-5e2f6bec-cdbc-45ca-ad81-52a498275779.png)

---

### Critério de negação

Foram executados testes onde devem apresentar erros.

1. Executado os testes sem owner ou post, sem os dois dados, sem String, Todos os testes apresentaram o Status Code 400 “Bad Request” Body invalido.

![Untitled](https://user-images.githubusercontent.com/91293456/162552599-11bc8db7-a11f-4857-a384-1ae8e2d005f5.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552608-691f5696-36ae-4872-a24e-a76c504b9011.png)

![Untitled](https://user-images.githubusercontent.com/91293456/162552614-dec8638b-3eb1-4a88-81cb-4251aa295673.png)

---

# **Get List**

Cria uma lista dos comentarios ordenada, a partir da data de registro.

### Criterio de aceite

1. Rodar o Endpoint `/comment`.
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552619-7f0b6320-d065-444d-aabc-0fe2edcb6371.png)

---

# **Get list by Post**

Retorna a lista de comentarios de um determinado post a partir do ID do mesmo.

### Criterio de aceite

1. Rodar o Endpoint `/post/:id/comment`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552625-685aa12a-9446-4bea-a5fe-16de5275cfbb.png)

---

### Critério de negação

1. Executado o teste com o ID do Post incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled(1)](https://user-images.githubusercontent.com/91293456/162552633-491fa3e2-5364-45d1-ac19-fbeb3c3d3a92.png)

---

# **Get list by User**

Retorna a lista de comentarios de um determinado usuario a partir do ID do mesmo.

### Criterio de aceite

1. Rodar o Endpoint `/user/:id/comment`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552645-fc9f31ab-2727-4981-832a-a5b0db5cbec2.png)

---

### Critério de negação

1. Executado o teste com o ID do Post incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552652-dc4f1036-520c-45b9-89f1-b752f06b0098.png)

---

# Delete User

Deleta um comentario de um post a partir do ID do mesmo.

### Criterio de aceite

1. Rodar o Endpoint `/comment/:id`
2. Após clicar no botão “**Send**”, verificar o retorno da requisição (**Status Code 200**) e verificar os dados retornados da request.

![Untitled](https://user-images.githubusercontent.com/91293456/162552666-5edffd2c-4363-4ac4-b675-666767aea04d.png)

---

### Critério de negação

1. Executado o teste com o ID do Post incorreto, o mesmo retorna um Status Code 400 “Bad Request” Parâmetros  não validos.

![Untitled](https://user-images.githubusercontent.com/91293456/162552676-a4de2a34-b1bf-4f68-8e74-fb4659a3e266.png)

---

# Bug

### Create Comment

Permite o envio de um comentário sem os dados do campo message.

![Untitled](https://user-images.githubusercontent.com/91293456/162552690-26714674-ecb5-4fea-a793-b01e508ab5ea.png)

---

### Create Comment

Há um erro de HTML caso os campos owner ou post estejam fora da String.

![Untitled](https://user-images.githubusercontent.com/91293456/162552700-9a814532-cfd6-4c26-bb07-0e0881220311.png)

