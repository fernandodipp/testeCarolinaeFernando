# Carolina & Fernando · 20.03.2027

Landing page do casamento. Um envelope com selo de cera abre e revela o convite, com brilhos discretos no fundo.
Os links levam ao site principal em [carolinaefernando.com.br](https://www.carolinaefernando.com.br).

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `index.html` | Página e links |
| `assets/style.css` | Envelope, convite, cores e animações |
| `assets/main.js` | Abertura do envelope, brilhos, som do brinde e links de agenda |
| `assets/js-ativo.js` | Marca que o JavaScript está ativo (evita mostrar o convite antes do envelope) |
| `assets/fontes/` | Fontes Cinzel, Gilda Display e Montserrat, hospedadas no próprio site |
| `assets/convite.webp` | Arte do convite (também em `convite.jpg`) |
| `assets/papel-envelope.webp` | Textura do envelope, tirada do canto esquerdo do convite, abaixo das folhas (repete sem emendas) |
| `assets/selo.webp` | Selo de cera em relevo |
| `assets/casamento.ics` | Evento para salvar na agenda (20/03/2027, 16h30 às 23h30) |
| `assets/monograma.png` | Monograma do selo de cera |
| `assets/compartilhar.jpg` | Imagem de prévia para WhatsApp e redes sociais |

## Como trocar um link

Edite os três links em `index.html`, dentro de `<nav class="t-botoes">`.

## Publicar

No GitHub, abra **Settings → Pages**, escolha **Deploy from a branch**, o branch `main` e a pasta `/ (root)`.

## Depois de cada alteração

Troque o número de versão (`?v=...`) em todos os endereços de arquivos:
em `index.html` (CSS, JavaScript e imagens) e em `assets/style.css` (imagens de fundo).
Isso obriga os celulares a baixar os arquivos novos em vez de usar a versão guardada no cache.

## Segurança

A página tem uma política de segurança de conteúdo (CSP) em `index.html`.
Ela só permite arquivos do próprio site. Por isso:

- não use `<script>` com código dentro da página nem atributos `style="..."`: coloque o código em `assets/main.js` e os estilos em `assets/style.css`;
- se for preciso usar um recurso de outro endereço (fonte, imagem, script), acrescente esse endereço na linha `Content-Security-Policy`.

## Acessibilidade

- Quem pede menos movimento no sistema vê a abertura do envelope em etapas curtas, sem animações.
- Data, endereço e botões têm área de toque de pelo menos 44 px e contorno visível ao navegar pelo teclado.
