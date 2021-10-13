# discord-fetch v1
Easy-to-use Discord API requests using node-fetch

## Instalation
`git clone https://github.com/ZumoDev/discord-fetch`

## Methods

`req(path[options])`

Returns a HTTPS request to 'https://discord.com/api/v9/path'

- `path`: The path to make the request to
- `object`: Request headers, body, etc.

## Example Usage

```js
const req = require('./discord-fetch')

const object = {
    method: 'METHOD',
    headers: {
        Authorization: 'my_super_secret_token'
    }
}

req('path', object)
.then(res => console.log(res))
```

### Get username Example

```js
const req = require('./discord-fetch')

const object = {
    method: 'GET',
    headers: {
        Authorization: 'my_token'
    },
}

req('/users/879785357800009788', object)
.then(res => console.log(res.username))
```

## Credits
- Zumo#0662 | Main Developer
