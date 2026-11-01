# Bora pelo RS

**Site publicado:** https://pedrobolson.github.io/bora-pelo-rs/

Abra **index.html** no navegador. Não precisa instalar nada. O HTML contém o catálogo, os estilos, o Leaflet e uma base local com os municípios do RS. Para o mapa de ruas, ele carrega MapLibre e a base comunitária Maptoolkit pela internet. Alguns aplicativos de mensagens mostram uma prévia limitada de HTML; para usar no celular, prefira publicar um link.

O carregamento foi corrigido para a abertura direta do arquivo (`file://`). O site usa agora a base comunitária Maptoolkit, sem chave, com os créditos exigidos. Não faz mais pedidos ao servidor de tiles que apresentava o bloqueio. Se a internet ou o recurso gráfico necessário à base de ruas falhar, o mapa continua mostrando os limites municipais do IBGE incorporados no HTML e os mesmos 100 pontos.

## O que está incluído

- 100 lugares em 20 municípios: 70 recuperados da conversa e 30 acrescentados por pesquisa em 01/11/2026.
- Mapa navegável com um marcador por lugar, nas coordenadas identificadas nas fontes de mapas.
- Busca por nome, cidade, categoria e descrição, com ou sem acentos.
- Filtros combinados por região, categoria e marcação pessoal.
- Quero ir, já fui e não gostei. Tocar novamente na mesma marcação remove a seleção.
- Layout responsivo; no celular, os botões Lista e Mapa alternam a visualização.
- Fonte da posição disponível em cada cartão e popup.

**As marcações são locais.** São guardadas no localStorage do navegador, por endereço do site. Não sincronizam entre aparelhos, navegadores ou entre você e sua esposa. Abrir outro arquivo ou mudar o endereço de hospedagem pode criar uma lista separada. Limpar os dados do navegador apaga as marcações. Se o navegador bloquear o armazenamento, o site informa que a seleção é temporária. Nenhuma marcação foi preenchida automaticamente com as opiniões relatadas na conversa.

## Cobertura recuperada e limitações

Em 01/11/2026, o catálogo recebeu 30 adições nas regiões já abordadas: 10 em Uva e Vinho, 12 em Hortênsias e 8 em Campos e Paranhana. Foram mantidos os 70 registros anteriores e seus identificadores, preservando as marcações já salvas no mesmo navegador e endereço.

O perfil continua incluindo natureza, cultura, aventura, parques e enoturismo. Cafés e restaurantes foram selecionados por uma experiência própria: almoço em casarão histórico, culinária familiar ou piquenique em pomar. Avaliações independentes apoiaram a escolha de Casa Vanni, Osteria Della Colombina, Castelinho Caracol e Casa Sander; seus cartões incluem links para consultar as opiniões atuais. Não há ranking nem notas automáticas. As descrições dos novos locais têm links para as fontes de informação.

Essas inclusões são pesquisa complementar, identificada em cada cadastro. Não representam a recuperação dos lugares que faltavam na conversa original.

O pedido original mencionava **222 pontos e nove regiões**. A leitura disponível da resposta foi cortada após o terceiro mapa. Foi possível recuperar **58 registros com nome nos mapas** e **12 lugares nomeados em outros trechos da mesma conversa**, incluindo todos os 25 lugares da seleção anterior. Não foram inventados os pontos restantes nem os nomes das seis regiões ausentes.

Os três agrupamentos recuperados são:

1. Serra Gaúcha — Uva e Vinho, Caxias e arredores.
2. Gramado, Canela e Nova Petrópolis.
3. Campos de Cima da Serra, Cambará, Ausentes e Paranhana.

“Outros locais citados” contém Quinta da Estância e Acqua Lokos; é um complemento da conversa, não uma região original recuperada. Os grupos originais foram preservados, inclusive os hotéis de Bento e o Parque da Ferradura que estavam no terceiro mapa. As categorias foram organizadas para navegação, com base nos nomes e no conteúdo da conversa.

Quinze posições dos três mapas apareceram apenas como referências internas, sem seus dados de estabelecimento. Algumas podem corresponder aos lugares recuperados em outros trechos; os códigos foram mantidos no JSON para auditoria, sem criar cadastros fictícios. A diferença entre 70 e 222 não significa que os 152 restantes foram identificados ou validados.

O arquivo **dados-recuperados.json** registra nomes, endereços, origem, coordenadas e respectivas fontes. O HTML incorpora os mesmos dados e funciona sozinho. Para completar os 222 futuramente, é necessário recuperar o texto ou a exportação integral dos seis mapas que faltam.

## Como as coordenadas foram obtidas

