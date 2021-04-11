# Strapi Upload Provider for Digital Ocean Spaces
- This provider is a fork of [AdamZikmund's](https://github.com/AdamZikmund) [strapi upload provider](https://github.com/AdamZikmund/strapi-provider-upload-digitalocean) for Digital Ocean spaces.

This provider will upload to the space using the AWS S3 API.

## Parameters
- **key** : [Space access key](https://cloud.digitalocean.com/account/api/tokens)
- **secret** : [Space access secret](https://cloud.digitalocean.com/account/api/tokens)
- **endpoint** : Base URL of the space (e.g. 'fra.digitaloceanspaces.com')
- **space** : Name of the space in the Digital Ocean panel.
- **directory** : Name of the sub-directory you want to store your files in. (Optionnal - e.g. '/example')
- **cdn** : CDN Endpoint - URL of the cdn of the space (Optionnal - e.g. 'cdn.example.com')

## How to use

1. Install this package

```
npm i strapi-provider-upload-do
```

2. Create config in `./extensions/upload/config/settings.js` with content

```
module.exports = {
  provider: "do",
  providerOptions: {
    key: process.env.DO_SPACE_ACCESS_KEY,
    secret: process.env.DO_SPACE_SECRET_KEY,
    endpoint: process.env.DO_SPACE_ENDPOINT,
    space: process.env.DO_SPACE_BUCKET,
    directory: process.env.DO_SPACE_DIRECTORY,
    cdn: process.env.DO_SPACE_CDN,
  }
}
```

3. Create `.env` and add to them 

```
DO_SPACE_ACCESS_KEY
DO_SPACE_SECRET_KEY
DO_SPACE_ENDPOINT
DO_SPACE_BUCKET
DO_SPACE_DIRECTORY
DO_SPACE_CDN
```

with values obtained from tutorial:

> https://www.digitalocean.com/community/tutorials/how-to-create-a-digitalocean-space-and-api-key

Parameter `DO_SPACE_DIRECTORY` and `DO_SPACE_CDN` is optional and you can ommit them both in `.env` and `settings`.

## Resources

- [MIT License](LICENSE.md)

## Links

- [Strapi website](http://strapi.io/)
- [Strapi community on Slack](http://slack.strapi.io)
- [Strapi news on Twitter](https://twitter.com/strapijs)
- [Strapi docs about upload](https://strapi.io/documentation/3.0.0-beta.x/plugins/upload.html#configuration)

## Contributors
<a href="https://github.com/AdamZikmund"><img src="https://avatars.githubusercontent.com/u/4062779?v=3" title="AdamZikmund" width="80" height="80"></a>
<a href="https://github.com/gustawdaniel"><img src="https://avatars.githubusercontent.com/u/16663028?v=3" title="gustawdaniel" width="80" height="80"></a>
