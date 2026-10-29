# 📄 ATS Friendly Resume Generator (JobMatch ATS)

> Aplicação Web para análise sintática, comparação de palavras-chave e otimização ética de currículos para sistemas de triagem automatizada (ATS - Applicant Tracking System).

---

## 📌 1. O Problema Resolvido

Muitos profissionais qualificados são descartados em processos seletivos antes mesmo de passarem por uma avaliação humana. Isso ocorre devido ao uso de **ATS (Applicant Tracking Systems)**, softwares de RH que ranqueiam candidatos com base no alinhamento semântico e estrutural entre o currículo e a descrição da vaga.

O **JobMatch ATS** resolve esse gargalo ao:
* Comparar o currículo atual do candidato com o texto exato da vaga.
* Identificar lacunas de palavras-chave cruciais, terminologias técnicas e competências.
* Reestruturar a apresentação do perfil profissional em um formato facilmente legível por leitores automáticos.

---

## 🛡️ 2. Regra de Ouro (Princípio Ético)

> **A aplicação otimiza a forma como o candidato apresenta sua trajetória, mas JAMAIS inventa, altera ou acrescenta experiências e competências que o usuário não possui.**

Todas as sugestões geradas são estritamente fundamentadas nos dados originais fornecidos pelo candidato, focando em reescrita estratégica, clareza e adequação vocabular ao mercado.

---

## 🎯 3. Fluxo da Análise e Funcionamento
1. **Entrada de Dados:** O usuário cola a descrição completa da oportunidade e o seu currículo atual nos campos de texto.
2. **Processamento Semântico:** A aplicação analisa a densidade de termos, relevância de competências e compatibilidade de cargos.
3. **Diagnóstico em Tempo Real:** Exibição de pontuação de aderência (*Match Score*), lista de palavras-chave presentes e termos ausentes prioritários.
4. **Reescrita Otimizada:** Geração de uma versão reestruturada, limpa e padronizada para exportação em PDF/Text.

---

## 🛠️ 4. Especificação e Mega Prompt Utilizado

Para a construção e orientação do modelo no **Lovable**, foi formulado o seguinte Mega Prompt em Markdown utilizando o design system **shadcn/ui**:


# Contexto e Objetivo
Atue como um Desenvolvedor Front-End Sênior e Especialista em UX/UI. Crie uma aplicação web responsiva chamada "JobMatch ATS" utilizando React, TailwindCSS e o design system shadcn/ui. O objetivo é comparar o currículo de um candidato com a descrição de uma vaga e gerar uma versão otimizada para sistemas ATS.

# Identidade Visual e Layout
- Paleta de Cores: Design limpo e profissional com tons de azul marinho (primary: #0f172a), cinza neutro (slate-100/800) e verde para métricas positivas (emerald-600).
- Componentes shadcn/ui: Card, Button, Textarea, Progress, Badge, Tabs, Alert.

# Estrutura de Telas e Interface
1. Header:
   - Logo "JobMatch ATS" com ícone de documento.
   - Badge descritivo: "Otimização Ética para RH".

2. Seção Principal (Entrada de Dados - Layout 2 Colunas no Desktop):
   - Coluna Esquerda: Card com Textarea para "Descrição da Vaga" (placeholder legível, limite dinâmico de caracteres).
   - Coluna Direita: Card com Textarea para "Seu Currículo Atual".
   - Botão de Ação Central: "Analisar e Otimizar para ATS" (com estado de loading/spinner).

3. Seção de Resultados (Exibida após processamento):
   - Card de Score: Barra de progresso circular ou linear indicando a porcentagem de Match (ex: 78%).
   - Painel de Palavras-Chave (Tabs/Badges):
     * Badges Verdes: Palavras-chave encontradas no currículo.
     * Badges Vermelhas/Amarelas: Termos críticos presentes na vaga que faltam no currículo.
   - Área do Currículo Ajustado:
     * Exibição em bloco formatado (Markdown/Preview) do currículo otimizado.
     * Aviso de integridade: "O currículo otimizado reorganizou suas informações sem criar experiências fictícias."
     * Botão "Exportar em PDF".

# Regras de Negócio e Comportamento
- Otimização sem alucinação: A reescrita deve apenas reorganizar e ajustar termos sinônimos, mantendo a veracidade dos dados do usuário.
- Validação de entrada: Desabilitar o botão de análise se algum dos dois campos estiver vazio.
