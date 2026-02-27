Nom du profil : "event peak"

context <<menuItem>>
inv prixUnitaire : self.prixTTC > 0
Propriété taguée : {tempsPreparation : Integer}


--- OCL ---

context SuperEvenement
inv: self.nom.size() <= 64

changer en pre condution quand on aura une methode "achat"
context Evenement
inv: self.nbBilletAcheté <= self.lieu.capacité

context Billet
inv: self.dateAchat <= self.evenement.date

context SuperEvenement::ajouterEvenement(event : Evenement)
pre evenementValide : not self.evenements.contains(event)

