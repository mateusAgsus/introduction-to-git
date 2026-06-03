## Passo 2: Adicione os arquivos do projeto em uma branch

Agora que o repositório está no seu computador, vamos fazer nossa primeira alteração. Em vez de editar a `main` diretamente, vamos trabalhar em uma **branch**, a forma segura e padrão de propor mudanças.

### 📖 Teoria: O que é uma branch?

Uma **branch** é uma linha de trabalho independente. Ela permite adicionar ou alterar arquivos sem afetar a branch `main` (a confiável) até que seu trabalho esteja pronto e revisado.

O fluxo típico é:

1. Criar uma branch.
2. Fazer e **commitar** suas alterações nela.
3. **Enviar** (push) a branch para o GitHub.
4. Abrir um **pull request** para mesclar na `main` (nos próximos passos!).

### ⌨️ Atividade: Crie uma branch, commite uma alteração e envie

> [!IMPORTANT]
> Use exatamente o nome de branch abaixo, para que a Mona consiga acompanhar seu progresso.

1. No GitHub Desktop, clique em **Current Branch** no topo e depois em **New Branch**.

2. Nomeie a branch exatamente assim:

   ```txt
   add-project-files
   ```

   Confirme que ela é baseada em `main` e clique em **Create Branch**.

3. Adicione um arquivo de projeto. Clique em **Open the repository in your external editor** (ou abra a pasta do repositório) e crie um novo arquivo chamado `PROJECT.md` com algum conteúdo, por exemplo:

   ```md
   # Stack Overflow

   Cópia do projeto do jogo Stack Overflow da nossa equipe.

   - Mantido por: <seu nome>
   ```

   Salve o arquivo.

1. De volta ao GitHub Desktop, você verá o `PROJECT.md` listado em **Changes**. Escreva um **resumo** (mensagem de commit) no canto inferior esquerdo:

   ```txt
   Add project description file
   ```
> [!NOTE]
> Não se procupe com a nossa política de commits por agora, vamos ter tempo para nos ambientarmos com isso depois.
   
   Em seguida, clique em **Commit to add-project-files**.

1. Clique em **Publish branch** (canto superior direito) para enviar sua branch e o commit para o GitHub.

2. Com sua branch enviada, a Mona vai verificar seu trabalho. Dê um instante a ela e fique de olho nos comentários. 👀

<details>
<summary>Com dificuldades? 🤷</summary><br/>

- O nome da branch precisa ser exatamente `add-project-files`.
- Confirme que você **commitou** a alteração antes de publicar; é o commit que a Mona procura.
- Se esqueceu de publicar, clique em **Publish branch** (ou **Push origin**) na barra superior.

</details>
