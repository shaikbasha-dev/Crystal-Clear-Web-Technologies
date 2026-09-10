# 11. HTML Multimedia

HTML5 allows us to put **audio and video directly inside a webpage**.

Think of a webpage like a small media player:

* `<audio>` → plays **sound/music**
* `<video>` → plays **video**
* `<source>` → tells the browser **where the media file is**
* `controls` → gives the user **play, pause, volume, etc.**
* `width` / `height` → control the size of a video

---

# Part A — HTML Audio

## 1. What is `<audio>`?

The `<audio>` tag is used to **embed/play audio in an HTML webpage**.

For example, you can use it to play:

* Songs
* Voice recordings
* Podcasts
* Sound effects
* Audio lessons

### Basic syntax

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

The browser creates an audio player.

Conceptually:

```text
┌────────────────────────────────────┐
│ ▶  ━━━━━━━━━━━ 🔊                 │
└────────────────────────────────────┘
       Audio Player
```

---

# 2. `controls` Attribute

Without `controls`, the browser normally doesn't provide the standard visible audio controls.

```html
<audio controls>
```

`controls` tells the browser:

> "Show the user the audio controls."

The controls can include things such as:

* Play
* Pause
* Volume
* Progress/seek bar

### Example

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

### Easy memory

**`controls` = Give the user buttons to control the media.**

---

# 3. `<source>` Tag

The `<source>` element specifies the **media file that should be played**.

Example:

```html
<source src="song.mp3" type="audio/mpeg">
```

It has two important attributes here:

```text
src  → Where is the audio file?
type → What type/format is the audio?
```

---

# 4. `src` in `<source>`

`src` specifies the location of the audio file.

Example:

```html
<source src="song.mp3">
```

If the file is inside a folder:

```text
website/
│
├── index.html
└── audio/
    └── song.mp3
```

Then:

```html
<source src="audio/song.mp3">
```

---

# 5. `type` Attribute for Audio

`type` tells the browser the **MIME/media type** of the file.

Example:

```html
<source src="song.mp3" type="audio/mpeg">
```

Here:

```text
song.mp3
   ↓
audio/mpeg
```

Some common audio types:

| File   | Type         |
| ------ | ------------ |
| `.mp3` | `audio/mpeg` |
| `.ogg` | `audio/ogg`  |
| `.wav` | `audio/wav`  |

For your basic learning, remember:

```html
type="audio/mpeg"
```

for MP3 audio.

---

# 6. Complete Audio Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Audio Example</title>
</head>

<body>

<h1>My Audio</h1>

<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>

</body>
</html>
```

### Flow

```text
<audio>
   ↓
Create audio player
   ↓
controls
   ↓
Show player controls
   ↓
<source>
   ↓
Find the audio file
   ↓
src
   ↓
song.mp3
   ↓
type
   ↓
audio/mpeg
```

---

# 7. Why Do We Put `<source>` Inside `<audio>`?

You could commonly see:

```html
<audio controls src="song.mp3"></audio>
```

But the `<source>` approach is useful because you can provide **multiple possible audio sources**.

Example:

```html
<audio controls>

    <source src="song.mp3" type="audio/mpeg">
    <source src="song.ogg" type="audio/ogg">

</audio>
```

The browser can try the available sources and use a format it supports.

---

# Part B — HTML Video

# 8. What is `<video>`?

The `<video>` tag is used to **display/play video on a webpage**.

For example:

* Movies
* Tutorials
* Training videos
* Demonstrations
* Recorded lectures

### Basic syntax

```html
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

The browser displays a video player.

Conceptually:

```text
┌──────────────────────────────┐
│                              │
│                              │
│          VIDEO               │
│                              │
│                              │
├──────────────────────────────┤
│ ▶  ━━━━━━━━━━━ 🔊   ⛶       │
└──────────────────────────────┘
```

---

# 9. `controls` in `<video>`

Just like audio, `controls` displays the video controls.

```html
<video controls>
```

The user can generally:

* Play
* Pause
* Change volume
* Seek through the video
* Enter fullscreen

Example:

```html
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

---

# 10. `<source>` in Video

`<source>` specifies the video file.

```html
<source src="movie.mp4" type="video/mp4">
```

Here:

```text
src  → video file location
type → video format
```

---

# 11. `width` in Video

`width` specifies the width of the video player.

Example:

```html
<video width="500" controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

The video player is given a width of approximately **500 pixels**.

---

# 12. `height` in Video

`height` specifies the height of the video player.

Example:

