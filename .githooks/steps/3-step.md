## Passo 3: Abra um Pull Request

Sua branch está no GitHub, mas ainda não faz parte da `main`. Para propor a mesclagem dela, você abre um **pull request** (PR).

### 📖 Teoria: O que é um Pull Request?

Um **pull request** é um pedido para mesclar as alterações de uma branch em outra (aqui, de `add-project-files` para `main`). Ele é o coração da colaboração no GitHub porque:

- Mostra exatamente **o que mudou**.
- Dá aos colegas um lugar para **revisar e discutir** antes de mesclar.
- Mantém a `main` estável, condicionando as mudanças a uma revisão.

### ⌨️ Atividade: Abra um pull request a partir da sua branch

1. No GitHub Desktop, com a branch `add-project-files` selecionada, clique no botão **Preview Pull Request** ou **Create Pull Request**. (Você também pode usar **Branch → Create Pull Request**.)

   <br/>

   > 🪧 **Observação**: O GitHub Desktop abre o navegador para finalizar a criação do pull request no GitHub.com.

2. No navegador, confirme que o pull request compara:

   - **base:** `main`  ⬅️  **compare:** `add-project-files`

3. Dê um **título** claro ao pull request, exemplo:

   ```txt
   Add project description file
   ```

4. Perceba que será apresentado um modelo de Pull Request no campo de descrição, esse modelo será utilizado por nossa organização para ajudar na rastreabilidade de mudanças, fique a vontade para alterar o modelo conforme a necessidade, veja como ficou o modelo clicando em preview.

5. Adicione uma breve **descrição** do que você alterou e clique em **Create pull request**.

6. Com seu pull request aberto, a Mona vai verificar seu trabalho e compartilhar o próximo passo. 🔎

<details>
<summary>Com dificuldades? 🤷</summary><br/>

- Se você não vê o botão **Create Pull Request**, confirme que a branch `add-project-files` está selecionada e publicada.
- O pull request precisa mesclar **para a `main`** a partir de **`add-project-files`**.

</details>
