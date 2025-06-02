# 🗂️ Laboratório - Amazon S3 Básico | Developer EDN | Escola da Nuvem

Este repositório contém o passo a passo do **Laboratório - Amazon S3 Básico** realizado no curso **Developer EDN** da Escola da Nuvem.  

> 🚀 **Objetivos**:
> - Criar buckets no Amazon S3 com configurações seguras.
> - Ativar e utilizar o versionamento.
> - Configurar regras de ciclo de vida.
> - Gerar URLs pré-assinadas.
> - Ativar e consultar logs de acesso usando um segundo bucket.

---

## 📂 Índice

- [1️⃣ Criação do Bucket (Repositório de Arquivos)](#1️⃣-criação-do-bucket-repositório-de-arquivos)
- [2️⃣ Upload de Arquivos e Versionamento](#2️⃣-upload-de-arquivos-e-versionamento)
- [3️⃣ Regras de Ciclo de Vida](#3️⃣-regras-de-ciclo-de-vida)
- [4️⃣ Geração de URLs Pré-assinadas](#4️⃣-geraçao-de-urls-pré-assinadas)
- [5️⃣ Criação do Bucket para Logs de Acesso](#5️⃣-criação-do-bucket-para-logs-de-acesso)
- [6️⃣ Configuração do Bucket de Logs](#6️⃣-configuração-do-bucket-de-logs)
- [7️⃣ Testando a Geração de Logs](#7️⃣-testando-a-geraçao-de-logs)

---

## 1️⃣ Criação do Bucket (Repositório de Arquivos)

1. Acesse o console do S3:  
   - Pesquise por **S3** no console da AWS e abra o serviço.  
2. Selecione a região **us-east-1 (Norte da Virgínia)**.  
3. Clique em **Criar bucket**.  
4. Nomeie o bucket (exemplo):
5. Configure:  
- **Bloquear todo o acesso público** ✅  
- **Versionamento**: Desativado (ativaremos depois).  
- **Criptografia**: Mantenha como SSE-S3.  
6. Clique em **Criar bucket**.

<!-- 📸 Adicione aqui o print do bucket criado -->

---

## 2️⃣ Upload de Arquivos e Versionamento

1. Crie o arquivo `Lab9.txt` na sua máquina com o conteúdo:
2. Faça o upload do arquivo para o bucket.
3. Ative o **versionamento** no bucket:
- Aba **Propriedades** > **Versionamento de bucket** > Ativar.
4. Edite o arquivo `Lab9.txt` adicionando:
5. Faça o upload novamente.
6. Visualize as versões na aba **Objetos** > Ativar "Mostrar versões".

<!-- 📸 Adicione aqui o print do versionamento habilitado e múltiplas versões -->

---

## 3️⃣ Regras de Ciclo de Vida

1. No bucket, vá em **Gerenciamento** > **Criar regra de ciclo de vida**.  
2. Configure:  
- Nome: `MoverParaGlacierApos30Dias`.  
- Aplicar a todos os objetos.  
- Transição para **Glacier Instant Retrieval** após 30 dias.  
- Expiração após 31 dias.  
3. Salve a regra.

<!-- 📸 Adicione aqui o print da regra criada -->

---

## 4️⃣ Geração de URLs Pré-assinadas

1. Na aba **Objetos**, clique no arquivo `Lab9.txt`.  
2. Clique em **Ações** > **Compartilhar com um URL pré-assinado**.  
3. Defina o tempo de expiração (exemplo: 1 minuto).  
4. Gere e copie a URL.  
5. Abra a URL em uma janela anônima para testar.

<!-- 📸 Adicione aqui o print da URL pré-assinada e do acesso -->

---

## 5️⃣ Criação do Bucket para Logs de Acesso

1. Crie um segundo bucket para os logs:
2. Configure:
- **Bloquear todo o acesso público** ✅  
- Demais configurações: padrão.  
3. Clique em **Criar bucket**.

<!-- 📸 Adicione aqui o print do bucket de logs -->

---

## 6️⃣ Configuração do Bucket de Logs

1. Acesse o bucket principal (do lab).  
2. Aba **Propriedades** > **Registro em log de acesso ao servidor** > Editar.  
3. Ative o registro de logs e selecione o bucket de logs como destino.  
4. Salve as alterações.

<!-- 📸 Adicione aqui o print da configuração de logs -->

---

## 7️⃣ Testando a Geração de Logs

1. Faça upload de um novo arquivo (ex.: uma imagem) no bucket principal.  
2. Aguarde cerca de **1h30** para que os logs sejam gerados no bucket de logs.  
3. Verifique o bucket de logs após o tempo.

<!-- 📸 Adicione aqui o print dos logs gerados no bucket de logs -->

---

## 8️⃣ Limpeza dos Recursos (Importante!)

Após concluir o laboratório, **exclua todos os buckets criados** para evitar custos desnecessários.  
- Exclua o bucket principal.
- Exclua o bucket de logs.  

---

## 📌 Notas Finais

📝 Esse laboratório me ajudou a entender as práticas recomendadas para **segurança, versionamento, gerenciamento de dados e monitoramento no Amazon S3**.  

👨‍💻 Feito com 💙 na **Escola da Nuvem | Developer EDN**.  

---

## 📎 Links úteis

- [Documentação Oficial do Amazon S3](https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/ServerLogs.html)

  
 
  
  
