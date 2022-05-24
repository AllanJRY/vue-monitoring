## Exercice

L'objectif, et d'utiliser la méthode de l'EventBus pour appliquer des changements a plusieurs composants.

- Vous devez coder la logique d'allumer et éteindre un serveur (en Prop down, event up entre ServerList et ServerListItem)
- Via EventBus, Quand on clique sur le bouton stopper dans le header, tous les serveurs up doivent être arrêtés
- Via EventBus, Quand on clique sur le bouton Relancer dans le header, tous les serveurs down doivent être relancés
- Via EventBus, A chaque lancement ou arrêt d'un serveur, il faut rajouter un message de log dans le composant MonitoringLogs
