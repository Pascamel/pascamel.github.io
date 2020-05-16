---
layout: article
---

### .bash_profile

{% highlight Bash linenos %}
connect () { printf "\$1" | /opt/cisco/anyconnect/bin/vpn -s connect "Americas East"; }

alias disconnect='/opt/cisco/anyconnect/bin/vpn disconnect'
{% endhighlight %}

### Hammerspoon

{% highlight Lua linenos %}
mods = { 'ctrl', 'alt', 'cmd' }
animationDuration = 0

function createMoveWindow(rect)
  return function ()
    hs.window.focusedWindow():move(rect, nil, true, animationDuration)
  end
end

hs.hotkey.bind(mods, 'm', createMoveWindow({ x = 0.0, y = 0.5, w = 1.0, h = 1.0 }))

hs.hotkey.bind(mods, 'down', createMoveWindow({ x = 0.0, y = 0.5, w = 1.0, h = 0.5 }))
hs.hotkey.bind(mods, 'left', createMoveWindow({ x = 0.0, y = 0.0, w = 0.5, h = 1.0 }))
hs.hotkey.bind(mods, 'Right', createMoveWindow({ x = 0.5, y = 0.0, w = 0.5, h = 1.0 }))
hs.hotkey.bind(mods, 'up', createMoveWindow({ x = 0.0, y = 0.0, w = 1.0, h = 0.5 }))

hs.hotkey.bind(mods, '1', createMoveWindow({ x = 0.0, y = 0.0, w = 0.5, h = 0.5 }))
hs.hotkey.bind(mods, '2', createMoveWindow({ x = 0.5, y = 0.0, w = 0.5, h = 0.5 }))
hs.hotkey.bind(mods, '3', createMoveWindow({ x = 0.0, y = 0.5, w = 0.5, h = 0.5 }))
hs.hotkey.bind(mods, '4', createMoveWindow({ x = 0.5, y = 0.5, w = 0.5, h = 0.5 }))

hs.hotkey.bind(mods, '5', createMoveWindow({ x = 0.00, y = 0.00, w = 0.75, h = 0.75 }))
hs.hotkey.bind(mods, '6', createMoveWindow({ x = 0.25, y = 0.00, w = 0.75, h = 0.75 }))
hs.hotkey.bind(mods, '7', createMoveWindow({ x = 0.00, y = 0.25, w = 0.75, h = 0.75 }))
hs.hotkey.bind(mods, '8', createMoveWindow({ x = 0.25, y = 0.25, w = 0.75, h = 0.75 }))

hs.hotkey.bind(mods, 'c', createMoveWindow({ x = 0.25, y = 0.25, w = 0.5, h = 0.5 }))
hs.hotkey.bind(mods, 'd', createMoveWindow({ x = 0.25, y = 0.5, w = 0.5, h = 0.5 }))
hs.hotkey.bind(mods, 'e', createMoveWindow({ x = 0.05, y = 0, w = 0.9, h = 1 }))

hs.hotkey.bind(mods, 'k', createMoveWindow({ x = 0.0, y = 0, w = 0.9, h = 1 }))
hs.hotkey.bind(mods, 'l', createMoveWindow({ x = 0.1, y = 0, w = 0.9, h = 1 }))

hs.hotkey.bind({"cmd", "alt", "ctrl"}, "W", function()
  hs.alert.show("Hello Pascamel!")
end)
{% endhighlight %}
