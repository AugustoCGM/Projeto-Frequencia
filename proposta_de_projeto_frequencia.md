# Proposta de Arquitetura e Implementação: Sistema Inteligente de Frequência Escolar

**Instituição:** UNINASSAU - Campina Grande  
**Disciplina:** Extensão  
**Equipe Desenvolvedora:** Augusto César, Arthur Vinícius, Joab Pessoa, Michael, Derick e Ramon  
**Instituição Parceira:** Colégio Normal  

---

## 1. Visão Geral e Objetivo

O presente documento propõe uma adequação no escopo do Sistema Inteligente de Controle e Acompanhamento da Frequência Escolar. O objetivo central permanece o mesmo: automatizar e otimizar o registro de presenças. Contudo, a abordagem técnica foi refinada para garantir que o sistema seja democrático, viável e condizente com a realidade socioeconômica e institucional do Colégio Normal.

## 2. Análise Crítica do Modelo Baseado em QR Code (Dispositivo do Aluno)

A proposta inicial sugeria a geração diária de QR Codes dinâmicos nos celulares dos alunos para leitura pelos professores. Embora inovadora, essa abordagem apresenta barreiras críticas de implantação em escolas públicas:

- **Barreira Socioeconômica:** Exige que os alunos possuam smartphones com acesso à internet, o que exclui alunos em situação de vulnerabilidade.
- **Atrito Institucional:** Vai de encontro às diretrizes pedagógicas que desencorajam ou proíbem o uso de aparelhos celulares por alunos dentro da sala de aula.
- **Inviabilidade Prática:** O custo e a infraestrutura exigida para que a solução funcione na totalidade da escola fogem do escopo de um projeto de extensão de baixo orçamento.

## 3. Solução Proposta: Modelo Híbrido Inclusivo (Dispositivo do Professor)

Para que a tecnologia cumpra seu papel social sem gerar segregação, propomos transferir o ônus tecnológico para a escola e para os docentes, removendo qualquer exigência de hardware por parte do aluno. O sistema será construído com **duas frentes operacionais**:

### Rota A: Chamada Digital Dinâmica (Foco Principal)
- **Como funciona:** O professor acessa a plataforma via smartphone ou tablet, visualiza a lista da turma e registra a presença/falta através de caixas de seleção (*checkboxes*).
- **Vantagens:** Adoção imediata, custo zero de implantação, e não depende de recursos avançados nos aparelhos dos docentes.
- **Integração Governamental:** Os dados são enviados para o dashboard da secretaria já formatados via API para consumo pelo programa **Pé de Meia**.

### Rota B: Validação por NFC (Piloto Experimental)
- **Como funciona:** Uso de cartões físicos com chips NFC. O aluno apresenta o cartão escolar, e o professor (cujo aparelho possua leitor NFC) apenas aproxima o celular para contabilizar a presença.
- **Fase de Testes:** Propõe-se a aquisição de um lote reduzido (aproximadamente 10 cartões) subsidiado pela faculdade para testar o fluxo em uma turma reduzida e controlada.
- **Objetivo:** Validar a automação sem tornar o sistema dependente dela. Caso o celular de um professor não tenha NFC ou haja problemas com os cartões, o fluxo retorna naturalmente à *Rota A*.

## 4. Gestão de Dados e Escalabilidade Comercial

- **Centralização e Segurança:** A secretaria escolar atua como guardiã central dos dados, responsável por cadastros e acompanhamento de indicadores.
- **Arquitetura Integrável:** O sistema nasce independente, porém estruturado para se acoplar nativamente a sistemas educacionais maiores, unindo plataformas sem perder a autonomia.

## 5. Próximos Passos

1. **Apresentação Acadêmica:** Levar esta proposta à coordenação e professora responsável para alinhamento e solicitação da verba simbólica das tags NFC.
2. **Desenvolvimento e Teste:** Iniciar a criação do MVP e aplicar o teste prático na turma reduzida do Colégio Normal.
3. **Expansão Comercial:** Após validação do modelo, mapear redes particulares da região de Campina Grande (como o Colégio Motiva, que já possui cultura de uso de cartões na portaria) para oferecer o sistema como produto de automação de acesso, buscando captação de clientes/patrocínio.
