CardioIA — Entrega (Parte 1, 2 e 3)

Este repositório reúne, de forma objetiva, os três tipos de dados solicitados para o projeto de IA em saúde cardiovascular.
Incluí README detalhado, a pasta docs/ com conteúdos e a pasta data/ com o dataset numérico.

Pasta pública (Drive) com todos os arquivos exigidos — CSV, textos .txt e ≥100 imagens:
https://drive.google.com/drive/folders/1RBI40cvqwsdEIZf81J9TRNCqQNq3_6Sg?usp=drive_link

Governança & Viés: respeito às licenças dos dados, atenção a variáveis sensíveis (sexo, idade) e risco de viés amostral. Detalhes ao final.

🎯 Objetivo Geral

Preparar dados numéricos, textuais e visuais para alimentar algoritmos de IA, treinar modelos, realizar análises comparativas e gerar soluções aplicadas à saúde cardiovascular.

🧩 Partes do Projeto
Parte 1 — Dados Numéricos (IoT/Clínico)

Origem dos dados: simulados (amostra com 300 linhas) em data/dados_cardio_limpo.csv.

Link público (Drive):
👉 https://drive.google.com/drive/folders/1RBI40cvqwsdEIZf81J9TRNCqQNq3_6Sg?usp=drive_link

Variáveis-chave e justificativa clínica:

idade — risco cardiovascular aumenta com a idade.

sexo — diferenças de apresentação e risco entre homens e mulheres.

pressao_arterial_repouso — hipertensão é um dos fatores de risco mais relevantes para DAC/AVC.

colesterol — hipercolesterolemia eleva o risco de aterosclerose.

frequencia_cardiaca_max — reflete condicionamento e carga hemodinâmica.

tipo_dor_peito (TA/ATA/NAP/ASY) — aproxima a probabilidade pré-teste de doença coronária.

glicemia_jejum — diabetes/pré-diabetes aumentam risco cardiovascular.

ecg_repouso, angina_exercicio, depressao_st, inclinacao_st — sinais que alteram a probabilidade de isquemia.

doenca_cardiaca (alvo) — rótulo binário para tarefas de classificação.

Uso previsto: EDA, classificação binária, calibração de probabilidades e explicabilidade (ex.: SHAP/permutação).

Parte 2 — Dados Textuais (NLP)

Arquivos .txt disponíveis na pasta docs/textos/ (neste repositório) e na pasta pública do Drive acima.

Como pretendo explorar com NLP:

Extração de entidades (sintomas, fatores de risco, tratamentos).

Classificação de tópicos (prevenção, diagnóstico, reabilitação).

Análise de sentimentos em narrativas relacionadas ao paciente.

Resumo automático e busca semântica para apoiar educação em saúde.

Relevância: dá contexto clínico e humanístico, auxiliando feature engineering e comunicação de achados.

Parte 3 — Dados Visuais (Visão Computacional)

Requisito atendido: ≥100 imagens (.jpg/.png) de exames relacionados ao coração (ex.: ECGs, angiogramas ou raio-X torácico).

Link público (Drive):
👉 https://drive.google.com/drive/folders/1RBI40cvqwsdEIZf81J9TRNCqQNq3_6Sg?usp=drive_link

Como pretendo explorar com VC:

Detecção de padrões/anomalias (bordas de vasos, suspeita de estenose).

Segmentação de estruturas relevantes.

Classificação (normal vs. suspeito) como baseline para estudos comparativos.

🔗 Fontes de Dados (exemplos para referência)

Numéricos (CSV): Heart Failure Prediction (fedesoriano), Heart Disease Cleveland (UCI), Framingham (Kaggle).

Imagens: Annotated X-ray Angiography (ARCADE) — MICCAI 2023 (Kaggle) e bases abertas de ECG/RX (ver licenças).

Textos/Diretrizes: OMS, AHA, ESC, SBC; portais SciELO/BVS (respeitando direitos autorais).

✅ Checklist de conformidade

 Dataset numérico (≥100 linhas) organizado e explicado no README.

 Textos .txt incluídos e contextualizados para NLP.

 Link público para ≥100 imagens (Drive) adicionado acima.

 Link público para o CSV (Drive) adicionado acima.

🛡️ Governança de Dados & Viés (resumo)

Licenças & créditos: uso apenas de material autorizado; manutenção de referências.

Privacidade: dados numéricos simulados/anonimizados; evitar atributos identificáveis.

Viés: monitorar distribuição por sexo/idade e checar paridade de desempenho entre subgrupos.

Rastreabilidade: registrar origem, datas e versões; documentar transformações aplicadas.
