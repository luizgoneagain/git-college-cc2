# Catálogo de Licenças Open Source

As licenças de código aberto mais usadas no mundo real: o que cada uma faz, prós e contras.

## Antes de começar

Licença é o documento que diz o que os outros podem fazer com o seu código. Sem ela, o código continua protegido por direito autoral e ninguém pode copiar, modificar ou redistribuir legalmente. Repositório público no GitHub sem arquivo `LICENSE` não é código aberto, é apenas código visível.<br>
Uma licença só é oficialmente open source se for aprovada pela OSI(Open Source Initiative), organização que mantém a definição de código aberto. Existem mais de 200 licenças por aí, cerca de 80 aprovadas pela OSI, mas na prática só umas dez aparecem com frequência.<br>
Elas se dividem em dois grupos. As **permissivas** dizem "faça o que quiser, só me dê os créditos", e permitem que o resultado derivado seja fechado. As **copyleft** dizem "faça o que quiser, mas o que derivar disso continua aberto". O copyleft ainda pode ser forte, quando contamina o projeto inteiro (GPL, AGPL), ou fraco, quando só obriga a abrir as partes originais e modificadas (LGPL, MPL).<br>
Cada licença também tem um identificador curto no padrão SPDX(Software Package Data Exchange), como `MIT` ou `Apache-2.0`, que é o nome usado por ferramentas automáticas e pelo próprio GitHub.

## MIT

Permissiva. SPDX `MIT`. A mais popular do mundo com folga: em 2025 teve mais de 1,5 milhão de acessos na página oficial da OSI, contra 344 mil da segunda colocada. O texto inteiro cabe em um parágrafo e diz basicamente: use, copie, modifique, venda, faça o que quiser, apenas mantenha o aviso de copyright junto e não me responsabilize por nada.<br>
Prós: curtíssima e compreensível até para quem não é advogado, compatível com quase tudo (inclusive GPL) e adotada sem medo por qualquer empresa.<br>
Contras: não fala nada sobre patentes, o que deixa uma brecha jurídica em projetos grandes, e permite que alguém pegue seu código, feche e venda sem devolver nada.<br>
Usada por React, Vue.js, Ruby on Rails, .NET Core e Bootstrap.

## Apache License 2.0

Permissiva. SPDX `Apache-2.0`. Criada em 2004 pela Apache Software Foundation, é a MIT de terno e gravata: permite as mesmas coisas, mas adiciona regras explícitas. Exige que você indique quais arquivos modificou e preserve o arquivo `NOTICE`, se houver. Seu grande diferencial é a concessão explícita de patentes, com cláusula de retaliação: quem processa alguém por patente ligada ao projeto perde automaticamente a licença.<br>
Prós: proteção real contra guerras de patente, aceitação garantida em departamento jurídico corporativo e liberdade para usar em produto fechado.<br>
Contras: texto bem mais longo que o da MIT e incompatível com a GPL-2.0, o que impede misturar código Apache em projetos como o kernel do Linux.<br>
Usada por Android, Kubernetes, TensorFlow, Swift e Kafka.

## BSD 3-Clause

Permissiva. SPDX `BSD-3-Clause`. Nasceu na Universidade da Califórnia, Berkeley (BSD é Berkeley Software Distribution). É praticamente igual à MIT, com uma cláusula extra que proíbe usar o nome do autor ou da instituição para promover produtos derivados. Você pode usar o código, mas não pode dizer que seu produto é endossado por quem escreveu.<br>
Prós: protege a reputação e o nome do autor original, é simples e é a terceira licença mais consultada do mundo.<br>
Contras: ignora patentes, assim como a MIT, e a diferença prática para a MIT é tão pequena que gera dúvida na hora de escolher.<br>
Usada por Go, Django, NumPy e partes do FreeBSD.<br>

## BSD 2-Clause

