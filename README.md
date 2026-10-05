# Macadamia Coletor

Coletor de telemetria para Le Mans Ultimate, com interface Windows e overlays 2D/VR. Este repositório público distribui documentação e versões compiladas; não contém o código-fonte do coletor ou do backend.

## Pré-alpha de teste local

A versão 0.2.0 é destinada à validação pelo desenvolvedor. Login Steam ainda depende do backend Macadamia em localhost; não há backend público nem sincronização de telemetria. Não é uma versão pronta para uso comunitário sem essa infraestrutura.

- [Versões e downloads](https://github.com/DaviMarino/macadamia-coletor/releases)
- Windows x64 com WebView2 instalado.
- Instalador por usuário, ícone e atalhos Macadamia.
- Verificação de versão via manifesto assinado no GitHub.
- Login Steam no navegador externo; nome/avatar e credenciais individuais.
- Coleta automática após login e versão válida, a 30 Hz ou 50 Hz.
- SQLite local ou exportação Parquet; sessões sem envio são preservadas.
- Overlays originais de pedais/volante e comparação de setores.
- VR depende do [OpenKneeboard](https://openkneeboard.com/).

## Instalação de teste

Baixe Macadamia-Setup-0.2.0.exe em Releases. Feche o coletor antes de instalar. Instalação fica no perfil Windows; dados e credenciais ficam fora da instalação e são preservados na desinstalação.

Mantenha o backend local ativo para login Steam. Depois use o atalho Macadamia. Para diagnóstico sem backend, execute macadamia.exe --local na pasta app da instalação. O modo --local é manual e não representa a experiência final.

## Atualizações e limites

updates/version.json identifica versão, pacote, tamanho e hash com assinatura Ed25519. Pacotes de atualização ficam em Releases. O updater valida os arquivos e substitui apenas o app, preservando dados. Falhas de verificação bloqueiam o modo conectado. Manifesto do canal de desenvolvimento tem validade limitada e precisa ser renovado pelo responsável.

Ainda pendentes: validação do instalador/updater real, assinatura digital Windows, hospedagem pública do backend, sincronização/analytics e testes em máquina sem Python/Node. Fullscreen exclusivo não exibe overlays 2D; use janela ou borderless.

Não publique senhas, tokens, .env, dados de pilotos ou logs brutos em issues. Futuras condições de uso/privacidade serão definidas antes da disponibilização pública do serviço. Coach e monetização não fazem parte desta versão.
