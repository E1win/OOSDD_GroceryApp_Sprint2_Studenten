# GroceryApp sprint2 

## Versiebeheer methodiek
In deze repository wordt de Gitflow branching strategie gebruikt. Hiervoor worden de onderstaande branches gebruikt:

- `main` - Op deze branch wordt alleen code gezet die klaar is voor productie. Er wordt alleen met deze branch gemerged d.m.v. pull requests. Alle nieuwe toevoegingen aan deze branch zijn voor een release. Alleen de hotfix en release branches maken pull requests naar de main-branch.
- `develop` - Feature-branches worden gemaakt vanuit deze branch en worden na voltooiing met een pull requests hierin gemerged wanneer ze klaar zijn voor het testen.
- `release/[release_nummer]` - Release-branches worden gebruikt ter voorbereiding van nieuwe releases. Deze branch wordt aangemaakt vanuit de develop-branch met alle features die met de nieuwe release mee gaan. Hierna worden er op de release-branch alleen kleine bugfixes en aanpassingen gedaan. Wanneer de release gereed is wordt het d.m.v. een pull request met de main-branch gemerged.
- `feature/[feature_naam]` - Feature-branches worden gebruikt voor alle nieuwe features. De branches worden gemaakt vanuit de develop-branch en wanneer ze gereed zijn met een pull request teruggevoegd.
- `hotfix/[hotfix_naam]` - Deze branch wordt gebruikt wanneer er snel belangrijke veranderingen nodig zijn in de main-branch. Deze veranderingen moeten ook met de develop-branch worden gemerged om te voorkomen dat de bug opnieuw wordt geïntroduceerd.

Pull requests op de main-, develop- en release-branches worden pas geaccepteerd nadat de pipeline tests een succesvol resultaat teruggeven.