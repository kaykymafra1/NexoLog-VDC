# OmniRoute TMS — V5 Rotas Reais

Atualização visual e operacional do mapa geográfico.

## Melhorias do mapa

- Rotas calculadas pelo OSRM usando a malha viária real.
- Paradas intermediárias passam a compor o cálculo da rota, e não apenas o ponto final.
- Linha moderna em quatro camadas: glow, contorno escuro, cor principal e brilho animado.
- Marcadores diferentes para Hub Principal, Primeira Entrega, Paradas Intermediárias, Entrega Final e Veículo em trânsito.
- Etiqueta flutuante por rota com nome e distância.
- Popups com Ordem de Carga, cliente, veículo e motorista.
- OpenStreetMap permanece como mapa-base sem exigir chave.
- Mantido fallback offline para a geometria demonstrativa quando o OSRM estiver indisponível.

## Cenários do protótipo

- Rota 1: Vitória da Conquista → Jequié → Feira de Santana → Salvador.
- Rota 2: Vitória da Conquista → Anagé → Brumado.
- Rota 3: Vitória da Conquista → Barra da Estiva → Lençóis → Seabra.

## Arquivo para validação

Abra `index.html` diretamente no navegador. Para ver as rotas rodoviárias calculadas e o mapa-base, é necessário acesso à internet.
