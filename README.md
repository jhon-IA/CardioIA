# CardioIA — Entrega Parte 1/2/3 (Mínimo Obrigatório)

Este repositório cumpre os requisitos solicitados:
- **README.md** detalhado: projeto, **3 partes**, **objetivos** e **fontes**.
- **Subpasta `docs/`** (com conteúdos) e **subpasta `data/`** (dataset numérico).
- **Textos `.txt`** adicionados em `docs/textos/`.
- **Espaço para link público de >100 imagens** (indicar no README abaixo).

> **Governança & Viés:** priorizamos origem e licenças dos dados; destacamos variáveis sensíveis (sexo, idade) e lembramos que modelos podem reproduzir vieses de amostragem. Consulte a seção final.

---

## 🎯 Objetivo Geral
Preparar **três tipos de dados** (numéricos, textuais e visuais) para alimentar algoritmos de IA, treinar modelos, fazer análises comparativas e gerar soluções em saúde cardiovascular.

---

## 🧩 Partes do Projeto

### Parte 1 — Dados Numéricos (IoT/Clínico)
- **Origem**: *simulado* (amostra com 300 linhas) em `data/dados_cardio_limpo.csv`.
- **Link público (preencha após subir no seu Drive/OneDrive):**  
  👉 **[SUBSTITUA AQUI PELO LINK COMPARTILHADO]**
- **Variáveis-chave (justificativa clínica):**
  - **idade**: risco cardiovascular cresce com a idade.
  - **sexo**: diferenças de apresentação e risco entre homens/mulheres.
  - **pressao_arterial_repouso**: hipertensão é fator de risco maior para DAC/AVC.
  - **colesterol**: hipercolesterolemia aumenta risco de aterosclerose.
  - **frequencia_cardiaca_max**: condicionamento/esforço; pode refletir carga hemodinâmica.
  - **tipo_dor_peito (TA/ATA/NAP/ASY)**: proxy de probabilidade pré-teste de DAC.
  - **glicemia_jejum**: DM/pré-DM associados a maior risco.
  - **ecg_repouso**, **angina_exercicio**, **depressao_st**, **inclinacao_st**: alteram probabilidade de isquemia.
  - **doenca_cardiaca (alvo)**: rótulo binário para classificação.
- **Uso:** EDA, classificação binária, calibração de probabilidades, explicabilidade.

### Parte 2 — Dados Textuais (NLP)
- **Arquivos `.txt` no repositório**: veja `docs/textos/`.
  - `texto_medico_prevencao_cardiovascular.txt`: panorama clínico de fatores de risco e prevenção (texto autoral de referência acadêmica).
  - `texto_literario_coracao.txt`: ensaio breve sobre o simbolismo do coração e sua relação com a experiência do paciente (texto autoral).
- **Como explorar com NLP:**
  - **extração de entidades** (ex.: sintomas, fatores de risco), **classificação de tópicos** (prevenção, diagnóstico, tratamento),
    **análise de sentimentos** (narrativas dos pacientes), **resumo automático** e **similaridade semântica** (busca de trechos relevantes).
- **Relevância:** dá contexto clínico e humanístico, melhora *feature engineering* e comunicação de resultados com leigos.

### Parte 3 — Dados Visuais (Visão Computacional)
- **Requisito**: reunir **≥100 imagens** (.jpg/.png) de ECGs/angiogramas/RX torácico.
- **Link público (preencha após subir no seu Drive/OneDrive):**  
  👉 **[SUBSTITUA AQUI PELO LINK COMPARTILHADO DAS 100+ IMAGENS]**
- **Possíveis análises de VC:**
  - **Detecção de padrões/anomalias** (calcificações, estenoses, bordas de vasos);
  - **Segmentação** (delimitar estruturas);
  - **Classificação** (normal vs suspeito).

---

## 🔗 Fontes de Dados (exemplos) — para uso/consulta pelo grupo
- **Numéricos (CSV):** Kaggle — *Heart Failure Prediction* (fedesoriano), *Heart Disease Cleveland*, *Framingham*.
- **Imagens:** Kaggle — *Annotated X-ray Angiography (ARCADE)*; bases abertas de ECG/raio-X (verificar licenças).
- **Textos/Diretrizes:** OMS, AHA, ESC, SBC; portais como SciELO/BVS (respeitar direitos).

> **Importante:** este repositório traz textos autorais em `.txt` por questões de licença. Você pode substituir pelos `.txt` baixados de SciELO/BVS/SUS/Projeto Gutenberg e manter aqui na pasta `docs/textos/`.

---

## ✅ Checklist de conformidade
- [x] Dataset numérico (≥100 linhas) organizado e **explicado** no README.
- [x] **Textos `.txt`** no repositório explicados e **contextualizados** para NLP.
- [ ] **Link público** para **100+ imagens** (Drive/OneDrive) **adicionado** acima.
- [ ] **Link público** para o **dataset numérico** (Drive/OneDrive) **adicionado** acima.

---

## 🛡️ Governança de Dados & Viés (resumo)
- **Licenças**: checar permissões de uso/redistribuição; manter créditos/fontes.
- **Privacidade**: usar dados anonimizados/sintéticos; evitar atributos identificáveis.
- **Viés**: monitorar distribuição por **sexo/idade**; avaliar *performance parity* (ex.: diferença de recall por subgrupos).
- **Rastreabilidade**: registrar origem, versões e data de coleta; documentar transformações (data prep).

---

© 2025