# toml-config-example

```

# default unless overridden by child settings
[locale]
audio = ja-JP
subtitle = de-DE

[locale.archive]
audio = [ ja-JP, en-US ] # this would override the default
subtitle = de-DE

[locale.download]
audio = en-US
subtitle = de-DE

[output]
format = "S{season_number}E{episode_number}"
preset = nvidia-h264-lossless

[output.archive]
#format = "S{season_number}E{episode_number}"
merge = audio

[output.download]
#format = "S{season_number}E{episode_number}"
#container = mp4
```
