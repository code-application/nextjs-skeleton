# プロジェクトの技術選定

## プロダクションコードに必要なライブラリ

実行に影響があるため、バージョンの指定には注意すること。

### ランタイムなど

- **[Node.js](https://nodejs.org/ja/)**  
  JavaScriptの実行環境。  
  （選定理由）JavaScriptランタイムのデファクトスタンダードであり、多くのライブラリが対応しているため。  
  （バージョン）[リリース一覧](https://nodejs.org/en/about/previous-releases/)にある ACTIVE LTS のバージョンをインストールする。  
- **[TypeScript](https://www.typescriptlang.org/)**  
  JavaScript に静的型付けを追加した言語。  
  （選定理由）JavaScript の型安全性を向上させるため。  
  （バージョン）[リリース一覧](https://github.com/microsoft/TypeScript/releases/)にある最新の Stable バージョンをインストールする。  

### フレームワーク

- **[Next.js](https://nextjs.org/)**  
  React ベースのフレームワーク。  
  （選定理由）React は Vue.js や Angular と比べて使用人口が多く、インターネット上に情報が多いため開発しやすい。また、多くの企業が採用していることから、働く場所を変える際にもスキルが活かせると考えられる。  
  （バージョン）[リリース一覧](https://github.com/vercel/next.js/releases/)にある Latest バージョンをインストールする。  
- **[Tailwind CSS](https://tailwindcss.com/)**  
  ユーティリティ指向で柔軟なスタイルが適用可能なオープンソースのCSS フレームワーク。  
  （選定理由）UIコンポーネントライブラリだけだと自由度が低いため、デザインの微調整ができるようにCSSのベースとしては Tailwind CSS を採用する。  
  （バージョン）[リリース一覧](https://github.com/tailwindlabs/tailwindcss/releases/)にある Latest バージョンをインストールする。  

## 開発・CI/CD・テスト関連のツール

### ランタイム・パッケージ管理

- **[Volta](https://volta.sh/)**  
  プロジェクトの Node.js 、pnpm のバージョンを管理するためのツール。  
  （選定理由）マルチプラットフォーム対応で、高速に動作し、パッケージマネージャーのバージョンまで管理できるため。  
- **[pnpm](https://pnpm.io/)**  
  プロジェクトのパッケージ管理を行うためのツール。  
  （選定理由）npm や yarn に比べて高速で、ディスク容量を節約できるため。2024年9月現在、多くのNode.jsライブラリのインストール手順にpnpmの対応がされていて十分にシェアを持っていると判断できる。  

### 静的解析・フォーマッター

- **[Biome](https://biomejs.dev/ja/)**  
  静的解析・フォーマッターを統合したツール。  
  （選定理由）リンターとフォーマッターを統合していて設定ファイルを一つにまとめることができ、開発の時間を短縮できる。また、ESLintやPrettierと比べて高速であり、設定の97%以上に互換性があるため。  

### テスト

- **[Jest](https://jestjs.io/ja/)**  
  テストフレームワーク。  
  （選定理由）Next.jsでのテストにおいて、Jestがデファクトスタンダードであるため。  
- **[React Testing Library](https://testing-library.com/)**  
  React コンポーネントのテストを行うためのライブラリ。  
  （選定理由）Reactコンポーネントのテストを行うためにJestと組み合わせて使用するライブラリとして、React Testing Libraryがデファクトスタンダードであるため。  

### コミットメッセージ管理とスタイル統一

- **[Husky](https://typicode.github.io/husky/)**  
  Git hooks を管理するためのツール。  
  （選定理由）使い慣れてるから。特にこだわりはないので他で代用可能。  