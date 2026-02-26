[README.md](https://github.com/user-attachments/files/25570830/README.md)
# Ferramentaria Elétrica CA — pronto para GitHub e Vercel

## O que tem nesta pasta
- `index.html`: aplicação principal
- `manifest.json`: metadados PWA
- `sw.js`: service worker para cache offline básico
- `favicon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: ícones
- `.gitignore`: ignora arquivos locais desnecessários

## Publicar no GitHub
1. Crie um repositório novo no GitHub.
2. Envie todos os arquivos desta pasta para a raiz do repositório.
3. Faça o commit e o push.

## Publicar na Vercel
1. Entre na Vercel.
2. Clique em **Add New > Project**.
3. Importe o repositório do GitHub.
4. Framework Preset: **Other**.
5. Build Command: deixe vazio.
6. Output Directory: deixe vazio.
7. Clique em **Deploy**.

## Atenção importante
Esta aplicação é **100% frontend**.
Os dados são salvos no navegador do usuário usando `localStorage` e `IndexedDB`.
Isso significa:
- cada navegador/dispositivo terá seus próprios dados
- não existe banco de dados compartilhado
- login e permissões não são seguros para produção
- publicar na Vercel hospeda a interface, mas **não cria backend**

## Antes de usar em produção
- trocar o admin padrão e remover credenciais expostas no frontend
- mover autenticação para backend
- salvar dados em banco real (Supabase, Firebase, PostgreSQL, etc.)
- revisar permissões e auditoria

## Observação
O HTML original já referencia `manifest.json`, ícones locais e `sw.js`, então estes arquivos foram adicionados para o deploy ficar redondo.
