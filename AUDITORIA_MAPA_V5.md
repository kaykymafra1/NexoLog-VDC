# Auditoria do Mapa — V5

A V4 já possuía roteirização OSRM, porém a visualização ainda tratava as entregas intermediárias como pontos aproximados ao longo da geometria.

Na V5, as paradas possuem coordenadas explícitas e são enviadas ao motor de roteirização. Assim, quando o OSRM responde, o percurso é calculado na sequência operacional: Hub → primeira entrega → demais paradas → entrega final.

A camada visual foi separada em panes do Leaflet para evitar conflito de z-index com a interface. A rota utiliza quatro traços sobrepostos para melhorar contraste e leitura sem encobrir o mapa.