```html
<video width="500" height="300" controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

So:

```text
width  = 500
height = 300
```

---

# 13. Complete Video Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Video Example</title>
</head>

<body>

<h1>My Video</h1>

<video width="600" height="400" controls>
    <source src="movie.mp4" type="video/mp4">
</video>

</body>
</html>
```

### What happens?

```text
<video>
   ↓
Create video player
   ↓
width + height
   ↓
Set player size
   ↓
controls
   ↓
Give user video controls
   ↓
<source>
   ↓
Find video file
   ↓
src="movie.mp4"
```

---

# 14. Multiple Video Sources

Just like audio, you can provide more than one source.

```html
<video width="600" height="400" controls>

    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">

</video>
```

The browser can choose a supported format.

---

# 15. Audio vs Video

| Feature    | Audio                               | Video                 |
| ---------- | ----------------------------------- | --------------------- |
| Main tag   | `<audio>`                           | `<video>`             |
| Purpose    | Play sound                          | Play video            |
| Source     | `<source>`                          | `<source>`            |
| `src`      | Audio file location                 | Video file location   |
| `type`     | `audio/...`                         | `video/...`           |
| `controls` | Player controls                     | Player controls       |
| `width`    | Not normally needed for basic audio | Controls video width  |
| `height`   | Not normally needed for basic audio | Controls video height |

---

# 16. Audio Example vs Video Example

### Audio

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

### Video

```html
<video width="600" height="400" controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

Notice the pattern:

```text
AUDIO
<audio>
    <source ...>
</audio>


VIDEO
<video>
    <source ...>
</video>
```

---

# 17. Important Difference: `<audio>` and `<source>`

Students sometimes think `<source>` itself plays the audio.

It doesn't.

Think of it this way:

```text
<audio>
    ↓
The PLAYER

<source>
    ↓
The FILE LOCATION
```

So:

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

means:

> **Create an audio player and give it this audio file.**

---

# 18. Important Difference: `<video>` and `<source>`

Same idea:

```text
<video>
    ↓
The VIDEO PLAYER

<source>
    ↓
The VIDEO FILE
```

Therefore:

```html
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

means:

> **Create a video player and give it this video file.**

---

# 19. Common Mistakes

### Mistake 1 — Using `href`

❌

```html
<audio href="song.mp3">
```

For the media source, use `src`.

✅

```html
<audio>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

---

### Mistake 2 — Forgetting `controls`

```html
<audio>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

The audio may be available, but the standard player controls are not displayed.

For a normal user-controlled player, use:

```html
<audio controls>
```

---

### Mistake 3 — Wrong file path

If your file is:

```text
audio/song.mp3
```

but you write:

```html
<source src="song.mp3">
```

the browser may not find it.

Correct:

```html
<source src="audio/song.mp3" type="audio/mpeg">
```

---

### Mistake 4 — Confusing `width` and `height`

Remember:

```text
width  → left ↔ right
height → up ↕ down
```

---

# 20. One Complete HTML Multimedia Program

```html
<!DOCTYPE html>
<html>

<head>
    <title>Multimedia</title>
</head>

<body>

<h1>My Audio</h1>

<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>

<h1>My Video</h1>

<video width="600" height="400" controls>
    <source src="movie.mp4" type="video/mp4">
</video>

</body>

</html>
```

This single webpage contains:

```text
HTML Page
   │
   ├── Audio Player
   │      └── song.mp3
   │
   └── Video Player
          └── movie.mp4
```

---

# 21. Quick Revision Table

| HTML       | Meaning                                   |
| ---------- | ----------------------------------------- |
| `<audio>`  | Creates an audio player                   |
| `<video>`  | Creates a video player                    |
| `<source>` | Specifies the media source                |
| `src`      | Specifies where the media file is located |
| `type`     | Specifies the media type/format           |
| `controls` | Displays media controls                   |
| `width`    | Specifies video width                     |
| `height`   | Specifies video height                    |

---

# 🧠 Final Memory Trick

Remember this pattern:

### AUDIO

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

**Audio → Source → File**

### VIDEO

```html
<video width="600" height="400" controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

**Video → Size + Controls → Source → File**

And the easiest way to remember the attributes:

```text
src      → WHERE is the file?
type     → WHAT TYPE is the file?
controls → CAN THE USER CONTROL it?
width    → HOW WIDE is the video?
height   → HOW TALL is the video?
```

### One-line interview answer

> **HTML5 multimedia elements `<audio>` and `<video>` allow audio and video content to be embedded directly into a webpage. The `<source>` element specifies the media file, `src` specifies its location, `type` specifies its format, `controls` displays playback controls, and `width`/`height` can specify video dimensions.**
