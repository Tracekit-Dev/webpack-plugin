# @tracekit/webpack-plugin

TraceKit source map upload plugin for webpack. Automatically uploads source maps during your build for server-side symbolication of production errors.

## Installation

```bash
npm install @tracekit/webpack-plugin --save-dev
```

## Quick Start

Add the plugin to your `webpack.config.js`:

```javascript
const { TraceKitWebpackPlugin } = require('@tracekit/webpack-plugin');

module.exports = {
  plugins: [
    new TraceKitWebpackPlugin({
      apiKey: 'your-api-key',
      org: 'your-org',
      project: 'your-project',
    }),
  ],
};
```

## Configuration

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `apiKey` | `string` | Required | Your TraceKit API key |
| `org` | `string` | Required | Organization slug |
| `project` | `string` | Required | Project slug |
| `include` | `string` | `'dist/**/*.js'` | Glob pattern for files to upload |
| `dryRun` | `boolean` | `false` | Validate without uploading |

## Documentation

Full documentation: https://app.tracekit.dev/docs/frontend/source-maps

## License

MIT
