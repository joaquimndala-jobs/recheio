# Redesenho da loja online Recheio

Redesenho académico da loja pública da Recheio Cash & Carry, S.A., em Moçambique, feito em HTML, CSS e JavaScript puro. A entrega parte da página de lista de desejos indicada no enunciado e refaz a experiência de compra, com conteúdo real recolhido do site oficial.

## Conteúdo recolhido

- 440 produtos identificados em 16 categorias e nas colecções públicas de Movimento rápido, Últimas novidades e Zona de ofertas.
- Nomes, marcas, subcategorias, descrições disponíveis, preços, stock e variantes de unidade associados às filiais divulgadas pela loja.
- 233 imagens individuais de produtos, 16 imagens de categoria e 4 banners guardados no projecto. Quando não foi possível obter uma imagem individual, o cartão usa a imagem local da categoria.
- Filiais, contactos, navegação institucional e links para políticas e fichas oficiais.
- Recolha de referência em 19 de Novembro de 2026. O catálogo público tem mais artigos; estes 440 registos são uma selecção local e estática. Preços e disponibilidade podem mudar.

O projecto não se liga à autenticação, inventário ou processamento de pagamentos da Recheio. O acesso à conta real abre a página oficial. O perfil local e o histórico de pedidos de demonstração ficam neste navegador; o checkout de demonstração não envia encomendas e não recolhe dados de cartão. Favoritos, carrinho, subtotal, partilha e newsletter continuam locais.

## Executar

É necessário servir a pasta por HTTP para carregar `data/catalog.json`.

```bash
python3 -m http.server 8000
```

Abra `http://localhost:8000`.

## Ficheiros principais

- `index.html` — estrutura, navegação, secções da loja, filtros, diálogos e painéis.
- `styles.css` — identidade visual, ícones SVG, cartões, responsividade, foco e estados interactivos.
- `app.js` — pesquisa, filtros, ordenação, paginação, variantes de filial/unidade, favoritos, carrinho e componentes.
- `data/catalog.json` — 440 produtos e variantes recolhidos do catálogo público.
- `assets/products/catalog/` — imagens individuais de produto disponíveis localmente.
- `assets/products/`, `assets/categories/`, `assets/banners/` — restantes imagens usadas no redesenho.
- `prompt.md` — especificação do redesenho.

## Funcionalidades

- Pesquisa por nome, marca, categoria e subcategoria, sem distinção de maiúsculas ou acentos.
- Filtros por categoria, subcategoria, marca, disponibilidade e intervalo de preço.
- Ordenação por relevância, Mais vendidos conforme a ordem pública observada, nome, preço e data; grelha ou lista; paginação de 24 produtos.
- Colecções separadas de Movimento rápido, Últimas novidades e Zona de ofertas, com ligações para as colecções oficiais.
- Ficha de produto com descrição disponível, marca, categoria, variantes de embalagem, preço, stock, produtos relacionados, partilha e ligação oficial.
- Lista de desejos com contadores, remoção e exportação para texto.
- Carrinho demonstrativo com filial, embalagem, quantidade, remoção, subtotal e opção para esvaziar.
- Revisão demonstrativa com dados de contacto e morada, entrega demonstrativa, opção de pagamento de referência e pedido local sem cobrança.
- Acesso ao login/criação de conta real no site Recheio, perfil de contacto local sem palavra-passe e histórico dos pedidos demonstrativos.
- Selector de filial no cabeçalho e no localizador; preços e disponibilidade mudam conforme as variantes locais do produto.
- Newsletter com validação do navegador, sem envio do endereço de e-mail.
- Estado guardado no `localStorage`, mensagens de feedback, estados vazios, navegação por teclado e layout para computador, tablet e telemóvel, incluindo menus e diálogos adaptados a ecrãs estreitos.

## Comparação com o site original

| No site original | No redesenho |
| --- | --- |
| Muitas categorias e subcategorias em menus extensos | Menu de categorias com subcategorias observadas, cartões e filtros de catálogo mais próximos dos produtos |
| Pesquisa, disponibilidade, preço e ordenação distribuídos pela página de colecção | Controlos agrupados, filtros por marca/subcategoria, paginação e escolha grelha/lista |
| Variantes dependem da filial e da unidade de venda | Filial e embalagem seleccionáveis com variantes de referência recolhidas localmente |
| Favoritos e carrinho dependem da conta/plataforma original | Lista e carrinho demonstrativos guardados neste navegador |
| Página inicial mistura movimentos, novidades, marcas e ofertas | Secções próprias, identificadas e ligadas às colecções oficiais |

## Roteiro de demonstração

1. Mostrar cabeçalho, selector de filial e categorias.
2. Abrir Movimento rápido, Novidades e Ofertas.
3. Filtrar por categoria/subcategoria e marca; testar o intervalo de preço e a ordenação.
4. Mudar filial e embalagem; abrir detalhes e produtos relacionados.
5. Guardar e exportar produtos da lista de desejos.
6. Adicionar ao carrinho, ajustar quantidades e consultar o subtotal de referência.
7. Abrir a conta, testar o perfil sem palavra-passe e o histórico local.
8. Rever um pedido demonstrativo, indicar a morada de entrega e limpar os dados de teste.
9. Demonstrar menu móvel, mensagens, estados vazios e newsletter local.

## Fontes públicas

- [Página inicial e catálogo](https://www.recheio.co.mz/pt-mz)
- [Lista de desejos](https://www.recheio.co.mz/pt-mz/pages/wishlist)
- [Movimento rápido](https://www.recheio.co.mz/pt-mz/collections/fast-moving)
- [Últimas novidades](https://www.recheio.co.mz/pt-mz/collections/latest-arrivals)
- [Zona de ofertas](https://www.recheio.co.mz/pt-mz/collections/offer-beira)
- [Informação institucional](https://www.recheio.co.mz/pt-mz/pages/about-us)
- [Localizador de lojas](https://www.recheio.co.mz/pt-mz/pages/store-locator)
- [Contacto](https://www.recheio.co.mz/pt-mz/pages/contact)

Redesenho académico independente. A marca, os produtos e os activos da loja pertencem à Recheio e aos respectivos titulares.


## Actualização do redesign

- O cabeçalho reúne a pesquisa, o acesso ao localizador de lojas e o contacto, sem uma faixa azul separada.
- A área de marcas usa 38 logótipos recolhidos da página pública “Marcas em alta” da Recheio. O catálogo local desta captura contém 213 nomes distintos no filtro de marcas. As marcas em destaque que não têm produtos correspondentes na captura abrem a respectiva colecção oficial.
- A pesquisa usa um índice local de prefixos por nome, marca, categoria e subcategoria, além de permitir ordenação e filtragem combinadas.
