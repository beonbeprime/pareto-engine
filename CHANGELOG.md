# Changelog

## 1.1.0

Pareto Engine deixa de ser só uma lente e vira um motor de decisão.

Adicionado:
- 7 modelos de decisão que se combinam com Pareto (custo de oportunidade, inversão,
  assimetria e downside, segunda ordem, minimização de arrependimento, impacto vs
  esforço) com um seletor de qual usar em cada tipo de decisão. Ver `docs/decision-models.md`.
- Camada anti-slop: 7 regras que forçam especificidade, posição e ação, mais um teste
  de slop antes de entregar. Ver `docs/anti-slop.md`.
- Exemplos antes e depois mostrando o motor em ação. Ver `docs/examples.md`.

Princípio mantido: o motor é denso mas disciplinado. Usa o modelo certo na hora certa,
nunca todos de uma vez. Decisão barata e reversível se resolve só com Pareto.

## 1.0.0

- Lente Pareto 80/20 para Claude Code: plugin, skill, regra e comando /pareto.
- Três formas de instalar e filtro supremo configurável por template.
