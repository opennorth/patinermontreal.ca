# Getting Started

    git clone git://github.com/opennorth/patinermontreal.ca.git
    bundle
    bundle exec rake db:migrate
    bundle exec rake import:donnees
    bundle exec rake import:sherlock
    bundle exec rake import:dorval
    bundle exec rake import:google
    bundle exec rake location:fix
    bundle exec rake location:geocommons
    bundle exec rake location:compare
    bundle exec rake location:import

It is normal to see the following output:

    "Parc de Beauséjour, 6891, boulevard Gouin Ouest (PP) (chalet)" matches no rink. Creating!
    "Parc des Hirondelles, 2574, rue Fleury Est (PPL)" matches no rink. Creating!
    "Parc Duff Court, 1830, croissant Roy (PPL)" matches no rink. Creating!
    "Parc de La Vérendrye, 5900, rue Drake (PPL) (chalet)" matches no rink. Creating!
    "Parc de la Cité Jardin, boulevard Rosemont/41e Avenue (PPL et C) (chalet pas toujours ouvert)" matches no rink. Creating!
    "Bassin Bonsecours* (Vieux-Port) (Métro Champ-de-Mars) (chalet)" matches no rink. Creating!
    "Parc Nicolas-Tillemont, 7833, avenue des Érables (PSE) (chalet)" matches no rink. Creating!
    "Parc René-Goupil, 8661, 25e Avenue (PSE) (chalet) (fermée en raison de travaux pour la saison 2011-2012) " matches no rink. Creating!
    "Parc Sainte-Yvette, 8950, 10e Avenue (PPL) (chalet)" matches no rink. Creating!

# Deployment

    gem install heroku
    heroku create --stack cedar APP_NAME
    git push heroku master
    heroku run rake db:migrate
    heroku run rake import:donnees
    heroku run rake import:sherlock
    heroku run rake import:dorval
    heroku run rake import:google
    heroku run rake location:fix
    heroku run rake location:geocommons
    heroku run rake location:compare
    heroku run rake location:import

# Misc.

* [Data sources](https://docs.google.com/spreadsheet/pub?hl=en_US&hl=en_US&key=0AtzgYYy0ZABtdFMwSF94MjRxcW1yZ1JYVkdqM1Fzanc&single=true&gid=0&output=html)