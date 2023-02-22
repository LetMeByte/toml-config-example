# toml-config-example

```
[locale]
audio = ja-JP
subtitle = de-DE

[locale.archive]
audio = [ ja-JP, en-US ]

[locale.download]
audio = en-US

[output]
format = "S{season_number}E{episode_number}"
preset = nvidia-h264-lossless

[output.archive]
format = "S{season_number}E{episode_number} - {episode_name}"
resolution = 1080p
#container = mkv
preset = none
merge = audio

[output.download]
#container = mp4
resolution = 720p

```
