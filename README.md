# crunchy-cli configuration file

## crunchy-cli.example.toml - a structural overview

```toml
[auth]
method = "credentials"
email = "spam@animail.jp"
password = "iLOVEanime123"

[connection]
proxy = "socks5://1.2.3.4:1234"
retries = 2

[locale]
audio = "ja-JP"
subtitle = "de-DE"
# keep_subs = false

[locale.archive]
audio = [ "ja-JP", "en-US" ]
keep_subs = true

[locale.download]
audio = "en-US"

[output]
format = "S{season_number}E{episode_number}"
preset = "nvidia-h264-lossless"
# skip_existing = false
batch_mode = true

[output.archive]
format = "S{season_number}E{episode_number} - {episode_name}"
resolution = "1080p"
# container = "mkv"
preset = "none"
merge = "audio"

[output.download]
# container = "mp4"
resolution = "720p"
skip_existing = true
```


## Detailed Configuration

### [auth] - Methods of Authentication

**You can download free content even without logging in, but you need a premium account to download premium content.**

Login using your account credentials:

```toml
[auth]
method = "credentials"
email = "spam@animail.jp"
password = "iLOVEanime123"
```

<hr>

Login using a refresh token:

```toml
[auth]
method = "etp-rt"
token = "your-etp-refresh-token"
```

<hr>

```toml
[auth]
method = "anonymous"
```


### [connection] - 

```
[connection]
proxy = none
retries = 0
```

