# Fullstack Blog alkalmazás

Ez a demo egy egyszerű full-stack alkalmazást mutat be. Két külön változat érhető el belőle, egy egyszerű blog és egy olyan, ami AI funkciókkal van kiegészítve. Ez utóbbi OpenAI-val (vagy Mistral-al) és DeepL-lel való integrációt mutatja be.

## Előkészületek

A példák futtatásához az alábbi telepített szoftverekre van szükség:

* [Visual Studio](https://visualstudio.microsoft.com/vs/community/)
    * `ASP.NET and web development` workload
    * `.NET 8.0 Runtime` és `.NET SDK`
* [Node.js](https://nodejs.org/en/download/prebuilt-installer)
* [Git](https://git-scm.com/)

A példához tartozó forráskód megtalálható a GitHub-on a [demók](https://github.com/VIAUBXAV081/demok) repositoryba. Kezdés előtt klónozd le a repositoryt a saját számítógépedre.

```bash
git clone https://github.com/VIAUBXAV081/demok.git
```

## Egyszerű blog

- Nyisd meg a `demok/FullStack/1_BlogDemo` mappát.
- Hozz létre egy új `appsettings.json` fájlt a `Blog.Server` mappában található `appsettings.example.json` fájl alapján.
- Futtasd a `dotnet publish -p:PublishProfile=FolderProfile` parancsot az alkalmazás közzétételéhez.
- Indítsd el az alkalmazást a `publish/Blog.Server.exe` állomány segítségével.
- Látogass el a `http://localhost:5000` címre a böngésző segítségével.

## AI szolgáltatásokkal kiegészített blog

- Nyisd meg a `demok/FullStack/2_BlogDemoWithAI` mappát.
- Hozz létre egy új `appsettings.json` fájlt a `Blog.Server` mappában található `appsettings.example.json` fájl alapján:
	- Hozz létre egy új OpenAI API tokent a [https://platform.openai.com/settings/profile?tab=api-keys](https://platform.openai.com/settings/profile?tab=api-keys) címen.
 		- Megjegyzés: Az aktuális szabályozás alapján ez akár költségeket is vonhat maga után, mindenképpen tájékozódj az OpenAI weboldalán az [aktuális felhasználási feltételekről](https://openai.com/api/pricing/)!	
		- Töltsd ki az `API Key` mezőt a `Services/OpenAi` részben.
	- Alternatívaként használhatod a [Mistral AI](https://mistral.ai/)-t is, ennek van ingyenes csomagja is, de a használatához regisztráció szükséges.
		- Hozz létre egy új Mistral API tokent az [API Keys](https://admin.mistral.ai/organization/api-keys) címen.
		- Töltsd ki az `API Key` mezőt a `Services/Mistral` részben.
		- A `Program.cs` fájlban cseréld le a `OpenAiSuggestionService`-t a `MistralSuggestionService` sorra.
	- Hozz létre egy új DeepL API tokent a [https://www.deepl.com/en/your-account/keys](https://www.deepl.com/en/your-account/keys) címen.
		- Töltsd ki az `API Key` mezőt a `Services/DeepL` részben.
- Futtasd a `dotnet publish -p:PublishProfile=FolderProfile` parancsot az alkalmazás közzétételéhez.
- Indítsd el az alkalmazást a `publish/Blog.Server.exe` állomány segítségével.
- Látogass el a `http://localhost:5000` címre a böngésző segítségével.
