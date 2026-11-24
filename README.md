# FlowBank

Um banco digital **inteiramente fictício**, criado com HTML, CSS e JavaScript puro. O projeto simula operações locais para demonstrar uma interface bancária moderna; não se conecta a bancos, ao Pix, a boletos reais ou a redes de cartão.

## Como abrir

Abra `index.html` em um navegador moderno ou publique os arquivos da raiz como site estático. Não há instalação, dependências de execução nem etapa de build.

Na tela inicial, entre com um dos três perfis de demonstração ou crie um perfil usando apenas nome e identificador **fictícios**. A entrada seleciona um perfil local; **não é autenticação segura**.

## Funcionalidades

- Painel com saldo, gráfico de entradas e saídas, despesas por categoria, cartão e movimentações recentes.
- Transferências e Pix simulados entre os perfis deste navegador.
- Pagamento de boleto fictício, aceitando apenas códigos no formato `FLOW-2026-001`.
- Registro de recebimentos fictícios para explorar receitas.
- Cartão virtual ilustrativo com bloqueio e ajuste do limite simulado.
- Extrato com filtros por texto, tipo e mês.
- Metas com reserva e retirada de valores fictícios.
- Simulador de investimento com taxa hipotética e capitalização mensal.
- Notificações de movimentações e temas claro/escuro.
- Layout responsivo para desktop e celular.

Cada operação modifica o estado local e atualiza imediatamente o saldo, as movimentações, os indicadores e os gráficos. Dados são salvos no `localStorage` sob a chave `flowbank-demo-v1`. Não há sincronização entre dispositivos. Limpar os dados do navegador remove os perfis e movimentos da simulação.

## Limites da demonstração

- Não informe CPF, senha, chaves Pix reais, números de cartão, códigos de boletos reais ou outros dados bancários.
- O número exibido no cartão não é um cartão utilizável.
- O simulador de investimento mostra apenas uma projeção matemática nominal. Não considera impostos, taxas, inflação ou variação de rendimento e não constitui recomendação financeira.
- Como toda a aplicação funciona no navegador, os dados e o acesso aos perfis podem ser alterados por quem usa o mesmo navegador. Para um produto real seriam necessários backend, autenticação segura, controles de autorização e integração financeira regulada.
