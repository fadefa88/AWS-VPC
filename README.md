# AWS-VPC

ho preso e modificato da AWS uno stack di Cloud Formation per costruire un VPC con 4 subnet (2 pubbliche e 2 private), così da avere un’infrastruttura di rete pronta all’uso e rimuoverla quando preferite.

Queste le componenti:

VPC:   “VPC-Test” subnet 10.0.0.0/16 su due Availability Zones (nella region Europe-Milano)
Public Subnets: “PublicSubnet1” 10.0.1.0/24 e “PublicSubnet2” 10.0.2.0/24
Private Subnets: “PrivateSubnet1” 10.0.3.0/24 e “PrivateSubnet2” 10.0.4.0/24
Internet Gateway: “InternetGateway-Test” che di fatto è l’oggetto che permette al VPC di uscire su internet
NAT Gateway (public): “NATGateway-Test” con ip privato 10.0.1.10 e pubblico 15.160.249.209 (il pubblico ovviamente sarà sempre diverso). Il suo compito è quello di far uscire su internet le VM che si trovano nelle private subnets (NB il NAT gateway costa circa 36$ al mese e l’ip statico 4$, quindi potete toglierli dall’architettura e non spendere nulla.. semplicemente le VM nelle private subnets non usciranno su internet).


 

In allegato le istruzioni per far partire lo stack, assieme al file in yaml.
