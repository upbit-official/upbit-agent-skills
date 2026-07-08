# Orderbooks

## Get Orderbook

| Name | Required | Description |
|------|:--------:|-------------|
| `markets` | ✓ | List of trading pairs to query. |
| `level` |  | Orderbook aggregation level. Only supported for KRW markets. |
| `count` |  | Number of orderbook entries to retrieve. |

```sh
upbit orderbooks list \
  --markets "KRW-BTC,KRW-ETH" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## List Orderbook Instruments

| Name | Required | Description |
|------|:--------:|-------------|
| `markets` | ✓ | List of trading pairs to query. |

```sh
upbit orderbooks list-instruments \
  --markets "KRW-BTC,KRW-ETH" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---
