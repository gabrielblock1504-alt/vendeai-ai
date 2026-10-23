# VendeAí AI — versão para Netlify com IA

Este projeto usa uma página estática e duas Netlify Functions. A chave da OpenAI deve ficar somente nas variáveis de ambiente do Netlify; nunca coloque a chave no HTML ou no repositório.

## Publicação
1. Crie um repositório GitHub e envie todos os arquivos mantendo as pastas.
2. No Netlify, importe o repositório usando **Add new site / Import an existing project**.
3. Configuração de build: publish directory `.`; functions directory `netlify/functions` (o `netlify.toml` já define essas opções).
4. Nas configurações do site, adicione uma variável de ambiente chamada `OPENAI_API_KEY` com uma chave da API OpenAI, usando ajuda de um responsável adulto. Mantenha o escopo Functions/runtime quando essa opção estiver disponível.
5. Faça um novo deploy após adicionar a variável.
6. Teste `https://SEU-SITE.netlify.app/health`: deve retornar JSON com `"ai_configured":true`.

Opcional: configure `OPENAI_MODEL` com um modelo disponível na sua conta. O padrão do projeto é `gpt-5.4-mini`.

## Importante
- A API da OpenAI é cobrada separadamente do ChatGPT e pode gerar custos. Um responsável deve configurar limites e acompanhar o uso antes de tornar o gerador público.
- Não compartilhe a chave, não a coloque em `index.html` nem em repositório público.
- O botão Pro e pagamentos continuam sendo apenas demonstração. Não existe cobrança, conta de usuário ou assinatura ativa.
- Esta versão foi preparada para deploy via integração Git do Netlify. Arrastar apenas o HTML/ZIP no Netlify Drop publica arquivos estáticos e não ativa as funções de IA.
