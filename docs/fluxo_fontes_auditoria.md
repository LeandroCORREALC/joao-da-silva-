# Fluxo de fontes e auditoria

1. **Entrada restrita:** o relato original fica em `ENTRADA/relato_bruto.md`; não enviar esse arquivo à IA.
2. **Sanitização:** preparar `APOIO/caso_sanitizado.md`, removendo identificadores e mantendo apenas os fatos necessários. CPF, endereço, telefone e número do pedido são proibidos na consulta.
3. **Seleção de fontes:** consultar apenas os arquivos listados em `docs/propts/consulta_rag.md`. `APOIO/fonte_1.md` contextualiza os dados selecionados da compra; `APOIO/fonte_2.md` contém o excerto normativo. Registrar a finalidade e os limites de cada fonte em `evidencias/verificacao.md`.
4. **Resposta rastreável:** para cada afirmação relevante, indicar arquivo e trecho. Separar fato relatado, conteúdo da fonte e inferência; apontar lacunas sem completá-las por suposição. Registrar prompt e arquivos consultados em `evidencias/resposta_inicial.md`.
5. **Auditoria independente:** usar `docs/propts/auditoria.md` para verificar suporte, citações, extrapolações, sigilo e limites. Registrar evidência, motivo, correção e status em `evidencias/auditoria.md`.
6. **Revisão humana:** resolver alertas ou documentar pendências em `evidencias/revisao_humana.md`. Não tratar a resposta como orientação profissional final antes da validação responsável.
7. **Entrega:** publicar somente a orientação revisada em `ENTREGA/Orientacao_inicial.md`; manter a trilha documental nas pastas `evidencias/`.

## Critério de rastreabilidade
Toda conclusão deve apontar para a fonte que a sustenta. Se a fonte ou os fatos não bastarem, declarar a lacuna e indicar o que precisa ser conferido. Trechos normativos devem ter sua versão conferida em fonte oficial antes de uso profissional.
