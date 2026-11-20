# code-backup-runner

Agendador de backup. Um workflow do GitHub Actions roda todo dia 06:00 UTC e
espelha (`git push --mirror`, histórico completo) os repositórios de código para
seus repositórios de backup separados:

- `matheusmmacedo/klaos` -> `matheusmmacedo/klaos-backup`
- `matheusmmacedo/frontdesk` -> `matheusmmacedo/frontdesk-backup`

O segredo `BACKUP_PAT` (token com acesso de leitura nas origens e escrita nos
backups) fica em Settings > Secrets and variables > Actions deste repositório.

Rodar sob demanda: aba Actions > "Espelho diario do codigo" > Run workflow.
