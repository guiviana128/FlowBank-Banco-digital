# FlowBank

Banco digital **inteiramente fictício** feito com HTML, CSS e JavaScript puro. Não há conexão com bancos, Pix, boletos reais ou redes de cartão.

## Abrir

Abra `index.html` em um navegador moderno ou publique os arquivos da raiz como site estático. Não há instalação nem etapa de build.

Na primeira visita, crie seu usuário com nome e identificador **fictícios** e escolha um banco de demonstração. Cada perfil local mantém saldo, extrato, cartões, metas e notificações próprios. O login apenas seleciona um perfil salvo no navegador: **não é autenticação segura**.

## Monitoramento de gastos

Em **Meus cartões**, cada perfil pode cadastrar até 12 cartões fictícios. Informe o nome do banco, escolha qualquer cor e defina um limite mensal simulado. Cada cartão tem bloqueio e limite próprios.

Use **Registrar gasto** para lançar uma compra fictícia no cartão escolhido. O lançamento reduz o saldo disponível, aparece no extrato e atualiza os gráficos, o gasto do mês, o limite restante e as categorias. Cartões bloqueados não aceitam novos lançamentos. O extrato pode ser filtrado por cartão, texto, tipo e mês.

Ao atualizar de uma versão anterior, o cartão existente passa a ser o primeiro da lista e os lançamentos antigos feitos com cartão são vinculados a ele.

## Outras funcionalidades

- Painel com saldo, gráfico de entradas e saídas em períodos de 3, 6 ou 12 meses e despesas por categoria.
- Transferências e Pix simulados entre perfis locais ou para destinatários fictícios externos, com banco de destino.
- Pagamento de boleto fictício, aceitando apenas códigos no formato `FLOW-2026-001`.
- Registro de recebimentos fictícios, metas com reserva e retirada de valores e notificações.
- Simulador de investimento com taxa hipotética e capitalização mensal.
- Temas claro e escuro e layout responsivo.

Os dados são salvos no `localStorage` sob a chave `flowbank-demo-v3`. Dados anteriores das versões v1 e v2 são migrados ao salvar. Não há sincronização entre dispositivos; limpar os dados do navegador remove os perfis e movimentos.

## Limites da demonstração

- Não informe CPF, senha, chaves Pix reais, números de cartão, códigos de boletos reais ou outros dados bancários.
- Os cartões e bancos não se conectam a serviços financeiros. Os quatro dígitos exibidos são decorativos.
- Para um destinatário externo fictício, a simulação registra apenas a saída no perfil atual. Transferências entre perfis locais atualizam ambos os saldos.
- O simulador de investimento é uma projeção matemática nominal, sem impostos, taxas, inflação ou variação de rendimento. Não constitui recomendação financeira.
