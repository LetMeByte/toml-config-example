# toml-config-example

```toml
[auth]
login = [ "user@mail.com", "password123" ]

[connection]
proxy = "socks5://1.2.3.4:123"

[locale]
audio = ja-JP
subtitle = de-DE
# keep_subs = no

[locale.archive]
audio = [ ja-JP, en-US ]
keep_subs = yes

[locale.download]
audio = en-US

[output]
format = "S{season_number}E{episode_number}"
preset = nvidia-h264-lossless
# skip_existing = no
batch_mode = yes

[output.archive]
format = "S{season_number}E{episode_number} - {episode_name}"
resolution = 1080p
# container = mkv
preset = none
merge = audio

[output.download]
# container = mp4
resolution = 720p
skip_existing = yes
```
