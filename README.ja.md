<div align="center">

![Last commit](https://img.shields.io/github/last-commit/Comamoca/baserepo?style=flat-square)
![Repository Stars](https://img.shields.io/github/stars/Comamoca/baserepo?style=flat-square)
![Issues](https://img.shields.io/github/issues/Comamoca/baserepo?style=flat-square)
![Open Issues](https://img.shields.io/github/issues-raw/Comamoca/baserepo?style=flat-square)
![Bug Issues](https://img.shields.io/github/issues/Comamoca/baserepo/bug?style=flat-square)

<img src="https://emoji2svg.deno.dev/api/🦊" alt="eyecatch" height="100">

# 🦊 tefu

Techful向けのローカルテストツール

<br>
<br>

</div>

<table>
  <thead>
    <tr>
      <th style="text-align:center">🍡日本語</th>
      <th style="text-align:center"><a href="README.md">🍔English</a></th>
    </tr>
  </thead>
</table>

<div align="center">

</div>

## 🚀 使い方


まず始めに、`tefu.toml`というテスト用のファイルを用意します。
`tefu.toml`の書き方は以下の通りです。

```toml
[[case]]
input = """
1
2 3
test
"""

output = """
6
test
"""
```

`input`はプログラムに入力される値です。
`output`はプログラムが出力することが期待される値です。

`input`や`output`は**複数行文字列である必要があります**。

`tefu.toml`ファイルが用意できたら`tefu`コマンドを実行します。
実行すると以下のような出力が表示されるはずです。

```
╒══════════╤══════════╤══════════╤══════════╕
│ INPUT    │ OUTPUT   │ RESULT   │ STATUS   │
╞══════════╪══════════╪══════════╪══════════╡
│ 1        │ 6        │ 6        │ PA       │
│ 2 3      │ test     │ test     │          │
│ test     │          │          │          │
├──────────┼──────────┼──────────┼──────────┤
│ 72       │ 456      │ 456      │ PA       │
│ 128 256  │ myonmyon │ myonmyon │          │
│ myonmyon │          │          │          │
╘══════════╧══════════╧══════════╧══════════╛
```

## ⬇️  Install

`pip install tefu`

## ⛏️   開発

このプロジェクトは[`rye`](https://rye-up.com/)を採用しています。

```sh
git clone https://github.com/Comamoca/tefu
cd ./tefu

rye sync

# execute tefu
rye run tefu

# run test
rye run pytest
```

## 📝 Todo

- [ ] 例外処理の追加。

## 📜 ライセンス

MIT

### 🧩 Modules

- [tabulate](https://github.com/gregbanks/python-tabulate)

## 👏 影響を受けたプロジェクト

- [pytest](https://github.com/pytest-dev/pytest)
