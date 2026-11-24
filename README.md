# FlowBank

Banco digital **inteiramente fictício** feito com HTML, CSS e JavaScript puro. Não há conexão com bancos, Pix, boletos reais ou redes de cartão.

## Abrir

Abra `index.html` em um navegador moderno ou publique os arquivos da raiz como site estático. Não há instalação nem etapa de build.

Na primeira visita, crie seu usuário com um **nome e identificador fictícios** e escolha um dos dez bancos de demonstração. Cada perfil local mantém saldo, extrato, cartão, metas e notificações próprios. O login apenas seleciona um perfil salvo no navegador: **não é autenticação segura**. Pessoas que usam o mesmo navegador podem acessar esses perfis. Para contas reais, sincronização entre aparelhos e autenticação de verdade, seria necessário um backend.

## O que funciona

- Painel com saldo, gráfico de entradas e saídas em períodos de 3, 6 ou 12 meses, despesas por categoria e movimentações recentes.
- Transferências e Pix simulados entre perfis locais ou para destinatários fictícios externos, com escolha do banco de destino.
- Pagamento de boleto fictício, aceitando apenas códigos no formato `FLOW-2026-001`.
- Registro de recebimentos fictícios para explorar receitas.
- Cartão virtual ilustrativo com bloqueio, ajuste de limite e cor livre com prévia e contraste automático.
- Extrato com filtros por texto, tipo e mês; metas com reserva e retirada de valores; notificações.
- Simulador de investimento com taxa hipotética e capitalização mensal.
- Temas claro e escuro, navegação responsiva e valores em tipografia numérica com algarismos tabulares.

Cada operação modifica o estado local e atualiza saldo, movimentações, indicadores e gráficos. Os dados são salvos no `localStorage` sob a chave `flowbank-demo-v2`. Dados anteriores de `flowbank-demo-v1` são lidos e migrados ao salvar. Não há sincronização entre dispositivos; limpar os dados do navegador remove os perfis e movimentos.

## Limites da demonstração

- Não informe CPF, senha, chaves Pix reais, números de cartão, códigos de boletos reais ou outros dados bancários.
- Os bancos listados na interface são fictícios. O número exibido no cartão não é utilizável.
- Para um destinatário externo fictício, a simulação registra apenas a saída no perfil atual. Transferências entre perfis locais atualizam ambos os saldos.
- O simulador de investimento é uma projeção matemática nominal, sem impostos, taxas, inflação ou variação de rendimento. Não constitui recomendação financeira.
