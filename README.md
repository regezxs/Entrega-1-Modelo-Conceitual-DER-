<!-- CABEÇALHO DOURADO -->
<div align="center" style="background: linear-gradient(135deg, #1e1e1e 0%, #2d2a26 100%); padding: 30px; border-bottom: 4px solid #c5a059; border-radius: 8px;">

# <span style="color: #c5a059;">Entrega 1 — Modelo Conceitual (DER)</span>
### <span style="color: #ffffff;">Modelagem de um Sistema de Gestão para a Odontologia Sasaki</span>

</div>

<br>

> 🎓 **Integrantes do Grupo**
> - **Letícia Valentim Reges** — RGM: `047369680`
> - **[Nome do Aluno 2]** — RGM: `[RGM do Aluno 2]`

---

## 🏛️ 1. Caracterização da Organização

| Campo | Detalhes |
| :--- | :--- |
| **Nome e Natureza** | **Odontologia Sasaki**, uma clínica odontológica privada de médio porte, com fins lucrativos. |
| **Contexto e Porte** | ~20 funcionários (dentistas, auxiliares, técnicos, recepcionistas, manutenção). ~500 atendimentos/mês. Possui setor de produção própria (implantes, aparelhos ortodônticos, impressão 3D) e parque tecnológico distribuído. |
| **Problemas Identificados** | Informações descentralizadas em planilhas e anotações. Dificuldade no acompanhamento da localização, situação operacional, histórico de manutenção e estoque de peças/insumos. |
| **Justificativa** | O alto volume de equipamentos e processos fabris internos torna a clínica o cenário ideal para estruturação de um banco de dados relacional. |

### 📍 Evidências da Organização
* **Endereço:** R. Jardim Tamoio, 1089 - Conj. Res. José Bonifácio, São Paulo - SP, 08255-010
* **Google Maps:** [Acessar localização no Google Maps](https://maps.app.goo.gl/ALuZBqSGNaq6kBxy9)
* **Contato:** `Luduque@hotmail.com` | `+55 11 99001-2968`

---

## 🔄 2. Processos de Negócio

1. **Cadastro e Controle de Equipamentos:** Registro individual, localização, responsável e situação atual.
2. **Controle de Manutenção:** Registro de manutenções preventivas e corretivas, histórico de falhas e serviços executados.
3. **Controle de Estoque:** Gestão de entradas e saídas de peças, materiais e componentes do setor técnico/fabril.
4. **Produção Interna:** Registro da fabricação de implantes, aparelhos ortodônticos e impressões 3D.
5. **Controle de Consultórios:** Acompanhamento e inventário dos equipamentos instalados em cada ambiente.

---

## 🎯 3. Requisitos do Sistema

### ⚙️ 3.1 Requisitos Funcionais
- [x] Cadastrar, alterar e consultar equipamentos.
- [x] Registrar a localização física e o funcionário responsável.
- [x] Registrar manutenções preventivas e corretivas.
- [x] Permitir consulta ao histórico operacional completo.
- [x] Controlar movimentações (entrada/saída) de estoque.
- [x] Registrar equipamentos e peças produzidos internamente.
- [x] Informar status em tempo real *(Disponível, Em Manutenção, Inativo, Em uso)*.
- [x] Mapear o inventário individual por consultório.

### 🛡️ 3.2 Requisitos Não Funcionais
* **Segurança:** Autenticação obrigatória para acesso às funcionalidades.
* **Usabilidade:** Interface intuitiva e de fácil operação no dia a dia.
* **Desempenho:** Respostas e consultas otimizadas.
* **Disponibilidade:** Acesso contínuo para suporte às rotinas operacionais.
* **Integridade:** Consistência nos dados, evitando inconsistências e duplicidades.

---



</div>
