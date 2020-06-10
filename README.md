**Visao Libertária - Documentação da API**
----

**Base  URL**
----
https://www.visaolibertaria.com/


**Endpoints**
----

* Vídeos
  * [GET - Listar Vídeos](#listar-vídeos)
  * [GET - Listar Vídeos por Categoria](#listar-vídeos-por-categoria)
  * [POST - Buscar Vídeos](#buscar-vídeos)
* Matérias
  * [GET - Listar Matérias](#listar-matérias)
  * [GET - Listar Matérias por Categoria](#listar-matérias-por-categoria)
  * [POST - Buscar Matérias](#buscar-matérias)
* Pautas
  * [GET - Listar Todas as Pautas](#listar-todas-as-pautas)
  * [GET - Listar Últimas Pautas](#listar-últimas-pautas)
  * [GET - Listar Pautas por Categoria](#listar-pautas-por-categoria)
  * [POST - Buscar Pautas](#buscar-pautas)

---

**Listar Vídeos**
----
Retorna lista de vídeos em formato json.

* **URL**

  _/api/Video/List_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Video/List?ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Ini": 0,
      "Total": 338,
      "Videos": [
        {
          "Id": "83bc98b6-710b-4112-a45e-2fb756715f35",
          "Title": "Presidente das Filipinas manda matar quem descumprir quarentena",
          "YoutubeLink": "https://youtu.be/biamPUlvdrU",
          "BitchuteLink": "",
          "StartingDescription": "Veja nosso site: https://visaolibertaria.com\n\n#Filipinas #Duterte #Ditadura #Absurdo\n\nAjude o canal:\n\nhttps://apoio.ancap.su\nhttps://apoia.se/ancapsu\nhttps://padrim.com.br/ancapsu\n16vmNcrA4Mvf7CaRLirAmpnjz1ZH3bWNkQ (Bitcoin)\nLSCnrubCVcpuLrGTTLMqpwRTXvYz7vMbbA (Litecoin)\n0x28aec946919c70e5e25d7c6785e",
          "Description": "",
          "DescriptionPars": [],
          "Script": "",
          "ScriptPars": [],
          "Tags": null,
          "Categories": {
            "MainCategory": {
              "Label": "video",
              "Category": "Vídeo"
            },
            "Categories": [
              {
                "Label": "video",
                "Category": "Vídeo"
              },
              {
                "Label": "news",
                "Category": "Novidades"
              },
              {
                "Label": "history",
                "Category": "História"
              },
              {
                "Label": "socialism",
                "Category": "Socialismo"
              },
              {
                "Label": "principles",
                "Category": "Princípios"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "health",
                "Category": "Saúde"
              }
            ]
          },
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Produzido por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "",
              "Id": ""
            },
            "Authored": {
              "Name": "Peter Turguniev",
              "Id": "23b0f439-72a2-4ea1-8f2f-f31e44d8fc2e"
            },
            "Revised": {
              "Name": "",
              "Id": ""
            },
            "Narrated": {
              "Name": "",
              "Id": ""
            },
            "Produced": {
              "Name": "",
              "Id": ""
            },
            "DateLabel": "em",
            "Date": "06/04/2020",
            "StatusText": "Rascunho"
          },
          "Actions": [],
          "Status": 1,
          "StatusName": "Publicado"
        },
      ]
    }
    ```

---

**Listar Vídeos por Categoria**
----
Retorna lista de vídeos em formato json filtrada por categoria.

* **URL**

  _/api/Video/ByCategory_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `categ=[string]` ["theory", "news", "comic"]


   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Video/ByCategory?categ=theory&ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```


* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Title": "Teoria",
      "Description": "Refere-se a teoria anarcocapitalista",
      "Ini": 0,
      "Total": 97,
      "Videos": [
        {
          "Id": "38b81295-7a54-4b1e-9d09-d4cec0132017",
          "Title": "Pele em risco e porque políticos criam regras absurdas",
          "YoutubeLink": "https://youtu.be/CHgpwIE4k7Q",
          "BitchuteLink": "",
          "StartingDescription": "Veja nosso site: https://visaolibertaria.com\n\n#Políticos #RegrasAbsurdas #PeleEmRisco\n\nAjude o canal:\n\nhttps://apoio.ancap.su\nhttps://apoia.se/ancapsu\nhttps://padrim.com.br/ancapsu\n16vmNcrA4Mvf7CaRLirAmpnjz1ZH3bWNkQ (Bitcoin)\nLSCnrubCVcpuLrGTTLMqpwRTXvYz7vMbbA (Litecoin)\n0x28aec946919c70e5e25d7c6785",
          "Description": "",
          "DescriptionPars": [],
          "Script": "",
          "ScriptPars": [],
          "Tags": null,
          "Categories": {
            "MainCategory": {
              "Label": "video",
              "Category": "Vídeo"
            },
            "Categories": [
              {
                "Label": "video",
                "Category": "Vídeo"
              },
              {
                "Label": "theory",
                "Category": "Teoria"
              },
              {
                "Label": "news",
                "Category": "Novidades"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "exec",
                "Category": "Executivo"
              },
              {
                "Label": "jud",
                "Category": "Judiciário"
              },
              {
                "Label": "leg",
                "Category": "Legislativo"
              },
              {
                "Label": "political",
                "Category": "Políticos"
              }
            ]
          }
        ]
      }
    }
    ```

---

**Buscar Vídeos**
----
Retorna busca de vídeos em formato json.

* **URL**

  _/api/Video/Search_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  `SearchString=[string]`



* **Exemplo:**

  ```javascript
    $.post(
      "https://www.visaolibertaria.com/api/Video/Search?ini=0&max=10",
      { SearchString="teste" },
      function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Ini": 0,
      "Total": 45,
      "Videos": [
        {
          "Id": "520d5283-cd37-4d69-a3bd-5958dcd3dc0e",
          "Title": "Estão faltando mortos nessa conta",
          "YoutubeLink": "https://youtu.be/hi3RbvhyCA8",
          "BitchuteLink": "",
          "StartingDescription": "Veja nosso site: https://visaolibertaria.com\n\n#Abin #5571 #486 #ModelosMatemáticosFurados\n\nAjude o canal:\n\nhttps://apoio.ancap.su\nhttps://apoia.se/ancapsu\nhttps://padrim.com.br/ancapsu\n16vmNcrA4Mvf7CaRLirAmpnjz1ZH3bWNkQ (Bitcoin)\nLSCnrubCVcpuLrGTTLMqpwRTXvYz7vMbbA (Litecoin)\n0x28aec946919c70e5e25d7c",
          "Description": "",
          "DescriptionPars": [],
          "Script": "",
          "ScriptPars": [],
          "Tags": null,
          "Categories": {
            "MainCategory": {
              "Label": "video",
              "Category": "Vídeo"
            },
            "Categories": [
              {
                "Label": "video",
                "Category": "Vídeo"
              },
              {
                "Label": "socialism",
                "Category": "Socialismo"
              },
              {
                "Label": "principles",
                "Category": "Princípios"
              },
              {
                "Label": "info",
                "Category": "Informação"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "health",
                "Category": "Saúde"
              }
            ]
          },
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Produzido por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "",
              "Id": ""
            },
            "Authored": {
              "Name": "Peter Turguniev",
              "Id": "23b0f439-72a2-4ea1-8f2f-f31e44d8fc2e"
            },
            "Revised": {
              "Name": "",
              "Id": ""
            },
            "Narrated": {
              "Name": "",
              "Id": ""
            },
            "Produced": {
              "Name": "",
              "Id": ""
            },
            "DateLabel": "em",
            "Date": "06/04/2020",
            "StatusText": "Rascunho"
          },
          "Actions": [],
          "Status": 1,
          "StatusName": "Publicado"
        }
      ]
    }
    ```

**Listar Matérias**
----
Retorna lista de matérias em formato json.

* **URL**

  _/api/Article/List_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   `sts=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Article/List?ini=0&max=10&sts=0",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Sts": 0,
      "Ini": 0,
      "Total": 638,
      "Articles": [
        {
          "Actions": [],
          "Links": [],
          "Comments": [],
          "Id": "e8713fdb-2ff9-41cb-a3c6-8ebd154db606",
          "Title": "Os bancos centrais e a moeda fiduciária",
          "Text": "",
          "Paragraphs": [],
          "StartingText": "Os governos precisam imprimir moeda para taxar as pessoas de maneira discreta, por meio da inflação, e os bancos precisam ser controlados pelo governo para que essa tarefa seja possível. Daí surge a ideia de um banco central. Mas como funcionam os bancos centrais? Como eles tornam o dinheiro mais “f",
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Escrito por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "Renan S",
              "Id": "16dd8932-7742-4538-8b06-537b5cea72d7"
            },
            "Authored": {
              "Name": "Renan S",
              "Id": "16dd8932-7742-4538-8b06-537b5cea72d7"
            },
            "Revised": {
              "Name": "Marco_Batalha",
              "Id": "2d4fe140-fb26-4eac-8b33-cb6689866f1b"
            },
            "Narrated": {
              "Name": "salander",
              "Id": "563554eb-43b5-4c0e-8f29-9e5b7cd22645"
            },
            "Produced": {
              "Name": "AJ",
              "Id": "7e911f23-9722-489f-884a-c6e691660bfb"
            },
            "DateLabel": "em",
            "Date": "04/06/2020",
            "StatusText": "Publicado"
          },
          "Target": {
            "Id": "",
            "Title": "",
            "Link": "",
            "StartingText": "",
            "Text": "",
            "Paragraphs": [],
            "Categories": {
              "MainCategory": {
                "Label": "",
                "Category": ""
              },
              "Categories": []
            },
            "Authors": {
              "SuggestedLabel": "Sugerido por",
              "AuthoredLabel": "Escrito por",
              "RevisedLabel": "Revisado por",
              "NarratedLabel": "Narrado por",
              "ProducedLabel": "Produzido por",
              "Suggested": {
                "Name": "",
                "Id": ""
              },
              "Authored": {
                "Name": "",
                "Id": ""
              },
              "Revised": {
                "Name": "",
                "Id": ""
              },
              "Narrated": {
                "Name": "",
                "Id": ""
              },
              "Produced": {
                "Name": "",
                "Id": ""
              },
              "DateLabel": "em",
              "Date": "N/D",
              "StatusText": "Rascunho"
            },
            "VoteWrite": 0,
            "VoteVery": 0,
            "VoteGood": 0,
            "VoteNot": 0,
            "VoteOld": 0,
            "VoteFake": 0,
            "UserVote": -1,
            "Actions": [],
            "Status": 0,
            "StatusName": ""
          },
          "Categories": {
            "MainCategory": {
              "Label": "article",
              "Category": "Artigo"
            },
            "Categories": [
              {
                "Label": "article",
                "Category": "Artigo"
              },
              {
                "Label": "principles",
                "Category": "Princípios"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "deepstate",
                "Category": "Estado profundo"
              },
              {
                "Label": "criptocurrency",
                "Category": "Criptomoedas"
              },
              {
                "Label": "book",
                "Category": "Livro"
              }
            ]
          },
          "Status": 6,
          "StatusNarration": 0,
          "Type": 3,
          "ArticleType": 4,
          "StatusName": "Publicado",
          "StatusNarrationName": "Aguardando",
          "TypeName": "Artigo",
          "ArticleTypeName": "Artigo",
          "VoteApprove": 5,
          "VoteNot": 0,
          "VoteAlready": 0,
          "VotePoorly": 0,
          "UserVote": 0,
          "preferredRevisor": "",
          "preferredNarrator": "",
          "preferredProducer": "",
          "preferredRevisorName": "N/D",
          "preferredNarratorName": "N/D",
          "preferredProducerName": "N/D",
          "beingRevised": "2d4fe140-fb26-4eac-8b33-cb6689866f1b",
          "beingNarrated": "563554eb-43b5-4c0e-8f29-9e5b7cd22645",
          "beingProduced": "7e911f23-9722-489f-884a-c6e691660bfb",
          "beingRevisedName": "Marco_Batalha",
          "beingNarratedName": "salander",
          "beingProducedName": "AJ"
        },
      ]
    }

    ```


**Listar Matérias por Categoria**
----
Retorna lista de matérias em formato json filtrada por categoria.

* **URL**

  _/api/Article/ByCategory_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `categ=[string]` ["theory", "news", "comic"]

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Article/ByCategory?categ=news&ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```


* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Title": "Novidades",
      "Description": "Refere-se a novidades, notícias recentes",
      "Ini": 0,
      "Total": 255,
      "Articles": [
        {
          "Actions": [],
          "Links": [],
          "Comments": [],
          "Id": "5c51ad86-9e78-4788-a245-f2ebae9c8e80",
          "Title": "Anonymous ameaça expor crimes estatais para o mundo.",
          "Text": "",
          "Paragraphs": [],
          "StartingText": "Na manhã do dia 31 de maio, domingo, o grupo hacker Anonymous publicou um vídeo no Twitter se manifestando sobre os últimos acontecimentos em Trumplândia e rogando justiça sobre o caso Geroge Floyd. Temos um vídeo sobre esse assunto, mas para explicar brevemente o caso: George Floyd foi um homem neg",
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Escrito por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "CriptoBR",
              "Id": "b34aacaa-3992-4264-8901-068423bf16f7"
            },
            "Authored": {
              "Name": "CriptoBR",
              "Id": "b34aacaa-3992-4264-8901-068423bf16f7"
            },
            "Revised": {
              "Name": "John Rothbard",
              "Id": "631b3cb4-b7f0-4909-bde6-2447bee9415e"
            },
            "Narrated": {
              "Name": "N/D",
              "Id": ""
            },
            "Produced": {
              "Name": "Peter Turguniev",
              "Id": "23b0f439-72a2-4ea1-8f2f-f31e44d8fc2e"
            },
            "DateLabel": "em",
            "Date": "03/06/2020",
            "StatusText": "Publicado"
          },
          "Target": {
            "Id": "",
            "Title": "",
            "Link": "",
            "StartingText": "",
            "Text": "",
            "Paragraphs": [],
            "Categories": {
              "MainCategory": {
                "Label": "",
                "Category": ""
              },
              "Categories": []
            },
            "Authors": {
              "SuggestedLabel": "Sugerido por",
              "AuthoredLabel": "Escrito por",
              "RevisedLabel": "Revisado por",
              "NarratedLabel": "Narrado por",
              "ProducedLabel": "Produzido por",
              "Suggested": {
                "Name": "",
                "Id": ""
              },
              "Authored": {
                "Name": "",
                "Id": ""
              },
              "Revised": {
                "Name": "",
                "Id": ""
              },
              "Narrated": {
                "Name": "",
                "Id": ""
              },
              "Produced": {
                "Name": "",
                "Id": ""
              },
              "DateLabel": "em",
              "Date": "N/D",
              "StatusText": "Rascunho"
            },
            "VoteWrite": 0,
            "VoteVery": 0,
            "VoteGood": 0,
            "VoteNot": 0,
            "VoteOld": 0,
            "VoteFake": 0,
            "UserVote": -1,
            "Actions": [],
            "Status": 0,
            "StatusName": ""
          },
          "Categories": {
            "MainCategory": {
              "Label": "article",
              "Category": "Artigo"
            },
            "Categories": [
              {
                "Label": "article",
                "Category": "Artigo"
              },
              {
                "Label": "theory",
                "Category": "Teoria"
              },
              {
                "Label": "news",
                "Category": "Novidades"
              },
              {
                "Label": "history",
                "Category": "História"
              },
              {
                "Label": "socialism",
                "Category": "Socialismo"
              },
              {
                "Label": "info",
                "Category": "Informação"
              },
              {
                "Label": "political",
                "Category": "Políticos"
              },
              {
                "Label": "deepstate",
                "Category": "Estado profundo"
              },
              {
                "Label": "abroad",
                "Category": "Exterior"
              }
            ]
          },
          "Status": 6,
          "StatusNarration": 0,
          "Type": 3,
          "ArticleType": 4,
          "StatusName": "Publicado",
          "StatusNarrationName": "Aguardando",
          "TypeName": "Artigo",
          "ArticleTypeName": "Artigo",
          "VoteApprove": 7,
          "VoteNot": 2,
          "VoteAlready": 0,
          "VotePoorly": 0,
          "UserVote": 0,
          "preferredRevisor": "",
          "preferredNarrator": "",
          "preferredProducer": "",
          "preferredRevisorName": "N/D",
          "preferredNarratorName": "N/D",
          "preferredProducerName": "N/D",
          "beingRevised": "631b3cb4-b7f0-4909-bde6-2447bee9415e",
          "beingNarrated": "563554eb-43b5-4c0e-8f29-9e5b7cd22645",
          "beingProduced": "",
          "beingRevisedName": "John Rothbard",
          "beingNarratedName": "salander",
          "beingProducedName": "N/D"
        }
      ]
    }

    ```

---




**Buscar Matérias**
----
Retorna busca de matérias em formato json.

* **URL**

  _/api/Article/Search_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  `SearchString=[string]`


* **Exemplo:**

  ```javascript
    $.post(
      "https://www.visaolibertaria.com/api/Article/Search?token=&ini=0&max=10",
      { SearchString="teste" },
      function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Sts": 0,
      "Ini": 0,
      "Total": 53,
      "Articles": [
        {
          "Actions": [],
          "Links": [],
          "Comments": [],
          "Id": "9b65862a-521b-4b6d-b60a-f97dad393cac",
          "Title": "Modelo catastrófico do Imperial College pode ter sido causado por um erro de software",
          "Text": "",
          "Paragraphs": [],
          "StartingText": "O modelo utilizado no estudo pelo Imperial College, aquele do médico epidemiologista britânico Neil Ferguson que se demitiu depois de ter sido flagrado descumprindo sua própria recomendação de quarentena com uma amante, previa 500 mil mortes no Reino Unido e que depois foi revisado para apenas 20 mi",
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Escrito por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "Peter Turguniev",
              "Id": "23b0f439-72a2-4ea1-8f2f-f31e44d8fc2e"
            },
            "Authored": {
              "Name": "Albert Jr",
              "Id": "64fed401-288d-4d58-b07c-48f3cb905386"
            },
            "Revised": {
              "Name": "Bitdov",
              "Id": "abb65bdb-34ab-4107-bb4b-68424e9c49ae"
            },
            "Narrated": {
              "Name": "salander",
              "Id": "563554eb-43b5-4c0e-8f29-9e5b7cd22645"
            },
            "Produced": {
              "Name": "AJ",
              "Id": "7e911f23-9722-489f-884a-c6e691660bfb"
            },
            "DateLabel": "em",
            "Date": "28/05/2020",
            "StatusText": "Publicado"
          },
          "Target": {
            "Id": "",
            "Title": "",
            "Link": "",
            "StartingText": "",
            "Text": "",
            "Paragraphs": [],
            "Categories": {
              "MainCategory": {
                "Label": "",
                "Category": ""
              },
              "Categories": []
            },
            "Authors": {
              "SuggestedLabel": "Sugerido por",
              "AuthoredLabel": "Escrito por",
              "RevisedLabel": "Revisado por",
              "NarratedLabel": "Narrado por",
              "ProducedLabel": "Produzido por",
              "Suggested": {
                "Name": "",
                "Id": ""
              },
              "Authored": {
                "Name": "",
                "Id": ""
              },
              "Revised": {
                "Name": "",
                "Id": ""
              },
              "Narrated": {
                "Name": "",
                "Id": ""
              },
              "Produced": {
                "Name": "",
                "Id": ""
              },
              "DateLabel": "em",
              "Date": "N/D",
              "StatusText": "Rascunho"
            },
            "VoteWrite": 0,
            "VoteVery": 0,
            "VoteGood": 0,
            "VoteNot": 0,
            "VoteOld": 0,
            "VoteFake": 0,
            "UserVote": -1,
            "Actions": [],
            "Status": 0,
            "StatusName": ""
          },
          "Categories": {
            "MainCategory": {
              "Label": "article",
              "Category": "Artigo"
            },
            "Categories": [
              {
                "Label": "article",
                "Category": "Artigo"
              },
              {
                "Label": "news",
                "Category": "Novidades"
              },
              {
                "Label": "info",
                "Category": "Informação"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "health",
                "Category": "Saúde"
              },
              {
                "Label": "wealth",
                "Category": "Riqueza"
              },
              {
                "Label": "tech",
                "Category": "Tecnologia"
              }
            ]
          },
          "Status": 6,
          "StatusNarration": 0,
          "Type": 3,
          "ArticleType": 4,
          "StatusName": "Publicado",
          "StatusNarrationName": "Aguardando",
          "TypeName": "Artigo",
          "ArticleTypeName": "Artigo",
          "VoteApprove": 5,
          "VoteNot": 0,
          "VoteAlready": 0,
          "VotePoorly": 0,
          "UserVote": 0,
          "preferredRevisor": "",
          "preferredNarrator": "",
          "preferredProducer": "",
          "preferredRevisorName": "N/D",
          "preferredNarratorName": "N/D",
          "preferredProducerName": "N/D",
          "beingRevised": "abb65bdb-34ab-4107-bb4b-68424e9c49ae",
          "beingNarrated": "563554eb-43b5-4c0e-8f29-9e5b7cd22645",
          "beingProduced": "7e911f23-9722-489f-884a-c6e691660bfb",
          "beingRevisedName": "Bitdov",
          "beingNarratedName": "salander",
          "beingProducedName": "AJ"
        }
      ]
    }
    ```


**Listar Todas as Pautas**
----
Retorna lista de pautas em formato json.

* **URL**

  _/api/Target/ListAll_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.

* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Target/ListAll?ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Ini": 0,
      "Total": 124,
      "Targets": [
        {
          "Id": "428a6df9-55ae-4955-8110-a31332961d3a",
          "Title": "4 intervenções estatais quase que imperceptíveis aos olhos do indíviduo.  Jornal Hora Extra",
          "Link": "https://jornalhoraextra.com.br/coluna/4-intervencoes-estatais-quase-que-imperceptiveis-aos-olhos-do-individuo/",
          "StartingText": "Por Ulysses Remy (@RemyUlysses) \nÉ bastante comum vermos em filmes e ler em livros sobre impérios e reinados, a atuação do estado na espoliação dos indivíduos em forma de cobranças de impostos e do cerceamento da liberdade por meio de leis (im)positivas regulando relações entre indivíduos, sendo est",
          "Text": "",
          "Paragraphs": [],
          "Categories": {
            "MainCategory": {
              "Label": "suggested",
              "Category": "Pauta sugerida"
            },
            "Categories": [
              {
                "Label": "suggested",
                "Category": "Pauta sugerida"
              }
            ]
          },
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Sugerido por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "",
              "Id": ""
            },
            "Authored": {
              "Name": "Mises Realista",
              "Id": "fc7c562f-3c7c-48b0-b505-039d271fdbe2"
            },
            "Revised": {
              "Name": "",
              "Id": ""
            },
            "Narrated": {
              "Name": "",
              "Id": ""
            },
            "Produced": {
              "Name": "",
              "Id": ""
            },
            "DateLabel": "Registrado em",
            "Date": "04/06/2020",
            "StatusText": ""
          },
          "VoteWrite": 0,
          "VoteVery": 0,
          "VoteGood": 0,
          "VoteNot": 0,
          "VoteOld": 0,
          "VoteFake": 0,
          "UserVote": 0,
          "Actions": [],
          "Status": 1,
          "StatusName": "Registrado"
        }
      ]
    }

    ```



