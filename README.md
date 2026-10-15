# LTS Monopad — Guia do projeto (v0.4.0)

Protótipo de interface do LTS Laboratory feito com React, TypeScript e Vite. Esta versão mantém o visual do terminal, os módulos de acesso livre e adiciona um player funcional para vídeos MP4 cadastrados na pasta `public/videos`.

## Executar no Windows

1. Instale o Node.js LTS: https://nodejs.org/
2. Extraia o ZIP para uma pasta fácil de encontrar.
3. Abra o VS Code e selecione **Arquivo > Abrir Pasta**. Escolha a pasta `lts-monopad` (a que contém `package.json`).
4. Abra **Terminal > Novo Terminal**.
5. Execute estes comandos, um de cada vez:

   ```bash
   npm install
   npm run dev
   ```

6. Abra o endereço que aparecer no terminal, normalmente `http://localhost:5173`.
7. Para encerrar o servidor, volte ao terminal e pressione `Ctrl + C`.

## Onde fica cada coisa?

| Caminho | Para que serve |
| --- | --- |
| `src/App.tsx` | Estrutura principal, navegação, conteúdo dos módulos e comportamento do site. |
| `src/styles.css` | Cores, aparência, espaçamento, efeitos e adaptação para celular. |
| `public/lts-logo.png` | Logo exibida na interface. Substitua por outra imagem mantendo o mesmo nome para trocar a logo. |
| `public/music/` | Arquivos MP3 usados na música ambiente. |
| `public/videos/` | Pasta onde você coloca os vídeos MP4 dos Avisos. |
| `public/videos/videos.json` | Lista de vídeos que aparece no módulo Avisos. Edite esse arquivo para adicionar, remover ou renomear vídeos, sem mexer no código React. |
| `public/videos/LEIA-ME.txt` | Instruções rápidas para cadastrar vídeos. |
| `package.json` | Dependências e comandos para iniciar/construir o projeto. |

## Adicionar um vídeo MP4 aos Avisos (sem mexer no código)

1. Copie o vídeo MP4 para `public/videos/`. Por exemplo: `luna-boas-vindas.mp4`.
2. Abra `public/videos/videos.json` no VS Code.
3. Cadastre o vídeo como um objeto dentro da lista. Exemplo:

   ```json
   [
     {
       "title": "LUNA // Boas-vindas",
       "subtitle": "Transmissão institucional",
       "file": "luna-boas-vindas.mp4",
       "description": "Mensagem de boas-vindas da LUNA."
     }
   ]
   ```

4. Salve o arquivo. Atualize a página do site se necessário.
5. Entre em **Avisos**. O cartão do vídeo aparecerá; clique nele para abrir o player e reproduzir.

Para cadastrar vários vídeos, coloque vários objetos entre `[` e `]`, separados por vírgulas. O campo `file` precisa corresponder exatamente ao nome do MP4 na pasta. Use aspas duplas e JSON válido. Se não houver vídeos cadastrados, o módulo mostrará uma mensagem explicando o que fazer.

## Adicionar uma música MP3

1. Copie o MP3 para `public/music/`.
2. Para que apareça no seletor de músicas, abra `src/App.tsx` e procure por `musicTracks`.
3. Adicione uma linha seguindo o formato das faixas existentes, usando o nome exato do arquivo.

## Publicar no GitHub e Vercel

Envie os arquivos do projeto para o repositório GitHub, incluindo `public/videos/videos.json` e os MP4 que pretende publicar. Na Vercel, configure o projeto como Vite; o comando de build é `npm run build` e a pasta de saída é `dist`. Cada alteração enviada ao repositório poderá iniciar um novo deploy.

**Atenção ao tamanho:** vídeos grandes podem deixar o GitHub lento ou ultrapassar limites de envio/build. Se isso acontecer, hospede os vídeos em um serviço de armazenamento de mídia e adapte os endereços dos vídeos.

## O que esta versão ainda não faz

- Não tem contas reais, banco de dados, login nem permissões de servidor.
- A lista `videos.json` é estática: para publicar/remover vídeos no site hospedado, altere o arquivo e faça novo deploy. Não há painel de upload dentro do site.
- Os dados de participantes, investigações e arquivos continuam sendo exemplos de demonstração.
- Temperatura e indicadores ambientais são ilustrativos.

Não coloque segredos, senhas, tokens ou informações confidenciais neste protótipo.
