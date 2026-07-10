# 📅 Day 09 - Multimedia in HTML (Video, Audio, SVG & iFrames)

## 🎯 What I Learned Today

- Adding videos in HTML
- Video attributes
- Adding audio in HTML
- Audio attributes
- SVG (Scalable Vector Graphics)
- iFrames

---

# 🎥 HTML Video

The `<video>` tag is used to embed videos directly into a webpage without requiring external plugins.

### Basic Syntax

```html
<video src="video.mp4" controls></video>
```

---

## Video Attributes

### 1. src

The `src` attribute specifies the path of the video file.

```html
<video src="video.mp4" controls></video>
```

**Example:**

```html
<video src="nature.mp4" controls></video>
```

---

### 2. controls

Displays built-in video controls such as:

- Play
- Pause
- Volume
- Full Screen
- Timeline

```html
<video src="video.mp4" controls></video>
```

Without `controls`, users cannot interact with the video.

---

### 3. autoplay

Automatically starts playing the video when the page loads.

```html
<video src="video.mp4" autoplay></video>
```

> Modern browsers usually allow autoplay only when the video is muted.

---

### 4. loop

Makes the video restart automatically after it ends.

```html
<video src="video.mp4" loop controls></video>
```

---

### 5. muted

Starts the video with the sound turned off.

```html
<video src="video.mp4" muted controls></video>
```

Useful together with `autoplay`.

---

### 6. poster

Displays an image before the video starts.

```html
<video src="video.mp4"
       poster="thumbnail.jpg"
       controls>
</video>
```

Think of it as the video's thumbnail.

---

### 7. width & height

Used to change the video's display size.

```html
<video
    src="video.mp4"
    width="500"
    height="300"
    controls>
</video>
```

You can use only width, and the height adjusts automatically.

---

## Complete Video Example

```html
<video
    src="nature.mp4"
    controls
    autoplay
    muted
    loop
    poster="thumbnail.jpg"
    width="600">
</video>
```

---

# 🎵 HTML Audio

The `<audio>` tag is used to play audio files on a webpage.

### Basic Syntax

```html
<audio src="song.mp3" controls></audio>
```

---

## Audio Attributes

### 1. src

Specifies the audio file.

```html
<audio src="song.mp3"></audio>
```

---

### 2. controls

Shows audio controls like:

- Play
- Pause
- Volume
- Timeline

```html
<audio src="song.mp3" controls></audio>
```

---

### 3. autoplay

Automatically starts the audio.

```html
<audio src="song.mp3" autoplay></audio>
```

> Browsers usually block autoplay unless muted or initiated by the user.

---

### 4. loop

Repeats the audio continuously.

```html
<audio src="song.mp3" controls loop></audio>
```

---

### 5. muted

Starts the audio with no sound.

```html
<audio src="song.mp3" muted controls></audio>
```

---

### 6. preload

Specifies how much audio should be loaded before playback.

Possible values:

### none

Loads nothing initially.

```html
<audio src="song.mp3" preload="none" controls></audio>
```

---

### metadata

Loads only basic information.

```html
<audio src="song.mp3" preload="metadata" controls></audio>
```

---

### auto

Browser decides to load the complete audio.

```html
<audio src="song.mp3" preload="auto" controls></audio>
```

---

## Complete Audio Example

```html
<audio
    src="song.mp3"
    controls
    autoplay
    muted
    loop
    preload="auto">
</audio>
```

---

# 🖼 SVG (Scalable Vector Graphics)

SVG stands for **Scalable Vector Graphics**.

It is used to create graphics using XML instead of pixels.

Unlike normal images, SVGs never lose quality when zoomed.

### Advantages

- Infinite scaling
- Small file size
- Editable using code
- Great for icons and logos
- Fast loading

---

## Basic SVG Example

```html
<svg width="200" height="200">
    <circle
        cx="100"
        cy="100"
        r="80"
        fill="blue"/>
</svg>
```

This creates a blue circle.

---

## Another Example

```html
<svg width="300" height="150">
    <rect
        width="300"
        height="150"
        fill="orange"/>
</svg>
```

This creates an orange rectangle.

---

## Where SVG is Used

- Logos
- Icons
- Graphs
- Charts
- Animations
- Illustrations
- UI Elements

---

# 🖥 iFrames

An **iFrame** (Inline Frame) is used to embed another webpage inside your webpage.

### Basic Syntax

```html
<iframe src="https://example.com"></iframe>
```

---

## Example

```html
<iframe
    src="https://www.wikipedia.org"
    width="800"
    height="500">
</iframe>
```

---

## Common iFrame Attributes

### src

Specifies the webpage to display.

```html
<iframe src="https://example.com"></iframe>
```

---

### width

Sets the width.

```html
width="600"
```

---

### height

Sets the height.

```html
height="400"
```

---

### title

Provides a description for accessibility.

```html
<iframe
    src="https://example.com"
    title="Example Website">
</iframe>
```

---

## Embedding YouTube Video

```html
<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="YouTube video">
</iframe>
```

---

# 📌 Quick Revision

## Video Tag

| Attribute | Purpose |
|----------|----------|
| src | Video file path |
| controls | Shows video controls |
| autoplay | Starts automatically |
| loop | Repeats video |
| muted | Starts with no sound |
| poster | Thumbnail image |
| width | Video width |
| height | Video height |

---

## Audio Tag

| Attribute | Purpose |
|----------|----------|
| src | Audio file path |
| controls | Shows controls |
| autoplay | Plays automatically |
| loop | Repeats audio |
| muted | Starts muted |
| preload | Controls loading behavior |

---

## SVG

- XML-based graphics
- Infinite scaling
- Best for logos and icons
- Lightweight
- High quality

---

## iFrame

- Embeds another webpage
- Can embed YouTube videos
- Can display maps
- Can show external websites
- Uses `src`, `width`, `height`, and `title`

---

# ⭐ Key Takeaways

- `<video>` is used to add videos.
- `<audio>` is used to play audio files.
- `controls` lets users interact with media.
- `autoplay` often requires `muted`.
- `poster` displays a video thumbnail.
- `preload` controls audio loading.
- SVG graphics remain sharp at every zoom level.
- iFrames allow embedding webpages, maps, videos, and other external content inside your website.
