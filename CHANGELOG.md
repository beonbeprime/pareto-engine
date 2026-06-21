# Changelog

## 1.1.0

Pareto Engine deixa de ser so uma lente e vira um motor de decisao.

Adicionado:
- 7 modelos de decisao que se combinam com Pareto (custo de oportunidade, inversao,
  assimetria e downside, segunda ordem, minimizacao de arrependimento, impacto vs
  esforco) com um seletor de qual usar em cada tipo de decisao. Ver `docs/decision-models.md`.
- Camada anti-slop: 7 regras que forcam especificidade, posicao e acao, mais um teste
  de slop antes de entregar. Ver `docs/anti-slop.md`.
- Exemplos antes e depois mostrando o motor em acao. Ver `docs/examples.md`.

Principio mantido: o motor e denso mas disciplinado. Usa o modelo certo na hora certa,
nunca todos de uma vez. Decisao barata e reversivel se resolve so com Pareto.

## 1.0.0

- Lente Pareto 80/20 para Claude Code: plugin, skill, regra e comando /pareto.
- Tres formas de instalar e filtro supremo configuravel por template.
