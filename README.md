# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

---

## Metadados

- **Nomes dos alunos e RGM:** Letícia Valentim Reges - 047369680| [Nome do Aluno 2 - RGM]

---

## 1. Caracterização da Organização

- **Nome e natureza da organização:** **Odontologia Sasaki**, uma clínica odontológica privada de médio porte, com fins lucrativos.
- **Contexto e porte:** Possui aproximadamente 20 funcionários (entre dentistas, auxiliares, técnicos, recepcionistas e profissionais responsáveis pela produção e manutenção de equipamentos). Realiza cerca de 500 atendimentos por mês. Além dos atendimentos clínicos, possui um setor responsável pela produção de implantes, aparelhos ortodônticos e equipamentos/acessórios utilizados nos consultórios (como peças em impressoras 3D, cadeiras odontológicas, refletores, etc.). Possui diversos equipamentos distribuídos entre consultórios, laboratório e área de produção.
- **Problemas e necessidades identificados:** Dificuldade no controle e acompanhamento dos equipamentos, com informações espalhadas em planilhas soltas e anotações. Isso impossibilita saber rapidamente a localização, a situação atual, o histórico de manutenção de cada equipamento e o controle de peças/materiais em estoque. A necessidade principal é centralizar essas informações em um sistema de banco de dados para facilitar a manutenção, organização e controle operacional.
- **Justificativa da escolha:** A clínica apresenta um volume expressivo de equipamentos, materiais e processos internos que necessitam de organização. Trata-se de um caso ideal para o projeto, pois a modelagem de um banco de dados permitirá resolver diretamente as falhas no acompanhamento das manutenções, no estoque e na gestão dos equipamentos.
- **Evidências da organização:**
  - **Endereço:** R. Jardim Tamoio, 1089 - Conj. Res. José Bonifácio, São Paulo - SP, 08255-010
  - **Link no Google Maps:** https://maps.app.goo.gl/ALuZBqSGNaq6kBxy9
  - **Contato:** Luduque@hotmail.com | +55 11 99001-2968

---

## 2. Processos de Negócio

- **Principais processos mapeados:**
  1. **Cadastro e controle de equipamentos:** Registro individual dos equipamentos, sua localização, responsável e situação atual.
  2. **Controle de manutenção:** Registro de manutenções preventivas e corretivas, problemas identificados e serviços executados.
  3. **Controle de estoque:** Gestão de entrada e saída de peças, materiais e componentes utilizados na manutenção e na produção.
  4. **Produção de equipamentos e materiais:** Registro da fabricação interna de implantes, aparelhos ortodônticos e peças em impressoras 3D.
  5. **Controle dos consultórios:** Acompanhamento e inventário dos equipamentos instalados em cada consultório e seu estado operacional.

- **Fluxogramas:** *(Opcional - Anexar imagens dos fluxogramas dos processos se houver)*

---

## 3. Requisitos do Sistema

### 3.1 Requisitos Funcionais
O sistema deverá:
- Permitir cadastrar, alterar e consultar equipamentos.
- Registrar a localização e o responsável por cada equipamento.
- Registrar manutenções preventivas e corretivas.
- Permitir consultar o histórico de manutenção dos equipamentos.
- Controlar a entrada e a saída de materiais e peças do estoque.
- Registrar equipamentos e peças produzidos pela própria clínica.
- Informar o status operacional dos equipamentos (disponível, em manutenção, inativo ou com problemas).
- Permitir consultar os equipamentos existentes em cada consultório.

### 3.2 Requisitos Não Funcionais
- **Segurança:** O acesso ao sistema deverá ser realizado por usuários autorizados mediante autenticação.
- **Usabilidade:** O sistema deverá possuir uma interface simples e fácil de utilizar pelos colaboradores.
- **Desempenho:** As consultas e registros deverão ser realizados de forma rápida.
- **Disponibilidade:** As informações deverão estar disponíveis sempre que necessárias para as atividades diárias da clínica.
- **Integridade:** Os dados cadastrados deverão permanecer organizados e consistentes, evitando duplicidades ou perda de histórico.

---

## 4. Regras de Negócio

- **Regras operacionais:**
  - Todo equipamento deve obrigatoriamente possuir um cadastro no sistema.
  - Cada equipamento deve estar vinculado a uma localização (ex.: consultório) dentro da clínica.
  - Toda manutenção realizada deve ser registrada no histórico do equipamento.
  - Equipamentos cadastrados em estado de "manutenção" não podem ser considerados disponíveis para uso.
  - Toda saída de peças e materiais do estoque deve ser devidamente registrada.
  - A produção de equipamentos ou materiais deve obrigatoriamente gerar um registro no sistema.

