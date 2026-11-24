# FlowBank

Banco digital **inteiramente fictício**, feito com HTML, CSS e JavaScript puro. Nenhuma operação movimenta dinheiro real, consulta bancos ou processa Pix e boletos verdadeiros.

## Acesso local

Crie um perfil com nome, identificador fictício e senha local de 12 a 128 caracteres. O navegador guarda um verificador PBKDF2-HMAC-SHA-256 com salt aleatório, e solicita a senha novamente após recarregar. Use HTTPS ou localhost para disponibilizar a Web Crypto API. Perfis antigos podem definir senha no primeiro acesso.

A senha funciona apenas como barreira de interface: os dados fictícios permanecem legíveis no `localStorage` e podem ser alterados por quem acessa o navegador. Não use senha, CPF, chaves Pix, números de cartão ou dados bancários reais. Não há recuperação de senha nem autenticação de produção.

## Cartões e faturas

Em **Meus cartões**, cada perfil pode cadastrar até 12 cartões fictícios, com banco, cor, limite, bloqueio, dia de fechamento e vencimento próprios. Uma compra pode ser dividida em até 12 parcelas. Ela ocupa o limite disponível e aparece na fatura correspondente. **O saldo só é descontado quando a fatura é paga**, evitando débito duplo. Compras registradas nas versões anteriores continuam tratadas como já pagas.

## Planejamento

- **Orçamentos** mensais por categoria, com notificações ao atingir 80% e 100%.
- **Recorrências** para contas e assinaturas, com edição, pausa, pagamento simulado e calendário de vencimentos. Elas não debitam automaticamente.
- **Metas** com reserva e retirada de valores fictícios.
- Comparação das despesas do mês com o mês anterior.

## Extrato e dados

O extrato permite buscar, filtrar por tipo, mês e cartão, e editar categoria e nota pessoal de cada lançamento. O painel atualiza saldo, indicadores e gráficos a cada movimentação. Transferências e Pix simulados podem circular entre perfis locais ou destinatários fictícios. Há ainda boleto de teste no formato `FLOW-2026-001`, recebimentos fictícios, notificações, simulador de investimentos e temas claro e escuro.

Em **Planejamento → Dados fictícios**, exporte um backup JSON do perfil sem o verificador de senha. A importação cria um novo perfil com uma nova senha local. **Reiniciar perfil** apaga os lançamentos e os dados de planejamento daquele perfil, preservando a senha e um cartão inicial. Os dados ficam apenas neste navegador sob `flowbank-demo-v4`; não há sincronização entre dispositivos.

O simulador de investimentos é uma projeção matemática nominal e não constitui recomendação financeira.
