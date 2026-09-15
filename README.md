# 🚀  Relatório Operacional de Pré-Decolagem

Projeto desenvolvido para a **Atividade Integradora da FIAP**, com o objetivo de desenvolver um sistema computacional capaz de analisar dados de telemetria de uma nave espacial simulada e determinar se ela está em condições seguras para realizar a decolagem.

O projeto utiliza **Python** para realizar verificações determinísticas dos parâmetros de segurança, além de uma **análise energética** e de uma **análise assistida por Inteligência Artificial**.

---

## 📌 Sobre o projeto

O sistema simula uma etapa de verificação operacional realizada antes da decolagem da missão espacial **Aurora Siger**.

A partir dos dados de telemetria informados pelo usuário, o programa verifica se os parâmetros estão dentro dos limites de segurança definidos pelo projeto.

Os principais parâmetros analisados são:

* 🌡️ Temperatura interna
* 🌡️ Temperatura externa
* 🛠️ Integridade estrutural
* 🔋 Nível de energia
* ⛽ Pressão dos tanques
* 🚀 Status do módulo de propulsão
* 📡 Status do módulo de comunicação
* 🧭 Status do módulo de navegação e controle

A decisão final do algoritmo é:

> **PRONTO PARA DECOLAR**
> ou
> **DECOLAGEM ABORTADA**

Todos os parâmetros precisam atender às condições estabelecidas para que a decolagem seja autorizada.

---

## 🎯 Objetivos

O projeto tem como principais objetivos:

* Desenvolver um algoritmo de verificação de segurança utilizando Python;
* Trabalhar com entrada e processamento de dados de telemetria;
* Utilizar estruturas condicionais para tomada de decisão;
* Identificar anomalias nos parâmetros da nave;
* Simular diferentes cenários operacionais;
* Realizar uma análise energética da nave;
* Utilizar Inteligência Artificial como ferramenta complementar de análise;
* Refletir sobre ética, responsabilidade e sustentabilidade na aplicação da tecnologia.

---

## Observação

As imagens dos códigos e execução do projeto estão contidas no arquivo PDF enviado.

## 📊 Parâmetros de segurança

| Parâmetro              | Unidade | Condição segura     |
| ---------------------- | ------- | ------------------- |
| Temperatura interna    | °C      | 15 °C a 30 °C       |
| Temperatura externa    | °C      | 0 °C a 40 °C        |
| Integridade estrutural | 0 ou 1  | Deve ser `1`        |
| Nível de energia       | %       | Mínimo de 80%       |
| Pressão dos tanques    | PSI     | 200 a 300 PSI       |
| Módulos críticos       | 0 ou 1  | Todos devem ser `1` |

Os limites foram definidos para a simulação do projeto e são utilizados pelo algoritmo para determinar a condição de segurança da nave.

---

## 💻 Tecnologias utilizadas

* **Python**
* Estruturas condicionais (`if`)
* Variáveis e tipos de dados (`float`, `int` e `bool`)
* Entrada de dados pelo usuário
* Operações matemáticas
* Análise de telemetria
* Inteligência Artificial

---

## ⚙️ Funcionamento

O algoritmo segue uma sequência de verificação:

```text
Entrada dos dados de telemetria
            ↓
Verificação dos parâmetros
            ↓
Comparação com os limites de segurança
            ↓
       Todos OK?
        ↙      ↘
      SIM       NÃO
       ↓         ↓
PRONTO PARA   Identificação
 DECOLAR      das anomalias
                 ↓
          DECOLAGEM ABORTADA
```

A variável booleana `pronto` é utilizada para representar inicialmente uma condição segura. Quando algum parâmetro está fora do padrão, o sistema identifica a falha e altera seu valor para `False`.

---

## 🧪 Cenários de teste

Foram desenvolvidos **10 cenários de telemetria** para validar o funcionamento do algoritmo.

| Cenário | Situação                        | Resultado             |
| ------- | ------------------------------- | --------------------- |
| 1       | Condição normal                 | ✅ Pronto para decolar |
| 2       | Temperatura interna elevada     | ❌ Decolagem abortada  |
| 3       | Temperatura externa elevada     | ❌ Decolagem abortada  |
| 4       | Energia insuficiente            | ❌ Decolagem abortada  |
| 5       | Pressão dos tanques baixa       | ❌ Decolagem abortada  |
| 6       | Pressão dos tanques elevada     | ❌ Decolagem abortada  |
| 7       | Falha na integridade estrutural | ❌ Decolagem abortada  |
| 8       | Falha no módulo de propulsão    | ❌ Decolagem abortada  |
| 9       | Falha no módulo de comunicação  | ❌ Decolagem abortada  |
| 10      | Múltiplas anomalias             | ❌ Decolagem abortada  |

Os testes foram planejados para verificar tanto situações normais quanto falhas individuais e múltiplas anomalias simultâneas.

