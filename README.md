# my docker compose for homepage development

I am not sure this setup is correct. I don't have much experience debugging node apps running in a docker container, 
but this works form development workflow. 

## debugging 

1. Run `docker compose up --build -d`
2. Navigate to `chrome://inspect/`
3. Click inspect underneath Target: `/usr/local/bin/pnpm
file:///usr/local/lib/node_modules/pnpm/bin/pnpm.cjs`
>*NOTE*: If the target does not exist, ensure  `Target discovery settings` contains `127.0.0.1:9229`.
4. Chrome devtools will open. Click continue in debugger. 
5. Navigate to `http://localhost:3000/`
6. Nagivate back to Chrome devtools to set breakpoints
7. Happy debugging! 
