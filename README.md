# Giullia's — apresentação do novo site

Apresentação para aprovação de Diretoria e Marketing, preparada pela OSSEL. Reúne a proposta visual, uma maquete da página inicial, a estrutura planejada e os próximos passos.

## O que funciona

- Leitura da apresentação, identidade e fases do projeto.
- Navegação por sete links para seções da própria página, por mouse e teclado.
- Layout adaptável e rolagem horizontal da lista de produtos ilustrativos.

Busca, conta, carrinho, categorias, preços, promoções, produtos e condições comerciais são demonstrativos. Não há loja, login, formulários, pedidos, pagamentos, painel administrativo ou coleta de dados pela aplicação. Protheus, WhatsApp, frete e parceiros são propostas futuras, sem integração neste repositório.

A aprovação é registrada respondendo ao e-mail que acompanhou a apresentação. A página não envia mensagens nem registra decisões.

## Arquivos e dependências

- `index.html`: documento completo, com estilos embutidos; sem JavaScript.
- `logo-giullias.png`: imagem de referência, com dimensões declaradas no HTML.
- `favicon.svg`: ícone provisório com a inicial G; sujeito à aprovação visual de Marketing.

Cormorant Garamond e Jost são carregadas de `fonts.googleapis.com` e `fonts.gstatic.com`. O navegador realiza essas requisições externas; sem elas, usa Georgia e as fontes de sistema declaradas no CSS. Não há dependências a instalar, variáveis de ambiente, build, lint, suíte automatizada ou CI/CD configurados.

## Execução local

Com Python 3 disponível, a partir da raiz deste repositório:

```bash
python3 -m http.server 8080 --bind 127.0.0.1
```

Abra [a apresentação local](http://127.0.0.1:8080/) e encerre o servidor com Ctrl+C. Não sirva diretórios-pai contendo arquivos privados. A página também pode ser aberta diretamente no navegador; o servidor local permite conferir os recursos e respostas HTTP.

## Checklist de verificação

Executar em contexto limpo de navegador; registrar versão, commit, resultados e screenshots fora da pasta publicada.

- Desktop 1440 × 900, janela estreita 390 × 900 e emulação móvel 390 × 900. Emulação móvel deve habilitar o modo móvel/toque, não apenas reduzir a janela desktop.
- UTF-8 e acentos corretos, idioma `pt-BR`, modo padrão (`document.compatMode === 'CSS1Compat'`) e viewport móvel correspondente à tela.
- Sete links chegam às seções sem encobrir seus títulos. Navegação permanece disponível em 900 px e larguras inferiores.
- Tab, Shift+Tab e Enter alcançam os links com foco visível. A região de produtos recebe foco e permite rolagem por teclado; conferir também por toque.
- Zoom de 200%, redução de movimento e ausência de overflow horizontal global; rolagem interna dos produtos é intencional.
- Logo sem distorção; favicon e recursos locais sem 404; console sem erros da página.
- Legibilidade com Google Fonts bloqueado somente no contexto de teste, confirmando fontes alternativas.
- Hierarquia de títulos, contraste dos textos e nomes acessíveis. Validação com leitor de tela precisa ser registrada separadamente; inspeção do DOM não a substitui.
- Aviso de demonstração e aprovação por e-mail claros; cliques na maquete não geram pedidos, autenticação, pagamentos ou mensagens.

## Preparação para publicação

Hospedagem, URL final e responsável pela publicação ainda não estão definidos neste repositório. Não há comando de deploy configurado.

1. Identificar o provedor e o responsável; registrar o procedimento específico antes da primeira publicação.
2. Publicar **somente** `index.html`, `logo-giullias.png` e `favicon.svg`. Não publicar `.git`, arquivos privados ou artefatos de auditoria.
3. Exigir HTTPS válido e `Content-Type: text/html; charset=utf-8` para o HTML. Definir cache de forma que atualizações do documento sejam revalidadas; não assumir que um 200 confirma a revisão publicada.
4. Manter `noindex` enquanto o conteúdo for uma apresentação para aprovação. `noindex` não restringe acesso: se houver necessidade de confidencialidade, usar o controle de acesso da hospedagem.
5. Verificar recursos, fontes, mobile e teclado na URL efetiva. Conferir a revisão entregue comparando o HTML publicado com o artefato aprovado.
6. Avaliar cabeçalhos de segurança suportados pelo provedor. Uma CSP precisa contemplar os estilos embutidos e Google Fonts; não aplicar uma política sem verificar que a apresentação continua íntegra.
7. Para reversão, preservar antes da publicação a versão dos três arquivos atualmente entregue, junto de seu commit ou checksum. Se a nova versão falhar, republicar o conjunto anterior pelo mesmo procedimento do provedor, revalidar o cache e repetir as verificações. O mecanismo específico depende da hospedagem e ainda não foi confirmado.

Não remover `noindex` nem adicionar canonical/sitemap com domínio presumido. A URL desenhada na maquete não comprova o endereço de publicação.

## Pendências de conteúdo e escopo futuro

Marketing deve aprovar o favicon, fornecer o logo vetorial, fotos e textos finais. A apresentação identifica os espaços e valores ilustrativos; esses materiais não tornam o comércio operacional.

Uma loja exige definição de plataforma, catálogo, estoque, pedidos, pagamentos, frete, contratos do Protheus e critérios próprios de segurança e aceite. Coroas, parceiros e portal pertencem a etapas separadas. Essas funcionalidades não fazem parte desta apresentação.