---

## 🔋 Análise energética

Além da verificação dos parâmetros de telemetria, o projeto realiza uma análise energética da nave.

### Parâmetros utilizados

* **Capacidade total:** 500 kWh
* **Carga mínima para decolagem:** 80%
* **Consumo estimado durante a decolagem:** 100 kWh
* **Perdas energéticas:** 10%
* **Consumo médio:** 50 kW

A análise calcula:

1. Energia disponível;
2. Perdas energéticas;
3. Energia útil;
4. Autonomia inicial;
5. Consumo durante a decolagem;
6. Energia restante;
7. Autonomia após a decolagem.

### Exemplo

No **Cenário 4**, a nave apresenta 65% de carga:

```text
Energia disponível: 325 kWh
Perdas energéticas: 32,5 kWh
Energia útil: 292,5 kWh
Consumo na decolagem: 100 kWh
Energia restante: 192,5 kWh
Autonomia após a decolagem: 3,85 horas
```

Apesar de existir energia suficiente para o consumo matematicamente previsto da decolagem, o cenário é classificado como **DECOLAGEM ABORTADA**, pois a carga inicial de 65% está abaixo do requisito mínimo de 80%.

---

## 🤖 Análise assistida por Inteligência Artificial

A Inteligência Artificial foi utilizada como uma **ferramenta complementar** ao algoritmo determinístico.

Enquanto o programa em Python utiliza regras objetivas para determinar se a nave pode decolar, a IA auxilia na:

* Interpretação dos dados;
* Identificação de possíveis anomalias;
* Classificação das situações;
* Identificação de riscos operacionais;
* Organização das informações.

Foram utilizadas as classificações:

* 🟢 **NORMAL**
* 🟡 **ATENÇÃO**
* 🔴 **CRÍTICA**

Um ponto importante do projeto é que a IA **não substitui o algoritmo determinístico** responsável pela decisão de decolagem.

---

## 🧠 Ética e responsabilidade

Por se tratar de um sistema aplicado a uma situação crítica, o projeto também aborda a importância da responsabilidade no desenvolvimento de sistemas computacionais.

A proposta considera que decisões críticas devem utilizar critérios objetivos, verificáveis e previamente estabelecidos, mantendo a **supervisão humana** mesmo quando ferramentas de Inteligência Artificial são utilizadas.

Dessa forma, o projeto separa a função do algoritmo determinístico da análise complementar realizada pela IA.

---

## 🌱 Sustentabilidade tecnológica

O projeto também considera a sustentabilidade no contexto da exploração espacial.

Entre os aspectos discutidos estão:

* Eficiência energética;
* Uso consciente de recursos;
* Redução de desperdícios;
* Impactos ambientais dos lançamentos;
* Descarte de equipamentos;
* Lixo espacial;
* Eficiência dos algoritmos e do processamento computacional.

A sustentabilidade é considerada não apenas na geração e utilização de energia, mas também na forma como **hardware e software são projetados e utilizados**.

---

## ▶️ Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/bianca-pavan16/ATIVIDADE-INTEGRADORA-RELAT-RIO-OPERACIONAL-DE-PR--DECOLAGEM.git
```

### 2. Acesse a pasta

```bash
cd ATIVIDADE-INTEGRADORA-RELAT-RIO-OPERACIONAL-DE-PR--DECOLAGEM
```

### 3. Execute o programa

```bash
python nome_do_arquivo.py
```

> Substitua `nome_do_arquivo.py` pelo nome do arquivo Python presente no projeto.

---

## 📁 Estrutura do projeto

```text
📦 ATIVIDADE-INTEGRADORA
│
├── 📄 README.md
├── 🐍 código Python
├── 📊 relatório
└── 📓 notebook
```

---

## 👩‍💻 Integrantes

* **Bianca Pavan Andre**
* **Julia de Oliveira Silva**
* **Maria Fernanda Barbosa Firmo**
* **Natiely Moreira Chaves**
* **Pedro Henrique Monteiro Scabio**

---

## 🔗 Links

**Google Colab:**
https://colab.research.google.com/drive/1liJYvPYkpA-z4licWm6XuhaaxdQ0vhqj?usp=sharing

**Repositório GitHub:**
https://github.com/bianca-pavan16/ATIVIDADE-INTEGRADORA-RELAT-RIO-OPERACIONAL-DE-PR--DECOLAGEM.git

---

## 📚 Considerações finais

O projeto  demonstra uma aplicação prática de conceitos de programação, análise de dados, lógica computacional, energia e Inteligência Artificial em um cenário de missão espacial simulada.

A atividade evidencia que o desenvolvimento de sistemas computacionais para situações críticas envolve não apenas a criação do código, mas também **testes, análise de riscos, responsabilidade ética e preocupação com a sustentabilidade tecnológica**.