- **Restrições organizacionais:**
  - A clínica necessita manter o controle atualizado para evitar o uso acidental de equipamentos com defeito, reduzindo paralisações nos atendimentos prestados aos pacientes.
  - O histórico completo é fundamental para acompanhar a vida útil dos aparelhos, planejar substituições, agendar manutenções preventivas e controlar custos operacionais.

---

## 5. Dicionário de Dados Conceitual (Preliminar)

### Entidade: Equipamentos (Exemplos de aparelhos mapeados na pesquisa)

| Atributo / Aparelho | Descrição | Regra de Negócio Associada |
| :--- | :--- | :--- |
| **Cadeira odontológica** | Equipamento utilizado para acomodar o paciente durante o atendimento. | Deve estar vinculada a um consultório cadastrado. Manutenções devem ser registradas. |
| **Scanner intraoral** | Realiza a captura digital da arcada dentária para criação de modelos 3D. | Deve ser utilizado por profissional autorizado e registrado no sistema. |
| **Scanner de bancada** | Digitaliza modelos físicos para utilização em projetos digitais. | Deve ser registrado e ter suas manutenções controladas. |
| **Impressora 3D odontológica** | Produz modelos, guias, placas e outras peças a partir de arquivos digitais. | Deve possuir controle de manutenção, materiais utilizados e status de funcionamento. |
| **Fresadora CAD/CAM** | Produz peças odontológicas a partir de projetos digitais. | Só pode ser utilizada quando estiver disponível e em condições adequadas de funcionamento. |
| **Forno de sinterização** | Realiza o processamento de determinados materiais utilizados na fabricação de próteses. | Deve possuir controle de manutenção e temperatura de operação. |
| **Forno para cerâmica** | Utilizado no processamento e acabamento de materiais cerâmicos. | Deve ser utilizado por profissional autorizado e possuir manutenção registrada. |
| **Polimerizadora** | Realiza a polimerização de materiais utilizados na produção odontológica. | Deve estar cadastrada e ter manutenção preventiva controlada. |
| **Jateadora** | Realiza tratamento e acabamento da superfície de peças odontológicas. | Deve ser utilizada por profissional autorizado e permanecer em condições adequadas de uso. |
| **Polidora** | Realiza o acabamento e polimento de próteses e peças odontológicas. | Deve possuir controle de manutenção e limpeza periódica. |
| **Fotopolimerizador** | Utilizado para endurecer materiais odontológicos por meio de luz. | Deve ser verificado periodicamente e ter seu funcionamento registrado. |
| **Autoclave** | Utilizada para esterilização de instrumentos odontológicos. | Deve possuir controle de manutenção e ciclos de esterilização. |
| **Aparelho de raio-X** | Utilizado para obtenção de imagens radiográficas odontológicas. | Deve ser utilizado por profissional autorizado e possuir manutenção e controle periódico. |
| **Compressor de ar** | Fornece ar comprimido para equipamentos odontológicos. | Deve possuir manutenção preventiva para garantir o funcionamento dos equipamentos conectados. |
| **Ultrassom odontológico** | Utilizado principalmente para procedimentos de limpeza e remoção de tártaro. | Deve ser cadastrado e passar por manutenção quando necessário. |
| **Jato de bicarbonato** | Utilizado para limpeza e remoção de resíduos da superfície dentária. | Deve possuir controle de limpeza, manutenção e abastecimento de material. |
| **Micromotor odontológico** | Equipamento utilizado em procedimentos e trabalhos de laboratório odontológico. | Deve ser cadastrado e ter seu histórico de manutenção atualizado. |
| **Caneta de alta rotação** | Instrumento rotatório utilizado em procedimentos odontológicos. | Deve ser esterilizada após o uso e possuir manutenção quando necessário. |
| **Caneta de baixa rotação** | Instrumento utilizado para procedimentos que necessitam de menor velocidade. | Deve ser higienizada e esterilizada conforme os procedimentos da clínica. |
| **Câmera intraoral** | Permite registrar imagens da cavidade bucal para auxiliar no diagnóstico e acompanhamento. | Deve estar cadastrada e disponível para utilização nos atendimentos. |
| **Computador de planejamento CAD** | Utilizado para criar e ajustar digitalmente modelos e próteses odontológicas. | Deve possuir acesso autorizado e armazenar os projetos de forma organizada. |

