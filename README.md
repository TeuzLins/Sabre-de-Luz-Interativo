# Sabre de Luz Interativo

Projeto web que simula sabres de luz com animações, cores configuráveis e resposta a eventos do usuário. Desenvolvido com HTML, CSS e JavaScript, priorizando semântica, acessibilidade e manutenção simples.

## Visão Geral
- Cada sabre é um componente que pode ser ativado e desativado.
- A cor e os efeitos são controlados por atributos de dados (por exemplo, `data-color`).
- A interação ocorre via clique ou toque, alternando estados e disparando animações.

## Como executar localmente
1. Abra um terminal na pasta do projeto: `Sabre-de-Luz-Interativo`.
2. Execute:
   ```bash
   npx --yes serve -l 5173 .
   ```
3. Acesse `http://localhost:5173/` no navegador.

Observação: qualquer servidor estático funciona (por exemplo, Live Server).

## Estrutura do projeto
```
Sabre-de-Luz-Interativo/
├── images/
│   └── sabreluz.png
├── index.html
├── style.css
└── README.md
```

## Atributos do sabre
- O atributo `data-color` controla:
  - Cor principal da lâmina
  - Gradientes e intensidade de iluminação
  - Efeitos de brilho, sombra e halo

## Interatividade
- Ao clicar em um sabre:
  - Alterna a classe `.active` no elemento correspondente
  - Controla a animação de expansão/retração da lâmina
  - Opcionalmente ativa/desativa efeitos sonoros e visuais, se configurados

## Personalização
Para adicionar novos sabres:
1. Duplique o bloco HTML do sabre existente em `index.html`.
2. Ajuste o valor do atributo `data-color` (por exemplo, `data-color="blue"`, `data-color="red"`).
3. Garanta que as classes e a estrutura sigam as regras de estilo em `style.css`.
4. Caso exista lógica em JavaScript, certifique-se de selecionar/escutar o novo elemento nos handlers.

## Manutenção e padrões
- Semântica HTML5
- CSS modular e escalável
- JavaScript limpo e documentado
- Padrões de acessibilidade (ARIA), quando aplicável

## Boas práticas recomendadas
- Prefira classes descritivas e evite acoplamento excessivo em seletores CSS.
- Use `data-*` para parametrização visual de cada sabre.
- Mantenha transições e animações performáticas (evite propriedades que forçam reflow).
- Teste a interação em dispositivos móveis (toque) e com teclado.

## Troubleshooting
- O servidor não inicia?
  - Verifique se o Node.js está instalado.
  - Tente outra porta: `npx --yes serve -l 5500 .`
- Os estilos não são aplicados?
  - Confirme classes e `data-color` no HTML.
  - Verifique se `style.css` está referenciado corretamente em `index.html`.

## Roadmap (ideias futuras)
- Sons de ignição e retração configuráveis
- Paleta de cores expandida com presets
- Suporte completo a navegação por teclado e leitores de tela
- Testes de interface e integração

## Contribuição
Sugestões de melhorias são bem-vindas, especialmente em acessibilidade, performance e organização de CSS/JS.

---
Documento técnico do projeto de sabres de luz interativo.

Cada sabre tem um atributo data-color (define a cor da lâmina).

O clique alterna a classe .active, fazendo a lâmina expandir ou retrair.

Você pode duplicar quantos sabres quiser, só mudando o data-color.
