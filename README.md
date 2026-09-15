# 🏭 Sistema de Monitoramento Proativo de EPIs e Segurança Industrial

## 👥 Integrantes
- Juliana Barbosa Sandes - 555605
- Clara Jullia Kondrasovas Costa e Silva- 556064
- Arthur Macedo Gouvea - 556499
- Lucas do Carmo Cima - RM: 564964
- Arthur Ederson de Oliveira Silva - RM: 557079

## ❌ O Problema
No ambiente industrial da Metaindústria, os modelos tradicionais de segurança do trabalho costumam ser reativos ou punitivos, identificando falhas no uso de Equipamentos de Proteção Individual (EPIs) apenas após a ocorrência de incidentes ou por meio de auditorias manuais esporádicas. Esse atraso na identificação de atitudes de risco aumenta a vulnerabilidade dos operadores e a probabilidade de acidentes graves em maquinários de alta periculosidade.

## 🚀 A Proposta de Solução
Nossa solução implementa um sistema de **Segurança Industrial Inteligente e Proativa** baseado em Visão Computacional. Utilizando câmeras IP instaladas diretamente nas células de trabalho e maquinários, o sistema analisa o fluxo de vídeo em tempo real para identificar de forma autônoma a ausência de EPIs obrigatórios (como capacetes, luvas e óculos) ou a aproximação de operadores de zonas de risco.

Quando uma inconformidade é detectada:
1. O evento é registrado imediatamente em um banco de dados relacional para fins de auditoria, permitindo que a gestão instrua e treine o colaborador posteriormente de forma direcionada.
2. Caso a atitude represente um risco iminente ou crítico, um alerta visual e sonoro é disparado instantaneamente na estação de trabalho para evitar a ocorrência do acidente.

## 🛠️ Tecnologias Selecionadas e Justificativa Técnica
* **Python**: Linguagem de programação principal, escolhida pela sua maturidade e ecossistema robusto para o desenvolvimento de inteligência artificial.
* **OpenCV / YOLO (You Only Look Once)**: Frameworks de Visão Computacional e redes neurais selecionados por permitirem a detecção de múltiplos objetos por frame com altíssima precisão e latência inferior a 500ms, atendendo ao requisito não funcional de tempo real industrial.
* **PostgreSQL / Oracle SQL**: Banco de dados relacional utilizado para persistência segura e estruturada dos logs de infração, garantindo integridade dos dados para relatórios de conformidade.

## 🗺️ Arquitetura da Solução (Modelagem UML)

Os artefatos de engenharia de software desenvolvidos para esta Sprint podem ser consultados abaixo e na pasta `/Diagramas`:

### 📌 Diagrama de Casos de Uso
<img src="https://github.com/ArthurGouvea/Eng-De-Software-Sprint1/blob/main/Diagramas/Diagrama%20de%20Casos%20de%20Uso.jpg" alt="Diagrama de Casos de Uso" width="100%">

### 📌 Diagrama de Atividades
<img src="https://github.com/ArthurGouvea/Eng-De-Software-Sprint1/blob/main/Diagramas/Diagrama%20de%20Atividades.jpg" width="100%">

### 📌 Diagrama de Classes
<img src="https://github.com/ArthurGouvea/Eng-De-Software-Sprint1/blob/main/Diagramas/Diagrama%20de%20Classes.jpg" alt="Diagrama de Classes" width="100%">

## 🚀 Entrega da Sprint - Protótipo e Documentação de Design

*   **Protótipo Navegável (Figma):** https://www.figma.com/make/nrBuN7wbsG7XjlX4jzlnKQ/Sprint3---Eng-de-Software?t=urBEgIVWR3K1afGG-1
*   **Vídeo de Walkthrough (Até 3 minutos):** https://youtu.be/Fl7BBQKYPAU
*   **Documentação das Cerimônias Scrum: https://docs.google.com/document/d/1KhLR_kX9VBLgVM7DTjNsZLj4j9MjOGIhUhVH86B4hd8/edit?usp=sharing
*   **Link Trello Organizado: https://trello.com/invite/b/6a89c3d2bb145b955e0cd319/ATTI71a9e22b7478e6da6274682fc72068728ED620B2/sprint3engsoft

## 🕹️ Instruções de Navegação do Protótipo

Para testar os fluxos principais conectados ao desafio do Metaindústria, siga o roteiro abaixo no modo de apresentação do Figma:

1. **Fluxo de EPIs:** Na barra lateral, clique em **Colaboradores** -> Selecione um funcionário para **Consultar EPIs** cadastrados ou clique em **Cadastrar Novo EPI**.
2. **Fluxo de Alertas de Risco (Visão Computacional):** Vá para a tela de **Monitoramento em Tempo Real**. Simule uma violação (ausência de capacete/óculos) para visualizar a **Emissão do Alerta de Risco** piscando no painel.
3. **Fluxo de Conformidade:** Acesse a aba **Relatórios** -> Selecione o setor desejado (ex: Usinagem / Montagem) para **Gerar o Relatório de Conformidade por Setor**.
Telas novas (Sprint 3)
4. **Tratamento de Ocorrência:** Fechamento do ciclo de segurança: A versão da Sprint 2 apenas alertava sobre infrações em tempo real, gerando sobrecarga cognitiva sem um caminho de resolução. A nova tela permite auditar o frame congelado da IA, validar se houve falso positivo e documentar a tratativa imediata exigida pelas normas regulamentadoras do SESMT.
5. **Configuração de Zonas e Câmeras:**  Escalabilidade e flexibilidade industrial: Ambientes fabris possuem áreas com diferentes níveis de periculosidade. Essa tela permite configurar dinamicamente o perímetro de risco (geofencing visual) e os EPIs específicos por máquina, eliminando alarmes falsos em áreas onde certos EPIs não são mandatórios.
