# Spotify.ahk
An AutoHotkey wrapper for the Spotify web API designed to allow control over Spotify's internal volume slider and provide various other functionality.

Uses a slightly modified version of the AHKhttp library by zhamlin (https://github.com/zhamlin/AHKhttp) and the AHKsock library by jleb (https://github.com/jleb/AHKsock)


Usage - 
Create a new Spotify object, and call `%SpotifyObjectName%.Util.IsReady()` to check if user authorization is complete.
```
loop {
  Sleep, -1
} until (%SpotifyObject.Util.InternalIsReady() = true)
```
Once you create a new Spotify object, a Spotify app authorization page will open in your default browser, and you will be prompted to authorize Spotify.ahk. 
While you can choose not to authorize Spotify.ahk, all functionality will be lost without a valid authorization token. Additionally, thanks to Spotify's refreshable user authorization, you will only need to use the browser to authorize Spotify.ahk occasionally after the first run.
