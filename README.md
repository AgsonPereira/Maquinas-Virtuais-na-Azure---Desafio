Minha Aventura Criando uma VM Windows no Azure! 🚀

E aí! Este repo aqui é o meu "diário de bordo" do desafio de criar uma Máquina Virtual lá no Microsoft Azure. A ideia é anotar tudo que eu fiz, o que aprendi e umas dicas que podem me ajudar (e quem sabe mais alguém) no futuro. Bora documentar essa jornada!

Primeiro passo: Antes de sair clicando, dei uma lida no guia oficial da Microsoft pra criar VM Windows pelo portal: Guia Rápido Azure VM Windows. Ajudou a ter uma ideia do caminho.

Pra que serve esse Repo? 🤔
Basicamente, é meu cantinho pra guardar um resumo rápido de como criar VMs no Azure. Mistura o que vi no guia e nas aulas da DIO com o que eu mesmo fiz na prática. Um guia rápido pra consultas futuras, saca?

📝 Mão na Massa: Como Criei a Minha VM no Azure (Com Emoção!)
Beleza, aqui foi como eu fiz pra subir a VM. Tentei anotar os passos principais, incluindo um pequeno susto no meio:

Login no Azure: Primeira coisa, né? Entrar no portal.azure.com com a minha conta.
Cadê as VMs?: Fui lá no menu buscar por "Máquinas Virtuais" e cliquei em "Criar". Segui o fluxo parecido com o do guia que li.
Configurações Iniciais:

Nome da VM: Chamei de myVM. Simples e direto.
Região: Escolhi Brazil South, pra ficar aqui pertinho.
Imagem: Selecionei a imagem Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 (a que estava no guia).
Tamanho: Aqui eu comecei escolhendo o tamanho menor. Spoiler: Deu ruim depois!
Conta Admin: Criei o usuário meuuser e defini uma senha aleatória direto no portal.
Discos: Mantive as sugestões padrão pro disco do Sistema Operacional.
Rede:
Aceitei as sugestões pra VNet e Sub-rede.
Pedi um IP Público pra conseguir acessar de fora.
Grupo de Segurança de Rede (NSG): IMPORTANTE! Aqui, na parte de Regras de porta de entrada, marquei Permitir portas selecionadas e escolhi RDP (3389). Isso é essencial pra conseguir conectar na VM Windows remotamente.
Gerenciamento e Avançado: Passei batido por essas partes pro lab inicial.
Revisar e Criar (A Hora da Verdade!): Cliquei no botão Rever + criar...
😱 EITA! Deu Erro!: Apareceu uma mensagem vermelha: "Falha na validação para o seguinte separador: Informações básicas. As informações necessárias estão em falta ou não são válidas." Pânico? Um pouco! Voltei na aba "Informações básicas".
A Solução: Percebi que talvez o problema fosse o Tamanho da VM que eu tinha escolhido inicialmente (talvez não estivesse disponível na região ou tivesse alguma outra treta). Resolvi mudar o tamanho para D4s_v3.
Segunda Tentativa: Com o novo tamanho selecionado, cliquei em Rever + criar de novo.
AGORA FOI! ✅: A validação passou! Ufa! Notei que apareceu o preço estimado: 0.0843 USD/h. É bom ficar de olho nisso! Mandei criar a VM.
VM Criada! (Mas não conectei 😅), o próximo passo seria pegar o IP Público e conectar via Área de Trabalho Remota (RDP) usando o usuário meuuser e a senha. MAS, pra garantir que não ia gerar custo extra deixando a VM rodando sem necessidade, eu parei por aqui mesmo! Só validei que a criação foi concluída com sucesso no portal. Missão cumprida por enquanto! 👍


🏁 Concluindo (Por Hora!)
Ufa! Missão dada, missão cumprida (com um pequeno desvio)! Consegui criar a VM Windows no portal, passei pelo perrengue do erro de validação, ajustei e vi que ela foi criada com sucesso. Não cheguei a conectar pra evitar custos, mas o processo de criação em si funcionou. Aprendi bastante na prática, principalmente sobre a importância de verificar os detalhes como tamanho e região.


Feito por: Agson Pereira
Data: 01/05/2025.
