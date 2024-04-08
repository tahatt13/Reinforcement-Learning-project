
# Allocation dynamique des ressources dans le cloud

Ce projet rentre dans le cadre d'un projet scolaire du module "Apprentissage par renforcement pour les réseaux" de la 2ème année à Télécom SudParis.

#  
Nous considérons le problème d’allocation des VMs dans un serveur physique d’un cloud en tenant compte de la charge, et du nombre de VM en fonctionnement. On contrôle le système en décidant d’allouer ou désallouer des VMs.

![image](https://github.com/tahatt13/Reinforcement-Learning-project/assets/95372659/fcf5677f-22f8-4023-a5e6-e850e330fccd)


Le serveur physique est représenté dans la figure ci-dessus, on supposera que :
- le nombre maximal de VMs est K,
- la capacité du système est B (file + nombre de VMs).
- le système est slotté, donc en temps discret, et le trafic en arrivée est représenté par un groupe (ou batch) de paquets par slot. On définit une distribution de probabilité pour les arrivées des paquets, notée PA, tel que PA(i) est la probabilité qu’il y ait i arrivées de paquets dans un slot. La taille maximale du batch est b.
- les VMs (1, . . . , K) peuvent avoir des débits différents, définis par le nombre de paquets
servis par slot : d1, d2, ...dK, on supposera pour simplifier que d1 = d2 = . . . = dK = d.
- αj (j = 0 . . . K), est l’action de maintenir j serveurs en activité. Ainsi, α2 est l’action d’avoir 2 serveurs en activité (on supposera que ce sont les serveurs 1 et 2)
