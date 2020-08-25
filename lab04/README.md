## Tarefa 1

![Tela 3](https://github.com/jep84/inf331/blob/master/lab04/images/tarefa1.png)

## Tarefa 2

![Tela 3](https://github.com/jep84/inf331/blob/master/lab04/images/tarefa2.png)

## Tarefa 3

![Tela 3](https://github.com/jep84/inf331/blob/master/lab04/images/tarefa3.png)

## Tarefa 4

### Serviço OMDb

* __Título do serviço__: The Open Movie Database
* __Breve descrição__: API para obter informações sobre filmes
* __URL completa da requisição__: http://www.omdbapi.com/?t=matrix&apikey=5773d12a&tomatoes=true&y=1999
* __Cabeçalho HTTP da chamada__:
~~~http
GET /?apikey=5773d12a&tomatoes=true&t=matrix&y=1999 HTTP/1.1
User-Agent: PostmanRuntime/7.26.3
Accept: */*
Postman-Token: fd96c096-4d45-4734-8b8b-3929d06e0663
Host: www.omdbapi.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Cookie: __cfduid=dcd9de91aa3e580f2450146ce6e0003841598280903
~~~
* __Cabeçalho HTTP da resposta__:
~~~http
HTTP/1.1 200 OK
Date: Mon, 24 Aug 2020 16:20:48 GMT
Content-Type: application/json; charset=utf-8
Transfer-Encoding: chunked
Connection: keep-alive
Cache-Control: public, max-age=86400
Expires: Mon, 24 Aug 2020 15:55:04 GMT
Last-Modified: Mon, 24 Aug 2020 14:55:04 GMT
Vary: *, Accept-Encoding
X-AspNet-Version: 4.0.30319
X-Powered-By: ASP.NET
Access-Control-Allow-Origin: *
CF-Cache-Status: HIT
cf-request-id: 04c2dec59f0000d020119c3200000001
CF-RAY: 5c7e671c38edd020-GRU
Age: 5144
Server: cloudflare
Content-Encoding: gzip
~~~
* __Conteúdo da resposta__:
~~~json
{
    "Title": "The Matrix",
    "Year": "1999",
    "Rated": "R",
    "Released": "31 Mar 1999",
    "Runtime": "136 min",
    "Genre": "Action, Sci-Fi",
    "Director": "Lana Wachowski, Lilly Wachowski",
    "Writer": "Lilly Wachowski, Lana Wachowski",
    "Actors": "Keanu Reeves, Laurence Fishburne, Carrie-Anne Moss, Hugo Weaving",
    "Plot": "A computer hacker learns from mysterious rebels about the true nature of his reality and his role in the war against its controllers.",
    "Language": "English",
    "Country": "USA",
    "Awards": "Won 4 Oscars. Another 37 wins & 50 nominations.",
    "Poster": "https://m.media-amazon.com/images/M/MV5BNzQzOTk3OTAtNDQ0Zi00ZTVkLWI0MTEtMDllZjNkYzNjNTc4L2ltYWdlXkEyXkFqcGdeQXVyNjU0OTQ0OTY@._V1_SX300.jpg",
    "Ratings": [
        {
            "Source": "Internet Movie Database",
            "Value": "8.7/10"
        },
        {
            "Source": "Rotten Tomatoes",
            "Value": "88%"
        },
        {
            "Source": "Metacritic",
            "Value": "73/100"
        }
    ],
    "Metascore": "73",
    "imdbRating": "8.7",
    "imdbVotes": "1,624,177",
    "imdbID": "tt0133093",
    "Type": "movie",
    "tomatoMeter": "N/A",
    "tomatoImage": "N/A",
    "tomatoRating": "N/A",
    "tomatoReviews": "N/A",
    "tomatoFresh": "N/A",
    "tomatoRotten": "N/A",
    "tomatoConsensus": "N/A",
    "tomatoUserMeter": "N/A",
    "tomatoUserRating": "N/A",
    "tomatoUserReviews": "N/A",
    "tomatoURL": "http://www.rottentomatoes.com/m/matrix/",
    "DVD": "21 Sep 1999",
    "BoxOffice": "N/A",
    "Production": "Warner Bros. Pictures",
    "Website": "N/A",
    "Response": "True"
}
~~~

### Serviço figshare

* __Título do serviço__: figshare
* __Breve descrição__: Repositório para divulgação de pesquisas científicas
* __URL completa da requisição__: https://api.figshare.com/v2/articles/search
* __Cabeçalho HTTP da chamada__:
~~~http
POST /v2/articles/search HTTP/1.1
Content-Type: application/json
User-Agent: PostmanRuntime/7.26.3
Accept: */*
Postman-Token: 3279ce3d-295c-486c-8fbc-2d8ec75c7de5
Host: api.figshare.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 74
{
    "page": 1,
    "page_size": 2,
    "search_for": "lorawan"
}
~~~
* __Cabeçalho HTTP da resposta__:
~~~http
HTTP/1.1 200 OK
Access-Control-Allow-Headers: Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Authorization
Access-Control-Allow-Methods: GET, POST, PUT, DELETE, OPTIONS
Access-Control-Max-Age: 3600
Content-Encoding: gzip
Content-Type: application/json
Date: Mon, 24 Aug 2020 16:19:07 GMT
Server: nginx
Vary: Accept-Encoding
X-Request-Id: NA
Content-Length: 617
Connection: keep-alive
~~~
* __Conteúdo da resposta__:
~~~json
[
    {
        "defined_type_name": "dataset",
        "handle": "",
        "url_private_html": "https://figshare.com/account/articles/11492088",
        "timeline": {
            "publisherPublication": "2018-04-11T00:00:00",
            "revision": "2020-01-03T23:40:32",
            "firstOnline": "2020-01-01T10:29:44",
            "posted": "2020-01-01T10:29:44"
        },
        "url_private_api": "https://api.figshare.com/v2/account/articles/11492088",
        "url_public_api": "https://api.figshare.com/v2/articles/11492088",
        "id": 11492088,
        "doi": "10.5281/zenodo.1217023",
        "thumb": "",
        "title": "Dataset for:  IoT deployment for city scale air quality monitoring with Low-Power Wide Area Networks",
        "url": "https://api.figshare.com/v2/articles/11492088",
        "defined_type": 3,
        "resource_title": "",
        "url_public_html": "https://zenodo.figshare.com/articles/dataset/Dataset_for_IoT_deployment_for_city_scale_air_quality_monitoring_with_Low-Power_Wide_Area_Networks/11492088",
        "resource_doi": "",
        "published_date": "2020-01-01T10:29:44Z",
        "group_id": 17126
    },
    {
        "defined_type_name": "dataset",
        "handle": "",
        "url_private_html": "https://figshare.com/account/articles/8969417",
        "timeline": {
            "publisherPublication": "2019-07-19T00:00:00",
            "revision": "2019-07-20T04:48:52",
            "firstOnline": "2019-07-20T04:48:52",
            "posted": "2019-07-20T04:48:52"
        },
        "url_private_api": "https://api.figshare.com/v2/account/articles/8969417",
        "url_public_api": "https://api.figshare.com/v2/articles/8969417",
        "id": 8969417,
        "doi": "10.5281/zenodo.3342253",
        "thumb": "",
        "title": "Sigfox and LoRaWAN Datasets for Fingerprint Localization in Large Urban and Rural Areas",
        "url": "https://api.figshare.com/v2/articles/8969417",
        "defined_type": 3,
        "resource_title": "",
        "url_public_html": "https://zenodo.figshare.com/articles/dataset/Sigfox_and_LoRaWAN_Datasets_for_Fingerprint_Localization_in_Large_Urban_and_Rural_Areas/8969417",
        "resource_doi": "",
        "published_date": "2019-07-20T04:48:52Z",
        "group_id": 17126
    }
]
~~~
