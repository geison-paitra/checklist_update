# Checklist Oracle - verificação de atualização

Este repositório publica o arquivo de metadados usado pelo Checklist Oracle Portable para **informar** quando existe uma versão mais nova. O aplicativo não baixa nem instala atualizações automaticamente.

## Arquivo `update.json`

Campos principais:

- `latest_version`: versão mais recente publicada, por exemplo `2.1.2.1`.
- `importance`: use `normal` para atualização comum ou `important` para destacar que a atualização deve ser aplicada assim que possível.
- `title`: título exibido no aviso.
- `message`: mensagem adicional opcional exibida junto ao aviso.
- `published_at`: data de publicação.
- `details_url`: link opcional para mais informações.

## Mensagem personalizada

O objeto `announcement` pode exibir um comunicado mesmo quando não houver uma versão nova:

```json
"announcement": {
  "enabled": true,
  "id": "2026-09-18-01",
  "title": "Aviso",
  "message": "Mensagem personalizada."
}
```

Para remover o comunicado, altere `enabled` para `false`.

O campo `id` deve ser alterado sempre que o comunicado mudar.
