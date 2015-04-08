# watchify-bug

a small example project to reproduce an outstanding bug in watchify that causes infinite rebuilds.

## how to reproduce

```bash
# install example
git clone https://github.com/ahdinosaur/watchify-bug
cd watchify-bug
npm install

# run watchify
npm run watch
```

actual output:

```
> watchify-bug@1.0.0 watch /home/michael/repos/ahdinosaur/watchify-bug
> watchify . -o bundle.js -v

129006 bytes written to bundle.js (0.68 seconds)
129006 bytes written to bundle.js (0.09 seconds)
129006 bytes written to bundle.js (0.03 seconds)
129006 bytes written to bundle.js (0.04 seconds)
129006 bytes written to bundle.js (0.03 seconds)
... forever and ever ...
```

expected output:

```
> watchify-bug@1.0.0 watch /home/michael/repos/ahdinosaur/watchify-bug
> watchify . -o bundle.js -v

129006 bytes written to bundle.js (0.68 seconds)
```
