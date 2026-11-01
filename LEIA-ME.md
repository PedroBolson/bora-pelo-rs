# Bora pelo RS

**Acesse:** https://pedrobolson.github.io/bora-pelo-rs/

Catálogo com 96 lugares para passear pelo Rio Grande do Sul. Busque por nome, cidade ou experiência, combine os filtros de região e tipo de passeio e explore os pontos no mapa.

Use **Quero ir**, **Já fui** e **Não gostei** para organizar suas escolhas. Tocar novamente na mesma marcação remove a seleção. As marcações ficam salvas no navegador e não sincronizam entre aparelhos. Limpar os dados do navegador apaga essas escolhas.

Os cartões trazem endereço e links de localização. Alguns incluem informações do passeio e avaliações. Confira horários, valores, reservas e condições de acesso diretamente com cada lugar.

## Arquivos e publicação

- `index.html`: página completa, com estilos, scripts e catálogo incorporados. Também pode ser aberta diretamente no navegador.
- `dados-recuperados.json`: os mesmos dados do catálogo, em arquivo separado.
- `.nojekyll`: permite servir os arquivos estáticos diretamente no GitHub Pages.
- `firebase.json`: configuração para hospedagem alternativa no Firebase Hosting.

O GitHub Pages publica automaticamente a raiz da branch `main`. Ao editar os lugares, mantenha o JSON separado e os dados incorporados no HTML iguais. Preserve os identificadores dos locais para manter as marcações existentes.

No celular, os botões **Lista de lugares** e **Explorar mapa** alternam a visualização. O mapa de ruas requer internet; se ele não carregar, a base municipal incorporada continua disponível.

## Créditos

- [Leaflet 1.9.4](https://leafletjs.com/), licença BSD; aviso de licença incorporado ao HTML.
- [Maptoolkit Community](https://maptoolkit.org/), com logotipo e atribuição no mapa. Renderização com MapLibre GL JS e integração maplibre-gl-leaflet.
- [© contribuidores do OpenStreetMap](https://www.openstreetmap.org/copyright), ODbL, para dados cartográficos e parte das posições.
- [Malhas geográficas do IBGE](https://servicodados.ibge.gov.br/api/docs/malhas), para a base municipal de reserva.
- Outras posições e informações: links de localização, estabelecimentos e órgãos de turismo indicados nos respectivos cadastros.
