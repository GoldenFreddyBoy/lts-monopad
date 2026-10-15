# LTS Monopad — Protótipo v0.1.0

Primeira versão visual do Monopad da LTS Laboratory, feita com React, TypeScript e Vite.

## O que já funciona
- Interface escura com detalhes vermelhos, estilo terminal sci-fi.
- Layout responsivo para computador e celular.
- Navegação entre os seis módulos.
- Cartões e janelas de detalhes com conteúdo demonstrativo.
- Relógio/data do dispositivo na página Clima / Horário.
- Controles visuais de áudio e botão para iniciar o sistema.
- Animações, scanlines e efeitos de hover.

## Importante
Este é um **protótipo de interface**. Ele ainda não tem contas reais, banco de dados, permissões seguras, uploads persistentes, áudio real nem bot do Discord. Os dados exibidos são fictícios. Não use esta versão para guardar informações confidenciais. As permissões verdadeiras precisam ser verificadas no servidor/banco de dados.

## Como executar no Windows
1. Instale uma versão LTS atual do Node.js: https://nodejs.org/
2. Extraia o ZIP.
3. Abra a pasta `lts-monopad` no VS Code.
4. No menu **Terminal > Novo Terminal**, execute:

   ```bash
   npm install
   npm run dev
   ```

5. O terminal mostrará um endereço local, geralmente `http://localhost:5173`. Abra-o no navegador.
6. Para encerrar, clique no terminal e pressione `Ctrl + C`.

## Onde personalizar
- `src/App.tsx`: textos, módulos e comportamento.
- `src/styles.css`: cores, tamanhos, layout e animações.
- `public/`: coloque imagens e, futuramente, músicas/vídeos do projeto.

## Próximas etapas sugeridas
1. Inserir o logotipo oficial da LTS.
2. Conectar os arquivos de música e efeitos sonoros reais.
3. Criar login e cadastro.
4. Conectar Supabase para dados, autenticação e armazenamento.
5. Aplicar permissões por cargo de forma segura.
6. Criar bot Discord para publicar/editar conteúdos.
7. Publicar a aplicação online.
