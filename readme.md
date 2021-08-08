# DLM Lifecycle Policy

Você pode usar o Amazon Data Lifecycle Manager para automatizar a criação, retenção e exclusão de snapshots EBS e AMIs apoiados por EBS. Quando você automatiza o gerenciamento de instantâneos e AMI, isso o ajuda a:

- Proteja dados valiosos, impondo uma programação de backup regular.
- Crie AMIs padronizados que podem ser atualizados em intervalos regulares.
- Reter backups conforme exigido pelos auditores ou conformidade interna.
- Reduza os custos de armazenamento, excluindo backups desatualizados.
- Crie políticas de backup de recuperação de desastres que façam backup de dados em contas isoladas.

Adicione a Tag Snapshot-Daily:Yes para que o backup ocorra.  

[AWS Lifecycle Docs for more information](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html])

## AWSDataLifecycleManagerDefaultRole

Some accounts will require the creation of the default role:

```bash
aws dlm create-default-role --resource-type image --profile \<profile>
```

- https://docs.aws.amazon.com/cli/latest/reference/dlm/create-default-role.html
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html