**Listar Últimas Pautas**
----
Retorna lista de pautas em formato json.

* **URL**

  _/api/Target/List_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Target/List?ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Ini": 0,
      "Total": 124,
      "Targets": [
        {
          "Id": "8494d430-ccb1-4782-9e70-2921d92fb852",
          "Title": "Cops, Karens, and the Coming Dystopia",
          "Link": "https://www.youtube.com/watch?v=GFbfDcELLxw",
          "StartingText": "Vídeo da Foundation for Economic Education comparando os acontecimentos dos últimos tempos com a Distopia apresentada em V de Vingança. Como a população abriu mão da liberdade pedindo segurança ao estado devido a um vírus. Apresenta um questionamento qual sociedade queremos viver? \n",
          "Text": "",
          "Paragraphs": [],
          "Categories": {
            "MainCategory": {
              "Label": "suggested",
              "Category": "Pauta sugerida"
            },
            "Categories": [
              {
                "Label": "suggested",
                "Category": "Pauta sugerida"
              },
              {
                "Label": "political",
                "Category": "Políticos"
              },
              {
                "Label": "deepstate",
                "Category": "Estado profundo"
              },
              {
                "Label": "expression",
                "Category": "Liberdade de expressão"
              }
            ]
          },
          "Authors": {
            "SuggestedLabel": "Sugerido por",
            "AuthoredLabel": "Sugerido por",
            "RevisedLabel": "Revisado por",
            "NarratedLabel": "Narrado por",
            "ProducedLabel": "Produzido por",
            "Suggested": {
              "Name": "",
              "Id": ""
            },
            "Authored": {
              "Name": "Rocha ",
              "Id": "62eae552-0d3c-4712-b1dd-af766f80b719"
            },
            "Revised": {
              "Name": "",
              "Id": ""
            },
            "Narrated": {
              "Name": "",
              "Id": ""
            },
            "Produced": {
              "Name": "",
              "Id": ""
            },
            "DateLabel": "Registrado em",
            "Date": "04/06/2020",
            "StatusText": ""
          },
          "VoteWrite": 0,
          "VoteVery": 0,
          "VoteGood": 1,
          "VoteNot": 0,
          "VoteOld": 0,
          "VoteFake": 0,
          "UserVote": 0,
          "Actions": [],
          "Status": 1,
          "StatusName": "Registrado"
        },
      ]
    }

    ```

**Listar Pautas por Categoria**
----
Retorna lista de pautas em formato json filtrada por categoria.

* **URL**

  _/api/Target/ByCategory_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `categ=[string]` ["suggested", "news", "comic"]

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  Nenhum.


* **Exemplo:**

  ```javascript
    $.ajax({
      url: "https://www.visaolibertaria.com/api/Target/ByCategory?categ=suggested&ini=0&max=10",
      dataType: "json",
      type : "GET",
      success : function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Title": "Pauta sugerida",
      "Description": "Pauta sugerida para notícia",
      "Ini": 0,
      "Total": 4553,
      "Targets": [
        {
          "Id": "8494d430-ccb1-4782-9e70-2921d92fb852",
          "Title": "Cops, Karens, and the Coming Dystopia",
          "Link": "https://www.youtube.com/watch?v=GFbfDcELLxw",
          "StartingText": "Vídeo da Foundation for Economic Education comparando os acontecimentos dos últimos tempos com a Distopia apresentada em V de Vingança. Como a população abriu mão da liberdade pedindo segurança ao estado devido a um vírus. Apresenta um questionamento qual sociedade queremos viver? \n",
          "Text": "",
          "Paragraphs": [],
          "Categories": {
            "MainCategory": {
              "Label": "suggested",
              "Category": "Pauta sugerida"
            },
            "Categories": [
              {
                "Label": "suggested",
                "Category": "Pauta sugerida"
              },
              {
                "Label": "political",
                "Category": "Políticos"
              },
              {
                "Label": "deepstate",
                "Category": "Estado profundo"
              },
              {
                "Label": "expression",
                "Category": "Liberdade de expressão"
              }
            ]
          },
        }
      ]
    }
    ```

---


**Buscar Pautas**
----
Retorna busca de pautas em formato json.

* **URL**

  _/api/Target/Search_

* **Method:**

  `GET`

*  **Parâmetros da URL**

   **Obrigatórios:**

   `max=[integer]`

   **Opcionais:**

   `ini=[integer]`

* **Data Params**

  `SearchString=[string]`


* **Exemplo:**

  ```javascript
    $.post(
      "https://www.visaolibertaria.com/api/Target/Search?ini=0&max=10",
      { SearchString="teste" },
      function(res) {
        console.log(res);
      }
    });
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      "Result": 0,
      "ResultComplement": "",
      "Ini": 0,
      "Total": 174,
      "Targets": [
        {
          "Id": "6304a01f-2676-4c69-9e12-614a3750efe8",
          "Title": "Professor da UFJF é condenado a ressarcir cofres públicos em R$ 160 mil por mais de 417 horas de serviço não prestado",
          "Link": "https://g1.globo.com/mg/zona-da-mata/noticia/2020/06/01/professor-da-ufjf-e-condenado-por-nao-cumprir-horario-e-deve-ressarcir-cofres-publicos.ghtml",
          "StartingText": " O professor da Faculdade de Medicina da Universidade Federal de Juiz de Fora (UFJF), Valdeci Manoel de Oliveira, foi condenado por improbidade administrativa. A decisão foi informada pelo Ministério Público Federal (MPF) nesta segunda-feira (1°). \n Conforme a condenação, o docente terá de devolver ",
          "Text": "",
          "Paragraphs": [],
          "Categories": {
            "MainCategory": {
              "Label": "suggested",
              "Category": "Pauta sugerida"
            },
            "Categories": [
              {
                "Label": "suggested",
                "Category": "Pauta sugerida"
              },
              {
                "Label": "comic",
                "Category": "Cômico"
              },
              {
                "Label": "socialism",
                "Category": "Socialismo"
              },
              {
                "Label": "principles",
                "Category": "Princípios"
              },
              {
                "Label": "info",
                "Category": "Informação"
              },
              {
                "Label": "econ",
                "Category": "Economia"
              },
              {
                "Label": "wealth",
                "Category": "Riqueza"
              }
            ]
          },
        }
      ]
    }

    ```
