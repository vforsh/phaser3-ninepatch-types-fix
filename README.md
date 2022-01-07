### General info

(Better) typescript definitions for the https://github.com/koreezgames/phaser3-ninepatch-plugin

The original plugin comes with the definitions, but they have some issues:
- `GameObjectFactory` and `GameObjectCreatore` are not properly patched
- some properties of the `NinePatch` marked as `private` and I need them to be `public` for my 9-patch editor


### Usage
Install the package
```
npm install @robowhale/phaser3-ninepatch-types-fix
```

Then add `phaser3-ninepatch.d.ts` file to the `files` section of `tsconfig.json`
```
"files": [
    "node_modules/@robowhale/phaser3-ninepatch-types-fix/phaser3-ninepatch.d.ts"
]
```


### Typescript compiler warnings
Typescript will throw some warnings because these types conflicts with the original types. 
To suppress them add `"skipLibCheck": true` to your `tsconfig.json`
