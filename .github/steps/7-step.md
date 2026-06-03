## Passo 7: Resolva um Conflito de Merge

Às vezes duas pessoas alteram a **mesma linha** de formas diferentes. O Git não consegue decidir qual versão está correta, então ele pede que um humano escolha. Isso é um **conflito de merge**, e faz parte normal da colaboração. 😌

Para você praticar de forma realista, **já abrimos um pull request para você** que tem um conflito: um colega alterou o subtítulo do jogo na branch base, enquanto outra branch (`resolve-this-conflict`) alterou a mesma linha.

### 📖 Teoria: Anatomia de um conflito

Quando ocorre um conflito, o GitHub (e o Git) marcam o trecho em disputa com três marcadores:

```diff
<<<<<<< conflict-base
A versão que está atualmente na branch base
=======
A versão da branch que está sendo mesclada
>>>>>>> resolve-this-conflict
```

Para resolver, você escolhe o conteúdo final (manter um lado, o outro ou combinar) e **remove os três marcadores**.

### ⌨️ Atividade 1: Resolva o conflito no GitHub.com (recomendado)

1. Abra a aba **Pull requests** do seu repositório e abra o **"Resolva o conflito de merge do subtítulo"**.

   [Abrir a aba Pull requests →](../../pulls)

2. O GitHub mostra *"This branch has conflicts that must be resolved."* Clique no botão **Resolve conflicts**.

3. No editor da web, encontre o conflito em `src/index.html`. Apague os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`) e mantenha uma **única** linha de subtítulo, por exemplo:

   ```html
   <div class="subtitle">Clear the errors to keep the stack stable! 🧱</div>
   ```

4. Clique em **Mark as resolved** e depois em **Commit merge**.

5. De volta ao pull request, clique em **Merge pull request** e depois em **Confirm merge**.

6. Com o conflito resolvido e mesclado, a Mona vai verificar seu trabalho e compartilhar o passo final. 🎉

### ⌨️ Atividade 2 (alternativa): Resolva no GitHub Desktop

Prefere resolver localmente? Também dá:

1. No GitHub Desktop, clique em **Fetch origin** e mude para a branch `resolve-this-conflict`.
2. Escolha **Branch → Merge into current branch...** e selecione **`conflict-base`**. O Desktop vai apontar o conflito.
3. Clique em **Open in your editor**, corrija `src/index.html` (remova os marcadores, mantenha uma linha) e salve.
4. De volta ao Desktop, commite o merge e clique em **Push origin**.
5. Por fim, abra o pull request no GitHub.com e faça o **Merge**.

<details>
<summary>Com dificuldades? 🤷</summary><br/>

- Confirme que você removeu **todos** os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`). O arquivo deve conter apenas uma linha de `subtitle`.
- O passo é concluído quando o pull request **"Resolva o conflito de merge do subtítulo"** é **mesclado** na `conflict-base`.

</details>
