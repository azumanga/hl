# hl
Condensed version of boatbomber/Highlighter! Useful for external Lua execution tools.


Usage:
```Lua
local Highlighter = require(path.to.Highlighter)

Highlighter.highlight({
	-- The object to syntax highlight
	textObject: TextLabel | TextBox,
	 -- The source text for highlighting- defaults to textObject.Text
	src: string?,
	-- Update even if there are no changes since last highlight
	forceUpdate: boolean?,
	-- Lexer for tokenizing src, defaults to the bundled Lua lexer
	lexer: Lexer?,
})
```

Changing the highlight colors:
```Lua
Highlighter.setTokenColors({
	tokenName = Color3.new(...),
	...
})
-- Automatically triggers Highlighter.refresh() which updates existing highlights to the new colors
```
