# Pareto Engine

Um motor de decisão 80/20 sempre ativo para o Claude Code.

Pareto Engine instala um cérebro de priorização e decisão dentro do Claude Code.
Em toda decisão, opinião, análise ou execução, ele separa os poucos vitais (os 20%
que geram 80% do resultado) dos muitos triviais, afia a escolha com os modelos
mentais certos e força clareza com uma camada anti-slop. Entrega o que importa
primeiro, toma posição e manda cortar o resto.

Não é mais uma ferramenta que você abre. É uma navalha de foco e um motor de decisão
que rodam por dentro de tudo que o Claude faz por você.

Três camadas, uma só disciplina:
- Pareto 80/20 acha o que importa.
- Seis modelos mentais (custo de oportunidade, inversão, assimetria, segunda ordem,
  arrependimento, impacto vs esforço) afiam a decisão, sem despejar todos de uma vez.
- A camada anti-slop força número, posição e próximo passo, e mata a resposta genérica.

---

## O problema que ele resolve

A IA, por padrão, trata tudo no mesmo peso. Você pede uma análise e recebe dez
pontos chapados, todos com a mesma importância. Você pede um plano e recebe uma
lista onde o item que muda o jogo está perdido no meio do que não muda nada.

Pareto Engine corrige isso na raiz. Ele força a IA a pensar como gente que produz
resultado: achar a alavanca, puxar ela, e ignorar o ruído.

---

## O que muda na prática

Sem o Pareto Engine:
> "Aqui estão 10 coisas que você pode fazer essa semana: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10."

Com o Pareto Engine:
> "Dessas 10, duas geram 80% do resultado: a 3 e a 7. Começa pela 3, ela destrava a 7.
> As outras oito podem esperar ou cair. Foca aqui."

---

## Instalação

Três formas, da mais simples à mais completa. Escolha uma.

### 1. Plugin do Claude Code (recomendado)

Se você usa o sistema de plugins do Claude Code, clone este repositório na sua pasta
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

Para a lente 80/20 rodar por dentro de TODA resposta, e não só quando você chama,
cole o conteúdo de [`snippet-CLAUDE.md`](snippet-CLAUDE.md) no `CLAUDE.md` do seu
projeto (ou no seu `~/.claude/CLAUDE.md` global). Esse é o passo que transforma o
Pareto numa lente permanente, não num comando sob demanda.

---

## Como usar

### Sob demanda

```
/pareto minha semana de trabalho
/pareto essas 3 opções de produto
/pareto onde cortar custo na operação
```

Você recebe o raio-X 80/20: o vital, o trivial, o que fazer agora e o que cortar.

### Automático

Com o snippet no `CLAUDE.md`, a lente roda sozinha. Quanto mais pesada a pergunta,
mais a estrutura aparece; em pergunta simples, ela só entrega o que importa, sem
ficar falando de Pareto.

---

## Como funciona

A intensidade da lente acompanha o peso do que você pede:

| Peso da tarefa | Modo | Comportamento |
|----------------|------|---------------|
| Trivial | mental | aplica por dentro, só o vital sai |
| Leve | leve | prioriza o vital, sem exibir a estrutura |
| Média | ativo | aponta vital vs trivial dentro da resposta |
| Pesada ou `/pareto` | raio-X | tabela 80/20 completa |

O método completo (as duas perguntas-motor, a aplicação por tipo de tarefa, o gate
e o anti-padrão) está em [`skills/pareto-8020/SKILL.md`](skills/pareto-8020/SKILL.md).

---

## Personalize o seu filtro supremo

A leitura genérica de Pareto é boa, mas fica muito mais afiada quando ela conhece a
SUA prioridade número um. Um vendedor mede o vital por receita. Um pesquisador, por
descoberta. Um operador, por tempo economizado.

Edite [`context/TEMPLATE-prioridade.md`](context/TEMPLATE-prioridade.md) com a sua
métrica suprema. A partir daí, o "20% vital" passa a ser medido pelo que de fato
importa pra você, e a lente avisa quando a leitura genérica contraria a sua prioridade.

---

## Documentação

O motor inteiro cabe em quatro documentos curtos. Leia nesta ordem:

| Documento | O que tem |
|-----------|-----------|
| [`skills/pareto-8020/SKILL.md`](skills/pareto-8020/SKILL.md) | a lente: princípio, perguntas-motor, gate, dosagem |
| [`docs/decision-models.md`](docs/decision-models.md) | os 7 modelos de decisão e o seletor de qual usar quando |
| [`docs/anti-slop.md`](docs/anti-slop.md) | as 7 regras que forçam clareza e o teste de slop |
| [`docs/examples.md`](docs/examples.md) | antes e depois: o motor em ação |

## Por que isso existe

Esse motor nasceu dentro de um sistema operacional de IA real, em produção, onde a
pergunta que separava lucro de desperdício era sempre a mesma: das mil coisas que
posso fazer, quais poucas movem o ponteiro? Pareto Engine é a versão destilada e
genérica dessa lente, liberada para qualquer pessoa apontar o próprio Claude Code
para o que importa.

---

## Créditos

Criado por Allysson Silveira (Zeus / Synkra AIOS).
Use, modifique, distribua. Se ajudar, deixe uma estrela e marque o autor.

## Licença

MIT. Veja [LICENSE](LICENSE).
