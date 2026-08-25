# Fila de Retorno — CRM da triagem

Acompanhamento das pendências da triagem com **régua de contato D1 · D3 · D5 · D10 · D15 · D30**,
histórico de contatos e painel do supervisor.

Feito para rodar na **Vercel** com banco **Neon** (Postgres).

---

## O que o sistema faz

- **Login por pessoa.** Cada cobrador vê apenas a própria carteira; o supervisor vê tudo.
- **Fila organizada por urgência:** régua esgotada, atrasadas, para hoje, próximos 7 dias, mais adiante, sem data, encerradas.
- **Régua automática.** Os prazos contam da *abertura* da pendência, não do último contato — quem atrasa
  um toque não empurra os seguintes. Cada contato registrado avança a etapa e já agenda a próxima data.
- **Desvio fica registrado.** Se o cobrador mudar a data sugerida, a pendência é marcada como
  *fora da régua* e isso aparece no painel do supervisor.
- **Concluir a pendência.** Botão próprio no detalhe: o cobrador registra o que recebeu, a pendência
  sai da fila e a entrega é sinalizada ao gestor na aba **Entregas** (com aviso numerado no menu,
  que some quando ele dá ciência).
- **Parcialmente concluído.** Quando vem só parte do que foi pedido, o cobrador descreve o que falta
  e a pendência entra numa **régua curta — D1 · D3 · D5** contada da data da entrega, porque já houve
  avanço. O que falta é anexado à observação e a entrega parcial também aparece para o gestor.
- **Depois do último toque da régua** a pendência sai da fila do cobrador e vai para o supervisor decidir:
  reiniciar a régua, encerrar sem êxito ou marcar como concluída.
- **Painel do supervisor** com atrasadas, para hoje, em aberto, régua esgotada, fora da régua,
  concluídas nos últimos 7 dias, entregas sem ciência e sem primeiro contato — e produtividade por cobrador.
- **Meu progresso** (cobrador) e **um painel por cobrador** (gestor, clicando no nome na tabela de
  produtividade): cadastradas, pendentes, concluídas, atrasadas, entregas parciais, concluídas na
  semana e no mês com comparação, taxa de resolução, adesão à régua, tempo médio até concluir e
  concluídas por mês nos últimos seis meses.

---

