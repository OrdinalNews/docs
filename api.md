# API

The [front-end for inscribe.news](https://inscribe.news) is powered by Cloudflare Pages, and contains not only the website but also a powerful API and indexer to interact _with any inscription and it's content_.

The following API endpoints are available and [documented at the root of the API](https://inscribe.news/api), where **ID** is either the inscription ID or the inscription number.

| URL                | Description                                                                      |
| ------------------ | -------------------------------------------------------------------------------- |
| /api/info/ID       | Returns on-chain inscription information as JSON                                 |
| /api/content/ID    | Returns on-chain inscription content, based on mime type                         |
| /api/news/ID       | Returns HTML by parsing the inscription body _(news only)_                       |
| /api/data/ID       | Returns the inscription info and content above in one call as JSON _(news only)_ |
| /api/data/ord-news | Returns all indexed and valid news inscriptions                                  |
| /api/data/ord-list | Returns all indexed inscriptions                                                 |

This API creates a cached layer of inscription data, and everything is returned from the edge when available. If not, the data is fetched then stored from the [Hiro Ordinals API](https://docs.hiro.so/ordinals) for future reads.

The API code exists in the [/functions directory of the project](https://github.com/OrdinalNews/client/tree/main/functions/api), and Typescript types are available [in this helper file](https://github.com/OrdinalNews/client/blob/main/lib/api-types.ts).

{% hint style="info" %}
This API is free to use for any website, if you find it useful or run into any errors, please [file an issue on GitHub](https://github.com/ordinalnews/client/issues)!
{% endhint %}
