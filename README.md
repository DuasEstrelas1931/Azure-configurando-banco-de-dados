# Passo a Passo: Configurando uma Instância de Banco de Dados no Azure

## 1. Acessar o Portal do Azure
- Acesse o [Azure Portal](https://portal.azure.com).
- Faça login com suas credenciais.

## 2. Criar uma Instância de Banco de Dados
1. No menu esquerdo, clique em **Criar um recurso**.
2. Pesquise por **Banco de Dados SQL** e selecione a opção **Banco de Dados SQL**.
3. Clique em **Criar**.

## 3. Configurar as Propriedades do Banco de Dados
1. **Nome do Banco de Dados**: Insira um nome único para o banco de dados.
2. **Servidor**:
   - Selecione um servidor existente ou clique em **Criar novo**.
   - Caso crie um novo servidor, forneça:
     - **Nome do Servidor**: Defina um nome exclusivo para o servidor.
     - **Login de Administrador do Servidor**: Defina o nome do administrador do servidor SQL.
     - **Senha**: Crie uma senha forte.
     - **Localização**: Escolha a região onde o servidor será hospedado.
3. **Plano de Preços**: Escolha o plano de preços com base nas suas necessidades:
   - **Básico**: Para cargas de trabalho pequenas.
   - **Padrão**: Para cargas de trabalho com necessidades moderadas de desempenho.
   - **Premium**: Para cargas de trabalho com altos requisitos de desempenho.

4. Clique em **Revisar + Criar** e depois em **Criar**.

## 4. Configurar Regras de Firewall do Servidor
1. Após a criação da instância, vá até o servidor SQL associado.
2. No menu do servidor, selecione **Configurações de Firewall e Rede Virtual**.
3. Adicione seu **endereço IP** para permitir conexões da sua máquina local.
4. Clique em **Salvar**.

## 5. Conectar-se à Instância de Banco de Dados
Agora que a instância de banco de dados foi criada, conecte-se usando uma das seguintes ferramentas:
- **SQL Server Management Studio (SSMS)**.
- **Azure Data Studio**.
- **Linha de Comando (CLI)** usando uma string de conexão.

### Exemplo de String de Conexão:
```bash
Server=tcp:<nome-do-servidor>.database.windows.net,1433;Initial Catalog=<nome-do-banco>;Persist Security Info=False;User ID=<nome-de-usuário>;Password=<sua-senha>;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
```

## Conclusão

Sua instância de banco de dados no Azure está agora configurada e pronta para uso. A partir daqui, você pode gerenciar dados, configurar aplicativos conectados e monitorar o desempenho através do portal do Azure.
