## ディレクトリ作成、TypeScriptインストール
```bash
mkdir xxx
cd xxx

npm init --yes
npm install --save-dev typescript @types/node
```

## tsconfig.jsonの準備
### tsconfig.json作成
```
npx tsc --init
```

### targetコンパイラオプションの変更
```
"target": "es2020"
```

### moduleコンパイラオプションの変更
```
"module": "esnext"
```

### moduleResolutionコンパイラオプションの変更
```
"moduleResolution": "node"
```

### outDirコンパイラオプションの変更
```
"outDir": "./dist"
```

### includeオプションの追加
```json
{
  "compilerOptions": {
    // Many options.
  },
  // Add here
  "include": ["./src**/*.ts"]
}
```

## コンパイル
```bash
npx tsc
```

## 実行
```bash
node ./dist/index.js
```
