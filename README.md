<div align="center">

![Last commit](https://img.shields.io/github/last-commit/Comamoca/tefu?style=flat-square)
![Repository Stars](https://img.shields.io/github/stars/Comamoca/tefu?style=flat-square)
![Issues](https://img.shields.io/github/issues/Comamoca/tefu?style=flat-square)
![Open Issues](https://img.shields.io/github/issues-raw/Comamoca/tefu?style=flat-square)
![Bug Issues](https://img.shields.io/github/issues/Comamoca/tefu/bug?style=flat-square)

<img src="https://emoji2svg.deno.dev/api/🦊" alt="eyecatch" height="100">

# tefu

Local testing tool for Techful. 

<br>
<br>


</div>

<table>
  <thead>
    <tr>
      <th style="text-align:center">🍔English</th>
      <th style="text-align:center"><a href="README.ja.md">🍡日本語</a></th>
    </tr>
  </thead>
</table>

<div align="center">

</div>

## 🚀 How to use

First, you must create testing file name to `tefu.toml`.
`tefu.toml` rule is below.

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

`input` is data to input program.
`output` is data that the program is expected to output.

`input` and `output` data **must use multi line sring**.

If you can prepare `tefu.toml`, run `tefu` command.
Then output like below.

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


## ⛏️   Development

This project use [`rye`](https://rye-up.com/).

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

- [ ] Add exception handling.

## 📜 License

MIT

### 🧩 Modules

- [tabulate](https://github.com/gregbanks/python-tabulate)

## 👏 Affected projects

- [pytest](https://github.com/pytest-dev/pytest)