Permissiva. SPDX `BSD-2-Clause`. É a BSD 3-Clause sem a cláusula de endosso. Sobram duas exigências: manter o aviso no código-fonte e na documentação das distribuições binárias. Funcionalmente equivale à MIT.<br>
Prós: mínima, sem burocracia e compatível com praticamente tudo.<br>
Contras: perde a proteção de nome da versão de três cláusulas, e sua existência ao lado de MIT, ISC e BSD-3 é exatamente o tipo de duplicação que a OSI tenta reduzir com seu projeto contra proliferação de licenças.<br>
Usada por FreeBSD e por bibliotecas antigas do ecossistema Unix.

## ISC

Permissiva. SPDX `ISC`. Criada pelo Internet Systems Consortium em 1995, é a menor licença séria que existe: uma BSD 2-Clause com a linguagem redundante removida. Juridicamente é considerada equivalente à MIT. Ficou popular por ser o padrão sugerido pelo npm(Node Package Manager) e pelo OpenBSD.<br>
Prós: texto tão enxuto que se lê em vinte segundos, e reconhecimento tanto da OSI quanto da FSF(Free Software Foundation).<br>
Contras: menos conhecida, o que às vezes gera perguntas desnecessárias do jurídico, e também não trata de patentes.<br>
Usada por OpenBSD e por boa parte dos pacotes Node.js.

## GPL-2.0

