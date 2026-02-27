Nom du profil : "event peak"

context <<menuItem>>
inv prixUnitaire : self.prixTTC > 0
Propriété taguée : {tempsPreparation : Integer}


--- OCL ---

context SuperEvenement
inv: self.nom.size() <= 64

context SuperEvenement::ajouterEvenement(event : Evenement)
pre evenementValide : not self.evenements.contains(event)