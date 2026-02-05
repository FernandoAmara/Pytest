# Domine Pytest

Este repositório contém os **arquivos e exemplos práticos** do curso **“Domine Pytest”** , organizados por seções, cobrindo desde o básico até tópicos avançados como **fixtures**, **parametrização**, **marcadores**, **exceções**, **plugins**, **testes de integração** e **CI/CD com GitHub Actions**.

---

## ✅ O que você encontra aqui

- Exemplos simples de testes (`assert`, organização, boas práticas)
- Testes estruturais e organização em módulos
- **Fixtures** (setup/teardown, escopo, mocks)
- **Parametrização** (simples, múltiplos parâmetros)
- **Marcadores** e configuração via `pytest.ini`
- Testes de **exceções** (`raise`, exceções genéricas)
- Uso de **plugins** (exemplos de execução e relatórios)
- **Integração/end-to-end** (app + testes)
- Pipeline de **CI/CD** executando `pytest` via **GitHub Actions**

---

## 🗂️ Estrutura do projeto

```text
Pytest/
├─ 2.Intro/
│  └─ test_basico.py
├─ 3.PrimeirosTestes/
│  ├─ 1testebasicos/
│  │  ├─ funcoes.py
│  │  ├─ test_basic1.py
│  │  ├─ test_basic2.py
│  │  └─ test_basic3.py
│  └─ 2testesestuturais/
│     └─ test_estruturais.py
├─ 4.Fixtures/
│  ├─ 1Exemplos/
│  │  ├─ test_basic.py
│  │  └─ test_mock.py
│  ├─ 2setupteardown/
│  │  └─ test_teardown.py
│  └─ 3escopo/
│     └─ test_fixturesscope.py
├─ 5.Parametrizado/
│  ├─ 1Simples/
│  │  ├─ soma.py
│  │  └─ test_soma.py
│  ├─ 2classificacao/
│  │  ├─ classifica_idade.py
│  │  └─ test_classifica_idade.py
│  └─ 3MultiplosParametros/
│     ├─ calcula_total.py
│     └─ test_calculo.py
├─ 6.Marcadores/
│  ├─ 1Basico/
│  │  ├─ pytest.ini
│  │  └─ test_operacoes.py
│  └─ 2MultiplsMarcadores/
│     ├─ pytest.ini
│     └─ test_variados.py
├─ 7.Excecoes/
│  ├─ 1.Raise/
│  │  ├─ verifica_idade.py
│  │  └─ test_verificaidade.py
│  └─ 2.GenericException/
│     ├─ divisao.py
│     └─ test_divisao.py
├─ 8.Plugins/
│  └─ 1Plugins/
│     ├─ funcoes.py
│     ├─ test_basic1.py
│     ├─ test_basic2.py
│     └─ test_basic3.py
├─ 10.Integracaoendtoend/
│  └─ 1Integracao/
│     ├─ app.py
│     └─ test_integration.py
├─ 11.cicd/
│  ├─ main.py
│  ├─ test_main.py
│  ├─ requirements.txt
│  └─ .github/workflows/python-app.yml
└─ 12,Avancado/
   ├─ 1performance/
   │  ├─ my_code.py
   │  └─ test_performance.py
   └─ 2.assincrono/
      ├─ fetch_data.py
      └─ test_async.py
```

---

## 🔧 Requisitos

- Python 3.8+ (recomendado 3.10+)
- Pytest instalado

Instalação rápida:

```bash
pip install pytest
```

---

## ▶️ Como rodar os testes

Na raiz do projeto (pasta que contém `Pytest/`):

```bash
pytest
```

Para rodar testes de uma seção específica:

```bash
pytest Pytest/4.Fixtures
pytest Pytest/5.Parametrizado/1Simples
```

Para mostrar detalhes (verbose):

```bash
pytest -v
```

Para parar no primeiro erro:

```bash
pytest -x
```

---

## 🧩 Marcadores (markers)

Algumas seções usam `pytest.ini` para definir/organizar marcadores.

Exemplo de execução por marcador (se estiver configurado nos testes):

```bash
pytest -m "nome_do_marcador"
```

---

## 🧪 Testes de exceções

A pasta **7.Excecoes** traz exemplos clássicos com `pytest.raises(...)`, cobrindo:
- validações que disparam erro
- exceções genéricas (ex.: divisão por zero)

---

## ⚡ Avançado: performance e assíncrono

Em **12,Avancado** você encontra exemplos de:
- testes de performance/tempo
- testes assíncronos (async) com Pytest

---

## 🔁 CI/CD com GitHub Actions

A pasta **11.cicd** contém um workflow que executa `pytest` automaticamente em **push** e **pull request**.

Arquivo:

- `.github/workflows/python-app.yml`

Para usar no seu repositório GitHub:
1. mantenha a pasta `.github/workflows/` no repo
2. faça push
3. o GitHub Actions executará os testes automaticamente

> Observação: no exemplo, o workflow instala `pytest` e executa `pytest`.  

---

## 💡 Dicas rápidas

- Nomeie seus arquivos como `test_*.py` para o Pytest descobrir automaticamente.
- Prefira funções pequenas e puras para facilitar o teste.
- Use **fixtures** para evitar repetição e melhorar organização.
- Combine **parametrização** + **fixtures** para testes mais expressivos.

---

## 📄 Licença

Defina a licença que preferir (MIT, Apache-2.0 etc.). Se este repositório for público, recomenda-se incluir um arquivo `LICENSE`.

---

## 👤 Autor

**Fernando Amaral** — EIA.ai
