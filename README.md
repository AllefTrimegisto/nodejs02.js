# nodejs02.js

Sem usar bibliotecas, crie um projeto simples em Node.js que seja capaz de responder requisições HTTP.
Explique como rodar e testar.

const http = require('http');

const server = http.createServer((request, response) => {
  response.writeHead(200, { 'Content-Type': 'text/plain' });
  response.end('Hello World!');
});

const port = 3000;
server.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
node server.js

Se tudo estiver correto, você deverá ver a mensagem "Server running at http://localhost:3000" no console. Para testar se o servidor está funcionando corretamente, você pode abrir o seu navegador e acessar "http://localhost:3000". Você deverá ver a mensagem "Hello World!" na tela.

Você também pode testar o seu servidor usando uma ferramenta como o "cURL" ou o "Postman". Para fazer isso com o "cURL", você pode executar o seguinte comando no terminal:

curl http://localhost:3000
