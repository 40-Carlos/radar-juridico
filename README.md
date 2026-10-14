# Radar Jurídico — Direito em Foco

Site estático (HTML) com notícias oficiais do Superior Tribunal de Justiça atualizadas automaticamente por RSS.

## Publicação gratuita no GitHub Pages

1. Crie um repositório **público** chamado `radar-juridico` no GitHub.
2. Envie **todo o conteúdo desta pasta**, incluindo a pasta oculta `.github/workflows`, para a raiz da branch `main`.
3. Em **Settings > Pages**, selecione **Deploy from a branch**, `main`, `/ (root)` e salve.
4. Seu endereço será `https://SEU-USUARIO.github.io/radar-juridico/` depois da publicação.
5. Em **Actions > Atualizar notícias jurídicas > Run workflow**, execute uma atualização inicial para gerar `noticias.json` com notícias reais.
6. O fluxo tentará atualizar diariamente às **07h15, horário de Belém**; o GitHub não garante execução no minuto exato.

O fluxo recebe dados somente do RSS oficial do STJ. O site exibe **título, data, resumo e link** da publicação, sem gerar análises automáticas por IA nem afirmar que matéria jornalística tem força de precedente. Se os feeds falharem, notícias antigas são preservadas.

**Atenção:** o agendamento das 7h feito no ChatGPT é independente desta automação do site. O site não será alimentado automaticamente pelo texto do ChatGPT; notícias RSS e boletins interpretativos são produtos distintos.

Para testar localmente: execute `python -m http.server 8000` nesta pasta e abra `http://localhost:8000`. Para buscar notícias agora, execute `python scripts/update_feed.py` em uma máquina com internet.
