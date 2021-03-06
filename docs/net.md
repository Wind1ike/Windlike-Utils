# Net
```js
interface NetModule {
  parseParams: (locationSearch: string) => object;
  parseUrl: (url: string) => UrlInfoObject;
}

interface UrlInfoObject {
  url: string
  host: string
  port: number
  path: string
  params: object
}
```

## parseParams
#### Describe
```js
(locationSearch: string) => object;
```

#### Arguments
  - locationSearch(string)

#### Returns
(object)

#### Example
```js
const SEARCH = '?key=value&search=windlike';

utils.net.parseParams(SEARCH);  // { key: 'value', search: 'windlike' }
```

## parseUrl
Parse URL string to object.
#### Describe
```js
interface UrlInfoObject {
  url: string
  host: string
  port: number
  path: string
  params: object
}

(url: string) => UrlInfoObject;
```

#### Arguments
  - url(string)

#### Returns
(UrlInfoObject)

#### Example
```js
const URL = 'https://github.com/MrWindlike/Windlike-Utils?key=value';

utils.net.parseUrl(URL);
// {
//   url: URL,
//   host: 'https://github.com',
//   port: 80,
//   path: '/MrWindlike/Windlike-Utils',
//   params: {
//     key: 'value',
//   },
// }
```