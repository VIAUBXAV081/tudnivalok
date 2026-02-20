# Egyszerű AI szolgáltatás

Ez a példa egy egyszerű gépi tanulási pipeline-t mutat be, ami strukturált adatokból egy neurális hálót betanít, majd a modellt ONNX formátumba exportálja későbbi futtatáshoz más platformon. A tanításhoz a [Palmerpenguins](https://allisonhorst.github.io/palmerpenguins/) adathalmazt használjuk, amely különböző pingvinfajok egyedeit tartalmazza mérési adatokkal (pl. csőrhossz, csőrszélesség, uszonyhossz, testsúly). A cél egy többosztályos klasszifikációs feladat megoldása, ami a numerikus jellemzőkből megjósolja a pingvin faját.

## Pipeline

1. adatok betöltése és előfeldolgozása,
2. neurális háló létrehozása TensorFlow-ban,
3. modell betanítása és kiértékelése,
4. modell exportálása ONNX formátumba,
5. inferencia futtatása .NET környezetben.

## Előkészületek

A példa futtatásához az alábbi telepített szoftverekre van szükség:

* [Python](https://www.python.org/) futtatókörnyezet (3.12-es verzió)
* [Poetry](https://python-poetry.org/) vagy egyéb függőségkezelő (opcionális, de erősen javasolt)
* [Visual Studio](https://visualstudio.microsoft.com/vs/community/)
    * `.NET 8.0 Runtime` és `.NET SDK`
* [Git](https://git-scm.com/)

A példához tartozó forráskód megtalálható a GitHub-on a [demók](https://github.com/VIAUBXAV081/demok) repositoryba. Kezdés előtt klónozd le a repositoryt a saját számítógépedre.

```bash
git clone https://github.com/VIAUBXAV081/demok.git
```

## A modell elkészítése

Ebben a lépésben elkészítjük a neurális hálót, betanítjuk a mintaadatseten és exportáljuk későbbi futtatásra.

- Nyiss meg egy parancssoros eszközt és lépj be a projekt könyvtárába:

    ```bash
    cd demok/CustomAIServiceIntegration/1_SimpleModel
    ```

- Készíts egy virtuális környezetet, és telepítsd a függőségeket:
  
    ```bash
    poetry install
    .\.venv\Scripts\activate
    ```
  
    vagy

    ```bash
    python -m venv venv
    .\venv\Scripts\activate
    pip install -r requirements.txt
    ```
  
- Futtasd a szkriptet:
  
    ```bash
    python main.py
    ```

- A modell a `data` mappában `model.onnx` néven fog létrejönni.
  
## Modell futtatása

Ebben a lépésben betöltjük a korábban létrejött modellt és futtatjuk.

- Másold át a korábbi lépésben létrejövő `data/model.onnx` és `data/datasets/labels.json` fájlokat a `demok/CustomAIServiceIntegration/2_RunModel/RunModel/Inputs` mappába változatlan névvel.
- Nyisd meg a `demok/CustomAIServiceIntegration/2_RunModel` fájlban található solution fájlt.
- Futtasd az alkalmazást.
- Az alkalmazás a háttérben betölti a modellt és elvégez egy predikciót. A kimeneten az `Adelie` feliratnak kell megjelennie.

