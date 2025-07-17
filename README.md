# DevTech.ApiAuth 🔒

API REST em ASP.NET Core com autenticação personalizada baseada em tokens GUID — ideal para estudos e protótipos de segurança.

---

## 🚀 Funcionalidades

- Senhas protegidas com **HmacSha256Signature**  
- Login que gera **token GUID** com validade (ex: 2 horas)  
- Middleware para proteger rotas autenticadas

---

## 🧩 Tecnologias utilizadas

- [ASP.NET Core](https://dotnet.microsoft.com/) (C#)  
- JWT customizado com tokens GUID

---

## 💡 Pré-requisitos

- SDK .NET 9.0  
- Ferramenta REST (Postman)

---

## ⚙️ Como executar

1. Clone o repositório  
   ```bash
   git clone https://github.com/pontesdevtech/DevTech.Estudo.ApiAuth.git
   cd DevTech.Estudo.ApiAuth
   ```

2. Restaure dependências e compile  
   ```bash
   dotnet restore
   dotnet build
   ```

3. Inicie a API:  
   ```bash
   dotnet run
   ```

---

## 🔐 Exemplos de uso

- **Registro**:  
  `POST /login`  
  ```json
  {
    "username": "batman",
    "password": "batman"
  }
  ```
  - Retorno:  
    ```json
  {
    "user": {
        "id": 1,
        "username": "batman",
        "password": "",
        "role": "manager"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImJhdG1hbiIsInJvbGUiOiJtYW5hZ2VyIiwibmJmIjoxNzUyNzEyMjU1LCJleHAiOjE3NTI3MTk0NTUsImlhdCI6MTc1MjcxMjI1NX0.uIt8isWT6_5sfQBoGpo0PKCXoMpCJk67HRoVwOtdbGg"
  }
    ```
  - O token expira em 2 horas. Após isso, será necessário logar novamente.

---

## 🔄 Próximas melhorias

- Mudar token GUID para **JWT padrão (Bearer)**  
- Implementar **Refresh Tokens**  
- Adicionar **Swagger/OpenAPI**  
- Testes automatizados (unitários e de integração)  
- Dockerização da aplicação e do banco

---

## 📝 License

Este projeto é aberto e está licenciado sob a **MIT License**.

---

**Made with ❤️ por PontesDevTech**