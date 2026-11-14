# MOOM CITY ONLINE — base 0.1

Base técnica React + Vite + Three.js + Supabase.

Inclui cenário 3D leve, movimento por toque, registo/entrada por e-mail, leitura do saldo e da posição, e gravação segura da posição via RPC.

## Supabase
1. No SQL Editor, executa `supabase/setup.sql` (a função foi criada na etapa anterior; podes executar este script novamente com segurança).
2. Confirma que existem `profiles` e `player_state` e o trigger de criação de jogador.

## Configurar e executar
1. Copia `.env.example` para `.env`.
2. Preenche `VITE_SUPABASE_URL` e `VITE_SUPABASE_PUBLISHABLE_KEY`.
3. Num computador com Node.js: `npm install` e `npm run dev`.
4. Para produção: `npm run build` e publica `dist` num hosting compatível com Vite; define as mesmas variáveis de ambiente no hosting.

Usa apenas a chave Publishable no frontend. Nunca coloques `sb_secret`, `service_role` ou a palavra-passe da base de dados no código.

Ainda não implementados: multiplayer em tempo real, chat, imóveis, construção, missões e economia/recompensas. O saldo não é distribuído automaticamente. Esta é a base inicial, não o jogo completo.
