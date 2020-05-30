## Ramdom one liners that can be entered into the browser console

#### get the current language
```javascript
kiwi.i18n.language
```

#### set current language to dev
```javascript
kiwi.i18n.changeLanguage('dev')
```

#### set the current theme to radioactive
```javascript
kiwi.themes.setTheme('radioactive')
```

#### set a custom theme url 
requires custom theme to be in config
```javascript
kiwi.themes.setCustomThemeUrl('https://cdn.rawgit.com/timkrumenacker/kiwiirc-themes/0acb6ce9/IE-ified/gruvbox-dark/theme.css')
```

#### get a setting
```javascript
kiwi.state.setting('settings.buffers.timestamp_format')
```

#### set a setting
```javascript
kiwi.state.setting('buffers.timestamp_format', '%H:%M')
```

#### set show_raw to true on current network
```javascript
kiwi.state.getActiveNetwork().setting('show_raw', true)
```

#### count of privmsg's in a channel
```javascript
_.filter(kiwi.state.getActiveBuffer().getMessages(), {type: "privmsg"}).length;
```

#### watch for all events
```javascript
kiwi.on('all', function(name, event){ console.log(name, event); })
```

### divert *raw to console
```javascript
kiwi.state.setting('showRaw',true);kiwi.on('message.new',(ev)=>{if(ev.buffer.name==='*raw')console.log(ev.message.message)});
```
