## Passo 5: Faça o Merge do seu Pull Request

Sua alteração foi revisada, hora de trazê-la para a `main`! Fazer o merge de um pull request adiciona os commits dele à branch base e (geralmente) fecha o pull request.

### 📖 Teoria: O que acontece ao mesclar?

Quando você faz o **merge** de um pull request, os commits da sua branch passam a fazer parte da `main`. A partir daí, todos que derem pull na `main` recebem suas alterações. A branch de feature cumpriu seu papel e pode ser apagada com segurança.

### ⌨️ Atividade: Faça o merge do pull request e sincronize

1. Abra seu pull request no GitHub.com.

2. Clique no botão verde **Merge pull request** revise a mensagem de commit e adicione uma descrição caso necessário e depois em **Confirm merge**.

3. (Recomendado) Clique em **Delete branch** para organizar; os commits estão seguros na `main` agora.

4. Volte ao GitHub Desktop. Clique em **Current Branch** e selecione **`main`**.

5. Clique em **Fetch origin** e depois em **Pull origin** para trazer as alterações mescladas para a sua `main` local, você pode ver o histórico de alterações na aba History do github desktop.

   > 🪧 **Observação**: O pull mantém a cópia do seu computador em sincronia com o GitHub.

6. Com seu pull request mesclado, a Mona vai verificar seu trabalho e compartilhar o próximo passo. 🎉

<details>
<summary>Com dificuldades? 🤷</summary><br/>

- Se o botão **Merge pull request** estiver acinzentado, confirme que não há verificações obrigatórias pendentes.
- O merge precisa ser feito no GitHub.com; o GitHub Desktop é usado depois para dar **pull** no resultado.

</details>
