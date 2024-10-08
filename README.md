### caddy file_server custom `browse.html` template with media extensions

**fork of [glowinthedark](https://github.com/glowinthedark/caddy-file-server-browse-extension)'s browse.html with a few personal tweaks and fixes**


Customized template for caddy [**`file_server`**](https://caddyserver.com/docs/caddyfile/directives/file_server). Compared to caddy's default [browse.html](https://github.com/caddyserver/caddy/blob/master/modules/caddyhttp/fileserver/browse.html) this template offers the following extra features:

- play all audios inline (with automatic sequential autoplay)
- dynamic preview mode for images, video, HTML and source code files without page reload
- image gallery mode with easy navigation using :arrow_left: & :arrow_right: keys
- play videos with VTT and SRT subtitles support
- markdown preview using [marked](https://github.com/markedjs/marked)
- code highlighting for common source file formats using [highlight](https://github.com/highlightjs/highlight.js)
- retain list/grid mode on navigation

### Usage

In your `Caddyfile` set the [**`browse`**](https://caddyserver.com/docs/caddyfile/directives/file_server#syntax) subdirective under `file_server` to point to the custom `browse.html` ([view source](https://github.com/SangeloDev/caddy-file-server-browse-extension/blob/master/browse.html)) file:

```Caddyfile
http:// {
    file_server {
        root /path/to/my/server/root
        browse /path/to/folder/caddy/templates/browse.html
    }
}
```

### Screenshots

#### inline audio player

![audio player](img/caddy_file_server.png)

#### markdown renderer

![markdown renderer](img/caddy_file_server_markdown.png)

#### source file highlighter

![source file highlighter](img/caddy_file_server_highlight.png)
