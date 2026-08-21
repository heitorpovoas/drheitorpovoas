# Registros profissionais — Dr. Heitor Portella Póvoas Filho

Fonte primária: Certificados de Especialista emitidos pelo **CREMEB — Conselho Regional de
Medicina do Estado da Bahia**, gerados eletronicamente em 21/08/2026.
Autenticidade verificável em https://sistemas.cfm.org.br/validacao/ba

## Identificação

| Campo | Valor |
|---|---|
| Nome completo | HEITOR PORTELLA POVOAS FILHO |
| Nome de publicação | Dr. Heitor Póvoas |
| CRM | **CRM-BA 11.157** (nos certificados aparece como `11157`) |

## RQE — Registro de Qualificação de Especialista

### RQE 4384 — Cirurgia Geral
- Registrado em **04/05/2001**, livro nº 13, folha nº 4384
- Especialidade: CIRURGIA GERAL
- Chave de validação: `c6dfad8be958fba80dc0be27dda0f35dcc0e3750`

### RQE 9689 — Medicina Intensiva
- Registrado em **23/11/2010**, livro nº 28, folha nº 8
- Especialidade: MEDICINA INTENSIVA
- Chave de validação: `60b027b2ecc603daed31e65ce85a4f95de544f0b`
- Titulação pela AMIB

### RQE 23086 — Cirurgia Bariátrica
- Registrado em **27/02/2023**, livro nº 66, folha nº 28
- Especialidade: CIRURGIA GERAL – Cirurgia Bariátrica
- Chave de validação: `99669cedbf80e6ca81505d4c31f8ede9bf3f0ad6`

## Erro conhecido: "RQE 2308"

O número **2308** circulou por engano como sendo o RQE de bariátrica. **Está errado.**
O correto é **23086** (cinco dígitos).

Histórico:
- O `_config.yml` do blog sempre trouxe o valor correto (`RQE 23086 — Cirurgia Bariátrica e Metabólica`).
- O bloco de assinatura manual, presente nos posts a partir de 26/05/2026, trazia `RQE 2308`.
- Como o layout renderiza o rodapé a partir do `_config.yml` **e** os posts trazem bloco manual,
  os dois números apareciam na mesma página publicada.
- Corrigido em **21/08/2026** em 8 arquivos de `_posts/` via `sed -E 's/RQE 2308([^0-9])/RQE 23086\1/g'`.

Peças fora do repositório que também precisam de conferência quando forem reeditadas:
carrossel de bioimpedância (slide 10), materiais impressos, receituário, assinatura de e-mail,
perfis em redes sociais e diretórios médicos.

## Formatos de assinatura

**Completo (posts do blog, materiais longos):**
```
Dr. Heitor Póvoas
CRM-BA 11.157 · RQE 23086 (Cirurgia Bariátrica e Metabólica) · RQE 9689 (Medicina Intensiva)
BAROS — Cirurgia Bariátrica e Metabólica · Salvador, Bahia
```

**Compacto (carrossel, peças gráficas):**
```
CRM-BA 11.157 · RQE 23086 · RQE 9689
```

**Valores no `_config.yml` (`site.doctor`):**
```yaml
name: Dr. Heitor Póvoas
full_name: Dr. Heitor Portella Póvoas Filho
crm: CRM-BA 11.157
rqe_bariatrica: RQE 23086 — Cirurgia Bariátrica e Metabólica
rqe_cirurgia_geral: RQE 4384 — Cirurgia Geral
rqe_intensiva: RQE 9689 — Medicina Intensiva (AMIB)
whatsapp: "557130398282"
whatsapp_display: "(71) 3039-8282"
```

## Disclaimer regulatório padrão

Resolução CFM 2.336/2023 — publicidade médica:

> Conteúdo educativo publicado em conformidade com a Resolução CFM 2.336/2023. Este texto não
> substitui avaliação médica individual, não estabelece relação médico-paciente e não deve ser
> usado para autodiagnóstico ou automedicação.

Relacionada e relevante para temas de emagrecimento e hormônios: **Resolução CFM 2.333/2023**,
que veda prescrição de terapias hormonais com finalidade estética, de ganho de massa muscular
ou de melhora de desempenho esportivo.
