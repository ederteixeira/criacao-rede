# criacao-rede
criação de rede
 1. Criar VNet

O que é: VNet (Virtual Network) é a rede virtual isolada onde seus recursos (VMs, bancos de dados, aplicativos) vão residir.

Como fazer:

No portal Azure: Criar recurso → Redes → Rede virtual

Definir:

Nome da rede

Região

Espaço de endereçamento (ex.: 10.0.0.0/16)

Por que é importante: Toda comunicação interna e externa dos recursos depende dessa rede.

2. Criar Sub-redes

O que é: Sub-redes são divisões dentro da VNet para organizar recursos e aplicar regras específicas.

Como fazer:

Dentro da VNet, clique em Sub-redes → Adicionar sub-rede

Defina: nome e intervalo de IP (ex.: 10.0.1.0/24)

Por que é importante: Permite separar serviços (ex.: front-end, banco de dados) e controlar acesso.

3. Associar NSG (Network Security Group)

O que é: NSG é um “firewall” que controla o tráfego de entrada e saída das sub-redes ou VMs.

Como fazer:

Criar NSG: Criar recurso → Segurança → Network Security Group

Associar a uma sub-rede ou a uma interface de rede (NIC)

Adicionar regras: permitir ou negar portas específicas (ex.: SSH 22, RDP 3389, HTTP 80)

Por que é importante: Garante segurança e segmentação do tráfego.

4. Configurar Gateway (opcional)

O que é: Permite conectar sua rede Azure com redes externas (on-premises ou outras VNets).

Tipos: VPN Gateway, ExpressRoute

Por que é importante: Necessário se você precisa de conexão segura com sua rede física.

5. Peering (opcional)

O que é: Conexão direta entre VNets diferentes dentro do Azure, permitindo comunicação privada.

Por que é importante: Evita usar a internet pública para comunicação entre VNets.
