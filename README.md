https://javascript.plainenglish.io/build-a-react-component-library-using-typescript-storybook-86d3562aa53a

1. $ npm init
2. $ npm install --save-dev react react-dom @types/node @types/react @types/react-dom typescript
3. package.json "devDependencies": {
   "@types/node": "^20.2.1",
   "@types/react": "^18.2.6",
   "@types/react-dom": "^18.2.4",
   "react": "^18.2.0",
   "react-dom": "^18.2.0",
   "typescript": "^5.0.4"
   },
   "peerDependencies": {
   "react": "^18.2.0",
   "react-dom": "^18.2.0"
   }
4. "main": "dist/cjs/index.js",
   "module": "dist/esm/index.js",
   "files": ["dist"],
   "scripts": {
   "build":"rm -rf /dist && npm run build:esm && npm run build:cjs",
   "build:esm": "tsc",
   "build:cjs": "tsc --module CommonJS --outDir dist/cjs",
   "test": "echo \"Error: no test specified\" && exit 1"
   },
# component-library-react-typescript
