<!-- CABEÇALHO DOURADO -->
<div align="center" style="background: linear-gradient(135deg, #1e1e1e 0%, #2d2a26 100%); padding: 30px; border-bottom: 4px solid #c5a059; border-radius: 8px;">

# <span style="color: #c5a059;">Entrega 1 — Modelo Conceitual (DER)</span>
### <span style="color: #ffffff;">Modelagem de um Sistema de Gestão para a Odontologia Sasaki</span>

</div>

<br>

>  **Integrantes do Grupo**
> - **Letícia Valentim Reges** — RGM: `047369680`
> - **Juan Arthur Franco** — RGM: `47232099`
> - **Isadora Do Nascimento Takami** - RGM: `47108932`
> - **Pedro Cândido Pyramides Pinheiro** - RGM: `04669634`
---

##  1. Caracterização da Organização

| Campo | Detalhes |
| :--- | :--- |
| **Nome e Natureza** | **Odontologia Sasaki**, uma clínica odontológica privada de médio porte, com fins lucrativos. |
| **Contexto e Porte** | ~20 funcionários (dentistas, auxiliares, técnicos, recepcionistas, manutenção). ~500 atendimentos/mês. Possui setor de produção própria (implantes, aparelhos ortodônticos, impressão 3D) e parque tecnológico distribuído. |
| **Problemas Identificados** | Informações descentralizadas em planilhas e anotações. Dificuldade no acompanhamento da localização, situação operacional, histórico de manutenção e estoque de peças/insumos. |
| **Justificativa** | O alto volume de equipamentos e processos internos tornando a clínica o cenário ideal para estruturação de um banco de dados relacional. |

