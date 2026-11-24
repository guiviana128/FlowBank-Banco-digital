# FlowBank

Banco digital **inteiramente fictício** feito com HTML, CSS e JavaScript puro. Não há conexão com bancos, Pix, boletos reais ou redes de cartão.

## Acesso demonstrativo

Na primeira visita, crie um perfil com nome e identificador fictícios, escolha um banco de demonstração e defina uma senha local de pelo menos 12 caracteres. O aplicativo salva um verificador derivado com PBKDF2-HMAC-SHA-256, 600.000 iterações e salt aleatório; **não salva a senha em texto puro**. A entrada volta a pedir a senha após recarregar a página. Perfis criados antes desta atualização precisam definir uma senha no primeiro acesso.

Abra o site por **HTTPS ou localhost** para que a Web Crypto API esteja disponível. Não reutilize uma senha de serviço real. Não há recuperação de senha: como os dados são locais, perder a senha pode impedir o acesso pela interface.

**Limite importante:** isto é apenas uma barreira de acesso na interface. Saldo, extrato e demais dados fictícios continuam em texto legível no `localStorage` e podem ser vistos ou modificados por quem tem acesso ao navegador e às ferramentas de desenvolvimento. A senha não oferece autenticação ou proteção de dados adequada para um banco real. Para isso seriam necessários backend, contas verificadas, sessões seguras e autorização no servidor.

## Monitoramento de gastos

Em **Meus cartões**, cada perfil pode cadastrar até 12 cartões fictícios. Informe o nome do banco, escolha qualquer cor e defina um limite mensal simulado. Cada cartão tem bloqueio e limite próprios.

Use **Registrar gasto** para lançar uma compra fictícia no cartão escolhido. O lançamento reduz o saldo disponível, aparece no extrato e atualiza os gráficos, o gasto do mês, o limite restante e as categorias. Cartões bloqueados não aceitam novos lançamentos. O extrato pode ser filtrado por cartão, texto, tipo e mês.

## Outras funcionalidades

- Painel com saldo, gráfico de entradas e saídas em períodos de 3, 6 ou 12 meses e despesas por categoria.
- Transferências e Pix simulados entre perfis locais ou para destinatários fictícios externos, com banco de destino.
- Pagamento de boleto fictício, aceitando apenas códigos no formato `FLOW-2026-001`.
- Registro de recebimentos fictícios, metas com reserva e retirada de valores e notificações.
- Simulador de investimento com taxa hipotética e capitalização mensal.
- Temas claro e escuro e layout responsivo.

Os dados são salvos no `localStorage` sob a chave `flowbank-demo-v3`. Não há sincronização entre dispositivos; limpar os dados do navegador remove os perfis e movimentos. Não informe CPF, chaves Pix reais, números de cartão ou outros dados bancários. O simulador de investimento é uma projeção matemática nominal e não constitui recomendação financeira.
