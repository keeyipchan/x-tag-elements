
## Syntax

The action bar a grouping of action that have 

```
<x-actionbar group="1">
	<x-action 
		group="1 2"
		command="new-content" 
		label="New" 
		icon="demo/plus.png">
	</x-action>
	<x-action
		group="2"
		command="refresh-content" 
		label="Refresh" 
		icon="demo/refresh.png">
	</x-action>
	<x-action
		group="1 2"
		command="more" 
		label="Advanced" 
		icon="demo/more-actions.png">
	</x-action>
<x-actionbar group="1">
```


### Live Example
<x-actionbar group="1">
	<x-action 
		group="1"
		command="new-content" 
		label="New" 
		icon="demo/plus.png">
	</x-action>
	<x-action
		group="1"
		command="refresh-content" 
		label="Refresh" 
		icon="demo/refresh.png">
	</x-action>
<x-actionbar group="1">

## Events
Command events are fired each time an action is clicked or pressed.

```
	document.getElementsByNames('x-actionbar')[0].addEventListener('command', function(e){
		var selectedCommand = e.command;
	});

```

## Usage

```
	var actionbar = document.getElementsByNames('x-actionbar')[0];
	// Change active group
	actionbar.group = 2;

	// listen for x-action click or press
	actionbar.addEventListen('command', function(e){
		switch(e.command){
			case 'more':
				actionbar.group = 2;
				break;
			// more commands
		}
	});

	actionbar.mode = "full";  // Show icons and text
	actionbar.mode = "icon";  // Show icons only
	actionbar.mode = "text";  // Show text

```