Os 100 lugares têm coordenadas de objetos cartográficos identificados no OpenStreetMap, links de localização ou mapas publicados por órgãos de turismo. Nas correspondências, foram conferidos nome, cidade e endereço quando disponível. Na ampliação, foram usados também os pontos do portal turístico de Igrejinha e o link de localização do restaurante Osteria Della Colombina no Tripadvisor, confrontado com seu site oficial. **Não foram usados centros de municípios, deslocamentos artificiais ou coordenadas estimadas para preencher lacunas.**

As notas de posição distinguem a área da Floresta Nacional, o mirante da Cachoeira do Tigre Preto e a passagem do rio no Passo da Ilha das respectivas portarias ou áreas de apoio. Foram conferidos homônimos como o parque de esculturas Pedras do Silêncio, que é diferente do pico de mesmo nome, e o Santuário de Caravaggio de Farroupilha. O cadastro do Museu Casa de Pedra no MuseusBr apresentava coordenadas divergentes; foi usada a edificação identificada no OpenStreetMap. A Casa Sander tem diferença de número entre o mapa e o endereço oficial, registrada na nota do ponto.

Foram distinguidos casos como Gasper Vale dos Vinhedos versus Eulália, a filial Santa Líbera da Monte Reale e o endereço atual do Xeque-Mate. O marcador da Maria Fumaça indica a estação de Bento; o da Cambará Off Road indica sua sede. Em atrativos naturais, a posição identifica o atrativo ou a área do parque e pode não ser uma portaria ou acesso para veículos. Não houve levantamento em campo; os dados cartográficos podem conter imprecisões. Não há informação de disponibilidade, preços ou horários em tempo real.

As consultas ao Nominatim foram feitas apenas durante a preparação, de forma sequencial, com intervalo superior a um segundo e cache local, conforme a [política de uso](https://operations.osmfoundation.org/policies/nominatim/). O site entregue não consulta esse serviço nem oferece geocodificação automática.

## Publicar um link: recomendação — GitHub Pages

É o caminho simples para este protótipo estático, sem ferramentas de desenvolvimento:

1. No GitHub, crie um repositório público, por exemplo `bora-pelo-rs`.
2. Use **Add file → Upload files** e envie **index.html** para a raiz do repositório. Confirme o envio.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha **main** e **/ (root)** e clique em **Save**.
6. Aguarde o endereço indicado pelo próprio GitHub e envie esse link pelo WhatsApp.

Um repositório público expõe seu conteúdo publicamente. Os arquivos entregues contêm o catálogo de turismo e as fontes, sem as mensagens pessoais da conversa. As marcações de cada visitante ficam no navegador dele e não são publicadas no repositório.

Você pode enviar somente o index.html: nenhum arquivo de apoio é exigido pelo site. Se quiser disponibilizar os dados para consulta, envie também dados-recuperados.json e preserve sua atribuição de fonte. Não precisa de chave do Google, banco de dados nem processo de compilação.

[Documentação oficial do GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Alternativa — Firebase Hosting

O arquivo firebase.json já aponta para esta pasta. Se você já usa Firebase, pode publicar o mesmo HTML:

1. No terminal, abra a pasta do projeto.
2. Execute `npx firebase-tools login`.
3. Execute `npx firebase-tools init hosting`, selecione seu projeto Firebase e use `.` como pasta pública. Responda **não** para configurar como aplicativo de página única e **não** para sobrescrever index.html. Automação com GitHub é opcional e dispensável aqui.
4. Execute `npx firebase-tools deploy --only hosting`.
5. Compartilhe o endereço que o Firebase informar.

Isso publica os arquivos estáticos. Não adiciona sincronização das marcações entre dispositivos.

[Documentação oficial do Firebase Hosting](https://firebase.google.com/docs/hosting/quickstart).

## Créditos

- Biblioteca de mapas: [Leaflet 1.9.4](https://leafletjs.com/), licença BSD de duas cláusulas; o aviso original está incorporado ao HTML.
- Base de ruas: [Maptoolkit Community](https://maptoolkit.org/), sem chave para uso pessoal, com logotipo e atribuição visíveis; [integração oficial com Leaflet](https://docs.maptoolkit.org/platform-libraries/leaflet/). Renderização com MapLibre GL JS 6.9.0 e a integração oficial maplibre-gl-leaflet 0.1.4.
- Dados cartográficos e parte das coordenadas: [© contribuidores do OpenStreetMap](https://www.openstreetmap.org/copyright), ODbL 1.0. As fontes de cada posição estão no catálogo.
- Base local de reserva: [malhas geográficas do IBGE](https://servicodados.ibge.gov.br/api/docs/malhas), municípios do Rio Grande do Sul. Seus limites não são usados como substituto das coordenadas das atrações.
- Outras posições: Google Maps e links de localização publicados pelos estabelecimentos e órgãos de turismo, individualizados nos cartões e no JSON.
- Ilustração: SVG original incluído no HTML, sem imagens externas.

Base preparada em 31/10/2026. Catálogo ampliado em 01/11/2026 e publicado pelo GitHub Pages a partir da branch `main`.
