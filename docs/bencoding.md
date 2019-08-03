|		Type		|				Format				|		Example		|
|		----		|				------				|		------		|
|	Byte strings	|	`<string length>:<string data>`	|		`4: spam`	|
|	Integers		|	`i<integer>e`					|	`i3e`, `i-3e`	|
|	Lists			|	`l<bencoded values>e`			|	`l4:spam4:eggs` |
|	Dictionaries	|	`d<bencoded string><bencoded element>e` | `d3:cow3:moo4:spam` |
