<p align = "center">
   <a href="#conceitos-envolvidos-memo">Conceitos</a>&nbsp;|&nbsp;
   <a href="#rotas-airplane">Rotas</a>&nbsp;|&nbsp;
   <a href="#instruções-scroll">Instruções</a>
</p>

## Conceitos envolvidos :memo:

* Conceitos Docker
* Trabalhando com migrations do TypeORM
* Criptografia de senha bcrypt
* Autenticação JWT
* Upload de arquivos (CSV/Imagens)
* Tratamento de erros

## Rotas :airplane:
### GET /transactions
Visualizar todas transações e o balanço atual.

<img alt="GET" src="https://uploaddeimagens.com.br/images/002/611/192/full/Sele%C3%A7%C3%A3o_031.png?1587762129" width="650px" />

### POST /transactions
Criar transação informando título, valor, tipo e categoria.

Caso a categoria já exista, não é criada uma categoria nova e ela é reaproveitada.

Caso não exista, é criada uma nova com o nome passado e atribui-se ela à transação.

Não é possível criar uma transação de retirada que extrapole o valor total do balanço atual.

<img alt="POST" src="https://uploaddeimagens.com.br/images/002/611/108/full/Sele%C3%A7%C3%A3o_027.png?1587760342" width="650px" />

### DELETE /transactions/:id
Deleta a transação id passada como parâmetro na rota.

<img alt="DELETE" src="https://uploaddeimagens.com.br/images/002/611/110/full/Sele%C3%A7%C3%A3o_028.png?1587760489" width="650px" />

### POST /transactions/import
Importar um arquivo CSV e criar transações contidas na planilha.

Também criam-se as novas categorias ou aproveitam-se as já existentes.

<img alt="CSV" src="https://uploaddeimagens.com.br/images/002/611/118/full/Sele%C3%A7%C3%A3o_029.png?1587760770" width="650px" />

<img alt="POST" src="https://uploaddeimagens.com.br/images/002/611/127/full/Sele%C3%A7%C3%A3o_030.png?1587760883" width="650px" />

## Instruções :scroll:

⚠️ Antes de rodar a API, crie um banco de dados com o nome "gostack_desafio06" ⚠️

Para baixar as dependências:
> yarn

⚠️ Antes de rodar os testes, crie um banco de dados com o nome "gostack_desafio06_tests" para que todos os testes possam executar corretamente ⚠️

Rodar os testes:
> yarn test

Rodar a api:
> yarn dev:server

<p align = "center">
  <a href="https://github.com/navarrotheus/gostack-challenges">Ver todos desafios</a>
</p>
