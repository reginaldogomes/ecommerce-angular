# E-commerce Angular - Catálogo de Produtos com Carrinho de Compras

## Descrição do Projeto
Este é um projeto de e-commerce desenvolvido em Angular que implementa as melhores práticas de Clean Code e SOLID. Ele utiliza a Fake Store API como fonte de dados para o catálogo de produtos e inclui funcionalidades para exibição de produtos, visualização de detalhes e gerenciamento de carrinho de compras.

## Funcionalidades
1. **Lista de Produtos**:
   - Exibição de todos os produtos com informações como título, preço, descrição, categoria e imagem.
   - Possibilidade de adicionar produtos ao carrinho diretamente da lista.

2. **Detalhes do Produto**:
   - Página dedicada com informações completas sobre o produto selecionado.
   - Visualização de imagem ampliada, descrição detalhada, preço e categoria.

3. **Carrinho de Compras**:
   - Adicionar e remover produtos do carrinho.
   - Exibição dos itens do carrinho com atualização dinâmica.

4. **Integração com API Pública**:
   - Dados de produtos são consumidos da [Fake Store API](https://fakestoreapi.com/).

## Tecnologias Utilizadas
- **Angular** (versão mais recente): Framework principal do projeto.
- **SCSS**: Estilização modular e customizada.
- **Angular Material**: Componentes pré-prontos para melhorar a experiência do usuário.
- **RxJS**: Gerenciamento de fluxos reativos e manipulação de dados.
- **Axios**: Biblioteca para requisições HTTP.

## Estrutura do Projeto
```
src/
├── app/
│   ├── core/                // Lógica compartilhada
│   │   ├── services/        // Services para API e negócio
│   │   │   ├── product.service.ts
│   │   │   ├── cart.service.ts
│   │   └── models/          // Interfaces e tipos
│   │       └── product.model.ts
│   ├── features/            // Módulos principais
│   │   ├── cart/            // Gerenciamento do carrinho
│   │   ├── products/        // Exibição e detalhes de produtos
│   └── app-routing.module.ts // Configuração de rotas
└── environments/            // Configurações de ambiente
```

## Endpoints da API
- **Lista de produtos**: `GET /products`
- **Detalhes do produto**: `GET /products/:id`

## Configuração e Execução
1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd ecommerce-angular
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Inicie o servidor de desenvolvimento:
   ```bash
   ng serve
   ```

4. Acesse a aplicação em `http://localhost:4200/`.

## Detalhamento das Funcionalidades
### Lista de Produtos
- **Arquivos principais**:
  - `product-list.component.ts`: Faz a requisição dos produtos via `ProductService`.
  - `product-list.component.html`: Renderiza os produtos em cards.

- **Interações**:
  - Exibição de produtos usando `*ngFor`.
  - Botão para adicionar produto ao carrinho com evento `(click)`.

### Detalhes do Produto
- **Arquivos principais**:
  - `product-details.component.ts`: Obtém os detalhes de um produto com base no ID da rota.
  - `product-details.component.html`: Renderiza detalhes completos do produto.

### Carrinho de Compras
- **Arquivos principais**:
  - `cart.service.ts`: Gerencia os produtos no carrinho.
  - Componentes podem acessar os itens do carrinho via `getCartItems()`.

- **Interações**:
  - Adicionar produtos ao carrinho.
  - Remover produtos por ID.

## Melhores Práticas Adotadas
1. **SOLID**:
   - **Responsabilidade única**: Cada serviço tem uma única responsabilidade (ex.: `ProductService` apenas gerencia produtos).
   - **Injeção de dependências**: Usado extensivamente para acoplamento reduzido.

2. **Clean Code**:
   - Nomes descritivos para variáveis, métodos e arquivos.
   - Componentes separados por funcionalidade.

3. **Reuso**:
   - Modelos de dados centralizados em `core/models`.
   - Serviços reutilizáveis.

## Contribuições
São bem-vindas contribuições para melhorias e novas funcionalidades! Abra uma *issue* ou envie um *pull request*.

## Licença
Este projeto é licenciado sob a [MIT License](LICENSE).

# ecommerce-angular
