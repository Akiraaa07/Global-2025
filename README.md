# 📦 Projeto GlobalSolution 2025 - Spring Boot + MongoDB + Azure DevOps

Este projeto consiste em uma aplicação web desenvolvida em **Java com Spring Boot**, que realiza o cadastro de **Usuarios** e **Rotas seguras**, persistindo os dados em um banco **MongoDB Atlas** na nuvem. A aplicação é implantada automaticamente no **Azure App Service** via **Azure DevOps Pipeline**.

---

## 🚀 Tecnologias Utilizadas
- Java 17
- Spring Boot 3
- MongoDB Atlas (banco na nuvem)
- Azure App Service (deploy)
- Azure DevOps (CI/CD)
- Gradle (build)
- Thymeleaf (templates HTML)

## ✅ Etapas para Testar no Azure DevOps (Professor)

### 1. Clonar o projeto:
```bash
git clone https://github.com/seu-usuario/Global-2025.git
```

### 2. Abrir o Azure DevOps
- Criar um novo projeto
- Criar uma pipeline apontando para este repositório GitHub
- Confirmar que o arquivo `azure-pipelines.yml` está na raiz

### 3. Conectar com Azure (uma vez):
- Em *Project Settings > Service Connections* → criar uma conexão chamada:
  ```
  MyazureSubscription
  ```

### 4. Executar a Pipeline
- Ela irá:
    - Criar o grupo de recurso, plano e App Service
    - Fazer o build do `.jar`
    - Publicar o deploy em:

```
https://saferoute-rm554227.azurewebsites.net/
```

### 5. Testar Funcionalidade
- Acessar `/usuarios/novo` e cadastrar um usuário
- Acessar `/api/rotasegura/cadastrar` e cadastrar um rota segura
- Verificar os dados salvos no MongoDB Atlas (coleções: `usuarios` e `rotasegura`)

---

## 🌐 MongoDB Atlas
- Banco: `odontoprevdb`
- Coleções criadas automaticamente: `usuarios`, `rotasegura`

---

## 📁 Scripts JSON (aplicável para API REST)
> Como esta aplicação usa Thymeleaf e formulários HTML, **não é necessário enviar scripts JSON**.

---

## 📌 Observações para o Professor
- O deploy pode levar de 1 a 2 minutos na primeira execução
- A aplicação já foi testada com cadastro, edição e exclusão funcionando
- A estrutura segue padrão MVC com DTOs e validação integrada

---

## 👨‍💻 Desenvolvido por
- Igor Akira
