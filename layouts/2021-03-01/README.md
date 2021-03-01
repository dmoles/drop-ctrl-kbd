This is a layout based on the Keychron K8 wireless mechanical keyboard,
similar to the previous layout from [2021-02-07](../2021-02-07), with the
following modifications:

1. Function keys send F11-F12 by default, and only send their media / brightness /
   Mission Control / etc. values when Fn is pressed.
2. LEDs are locked into a pattern that produces maximum readability when using 
   gray/red Keychron keycaps for modifier, function, and navigation keys (plus 
   `\|`, but white Drop Skylight keycaps for the other keys.

## Layout

Layer 0 (no modifiers):

![Layer 0](layer0.png "Layer 0")

Layer 1 (modified w/Fn)

![Layer 1](layer1.png "Layer 1")

## LED maps

Layer 0 (no modifiers):

![Layer 0 LEDs](leds-layer0.png "Layer 0 LEDs")

Layer 1 (modified w/Fn)

![Layer 1 LEDs](leds-layer1.png "Layer 1 LEDs")

## Required keyboard shortcuts

| Preference section | Shortcut            | Keys      |
| ---                | ---                 | ---       |
| Display            | Decrease brightness | F14       |
| Mission Control    | Mission Control     | ⌃↑        |
|                    | Application Windows | ⌃↓        |
| Services           | Toggle Microphone*  | ⌃⌥⇧⌘F10 † |

* This is an Automator 'quick action' with the script below

† Drop's configurator displays this as HYPR(KC_F10)

### Mic toggle AppleScript

```osascript
on run {input, parameters}
	set currentInputLevel to input volume of (get volume settings)
	
	if currentInputLevel is 0 then
		set volume input volume 65
	else
		set volume input volume 0
	end if
	
	return input
end run
```
