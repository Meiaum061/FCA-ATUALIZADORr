# Publicar Retifoz 1.0.1 no GitHub

Esta pasta contém o executável inicial para publicar no repositório de releases:

https://github.com/Meiaum061/FCA-ATUALIZADORr

## Criar a release

1. Abra a página **Releases** do repositório e escolha **Create a new release**.
2. Crie a tag `v1.0.1` e selecione a branch `main` como destino.
3. Use o título `Retifoz 1.0.1`.
4. Anexe somente o arquivo `retifoz.exe` desta pasta.
5. Publique como release estável, sem marcar como pre-release.

O GitHub calcula e disponibiliza o SHA-256 do arquivo enviado. O atualizador do
Retifoz valida esse hash antes de instalar qualquer executável.

## Importante

Este é o executável inicial com o código do atualizador. Como a versão dele é
`1.0.1`, ele não vai se atualizar pela própria release `v1.0.1`. Distribua
este executável aos usuários pelo método atual. Atualizações posteriores devem
usar versões maiores, por exemplo `v1.0.2`, para que o app as detecte e ofereça
a instalação automaticamente.

O workflow automático de build e publicação só será executado quando o arquivo
`.github/workflows/publicar-release.yml` estiver no repositório-fonte
`Meiaum061/retifoz` e o secret `RETIFOZ_RELEASE_TOKEN` estiver configurado nesse
repositório. Até lá, publique as releases manualmente.
