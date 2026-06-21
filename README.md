# Pareto Engine

Um motor de decisao 80/20 sempre ativo para o Claude Code.

Pareto Engine instala um cerebro de priorizacao e decisao dentro do Claude Code.
Em toda decisao, opiniao, analise ou execucao, ele separa os poucos vitais (os 20%
que geram 80% do resultado) dos muitos triviais, afia a escolha com os modelos
mentais certos e forca clareza com uma camada anti-slop. Entrega o que importa
primeiro, toma posicao e manda cortar o resto.

Nao e mais uma ferramenta que voce abre. E uma navalha de foco e um motor de decisao
que rodam por dentro de tudo que o Claude faz por voce.

Tres camadas, uma so disciplina:
- Pareto 80/20 acha o que importa.
- Seis modelos mentais (custo de oportunidade, inversao, assimetria, segunda ordem,
  arrependimento, impacto vs esforco) afiam a decisao, sem despejar todos de uma vez.
- A camada anti-slop forca numero, posicao e proximo passo, e mata a resposta generica.

---

## O problema que ele resolve

A IA, por padrao, trata tudo no mesmo peso. Voce pede uma analise e recebe dez
pontos chapados, todos com a mesma importancia. Voce pede um plano e recebe uma
lista onde o item que muda o jogo esta perdido no meio do que nao muda nada.

Pareto Engine corrige isso na raiz. Ele forca a IA a pensar como gente que produz
resultado: achar a alavanca, puxar ela, e ignorar o ruido.

---

## O que muda na pratica

Sem o Pareto Engine:
> "Aqui estao 10 coisas que voce pode fazer essa semana: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10."

Com o Pareto Engine:
> "Dessas 10, duas geram 80% do resultado: a 3 e a 7. Comeca pela 3, ela destrava a 7.
> As outras oito podem esperar ou cair. Foca aqui."

---

## Instalacao

Tres formas, da mais simples a mais completa. Escolha uma.

### 1. Plugin do Claude Code (recomendado)

Se voce usa o sistema de plugins do Claude Code, clone este repositorio na sua pasta
de plugins ou aponte seu marketplace para ele. O plugin registra o comando `/pareto`
e a skill automaticamente.

### 2. Copia e cola (funciona em qualquer setup)

Copie as pastas para o seu projeto:

```
cp -r commands/pareto.md       SEU_PROJETO/.claude/commands/
cp -r skills/pareto-8020       SEU_PROJETO/.claude/skills/
cp rules/pareto-8020.md        SEU_PROJETO/.claude/rules/
```

### 3. Sempre ativo (a lente roda em toda mensagem)

Para a lente 80/20 rodar por dentro de TODA resposta, e nao so quando voce chama,
cole o conteudo de [`snippet-CLAUDE.md`](snippet-CLAUDE.md) no `CLAUDE.md` do seu
projeto (ou no seu `~/.claude/CLAUDE.md` global). Esse e o passo que transforma o
Pareto numa lente permanente, nao num comando sob demanda.

---

## Como usar

### Sob demanda

```
/pareto minha semana de trabalho
/pareto essas 3 opcoes de produto
/pareto onde cortar custo na operacao
```

Voce recebe o raio-X 80/20: o vital, o trivial, o que fazer agora e o que cortar.

### Automatico

Com o snippet no `CLAUDE.md`, a lente roda sozinha. Quanto mais pesada a pergunta,
mais a estrutura aparece; em pergunta simples, ela so entrega o que importa, sem
ficar falando de Pareto.

---

## Como funciona

A intensidade da lente acompanha o peso do que voce pede:

| Peso da tarefa | Modo | Comportamento |
|----------------|------|---------------|
| Trivial | mental | aplica por dentro, so o vital sai |
| Leve | leve | prioriza o vital, sem exibir a estrutura |
| Media | ativo | aponta vital vs trivial dentro da resposta |
| Pesada ou `/pareto` | raio-X | tabela 80/20 completa |

O metodo completo (as duas perguntas-motor, a aplicacao por tipo de tarefa, o gate
e o anti-padrao) esta em [`skills/pareto-8020/SKILL.md`](skills/pareto-8020/SKILL.md).

---

## Personalize o seu filtro supremo

A leitura generica de Pareto e boa, mas fica muito mais afiada quando ela conhece a
SUA prioridade numero um. Um vendedor mede o vital por receita. Um pesquisador, por
descoberta. Um operador, por tempo economizado.

Edite [`context/TEMPLATE-prioridade.md`](context/TEMPLATE-prioridade.md) com a sua
metrica suprema. A partir dai, o "20% vital" passa a ser medido pelo que de fato
importa pra voce, e a lente avisa quando a leitura generica contraria a sua prioridade.

---

## Documentacao

O motor inteiro cabe em quatro documentos curtos. Leia nesta ordem:

| Documento | O que tem |
|-----------|-----------|
| [`skills/pareto-8020/SKILL.md`](skills/pareto-8020/SKILL.md) | a lente: principio, perguntas-motor, gate, dosagem |
| [`docs/decision-models.md`](docs/decision-models.md) | os 7 modelos de decisao e o seletor de qual usar quando |
| [`docs/anti-slop.md`](docs/anti-slop.md) | as 7 regras que forcam clareza e o teste de slop |
| [`docs/examples.md`](docs/examples.md) | antes e depois: o motor em acao |

## Por que isso existe

Esse motor nasceu dentro de um sistema operacional de IA real, em producao, onde a
pergunta que separava lucro de desperdicio era sempre a mesma: das mil coisas que
posso fazer, quais poucas movem o ponteiro? Pareto Engine e a versao destilada e
generica dessa lente, liberada para qualquer pessoa apontar o proprio Claude Code
para o que importa.

---

## Creditos

Criado por Allysson Silveira (Zeus / Synkra AIOS).
Use, modifique, distribua. Se ajudar, deixe uma estrela e marque o autor.

## Licenca

MIT. Veja [LICENSE](LICENSE).
