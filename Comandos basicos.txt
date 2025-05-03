---

### **Configuração Inicial**
1. **Configurar usuário**  
   ```bash
   git config --global user.name "Seu Nome"
   git config --global user.email "seu@email.com"
   ```

2. **Verificar configurações**  
   ```bash
   git config --list
   ```

---

### **Repositórios**
3. **Inicializar um repositório**  
   ```bash
   git init
   ```

4. **Clonar um repositório remoto**  
   ```bash
   git clone <URL-do-repositório>
   ```

---

### **Trabalhando com Arquivos**
5. **Verificar status dos arquivos**  
   ```bash
   git status
   ```

6. **Adicionar arquivos ao staging (preparação)**  
   ```bash
   git add <nome-do-arquivo>  # Adiciona um arquivo específico
   git add .                  # Adiciona todos os arquivos modificados
   ```

7. **Remover arquivo do staging**  
   ```bash
   git reset <nome-do-arquivo>
   ```

---

### **Commits**
8. **Criar um commit**  
   ```bash
   git commit -m "Mensagem do commit"
   ```

9. **Corrigir último commit**  
   ```bash
   git commit --amend -m "Nova mensagem"
   ```

---

### **Branches (Ramificações)**
10. **Listar branches**  
    ```bash
    git branch           # Locais
    git branch -a        # Locais e remotas
    ```

11. **Criar uma branch**  
    ```bash
    git branch <nome-da-branch>
    ```

12. **Mudar de branch**  
    ```bash
    git checkout <nome-da-branch>
    ```
    ou (versões mais recentes do Git):  
    ```bash
    git switch <nome-da-branch>
    ```

13. **Criar e mudar para uma branch**  
    ```bash
    git checkout -b <nome-da-branch>
    ```

14. **Deletar uma branch**  
    ```bash
    git branch -d <nome-da-branch>      # Deleta local
    git push origin --delete <branch>   # Deleta remota
    ```

---

### **Sincronizando com o Repositório Remoto (GitHub)**
15. **Adicionar um repositório remoto**  
    ```bash
    git remote add origin <URL-do-repositório>
    ```

16. **Enviar commits para o remoto**  
    ```bash
    git push -u origin <nome-da-branch>  # Primeiro push
    git push                             # Pushs seguintes
    ```

17. **Baixar alterações do remoto**  
    ```bash
    git pull origin <nome-da-branch>
    ```

18. **Atualizar branches remotas**  
    ```bash
    git fetch
    ```

---

### **Histórico e Diferenças**
19. **Ver histórico de commits**  
    ```bash
    git log
    git log --oneline    # Versão resumida
    ```

20. **Ver diferenças entre arquivos**  
    ```bash
    git diff             # Alterações não stageadas
    git diff --staged    # Alterações stageadas
    ```

---

### **Desfazendo Coisas**
21. **Desfazer alterações em um arquivo**  
    ```bash
    git checkout -- <nome-do-arquivo>
    ```

22. **Resetar para um commit anterior**  
    ```bash
    git reset --hard <hash-do-commit>  # CUIDADO: perde alterações
    ```

23. **Reverter um commit**  
    ```bash
    git revert <hash-do-commit>
    ```

---

### **Outros Úteis**
24. **Ignorar arquivos (`.gitignore`)**  
    Crie um arquivo `.gitignore` e liste arquivos/pastas que não devem ser rastreados.

25. **Stash (salvar alterações temporárias)**  
    ```bash
    git stash           # Salva alterações
    git stash pop       # Recupera alterações
    ```

---