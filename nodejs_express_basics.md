```
npm install

# To install globally
npm install -g

# To install a specific tag
# "latest" is the default tag
npm install <package-name>@<tag>
```

It reads the `package.json` and installs all dependencies.

```
node app.js
```

Where `app.js` is the starting point

### Scripts in `package.json`

If there are scripts in the `package.json` file

you can do

```
npm run start
```

`run` is the keyword. `start` is the name of the script

---

Development server part of `nodejs` is not recommended for production.

Use 

- supervisord
- forever
- pm2 (process manager 2)

#### To Start

```
pm2 start app.js -i 4
```

`-i 4` means it runs 4 instances of the app and automatically loadbalances it.

#### To Stop

```
pm2 delete app.js
```

