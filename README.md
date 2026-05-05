# ▶️ Como Executar o Projeto

## 1. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/pos-tech-challenge-fase-1.git
cd pos-tech-challenge-fase-1
```

---

## 2. Criar ambiente virtual (recomendado)

```bash
python -m venv venv
```

### Ativar o ambiente:

**Windows:**
```bash
venv\Scripts\activate
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

---

## 3. Instalar dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn shap jupyter
```

---

## 4. Executar o Jupyter Notebook

```bash
jupyter notebook
```

Depois:

- Acesse a pasta `notebook/`
- Abra o arquivo `.ipynb`
- Execute todas as células (Run → Run All)

---

## 5. Observações

- Certifique-se de que o dataset está no caminho correto:

  `data/cervical-cancer_csv.csv`

- Caso ocorra erro de caminho, ajuste o diretório conforme a localização do notebook.
