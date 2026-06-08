## Passo 7: Resolva um Conflito de Merge

Às vezes duas pessoas alteram a **mesma linha** de formas diferentes. O Git não consegue decidir qual versão está correta, então ele pede que um humano escolha. Isso é um **conflito de merge**, e faz parte da colaboração. 😌

Para você praticar de forma realista, **criamos a branch `resolve-this-conflict`** que altera o subtítulo do projeto. Enquanto isso, um colega alterou **a mesma linha** na `main`. Quando você abrir um pull request dessa branch para a `main`, o GitHub vai apontar o conflito para você resolver.

### 📖 Teoria: Anatomia de um conflito

Quando ocorre um conflito, o GitHub (e o Git) marcam o trecho em disputa com três marcadores:

```diff
<<<<<<< main
A versão que está atualmente na main
=======
A versão da branch que está sendo mesclada
>>>>>>> resolve-this-conflict
```

Para resolver, você escolhe o conteúdo final (manter um lado, o outro ou combinar) e **remove os três marcadores**.

### ⌨️ Atividade 1: Abra o pull request e resolva o conflito (recomendado)

1. Abra o formulário de novo pull request já preenchido pelo link abaixo (base `main`, comparando com `resolve-this-conflict`):

   [Abrir o pull request →](../../colaborar-com-github-desktop/compare/main...resolve-this-conflict?expand=1)

1. Dê um título, por exemplo `Resolver conflito do subtítulo`, e clique em **Create pull request**.

1. O GitHub mostra *"This branch has conflicts that must be resolved."* Clique no botão **Resolve conflicts**.

1. No editor da web, encontre o conflito em `src/index.html`. Apague os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`) e mantenha uma **única** linha de subtítulo, por exemplo:

   ```html
   <div class="subtitle">Clear the errors to keep the stack stable! 🧱</div>
   ```

1. Clique em **Mark as resolved** e depois em **Commit merge**.

1. De volta ao pull request, clique em **Merge pull request** e depois em **Confirm merge**.

1. Com o conflito resolvido e mesclado, a Mona vai verificar seu trabalho e compartilhar o passo final. 🎉

### ⌨️ Atividade 2 (alternativa): Resolva no GitHub Desktop

Prefere resolver localmente? Também dá (depois ainda será preciso abrir e mesclar o pull request no GitHub.com):

1. No GitHub Desktop, clique em **Fetch origin** e mude para a branch `resolve-this-conflict`.
1. Escolha **Branch → Merge into current branch...** e selecione **`main`**. O Desktop vai apontar o conflito.
1. Clique em **Open in your editor**, corrija `src/index.html` (remova os marcadores, mantenha uma linha) e salve.
1. De volta ao Desktop, commite o merge e clique em **Push origin**.
1. Por fim, abra o pull request (`resolve-this-conflict` → `main`) no GitHub.com e faça o **Merge**.

<details>
<summary>Com dificuldades? 🤷</summary><br/>

- Confirme que o pull request vai de **`resolve-this-conflict`** (compare) para **`main`** (base).
- Confirme que você removeu **todos** os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`). O arquivo deve conter apenas uma linha de `subtitle`.
- O passo é concluído quando esse pull request é **mesclado** na `main`.

</details>
