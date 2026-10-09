# Macadamia Coletor

Coletor de telemetria para Le Mans Ultimate, com interface Windows e overlays. Este repositório distribui documentação e versões compiladas. O acesso ao serviço está restrito a convidados aprovados na pré-alpha.

## Instalação e migração para produção

1. Feche o coletor e baixe **Macadamia-Setup-0.2.2.exe** nas [versões oficiais](https://github.com/DaviMarino/macadamia-coletor/releases/tag/v0.2.2).
2. Execute o instalador sobre a instalação atual para atualizar o aplicativo, o helper e os atalhos.
3. Abra Macadamia e entre com a mesma conta Steam utilizada em [macadamia.racing](https://macadamia.racing). Aceite os termos no site e aguarde aprovação se necessário.
4. Mantenha o coletor aberto durante uma sessão do LMU. Novas capturas usam Parquet e sincronizam com o site. Corridas com menos de cinco minutos podem exigir Sincronizar agora.

Windows x64 e Microsoft Edge WebView2 são necessários. O login acontece no navegador externo; o coletor nunca pede sua senha Steam. Credenciais locais são protegidas por DPAPI. Ao migrar do servidor local para produção, um novo login é esperado. Sessões locais antigas não são transferidas automaticamente.

O instalador funciona por usuário. Dados e configurações ficam fora da instalação e são preservados na desinstalação. Para desinstalar, use Aplicativos instalados nas Configurações do Windows.

## Atualizações

O ZIP é o pacote interno do atualizador. Para migrar instalações antigas à 0.2.2, use o novo Setup: o ZIP sozinho não troca helper/atalhos e um helper antigo pode continuar encaminhando o endereço do servidor local.

O manifesto updates/version.json é assinado com Ed25519 e vincula o pacote ao tamanho e SHA256. Falha de verificação bloqueia o modo conectado. O canal atual tem validade limitada e exige renovação do manifesto pelo responsável. A assinatura do manifesto não é assinatura Authenticode; os executáveis ainda não possuem assinatura digital Windows.

## Pré-alpha e suporte

Validação da distribuição atual, login nativo e captura/envio em produção ainda em andamento. Overlays 2D dependem de janela ou borderless; VR utiliza [OpenKneeboard](https://openkneeboard.com/). Convidados podem falar diretamente com o responsável.

[Termos](https://macadamia.racing/terms) e [Privacidade](https://macadamia.racing/privacy) estão disponíveis no site. Não publique senhas, tokens, arquivos .env, telemetria ou logs brutos em issues.
