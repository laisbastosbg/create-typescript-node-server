# Step-by-step guide to create a new node server with typescript

1. Create project folder and enter it
```bash
mkdir [APPLICATION_NAME] & cd [APPLICATION_NAME]
```

2. Create package.json
```bash
yarn init -y
```

3. Install express
```bash
yarn add express
```

4. Install types for express
```bash
yarn add @types/express
```

5. Install typescript as a development dependency
```bash
yarn add typescript -D
```

6. Set project as a typescript project (create tsconfig.json)
```bash
yarn tsc --init
```

7. Set path to generate build
- Open tsconfig.json file and add the following line
```json
"outDir": "./dist",
```

8. Create scripts to build and run project
- Open package.json file and add the following lines
```json
"scripts": {
    "build": "yarn tsc",
    "dev": "node dist/server.js"
  }
```

- Your package.json file should look like this
```json
{
  "name": "typescript",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",
  "dependencies": {
    "@types/express": "^4.17.13",
    "express": "^4.17.1"
  },
  "devDependencies": {
    "typescript": "^4.4.3"
  },
  "scripts": {
    "build": "yarn tsc",
    "dev": "node dist/server.js"
  }
}
```