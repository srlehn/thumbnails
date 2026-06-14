# thumbnails

Generate and cache image thumbnails in Go.

[![PkgGoDev](https://pkg.go.dev/badge/github.com/srlehn/thumbnails)](https://pkg.go.dev/github.com/srlehn/thumbnails@main)
[![Go Report Card](https://goreportcard.com/badge/srlehn/thumbnails)](https://goreportcard.com/report/srlehn/thumbnails)
![Lines of code](https://tokei.rs/b1/github/srlehn/thumbnails?type=Go&category=code)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

```go
import "github.com/srlehn/thumbnails"

// Exactly one of size.X / size.Y must be 0 (the other sets the side; aspect ratio is kept).
img, err := thumbnails.OpenThumbnail("photo.jpg", image.Point{X: 256}, true)
```

Set `runThumbnailer` to also use installed system thumbnailer helpers where available.

## Platforms

Linux is fully supported; thumbnails are cached following the [freedesktop spec](https://specifications.freedesktop.org/thumbnail/latest/). Other platforms are a work in progress.

## License

See [LICENSE](LICENSE).