###  Evidências da Organização
* **Endereço:** R. Jardim Tamoio, 1089 - Conj. Res. José Bonifácio, São Paulo - SP, 08255-010
* **Google Maps:** [Acessar localização no Google Maps](https://maps.app.goo.gl/ALuZBqSGNaq6kBxy9)
* **Contato:** `Luduque@hotmail.com` | `+55 11 99001-2968`
<p align="center">
  <img src="IMG_0183.JPG" alt="Porta da Clínica" width="300">
  <img src="image (1).png" alt="Aluna Letícia com o Dr. Marcelo que mostrou os pontos de dores da clínica" width="300">
</p>

---

##  2. Processos de Negócio

1. **Cadastro e Controle de Equipamentos:** Registro individual, localização, responsável e situação atual.
2. **Controle de Manutenção:** Registro de manutenções preventivas e corretivas, histórico de falhas e serviços executados.
3. **Controle de Estoque:** Gestão de entradas e saídas de peças, materiais e componentes do setor técnico/fabril.
4. **Produção Interna:** Registro da fabricação de implantes, aparelhos ortodônticos e impressões 3D.
5. **Controle de Consultórios:** Acompanhamento e inventário dos equipamentos instalados em cada ambiente.

---

##  3. Requisitos do Sistema

###  3.1 Requisitos Funcionais
- [x] Cadastrar, alterar e consultar equipamentos.
- [x] Registrar a localização física e o funcionário responsável.
- [x] Registrar manutenções preventivas e corretivas.
- [x] Permitir consulta ao histórico operacional completo.
- [x] Controlar movimentações (entrada/saída) de estoque.
- [x] Registrar equipamentos e peças produzidos internamente.
- [x] Informar status em tempo real *(Disponível, Em Manutenção, Inativo, Em uso)*.
- [x] Mapear o inventário individual por consultório.

###  3.2 Requisitos Não Funcionais
* **Segurança:** Autenticação obrigatória para acesso às funcionalidades.
* **Usabilidade:** Interface intuitiva e de fácil operação no dia a dia.
* **Desempenho:** Respostas e consultas otimizadas.
* **Disponibilidade:** Acesso contínuo para suporte às rotinas operacionais.
* **Integridade:** Consistência nos dados, evitando inconsistências e duplicidades.

---
##  4. Regras de Negócio

###  Regras Operacionais
* **RN01:** Todo equipamento deve obrigatoriamente ter cadastro no sistema.
* **RN02:** Todo equipamento deve estar associado a um consultório ou localização física.
* **RN03:** Toda manutenção executada deve ser vinculada ao histórico do equipamento.
* **RN04:** Equipamentos com status `"Em Manutenção"` ficam bloqueados para uso.
* **RN05:** Toda saída de peças/materiais do estoque exige registro imediato.
* **RN06:** Qualquer lote de produção deve gerar uma ordem correspondente no sistema.

###  Restrições Organizacionais
> A atualização rigorosa do sistema previne o uso de equipamentos defeituosos, reduzindo paralisações nos atendimentos. O histórico centralizado permite acompanhar a vida útil dos aparelhos, planejar substituições preventivas e controlar custos operacionais.

---

##  5. Dicionário de Dados Conceitual (Preliminar)

###  Mapeamento do Parque Tecnológico (Equipamentos)

| Aparelho / Equipamento | Descrição | Regra de Negócio Associada |
| :--- | :--- | :--- |
| **Cadeira Odontológica** | Acomodação do paciente durante o atendimento. | Vinculada a um consultório. Manutenções registradas. |
| **Scanner Intraoral** | Captura digital da arcada dentária para modelos 3D. | Restrito a profissionais autorizados. |
| **Scanner de Bancada** | Digitalização de modelos físicos para projetos CAD. | Registro e manutenção controlados no sistema. |
| **Impressora 3D Odontológica** | Fabricação de modelos, guias e placas digitais. | Controle rigoroso de manutenção e insumos. |
| **Fresadora CAD/CAM** | Usinagem de peças a partir de projetos digitais. | Operação permitida apenas no status "Disponível". |
| **Forno de Sinterização** | Processamento térmico de materiais sintéticos. | Controle de ciclos e temperatura de operação. |
| **Forno para Cerâmica** | Acabamento de próteses cerâmicas. | Restrito a profissionais autorizados. |
| **Polimerizadora** | Polimerização de resinas e materiais odontológicos. | Requer manutenção preventiva regular. |
| **Jateadora / Polidora** | Tratamento de superfície, acabamento e polimento. | Manutenção e higienização periódicas. |
| **Autoclave** | Esterilização de instrumentos operacionais. | Controle de ciclos e revisões periódicas. |
| **Aparelho de Raio-X** | Obtenção de imagens radiográficas. | Inspeção técnica e manutenção preventiva obrigatórias. |
| **Compressor de Ar** | Fornecimento de ar comprimido aos consultórios. | Manutenção preventiva para evitar parada geral. |
| **Computador CAD** | Planejamento digital de próteses e implantes. | Acesso restrito e backup dos projetos digitais. |

<br>

### Estrutura da Entidade `EQUIPAMENTO` 
| Atributo | Descrição | Restrição / Regra |
| :--- | :--- | :--- |
| `id_equipamento` | Identificador único do equipamento | Chave Primária (PK), Obrigatório |
| `nome_equipamento` | Nome comercial do aparelho | Obrigatório |
| `tipo_equipamento` | Categoria/tipo do equipamento | Obrigatório |
| `numero_serie` | Número de série do fabricante | Único |
| `data_aquisicao` | Data de compra do ativo | Obrigatório |
| `status` | Situação operacional do ativo | *Disponível, Manutenção, Inativo,Em uso* |
| `localizacao` | Consultório ou sala onde está instalado | Informado obrigatoriamente |
| `responsavel` | Funcionário responsável pelo ativo | Cadastrado previamente |
| `ultima_manutencao` | Data da última intervenção técnica | Atualizado automaticamente |
| `proxima_manutencao` | Data prevista para próxima revisão | Controle Preventivo |
---

## 6. Modelagem Conceitual 
### Entidades Mapeadas 
* **`EQUIPAMENTO`**: Representa os ativos e aparelhos da clínica.
* **`MANUTENÇÃO`**: Registra as intervenções técnicas e histórico de reparos.
* **`ESTOQUE`**: Controla insumos, peças e componentes do setor técnico.
* **`PRODUÇÃO`**: Registra os itens/próteses fabricados internamente.
* **`CONSULTÓRIO`**: Ambientes físicos onde ficam alocados os equipamentos.
* **`FUNCIONÁRIO`**: Colaboradores envolvidos no uso, manutenção e gestão.

### Relacionamentos e Cardinalidades 
* **Consultório — Equipamento `(1:N)`:** Um consultório pode possuir vários
equipamentos; cada equipamento está instalado em um único consultório.
* **Equipamento — Manutenção `(1:N)`:** Um equipamento pode passar por várias
manutenções; cada manutenção pertence a um equipamento.
* **Funcionário — Manutenção `(1:N)`:** Um funcionário pode executar/registrar
várias manutenções; cada registro tem um responsável.
* **Funcionário — Equipamento `(1:N)`:** Um funcionário pode responder por
múltiplos equipamentos.
* **Estoque — Produção `(N:N)`:** Uma ordem de produção consome múltiplos itens
do estoque; cada item do estoque atende a várias produções. *(Nota: Na modelagem
lógica, este relacionamento será convertido na entidade associativa
`ITEM_PRODUÇÃO`)*.
---
## 7. **Modelo Entidade-Relacionamento (DER)**
<p align="center">
  <img src="DER.jpg" alt="Modelo entidade-Relacionamento" width="600">
</p>

O modelo foi desenvolvido para organizar as principais informações relacionadas à infraestrutura e aos processos internos da clínica, permitindo representar:

* Consultórios e seus equipamentos
* Equipamentos e seus responsáveis
* Histórico de manutenções
* Funcionários
* Controle de estoque
* Produções e próteses
* Utilização de itens do estoque nas produções

---

## Modelo no BRModelo

O modelo também pode ser visualizado diretamente no **BRModelo Web**:

<p align="center">

**[Visualizar modelo no BRModelo Web](https://app.brmodeloweb.com/publicview/6ab1f51fd4acd21f13d78167)**

</p>

---

# Entidades

O banco de dados é composto pelas seguintes entidades:

| Entidade              | Descrição                                                    |
| --------------------- | ------------------------------------------------------------ |
| **CONSULTÓRIO**    	| Representa os ambientes físicos da clínica                   |
| **EQUIPAMENTO**    	| Representa aparelhos e ativos utilizados pela clínica        |
| **FUNCIONÁRIO** 	| Representa os colaboradores responsáveis pelas atividades    |
| **MANUTENÇÃO**     	| Registra intervenções técnicas realizadas nos equipamentos   |
| **ESTOQUE**        	| Controla insumos, peças e materiais disponíveis              |
| **PRODUÇÃO**       	| Registra produtos, próteses ou itens fabricados internamente |
| **ITEM_PRODUÇÃO**  	| Entidade associativa entre estoque e produção                |

---

# CONSULTÓRIO

Representa os ambientes físicos onde os equipamentos da clínica estão instalados.

### Atributos

| Atributo           | Tipo    | Restrição   |
| ------------------ | ------- | ----------- |
| `id_consultorio`   | INT     |     PK	     |
| `nome_consultorio` | VARCHAR | Obrigatório |
| `numero_sala`      | VARCHAR | Único       |
| `andar`            | INT     | Opcional    |
| `status`           | VARCHAR | Obrigatório |

### Status possíveis

* Disponível
* Ocupado
* Manutenção
* Inativo

---

# EQUIPAMENTO

Representa os aparelhos e ativos utilizados pela clínica.

### Atributos

| Atributo             | Tipo    | Restrição           |
| -------------------- | ------- | ------------------- |
| `id_equipamento`     | INT     |    PK               |
| `nome_equipamento`   | VARCHAR | Obrigatório         |
| `tipo_equipamento`   | VARCHAR | Obrigatório         |
| `numero_serie`       | VARCHAR | Único               |
| `data_aquisicao`     | DATE    | Obrigatório         |
| `status`             | VARCHAR | Obrigatório         |
| `id_consultorio`     | INT     |    FK               |
| `id_funcionario`     | INT     |    FK               |
| `ultima_manutencao`  | DATE    | Automático          |
| `proxima_manutencao` | DATE    | Controle preventivo |

### Status possíveis

* Disponível
* Manutenção
* Inativo
* Em uso

---

#  FUNCIONÁRIO

Representa os colaboradores envolvidos no uso, manutenção e gerenciamento dos recursos da clínica.

### Atributos

| Atributo         | Tipo    | Restrição   |
| ---------------- | ------- | ----------- |
| `id_funcionario` | INT     | 	 PK        |
| `nome`           | VARCHAR | Obrigatório |
| `cpf`            | VARCHAR | Único       |
| `cargo`          | VARCHAR | Obrigatório |
| `telefone`       | VARCHAR | Opcional    |
| `email`          | VARCHAR | Único       |
| `data_admissao`  | DATE    | Obrigatório |
| `status`         | VARCHAR | Obrigatório |

---

# MANUTENÇÃO

Registra as intervenções técnicas realizadas nos equipamentos.

### Atributos

| Atributo          | Tipo    | Restrição   |
| ----------------- | ------- | ----------- |
| `id_manutencao`   | INT     |  PK         |
| `id_equipamento`  | INT     |  FK         |
| `id_funcionario`  | INT     |  FK         |
| `tipo_manutencao` | VARCHAR | Obrigatório |
| `data_manutencao` | DATE    | Obrigatório |
| `descricao`       | TEXT    | Obrigatório |
| `custo`           | DECIMAL | Opcional    |
| `observacao`      | TEXT    | Opcional    |

### Tipos de manutenção

* Preventiva
* Corretiva

---

# ESTOQUE

Responsável pelo controle dos insumos, peças, componentes e materiais utilizados pela clínica.

### Atributos

| Atributo         | Tipo    | Restrição   |
| ---------------- | ------- | ----------- |
| `id_item`        | INT     |    PK       |
| `nome_item`      | VARCHAR | Obrigatório |
| `tipo_item`      | VARCHAR | Obrigatório |
| `descricao`      | TEXT    | Opcional    |
| `quantidade`     | INT     | Obrigatório |
| `unidade_medida` | VARCHAR | Obrigatório |
| `estoque_minimo` | INT     | Obrigatório |
| `data_validade`  | DATE    | Opcional    |
| `localizacao`    | VARCHAR | Opcional    |
| `status`         | VARCHAR | Obrigatório |

### Status possíveis

* Disponível
* Baixo
* Esgotado
* Inativo

---

# PRODUÇÃO

Representa os produtos, próteses ou itens fabricados internamente pela clínica.

### Atributos

| Atributo         | Tipo    | Restrição   |
| ---------------- | ------- | ----------- |
| `id_producao`    | INT     |  PK         |
| `descricao`      | TEXT    | Obrigatório |
| `tipo_producao`  | VARCHAR | Obrigatório |
| `data_inicio`    | DATE    | Obrigatório |
| `data_conclusao` | DATE    | Opcional    |
| `quantidade`     | INT     | Obrigatório |
| `status`         | VARCHAR | Obrigatório |
| `id_funcionario` | INT     |  FK         |
| `observacao`     | TEXT    | Opcional    |

### Status possíveis

* Em produção
* Concluída
* Cancelada

---

# ITEM PRODUÇÃO

Entidade associativa responsável por representar o relacionamento **N:N entre ESTOQUE e PRODUÇÃO**.

Uma produção pode utilizar diversos itens do estoque, enquanto um mesmo item pode ser utilizado em diversas produções.

### Atributos

| Atributo               | Tipo    | Restrição     |
| ---------------------- | ------- | ------------- |
| `id_item`              | INT     |  	PK /  FK   |
| `id_producao`          | INT     |    PK /  FK   |
| `quantidade_utilizada` | INT     | Obrigatório   |
| `unidade_medida`       | VARCHAR | Obrigatório   |

### Chave primária composta

```text
PK = (id_item, id_producao)
```

---

# Relacionamentos

| Relacionamento                | Cardinalidade | Descrição                                                                             |
| ----------------------------- | ------------: | ------------------------------------------------------------------------------------- |
| **CONSULTÓRIO → EQUIPAMENTO** |           1:N | Um consultório pode possuir vários equipamentos                                       |
| **EQUIPAMENTO → MANUTENÇÃO**  |           1:N | Um equipamento pode possuir várias manutenções                                        |
| **FUNCIONÁRIO → MANUTENÇÃO**  |           1:N | Um funcionário pode realizar várias manutenções                                       |
| **FUNCIONÁRIO → EQUIPAMENTO** |           1:N | Um funcionário pode ser responsável por vários equipamentos                           |
| **FUNCIONÁRIO → PRODUÇÃO**    |           1:N | Um funcionário pode ser responsável por várias produções                              |
| **ESTOQUE ↔ PRODUÇÃO**        |           N:N | Uma produção pode utilizar vários itens e um item pode participar de várias produções |

---

# Regras de Negócio

### Equipamentos

* Cada equipamento possui um identificador único.
* O número de série não pode ser duplicado.
* Todo equipamento deve estar associado a um consultório.
* Todo equipamento possui um funcionário responsável.
* Um equipamento pode possuir vários registros de manutenção.
* As datas de manutenção permitem o controle preventivo dos equipamentos.

### Manutenções

* Cada manutenção está vinculada a exatamente um equipamento.
* Cada manutenção possui um funcionário responsável.
* Uma manutenção pode ser preventiva ou corretiva.
* O histórico de manutenção permite acompanhar intervenções realizadas.

### Estoque e Produção

* Uma produção pode consumir diversos itens do estoque.
* Um mesmo item do estoque pode ser utilizado em diversas produções.
* O relacionamento N:N é resolvido pela entidade associativa `ITEM_PRODUÇÃO`.
* A quantidade utilizada deve ser registrada para cada item em cada produção.
  
---
## 8. Justificativa Técnica 
> A modelagem conceitual foi estruturada especificamente para responder às
demandas operacionais da **Odontologia Sasaki**. A entidade **`EQUIPAMENTO`**
assume o papel central, organizando dados que antes ficavam dispersos.
>
> A criação da entidade **`MANUTENÇÃO`** de forma independente permite o
registro de um histórico ilimitado de intervenções sem poluir a tabela de
equipamentos. O desacoplamento de **`CONSULTÓRIO`** e **`FUNCIONÁRIO`** elimina
duplicidades de cadastro, enquanto as entidades **`ESTOQUE`** e **`PRODUÇÃO`**
garantem rastreabilidade aos insumos utilizados na fabricação de peças 3D e
próteses.
---
## 9. Uso de Inteligência Artificial 
A Inteligência Artificial foi utilizada estritamente como **ferramenta de
apoio** para organização, estruturação de ideias, revisão e padronização do
código. Todas as decisões técnicas e validações do negócio foram efetuadas pelo
grupo.
### 9.1 ChatGPT
* **Etapa:** Organização das ideias, levantamento inicial dos processos de
negócio, requisitos e estrutura do dicionário de dados.
* **Prompts:** *"Com base no pdf, organize os equipamentos e crie nomes para serem identificados no cód"*
* **Avaliação Crítica:** As sugestões genéricas foram revisadas e adaptadas à
realidade operacional da Odontologia Sasaki.
### 9.2 Claude
* **Etapa:** Harmonização do código, otimização da estrutura em Markdown/HTML e
padronização para exibição no GitHub.
* **Prompts:** Pedidos para analisar, harmonizar e estilizar o documento em tons
elegantes de dourado e branco.
* **Avaliação Crítica:** As alterações estéticas foram aprovadas preservando
100% do conteúdo conceitual e lógico desenvolvido.
---

<div align="center">
<span style="color:#c5a059; font-weight: bold;">Odontologia Sasaki ©
2026</span> • *Documentação do Projeto de Banco de Dados*
</div>


</div>
