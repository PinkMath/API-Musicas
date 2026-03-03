## 🎵 API de Músicas - Express.js

API REST simples desenvolvida com Node.js e Express para gerenciar uma coleção de músicas.

Com esta API você pode:

- Listar todas as músicas

- Buscar música por ID

- Buscar música por nome

- Cadastrar nova música

- Atualizar música

- Remover música

## 🚀 Tecnologias utilizadas

- Node.js

- Express.js

- JSON (para envio e recebimento de dados)

## 📦 Instalação

1. Clone o repositório:
```bash
https://github.com/PinkMath/API-Musicas.git
```

2. Entre na pasta do projeto:
```bash
cd API-Musicas 
```

3. Instale as dependências:
```bash
npm install
```

4. Execute o servidor:
```bash
node desafio.js
```

O servidor será iniciado em:
```code
http://localhost:3000
```

## 📁 Dados Iniciais

A API inicia com as seguintes músicas cadastradas:

- Pay no Rent – Turnpike Troubadours

- Ain't Worth the Trouble – Turnpike Troubadours

- The Bad Help – The Black Angels

- You Can't Make Old Friends – Kenny Rogers & Dolly Parton

## 📌 Endpoints da API
🔎 GET - Listar todas as músicas
```code
GET /musicas
```
Retorna todas as músicas cadastradas.

🔎 GET - Buscar música por ID
```code
GET /musicas/:id
```
Exemplo:
```code
GET /musicas/1
```
✅ Resposta (200)
```json
{
  "id": 1,
  "nomemusica": "Pay no Rent",
  "autor": "Turnpike Troubadours",
  "link": "https://..."
}
```
❌ Resposta (404)
```json
{
  "message": "este produto nao pode ser encontrada :("
}
```

🔎 GET - Buscar música por Nome
```code
GET /musicas/nome/:nomeid
```
Exemplo:
```code
GET /musicas/nome/Pay no Rent
```

#### ➕ POST - Cadastrar nova música
```code
POST /musicas
```

📥 Body (JSON)
```json
{
  "nomemusica": "Nome da Música",
  "autor": "Nome do Autor",
  "link": "https://youtube.com/..."
}
```
> ⚠ Campos obrigatórios
- nomemusica
- autor
- link

✅ Resposta (201)
Retorna o objeto recém-criado.

#### ✏ PUT - Atualizar música
```code
PUT /musicas/:id
```

📥 Body (JSON)
```json
{
  "nomemusica": "Novo Nome",
  "autor": "Novo Autor",
  "link": "https://youtube.com/..."
}
```

✅ Resposta (200)
Retorna o objeto atualizado.

#### 🗑 DELETE - Remover música
```code
DELETE /musicas/:id
```

✅ Resposta (200)
```json
{
  "message": "Produto removido com sucesso!"
}
```

## 🧪 Testando a API
Você pode testar utilizando:

- Postman

- Insomnia

- Thunder Client (extensão do VS Code)

- curl
