# 🚀 Professional Python Development Environment

Padrão de configuração para projetos Python, focado em segurança, organização e reprodutibilidade.

---

## 🛠️ Guia de Configuração do Ambiente

### 1. Isolamento com `.venv`

Utilizamos o **Virtual Environment** para garantir que as dependências de cada projeto permaneçam isoladas, evitando conflitos de versões.

```powershell
# Criar o ambiente virtual na raiz do projeto
python -m venv .venv

# Ativar o ambiente no Windows (PowerShell)
.\.venv\Scripts\Activate.ps1
```

### 2. Variáveis de Ambiente com `.env`

Segurança em primeiro lugar. Nunca escreva senhas ou chaves de API diretamente no código.

- Crie um arquivo chamado `.env` na raiz do projeto.
- Adicione suas variáveis: `DB_USER=Xande`
- Instale a biblioteca necessária: `pip install python-dotenv`

### 3. Versionamento Seguro com `.gitignore`

Arquivo essencial para impedir o upload de arquivos sensíveis ou pastas pesadas ao GitHub. O arquivo deve conter:

```plaintext
.venv/
.env
__pycache__/
.vscode/
data/
```

### 4. Reprodutibilidade com `requirements.txt`

Sempre documente as bibliotecas instaladas para que o ambiente possa ser replicado.

```powershell
# Gerar lista de dependências
pip freeze > requirements.txt

# Instalar dependências em um novo setup
pip install -r requirements.txt
```

---

## 🔌 Extensões VS Code

- **GitLens — Git supercharged:** Visualização detalhada de commits e histórico de código.
- **Material Icon Theme:** Ícones visuais para arquivos e pastas no explorador.
- **Pylance:** Language server performática com type checking e autocompletion.
- **Python (Microsoft):** Suporte completo à linguagem e IntelliSense.
- **Python Debugger:** Extensão de debugging para Python.
- **Python Environments:** Gerenciamento unificado de ambientes virtuais Python.
