### Download a youtube video with best audio + best video:

```bash
yt-dlp -f bestaudio+bestvideo "<video-link>"
```

### Download a clip from a youtube video:

```bash
yt-dlp -f bestaudio+bestvideo --postprocessor-args "-ss hh:mm:ss -to hh:mm:ss" "<video-link>"
```
