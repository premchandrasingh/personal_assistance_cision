## make npm install always successful

	npm install --legacy-peer-deps

## List of packages installed globally
	npm ls -g 

More at https://www.warp.dev/terminus/list-installed-npm-packages

	
## Remove folder recursively using `npkill`

- Instlalation
	`npm i -g npkill`

	
- Usage
	1. `npkill` -- will search for default target folder 'node_module'. Can delete by pressing `space bar`
	2. `npkill -t "bin"` or `npkill -t "obj"` -- will search for custom target 'bin' or 'obj'
	3. `npkill -D` -- delete the folder as found without confirming
	
- My Experience

This was very useful to clean up 'node_module' and .net 'bin' and 'obj' folder while transfering data.

## Quickly run a static server using `http-server`

	$ cd my-website
	$ npx http-server
	> Starting up http-server, serving ./
	> Available on:
	>  http://192.168.36.65:8080
	>  http://127.0.0.1:8080
	> Hit CTRL-C to stop the server

## Other fun npm packages

	- npx cowsay goodbye! -- Display a messasge with figlet cow saying the message
	- npx https://gist.github.com/zkat/4bc19503fe9e9309e2bfaa2c58074d32  -- npx can run code directly from gist
	