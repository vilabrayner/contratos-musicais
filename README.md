# 🎵 Contratos Musicais
### Gerador de contratos profissionais para apresentações musicais (macOS / Windows)

O **Contratos Musicais** é uma ferramenta desktop desenvolvida em **Python + CustomTkinter** para facilitar a criação rápida e profissional de contratos de apresentações musicais.

Ele permite:

- Preencher dados do **Contratante** e **Contratado**
- Cadastrar detalhes do **Evento** (local, data, horário, duração, chegada do staff)
- Determinar quem fornece o **som** (banda ou contratante)
- Configurar regras de **alimentação**
- Definir diversas formas de **pagamento**, incluindo cálculo automático de sinal
- Inserir dados completos de **favorecido** (incluindo chave PIX e opção “mesmo que o contratado”)
- Gerar um **resumo** do contrato em tempo real
- Produzir automaticamente o arquivo final `.docx` totalmente preenchido
- Gerar também um `.json` com snapshot para reedição posterior
- Manter versionamento automático `_v1`, `_v2`, `_v3...`

---

## 📦 Downloads

As versões compiladas ficam na aba **Releases** do GitHub:

https://github.com/seu-usuario/contratos-musicais/releases

---

## 🖥️ Como usar

1. Abrir o aplicativo.
2. Preencher as abas:
   - Contratante
   - Contratado
   - Evento / Local
   - Som
   - Alimentação
   - Pagamento
   - Favorecido
3. Ir na aba **Resumo** para visualizar o contrato antes da geração.
4. Clicar em **Gerar contrato**.
5. Os arquivos são criados na pasta `contratos_gerados/`.

---

## 🛠️ Ambiente de desenvolvimento

### Instalação

```
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
.\.venv\Scripts\activate       # Windows

pip install -r requirements.txt
```

### Executar

```
python contracts.py
```

---

## 🏗️ Build manual (PyInstaller)

### macOS

```
pyinstaller --name ContratosMusicais --onefile --windowed --add-data "templates:templates" contracts.py
```

### Windows

```
pyinstaller --name ContratosMusicais --onefile --windowed --add-data "templates;templates" contracts.py
```

---

## 🤖 Build automático (GitHub Actions)

Crie uma tag para disparar o build:

```
git tag -a v0.1.0 -m "Primeira versão"
git push origin v0.1.0
```

O GitHub cria a Release automaticamente.

---

## 📁 Estrutura do projeto

```
contratos-musicais/
├── contracts.py
├── templates/
│   └── contrato_som_banda.docx
├── contratos_gerados/
├── requirements.txt
└── .github/
    └── workflows/
        └── build.yml
```

---

## ❤️ Créditos

Criado por **Vila Brayner**.

