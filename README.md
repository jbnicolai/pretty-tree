# color-tree

Make colorful trees out of JSON objects using [archy](https://github.com/substack/node-archy)

	npm install color-tree

## Usage

``` js
var tree = require('color-tree');

var str = tree({
	label: '(root)', // the label of this node
	nodes: [{
		label: '(child)',
		leaf: {
			hello: 'world',
			hej: 'verden'
		}
	}]
});

console.log(str);
```

The above example results in the following output:

![example](https://raw.github.com/mafintosh/color-tree/master/example.png)

The node passed to tree can contain the following options

``` js
tree({
	label: '(child)', // an optional lable of this node
	leaf: {           // set this if you want to print an object
		key: value,
		...
	},
	nodes: [          // or put in some child nodes
		child_nodes_with_same_structure
	]
})
```

Note you can't have both `.nodes` and `.leaf`

## License

MIT