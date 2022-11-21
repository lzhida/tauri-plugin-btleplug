# Tauri Plugin demo

## 快速开始

```shell
# 运行示例
cd ./examples/svelte-app
yarn
yarn tauri dev

# 项目打标签
yarn release

# 打包项目
yarn build

```

## 使用方式

### RUST

在 `src-tauri/Cargo.toml` 文件中添加依赖:

```toml
[dependencies.tauri-plugin-spreadsheet]
git = "https://github.com/tauri-plugin-demo"
tag = "v0.1.0"
```

在 `src-tauri/src/main.rs` 文件中引用插件:

```RUST
use tauri_plugin_demo;

fn main() {
    tauri::Builder::default()
        .plugin(tauri_plugin_demo::init())
        .build()
        .run();
}
```

### WEBVIEW

在 `pacakge.json` 文件中添加依赖:

```json
  "dependencies": {
    "tauri-plugin-demo-api": "github:lzhida/tauri-plugin-demo#v0.1.0",
  }
```

或者在项目根目录下执行以下命令:

```
npm install https://github.com/lzhida/tauri-plugin-demo\#v0.1.0
# or
yarn add https://github.com/lzhida/tauri-plugin-demo\#v0.1.0
```

### 引用

在 `JavaScript` 或 `TypeScript` 文件中使用:

```TypeScript
import { execute } from 'tauri-plugin-demo-api';
```
