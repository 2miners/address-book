# 🗒️ TON address book

This is an address book for [tonscan.org](https://tonscan.org) explorer. It is build automatically from `.yaml` files and published at [this url](https://address-book.tonscan.org/addresses.json).

Address book is used to substitute some popular or important TON addresses with human readable names: for example, `Ef8zMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzMzM0vF` will be shown as `Elector`. It is **not** used in search.

If you want to make a pull request, please commit to `source/[category].yaml` file only. Most likely you'll need `community.yaml` or `exchanges.yaml` file.

Entry structure must be as follows:

```yaml
# new line
- address: TON address in any format
  tonIcon: Special field, please don't fill it out
  name: Short name for your project, 3-32 symbols
  description: |-
    Please provide short description for your project.
    Any amount of text and links are allowed.
  type: Contract type (see below)
# new line
```

### Contract type
`type` field can either be empty (just don't use it in entry) or one of these values: `wallet`, `nft_collection`, `jetton`, `pool`. Use `wallet` type for _all_ wallets (including validator addresses) and uninit addresses.


## Building
```bash
npm install && npm run build
```
