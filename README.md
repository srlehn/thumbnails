# thumbnails

Generate and cache image thumbnails in Go.

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
