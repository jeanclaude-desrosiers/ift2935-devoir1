# Exercice 2 (pt.2)

> J'assume que 2 entités distinctes ne peuvent avoir un même numéro de
> téléphone et avoir 2 emplacements différents. Donc on ne peut avoir un
> gérant qui entre son numéro personnel pour celui de son magasin
Adresse(*num_telephone*, ville, code_postal, rue, num_civique)

Magasin(*num_agence*, #num_telephone)

> la FK #num_agence, pointe vers le magasin que l'employé gère
Employe(*num_employe*, nom, prenom, poste, salaire, #num_agence)

EstEmployeAu(*#num_employe*, #num_agence)

Categorie(categorie)

PrenomActeur(*#acteur_id*, *prenom_acteur*)

> Besoin d'un acteur_id, pour que 2 acteurs puissent avoir le même nom sur
> un même film
Acteur(*acteur_id*, nom, #num_catalogue)

PrenomRealisateur(*#realisateur_id*, *prenom_realisateur*)

Realisateur(*realisateur_id*, nom)

Film(*num_catalogue*, titre, #realisateur_id, #categorie)

Casette(*num_casette*, #num_catalogue, #num_agence, montant_location,
        prix_achat, etat)

Membre(*num_membre*, nom, prenom, #num_telephone, inscription_jour,
        inscription_mois, inscription_annee)

LouePar(*num_location*, location_jour, location_mois, location_annee,
        restitution_jour, restitution_mois, restitution_annee)