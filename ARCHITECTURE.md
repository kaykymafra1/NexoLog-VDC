# Arquitetura da V3

## Regra de dependência

`Presentation → Application → Domain`

`Infrastructure → Application ports`

- **Domain:** entidade imutável `RoutePlan` e regras de ocupação, custo e economia.
- **Application:** casos de uso para carregar e filtrar o dashboard; contratos `TmsRepository` e `RoutingService`.
- **Infrastructure:** mock demonstrativo, adapter OSRM, mapa SVG e renderizador 3D em Canvas.
- **Presentation:** shell, componentes, telas e controller. Nenhuma regra de negócio é calculada no HTML.
- **Composition root:** `src/main.js`, único ponto que escolhe as implementações concretas.

## Decisões

1. O domínio não conhece navegador, Sankhya, OSRM, HTML ou Canvas.
2. Falhas de roteirização são convertidas em uma rota demonstrativa no caso de uso.
3. Dados exibidos são escapados antes da interpolação no DOM.
4. Mapa e 3D não exigem bibliotecas externas, garantindo a demonstração offline.
5. O standalone é gerado dos mesmos módulos usados no desenvolvimento.

## Próxima integração

Um adapter Sankhya deverá transformar as respostas REST/JX no contrato do repositório. Credenciais não devem ser armazenadas no navegador; a integração produtiva deve passar por um backend ou gateway autenticado.
