# CardioIA: meu pacote de dados para análise cardiovascular com IA

Reuni um conjunto **Prático e testável** de dados **numéricos**, **textuais** e **visuais** para sustentar experimentos de IA em saúde cardiovascular. A ideia é simples: criar uma base que permita **explorar, comparar e evoluir** modelos de forma ágil nas próximas fases do projeto.

> **Pasta pública (Drive) com CSV, textos `.txt` e a coleção de ≥100 imagens:**  
> **https://drive.google.com/drive/folders/1RBI40cvqwsdEIZf81J9TRNCqQNq3_6Sg?usp=drive_link**

---

## Por que estas três frentes?

- **Numéricos**: permitem hipóteses rápidas e mensuráveis (classificação binária, curvas ROC, explicabilidade).  
- **Textos**: conectam clínica e contexto humano (NLP para extrair sintomas, tópicos, sentimentos).  
- **Imagens**: trazem o componente visual do diagnóstico (VC para padrões, bordas e anomalias).

Juntas, elas formam um **laboratório completo**: consigo testar ideias em paralelo, cruzar achados e iterar com velocidade.

---

---

## Parte 1: Dados numéricos (IoT/Clínico)

- **O que eu preparei**: `data/dados_cardio_limpo.csv` (300 linhas, **simulado**), espelhando variáveis que realmente aparecem em estudos clínicos.
- **Link público (Drive)**: mesmo link acima.
- **Variáveis-chave e por quê**:
  - **idade** e **sexo** o risco e a apresentação clínica variam entre faixas etárias e entre homens/mulheres.  
  - **pressao_arterial_repouso** e **colesterol** — fatores centrais para risco de DAC/AVC (hipertensão e dislipidemia).  
  - **frequencia_cardiaca_max** proxy de condicionamento/carga hemodinâmica.  
  - **tipo_dor_peito (TA/ATA/NAP/ASY)** aproxima a probabilidade pré-teste de coronariopatia.  
  - **glicemia_jejum** — diabetes/pré-diabetes aumentam risco.  
  - **ecg_repouso, angina_exercicio, depressao_st, inclinacao_st** adicionam sinal clínico relevante.  
  - **doenca_cardiaca (alvo)** rótulo binário para treino e avaliação.
- **Como vou usar**: EDA, modelos de classificação, calibração de probabilidade e explicabilidade (ex.: SHAP).

> **Mapa rápido do “tipo_dor_peito”**  
> **TA** (angina típica), **ATA** (angina atípica), **NAP** (dor não-anginosa), **ASY** (assintomático).

---

## Parte 2: Textos (NLP)

- **Onde estão**: `docs/textos/` neste repositório e também no Drive.  
- **Como pretendo explorar**:
  - **Extração de entidades** (sintomas, fatores de risco, tratamentos);  
  - **Classificação de tópicos** (prevenção, diagnóstico, reabilitação);  
  - **Análise de sentimentos** em narrativas do paciente;  
  - **Resumo automático** e **busca semântica** para material educativo.
- **Por que isso importa**: dá profundidade clínica e humana, melhora *feature engineering* e ajuda a comunicar achados de forma clara.

---

## Parte 3: Imagens (Visão Computacional)

- **Coleção (≥100 imagens)**: ECGs/angiogramas/RX torácico **hospedados no Drive** (link acima).  
- **O que vou testar**:
  - **Detecção de padrões/anomalias** (bordas de vasos, suspeita de estenose);  
  - **Segmentação** de estruturas;  
  - **Classificação** (normal vs. suspeito) como baseline para comparações.

---

## Como isso se conecta na prática

1. **Exploro** cada modalidade separadamente (numérico, texto, imagem).  
2. **Comparo** o que os modelos aprendem (pontos fortes/limitações).  
3. **Integro** insights para novos ciclos (ex.: features textuais que reforçam sinais numéricos, ou rótulos visuais que ajudam a refinar a probabilidade clínica).

---

## Governança, privacidade e viés

- **Licenças & créditos**: uso somente material autorizado e mantenho referências.  
- **Privacidade**: dados numéricos **simulados/anonimizados**; sem atributos identificáveis.  
- **Viés**: monitoro distribuição por **sexo/idade** e verifico paridade de desempenho entre subgrupos.  
- **Rastreabilidade**: documento origem, datas/versões e transformações aplicadas.

---

## Como navegar

```
.
├─ README.md
├─ data/
│  └─ dados_cardio_limpo.csv
└─ docs/
   └─ textos/
      ├─ texto_medico_prevencao_cardiovascular.txt
      └─ texto_literario_coracao.txt
```

Dados e insumos (CSV completo, textos e a coleção de imagens), **está tudo no Drive do link acima**. 
