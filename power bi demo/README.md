# RBT — Inspeções RFB & Mapa

Modelo semântico e dashboard construídos a partir de `Analise_RFB_Mapa_Cntr.xlsm`
(aba `Planilha1`: Mês, Volume, RFB, Mapa).

## Arquivos

- **`Analise_RFB_Mapa_Cntr.xlsm`** — planilha de origem.
- **`RBT_Inspecoes_Contentores.pbit`** — template Power BI com o modelo semântico pronto.
- **`mapa.pbit`** — template em branco original (mantido como estava).

## Modelo semântico (`RBT_Inspecoes_Contentores.pbit`)

**Tabelas**
- `Fato Inspeções` — Data, Volume, RFB, Mapa (importado da aba `Planilha1` via Power Query).
- `Calendário` — Data, Ano, Trimestre, Mês Núm, AnoMês (tabela calendário calculada, 2025–2026).
- Relacionamento: `Fato Inspeções[Data]` → `Calendário[Data]` (muitos-para-um).

Os percentuais **não são colunas importadas** — são medidas DAX (`% RFB`, `% Mapa`) para
somar corretamente em qualquer nível de agregação.

**Medidas principais:** Volume Total, Total RFB, Total Mapa, Total Inspeções, % RFB,
% Mapa, % Taxa de Inspeção Combinada, Variação Volume MoM %, Var. Taxa RFB/Mapa MoM (p.p.),
Média Móvel 3M % RFB/Mapa.

## Como abrir

1. Abra `RBT_Inspecoes_Contentores.pbit` no Power BI Desktop.
2. Ele vai pedir o parâmetro **`SourceFolder`** — informe o caminho completo da pasta
   onde está `Analise_RFB_Mapa_Cntr.xlsm` (com `\` no final), ex.:
   `C:\Users\SeuUsuario\meu_projeto\power bi demo\`
3. Clique em **Carregar**.
4. (Recomendado) Na view de Modelo, clique com o botão direito em `Calendário` →
   **Marcar como tabela de datas** → coluna `Data`.
5. A página **Visão Geral** já vem com cartões de KPI, gráfico de linha (% RFB vs % Mapa),
   gráfico de colunas (Volume por mês) e uma tabela detalhada.

Para trocar o caminho depois: **Página Inicial → Transformar dados → Editar parâmetros**.

## Preview do dashboard

Uma prévia visual (HTML, fora do Power BI) foi publicada como artifact nesta conversa —
mesma lógica de cálculo das medidas do modelo.
