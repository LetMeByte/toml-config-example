# crunchy-cli configuration reference

<!-- ## Table of Content -->
<!-- Authentication -->
<!-- Connection -->
<!-- Locales -->
<!-- Output -->

## Example Configuration

```toml
[auth]
method = "credentials"
email = "spam@animail.jp"
password = "iLOVEanime123"

[connection]
proxy = "socks5://proxy.host:8080"
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

## [auth] Methods of Authentication

**You can download free content without logging in, but you need a premium account to download premium content.**

### Authenticate using your account credentials:

```toml
[auth]
method = "credentials"
email = "spam@animail.jp"
password = "iLOVEanime123"
```

### Authenticate using a refresh token:

```toml
[auth]
method = "etp-rt"
token = "your-etp-refresh-token"
```

To extract a refresh token from your browser, you can use an addon like [cookies.txt](https://addons.mozilla.org/en-US/firefox/addon/cookies-txt/). Log into your account, then use the addon to extract the cookie called `etp_rt`. It will look like this: `306ce014-961f-49f5-bb17-5e1451246d4c`

### No authentication:

```toml
[auth]
method = "anonymous"
```


## [connection]

```toml
[connection]

# # Controls how often crunchy-cli will retry to download each file. 0 (disabled) by default, maximum is 10.
# retries = 0

# # Connect using a proxy
# proxy = "http://proxy.host:8080"
# proxy = "https://proxy.host:8080"
# proxy = "socks5://proxy.host:8080"
```

## [locale] Audio & Subtitles

The default locale for **audio** is `ja-JP`. The default locale for **subtitles** is your system locale. Should your system locale not be supported by Crunchyroll or not be available for the content you are tyring to download, the `en-US` locale will be used.
<!-- Fallback Handling? -->

```toml
[locale]
audio = "ja-JP"
subtitle = "de-DE"
# keep_subs = false

[locale.archive]
audio = [ "ja-JP", "en-US" ]
keep_subs = true

[locale.download]
audio = "en-US"
```

*The Crunchy-Labs Team does not endorse piracy, what you do with downloaded content is completely up to you!*
