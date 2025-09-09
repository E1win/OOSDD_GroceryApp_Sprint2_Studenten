# GroceryApp sprint2 

## Docentversie  
In deze versie zijn de wijzigingen doorgevoerd en is de code compleet.  

## Versiebeheer methodiek
In deze repository wordt de Gitflow branching strategie gebruikt. Hiervoor worden de onderstaande branches gebruikt:

- `main` - Op deze branch wordt alleen code gezet die klaar is voor productie. Er wordt alleen met deze branch gemerged d.m.v. pull requests. Alle nieuwe toevoegingen aan deze branch zijn voor een release. Alleen de hotfix en release branches maken pull requests naar de main-branch.
- `develop` - Feature-branches worden gemaakt vanuit deze branch en worden na voltooiing met een pull requests hierin gemerged wanneer ze klaar zijn voor het testen.
- `release/[release_nummer]` - Release-branches worden gebruikt ter voorbereiding van nieuwe releases. Deze branch wordt aangemaakt vanuit de develop-branch met alle features die met de nieuwe release mee gaan. Hierna worden er op de release-branch alleen kleine bugfixes en aanpassingen gedaan. Wanneer de release gereed is wordt het d.m.v. een pull request met de main-branch gemerged.
- `feature/[feature_naam]` - Feature-branches worden gebruikt voor alle nieuwe features. De branches worden gemaakt vanuit de develop-branch en wanneer ze gereed zijn met een pull request teruggevoegd.
- `hotfix/[hotfix_naam]` - Deze branch wordt gebruikt wanneer er snel belangrijke veranderingen nodig zijn in de main-branch. Deze veranderingen moeten ook met de develop-branch worden gemerged om te voorkomen dat de bug opnieuw wordt geïntroduceerd.

## Studentversie:  
### UC04 Kiezen kleur boodschappenlijst  
Is compleet.

### UC05 Product op boodschappenlijst plaatsen:   
- `GetAvailableProducts()`  
	De header van de functie bestaat maar de inhoud niet.  
	Zorg dat je een lijst maakt met de beschikbare producten (dit zijn producten waarvan nog voorraad bestaat en die niet al op de boodschappenlijst staat).  
- `AddProduct()`   
	Zorg dat het gekozen beschikbare product op de boodschappenlijst komt (door middel van de GroceryListItemsService).  

### UC06 Inloggen  
Een collega is ziek maar heeft al een deel van de inlogfunctionaliteit gemaakt.  
Dit betreft het Loginscherm (LoginView) met bijbehorend ViewModel (LoginViewModel),  
maar ook al een deel van de authenticatieService (AuthService in Grocery.Core),  
de clientrepository (ClientRepository in Grocery.Core.Data)  
en de client class (Client in Grocery.Core).  
De opdracht is om zelfstandig de login functionaliteit te laten werken.  

*Stappenplan:*  
1. Begin met de Client class en zorg dat er gebruik wordt gemaakt van Properties.  
2. In de ClienRepository wordt nu steeds een vaste client uit de lijst geretourneerd. Werk dit uit zodat de juiste Client wordt geretourneerd.  
3. Werk de klasse AuthService verder uit, zodat daadwerkelijk de controle op het ingevoerde password wordt uitgevoerd.
4. Zorg dat de LoginView.xaml wordt toegevoegd aan het Grocery.App project in de Views folder (Add ExistingItem). De file bevindt zich al op deze plek, maar wordt nu niet meegecompileerd.  
5. In MauiProgramm class van de Grocery.App staan de registraties van de AuthService en de LoginView in comment --> haal de // weg.  
6. In App.xaml.cs staat /*LoginViewModel viewModel*/ haal hier /* en */ weg, zodat het LoginViewModel beschikbaar komt.  
7. In App.xaml.cs staat //MainPage = new LoginView(viewModel); Haal hier de // weg en zet de regel erboven in commentaar, zodat AppShell wordt uitgeschakeld.  
8. Uncomment de route naar het Login scherm in AppShell.xaml.cs: //Routing.RegisterRoute("Login", typeof(LoginView)); 