Copyleft forte. SPDX `GPL-2.0-only`. Criada em 1991 dentro do projeto GNU(GNU's Not Unix) de Richard Stallman, foi a licença que definiu o que é software livre para uma geração inteira. Se você distribui um programa que usa código GPL-2.0, precisa distribuir o código-fonte do seu programa inteiro sob a mesma licença. Detalhe importante: a obrigação só é acionada quando há distribuição, então usar internamente numa empresa não obriga a abrir nada. Curiosidade útil para este trabalho: o próprio Git é licenciado sob GPL-2.0.<br>
Prós: garante que as melhorias voltem para a comunidade, impede que empresas fechem e vendam seu trabalho sem contrapartida, e tem uma base instalada gigantesca.<br>
Contras: o efeito viral afasta empresas e reduz a adoção, não trata patentes explicitamente e é incompatível tanto com a Apache-2.0 quanto com a própria GPL-3.0.<br>
Usada por kernel do Linux, Git, WordPress e MySQL.

## GPL-3.0

Copyleft forte. SPDX `GPL-3.0-only`. Lançada em 2007 para corrigir problemas surgidos nos anos 2000. Mantém tudo da GPL-2.0 e acrescenta concessão explícita de patentes, compatibilidade com a Apache-2.0 e a cláusula anti-tivoização, que impede fabricantes de travar o hardware para que o usuário não consiga rodar sua própria versão modificada do software.<br>
Prós: fecha as brechas de patente e de hardware travado e protege melhor a liberdade do usuário final.<br>
Contras: texto longo e denso, adoção corporativa baixa (várias empresas proíbem por política interna) e rejeitada por Linus Torvalds, que manteve o kernel na versão 2.<br>
Usada por GIMP, Inkscape, Bash e GCC.

## LGPL-3.0

Copyleft fraco. SPDX `LGPL-3.0-only`. O "L" é de Lesser, menor. Foi feita especificamente para bibliotecas: se você apenas usa a biblioteca, seu programa pode continuar fechado; se você modifica a própria biblioteca, precisa publicar essas modificações. Também exige que o usuário consiga trocar a biblioteca por outra versão.<br>
Prós: meio-termo inteligente, permite que bibliotecas livres sejam adotadas por software proprietário sem contaminá-lo.<br>
Contras: a distinção entre ligação estática e dinâmica é confusa e fonte constante de dúvida jurídica, e o texto herda toda a complexidade da GPL-3.0.<br>
Usada por GTK, glibc e Qt (em conjunto com licença comercial).

## AGPL-3.0

Copyleft forte, incluindo uso em rede. SPDX `AGPL-3.0-only`. A GPL tinha uma brecha: se a empresa não distribui o programa e sim roda ele num servidor, oferecendo como serviço, nunca precisa publicar nada. A AGPL fecha exatamente isso, obrigando a oferecer o código-fonte também aos usuários que interagem com o sistema pela rede. Virou peça central na disputa entre empresas de infraestrutura e provedores de nuvem: o Redis, depois de adotar licenças restritivas em 2024 e sofrer forte reação da comunidade, migrou para AGPLv3 no Redis 8 em maio de 2025 e voltou ao status aprovado pela OSI.<br>
Prós: é a única licença comum que protege contra o modelo de pegar código aberto e revender como SaaS(Software as a Service), e continua sendo open source de verdade.<br>
Contras: muitas empresas grandes proíbem por política, o Google entre elas, o que derruba a adoção, e o escopo do que conta como "o serviço inteiro" gera insegurança jurídica.<br>
Usada por Nextcloud, Mastodon, Grafana e Redis a partir da versão 8.

## MPL-2.0

Copyleft fraco. SPDX `MPL-2.0`. Criada pela Mozilla em 2012, adota uma abordagem original: o copyleft vale arquivo por arquivo. Se você modifica um arquivo licenciado sob MPL, precisa publicar aquele arquivo; os arquivos novos que criar podem permanecer fechados. É o meio-termo mais equilibrado entre MIT e GPL.<br>
Prós: permite misturar código aberto e fechado no mesmo projeto sem dor de cabeça, é compatível com GPL, LGPL e AGPL por meio da cláusula de licença secundária, e tem texto moderno e legível.<br>
Contras: menos conhecida, exige explicação para quem nunca viu, e a granularidade por arquivo complica quando o código passa por muita refatoração.<br>
Usada por Firefox, Thunderbird e Terraform até a versão 1.5.7.

## Bônus: o que parece open source mas não é

Existem licenças chamadas de source-available, em que o código é visível mas o uso é restrito. Elas não são aprovadas pela OSI e enganam muita gente.<br>
A BSL(Business Source License) restringe o uso comercial que compita com a empresa dona do software e converte automaticamente para uma licença aberta depois de um prazo, normalmente quatro anos. Em agosto de 2023 a HashiCorp migrou o Terraform da MPL 2.0 para a BSL, o que provocou a criação do OpenTofu, um fork mantido pela Linux Foundation. A IBM comprou a HashiCorp em 2025 e manteve a BSL.<br>
A SSPL(Server Side Public License), criada pelo MongoDB, exige que quem oferece o software como serviço publique todo o código da infraestrutura de gerenciamento em volta, não apenas as modificações. A RSAL(Redis Source Available License) seguiu a mesma linha e foi usada pelo Redis entre 2024 e 2025, gerando o fork Valkey, apoiado por AWS, Google Cloud e Oracle.<br>
A moral é simples: código no GitHub e código aberto não são a mesma coisa. Sempre leia o arquivo `LICENSE`.

## Como aplicar uma licença no GitHub

Na criação do repositório, o GitHub oferece um seletor de licença. Em repositório já existente, basta criar um arquivo chamado `LICENSE`, sem extensão, na raiz: ao digitar esse nome, o GitHub sugere os modelos prontos, e você só preenche ano e nome do autor. Feito isso, o GitHub detecta a licença sozinho e mostra o nome dela na barra lateral do repositório. Para comparar opções antes de decidir, o site oficial é o choosealicense.com, mantido pelo próprio GitHub.<br>
Na dúvida sobre qual escolher: MIT para máxima adoção sem complicação, Apache-2.0 quando também quiser proteção de patente, GPL-3.0 para garantir que tudo continue aberto, AGPL-3.0 para se proteger contra uso em nuvem por terceiros, e LGPL-3.0 ou MPL-2.0 para bibliotecas que precisam ser usáveis por software fechado.

## Fontes

Lista oficial de licenças aprovadas pela OSI: https://opensource.org/licenses
Top Open Source licenses in 2025, publicado pela OSI em 17/12/2025: https://opensource.org/blog/top-open-source-licenses-in-2025
Choose a License, do GitHub: https://choosealicense.com
SPDX License List: https://spdx.org/licenses/

Este catálogo é material de estudo e não constitui orientação jurídica.