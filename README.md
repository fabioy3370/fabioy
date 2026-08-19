# Site pessoal — Fabio Yamagishi

Site estático (HTML puro, sem build, sem dependências) com bio, currículo e
experiência profissional.

## Estrutura

```
index.html              página única do site
foto-hero.jpg            foto da seção Hero
foto-secundaria.jpg      foto da seção Contato
foto-pedra-grande.jpg    imagem panorâmica da seção Sobre
galeria-pessoal.jpg      galeria de fotos da seção "Fora do Escritório"
```

Não há build nem servidor — é só abrir `index.html` num navegador para
conferir localmente, ou publicar a pasta inteira no GitHub Pages.

## Publicar no GitHub Pages — passo a passo

### 1. Criar o repositório
1. Acesse [github.com](https://github.com) e faça login (ou crie uma conta).
2. Clique no **+** no canto superior direito → **New repository**.
3. Dê um nome ao repositório, por exemplo `site-fabio-yamagishi`.
4. Deixe como **Public** (obrigatório no plano gratuito para usar o GitHub
   Pages sem custo).
5. NÃO marque a opção "Add a README file" (para evitar conflito, já que já
   temos um README pronto).
6. Clique em **Create repository**.

### 2. Enviar os arquivos

**Opção A — pela interface do GitHub (sem usar terminal):**
1. Na página do repositório recém-criado, clique em
   **uploading an existing file** (ou **Add file → Upload files**).
2. Arraste todos os arquivos desta pasta (`index.html`, as 4 imagens `.jpg`
   e o `.gitignore`/`README.md`) para a área de upload.
3. Role até o final da página e clique em **Commit changes**.

**Opção B — pelo terminal (Git):**
```
cd pasta-do-site
git init
git add .
git commit -m "Site pessoal"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/site-fabio-yamagishi.git
git push -u origin main
```

### 3. Ativar o GitHub Pages
1. No repositório, vá em **Settings** (aba no topo).
2. No menu lateral, clique em **Pages**.
3. Em "Build and deployment" → **Source**, selecione **Deploy from a
   branch**.
4. Em **Branch**, escolha `main` e a pasta `/ (root)`.
5. Clique em **Save**.
6. Aguarde 1–2 minutos. O GitHub vai mostrar o link do site no topo dessa
   mesma página, algo como:
   `https://SEU_USUARIO.github.io/site-fabio-yamagishi/`

### 4. Domínio próprio (opcional)
Se quiser usar um domínio próprio (ex: `fabioyamagishi.com.br`), na mesma
tela de **Settings → Pages** há um campo **Custom domain** — basta digitar
o domínio e seguir as instruções de configuração de DNS que o GitHub
mostra.

## Atualizações futuras

Qualquer alteração no `index.html` ou nas imagens: substitua o arquivo no
repositório (pela interface de upload ou via `git add`, `git commit`,
`git push`) e o GitHub Pages atualiza o site automaticamente em 1–2
minutos.
