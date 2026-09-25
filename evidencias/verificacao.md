# Verificacao do fluxo de fontes e auditoria

## Caso
Caso ficticio sobre celular com defeito, com orientacao inicial destinada a equipe do escritorio.

## 1. Triagem e sanitizacao
- Entrada consultada: `ENTRADA/relato_bruto.md`.
- Base sanitizada encaminhada para a consulta: `APOIO/caso_sanitizado.md`.
- Dados excluidos da consulta: CPF, endereco, telefone e numero do pedido.
- Regra aplicada: usar somente o caso sanitizado e as fontes armazenadas em `APOIO/`.

## 2. Mapa de fontes
| Fonte | Finalidade | Limite de uso |
|---|---|---|
| `APOIO/caso_sanitizado.md` | Registrar os fatos iniciais do defeito e a pergunta de trabalho. | Nao comprova fatos alem do relato apresentado. |
| `APOIO/fonte_1.md` | Contextualizar a compra e o valor informado. | Nao contem identificacao pessoal nem prova outros eventos. |
| `APOIO/fonte_2.md` | Conferir o art. 18, § 1º, do CDC e as alternativas mencionadas. | Nao permite concluir o direito sem conferir fatos, prazo e demais requisitos. |

## 3. Consulta
- Prompt aplicado: `docs/propts/consulta_rag.md`.
- Arquivos enviados: caso sanitizado, nota fiscal e trecho do art. 18 do CDC.
- Resultado registrado em: `evidencias/resposta_inicial.md`.
- Regra de citacao atendida: a resposta indicou `trecho_cdc_art18.md` e o art. 18, § 1º.

## 4. Auditoria
- Prompt aplicado: `docs/propts/auditoria.md`.
- Auditoria registrada em: `evidencias/auditoria.md`.
- Achado ALERTA: a formulacao sobre restituição imediata era categorica e exigia conferencia dos fatos e do prazo.
- Achado OK: nao foram encontrados dados pessoais no caso sanitizado.
- Correcao: substituir a conclusao categorica por orientacao condicional.

## 5. Revisao humana
- Registro: `evidencias/revisao_humana.md`.
- Decisao: corrigir o Achado 1.
- Justificativa: a fonte normativa nao sustenta conclusao sem a ressalva sobre os fatos comprovados.

## 6. Resultado e pendencias
- A orientacao inicial em `ENTREGA/Orientacao_inicial.md` declara suas fontes e limites.
- Nao ha conclusao individual nem exposicao dos dados proibidos.
- Pendencias: conferir documentos do caso, datas do reparo e a versao final do trecho normativo antes de qualquer uso profissional.
- Responsavel pela validacao final: revisao humana responsavel pelo escritorio.