---

### Estrutura dos Atributos da Entidade `EQUIPAMENTO`

| Atributo | Descrição | Regra de Negócio |
| :--- | :--- | :--- |
| `id\_equipamento` | Identificação única do equipamento | Chave Primária, Único e Obrigatório |
| `nome\_equipamento` | Nome do aparelho | Obrigatório |
| `tipo\_equipamento` | Categoria do aparelho | Obrigatório |
| `numero\_serie` | Identificação fornecida pelo fabricante | Deve ser único |
| `data\_aquisicao` | Data em que o item foi adquirido | Obrigatória |
| `status` | Situação atual do aparelho | Valores permitidos: Disponível, Manutenção, Inativo ou Em uso |
| `localizacao` | Local onde está instalado na clínica | Deve ser informado |
| `responsavel` | Funcionário responsável pelo equipamento | Deve estar cadastrado previamente |
| `ultima\_manutencao` | Data da última manutenção realizada | Atualizada automaticamente após cada manutenção |
| `proxima\_manutencao` | Data prevista para a próxima intervenção | Utilizada para controle preventivo |

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

- **Entidades reconhecidas:**
  - **Equipamento:** Representa os equipamentos/aparelhos da clínica, permitindo controlar sua situação, localização e aquisição.
  - **Manutenção:** Registra as manutenções preventivas/corretivas realizadas nos equipamentos e mantém seu histórico.
  - **Estoque:** Controla peças, suprimentos e materiais disponíveis na clínica.
  - **Produção:** Registra os produtos, próteses e equipamentos fabricados internamente.
  - **Consultório:** Representa os ambientes físicos onde os equipamentos estão instalados e utilizados.
  - **Funcionário:** Representa os colaboradores envolvidos na operação, responsáveis por equipamentos, manutenções e produções.

- **Relacionamentos e Cardinalidades:**
  - **Consultório — Equipamento (1:N):** Um Consultório pode possuir vários Equipamentos, mas cada equipamento está localizado em um único consultório por vez.
  - **Equipamento — Manutenção (1:N):** Um Equipamento pode ter várias Manutenções registradas ao longo do tempo, mas cada manutenção pertence a um único equipamento.
  - **Funcionário — Manutenção (1:N):** Um Funcionário pode realizar ou registrar várias Manutenções, enquanto cada manutenção possui um único funcionário responsável.
  - **Funcionário — Equipamento (1:N):** Um Funcionário pode ser responsável por vários Equipamentos, mas cada equipamento tem um único funcionário responsável.
  - **Estoque — Produção (N:N):** Uma Produção pode utilizar diversos itens do Estoque, e um item do Estoque pode ser utilizado em diferentes produções. *(Nota: Na modelagem lógica futura, este relacionamento N:N será transformado na entidade associativa ITEM_PRODUÇÃO)*.

---

## 8. Justificativa Técnica
**A modelagem conceitual foi desenvolvida com base nas necessidades operacionais reais mapeadas na Odontologia Sasaki: controle de equipamentos, manutenção, estoque e produção interna. A entidade Equipamento assume papel central no modelo, garantindo o rastreamento dos ativos da clínica e evitando a dispersão de informações que antes ocorria em anotações soltas.
A criação da entidade Manutenção de forma separada permite o armazenamento do histórico ilimitado de reparos sem poluir os dados do equipamento, assegurando o acompanhamento da sua vida útil e a programação preventiva.
A separação entre Equipamento, Consultório e Funcionário evita a duplicidade de dados e padroniza a gestão de responsabilidade e localização física dos ativos. Por sua vez, a inclusão das entidades Estoque e Produção resolve o problema de rastreabilidade de insumos utilizados na fabricação interna de próteses, peças em 3D e implantes.
As cardinalidades refletem fielmente o funcionamento cotidiano da clínica, permitindo escalabilidade e facilidade de manutenção para as fases futuras de modelagem lógica e física do banco de dados.**

---

## 9. Uso de Inteligência Artificial

Durante o desenvolvimento do projeto, o grupo utilizou ferramentas de Inteligência Artificial como **apoio às atividades**, principalmente para organização de ideias, revisão, aprimoramento do material e organização do código. A IA não foi utilizada para substituir a análise e as decisões do grupo. As respostas geradas foram analisadas, adaptadas e, quando necessário, corrigidas pelos integrantes.

