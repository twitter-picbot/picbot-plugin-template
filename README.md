# picbot-plugin-template

Template with the interface every plugin must expose in order to be used by twitter-picbot.

## Interface

The plugin will be required by its `index.js` or the main script defined in `package.json`
which should export the following:

```
module.exports = {
  /**
   * Gets source of an image related to the query.
   * @param {string} query - topic of the image.
   * @return {Promise} promise handler.
   */
  getSource: function(query) { ... }
}
```

Resolving an object:

```
{
  url: 'image-url',
  source: 'image-source' // deviantart post, tumblr post, zerochan post, google...
}
```

## Development tips

- Remember to include all files necessary for your plugin in a path under the root
of it.
- Remember to document everything related to credentials, functions, changelog, readme...
- Don't upload your keys!

## Using the plugin

Once your plugin is ready to integrate, place it under `plugins` directory of
twitter-picbot with a distinct name, add and install necessary dependencies in
twitter-picbot and it will be randomly used amongst other plugins that you
installed in your twitter-picbot!