### 9.1 ChatGPT

| Item | Registro |
|------|----------|
| **Ferramenta e etapa** | **ChatGPT** — utilizado durante a organização das ideias, definição da estrutura da organização, levantamento dos processos de negócio, requisitos do sistema, regras de negócio e organização preliminar das entidades e atributos do banco de dados. |
| **Motivação** | Utilizar a IA como apoio para organizar as informações levantadas pelo grupo, sugerir possibilidades de estruturação e auxiliar na identificação de elementos que poderiam fazer parte do sistema. |
| **Prompt(s) utilizados** | "Crie uma clínica com o nome Odontologia Sasaki e desenvolva informações sobre seu contexto, porte, problemas e necessidades relacionadas ao controle de equipamentos." Também foram utilizados prompts para estruturar processos, requisitos, regras de negócio, dicionário de dados e entidades do sistema. |
| **Resposta recebida** | A IA apresentou sugestões de processos, equipamentos, requisitos, regras de negócio, entidades, atributos e relacionamentos que poderiam ser utilizados como ponto de partida para o projeto. |
| **Fontes consultadas e verificadas** | As sugestões foram analisadas pelo grupo e comparadas com as informações definidas para a organização e com os conhecimentos obtidos durante o desenvolvimento do projeto. Informações técnicas sobre equipamentos odontológicos foram pesquisadas e verificadas antes de serem utilizadas. |
| **Trechos rejeitados ou corrigidos** | Algumas sugestões foram modificadas ou descartadas por serem muito genéricas, não representarem a realidade definida para a Odontologia Sasaki ou adicionarem funcionalidades que não faziam parte do objetivo principal do projeto. |
| **Justificativa da escolha final** | O grupo manteve apenas as sugestões consideradas coerentes com o problema identificado. As decisões finais sobre processos, entidades, atributos e regras de negócio foram discutidas e definidas pelos integrantes do grupo. |
| **Reflexão crítica** | A IA pode apresentar respostas genéricas, informações incompletas ou sugestões que não correspondem exatamente à realidade da organização. Por isso, o grupo utilizou a ferramenta como apoio e não como fonte única de decisão. As respostas foram avaliadas criticamente antes de serem incorporadas ao projeto. |

### 9.2 Claude

| Item | Registro |
|------|----------|
| **Ferramenta e etapa** | **Claude** — utilizado na etapa de organização e harmonização do código desenvolvido para o projeto e preparado para publicação no GitHub. |
| **Motivação** | Auxiliar na padronização e organização do código, buscando melhorar sua estrutura, legibilidade e consistência antes da disponibilização no repositório do grupo. |
| **Prompt(s) utilizados** | Foram realizados pedidos para analisar e harmonizar a estrutura do código, mantendo sua funcionalidade e deixando sua organização mais consistente para utilização no GitHub. |
| **Resposta recebida** | O Claude apresentou sugestões de organização, padronização e ajustes no código. |
| **Fontes consultadas e verificadas** | O código sugerido foi analisado pelos integrantes e comparado com a versão desenvolvida pelo grupo antes da utilização. |
| **Trechos rejeitados ou corrigidos** | Alterações que poderiam modificar a lógica ou o funcionamento esperado do projeto foram revisadas e, quando necessário, descartadas ou modificadas pelo grupo. |
| **Justificativa da escolha final** | Foram aplicadas somente as alterações consideradas adequadas para melhorar a organização e a apresentação do código, preservando a lógica desenvolvida pelos integrantes. |
| **Reflexão crítica** | O uso do Claude foi considerado uma ferramenta de apoio à organização do código. A ferramenta não substituiu o conhecimento dos integrantes sobre o funcionamento do projeto, e todas as alterações foram revisadas antes de serem utilizadas no GitHub. |

### 9.3 Reflexão Geral sobre o Uso de IA

O grupo entende a Inteligência Artificial como uma **ferramenta de apoio ao desenvolvimento**, e não como substituta do conhecimento ou das decisões dos integrantes.

A IA foi utilizada para auxiliar na organização de informações, geração de possibilidades, revisão, melhoria do material e harmonização do código. As decisões finais foram tomadas pelo próprio grupo, considerando os objetivos do projeto e as necessidades identificadas para a **Odontologia Sasaki**.

Dessa forma, a utilização da IA contribuiu para o desenvolvimento do trabalho sem substituir a participação, análise crítica e aprendizado dos estudantes.

