# Pockets

## List Pockets
Auth required

```sh
upbit pockets list --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## Get Sub-Pocket Balance
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `uuid` | ✓ | UUID of the sub-pocket to query. |

```sh
upbit pockets retrieve-balance \
  --uuid "9ca023a5-851b-4fec-9f0a-48cd83c2eaae" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## Universal Transfer
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `from` |  | UUID of the sending pocket. |
| `to` | ✓ | UUID of the receiving pocket. |
| `currency` | ✓ | Asset code to transfer. |
| `amount` | ✓ | Asset quantity to transfer. |
| `identifier` |  | Client-provided identifier for the asset transfer request. |

```sh
upbit pockets universal-transfer \
  --from "9ca023a5-851b-4fec-9f0a-48cd83c2eaae" \
  --to "9ca023a5-851b-4fec-9f0a-48cd83c2eaae" \
  --currency "XRP" \
  --amount "10.00" \
  --identifier "unique_transfer_id_20260531_01" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## List Universal Transfers
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `from` |  | UUID of the pocket that sent the asset. |
| `to` |  | UUID of the pocket that received the asset. |
| `states` |  | Asset transfer request states. Available values: `submitted`, `processing`, `done`, `failed`. |
| `uuids` |  | List of UUIDs identifying asset transfer requests. |
| `identifiers` |  | List of client-provided identifiers specified when requesting transfers. |
| `start_time` |  | Start time of the query period. |
| `end_time` |  | End time of the query period. |
| `currency` |  | Asset code to query. |
| `limit` |  | Number of results to request (default 20, max 100). |
| `order_by` |  | Sort order. `asc` for oldest first, `desc` for newest first. |

```sh
upbit pockets list-universal-transfers \
  --state "processing" \
  --state "done" \
  --currency "XRP" \
  --limit 2 \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## Transfer
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `to` | ✓ | UUID of the receiving pocket. |
| `currency` | ✓ | Asset code to transfer. |
| `amount` | ✓ | Asset quantity to transfer. |
| `identifier` |  | Client-provided identifier for the asset transfer request. |

```sh
upbit pockets transfer \
  --to "9ca023a5-851b-4fec-9f0a-48cd83c2eaae" \
  --currency "XRP" \
  --amount "10.00" \
  --identifier "unique_transfer_id_20260531_01" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## List Transfers
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `direction` |  | Transfer direction. — `in`: Transfers into the sub-pocket, `out`: Transfers out of the sub-pocket, `all`: Transfers in all directions |
| `states` |  | Asset transfer request states. |
| `uuids` |  | List of UUIDs identifying asset transfer requests. |
| `identifiers` |  | List of client-provided identifiers specified when requesting transfers. |
| `start_time` |  | Start time of the query period. |
| `end_time` |  | End time of the query period. |
| `currency` |  | Asset code to query. |
| `limit` |  | Number of results to request (default 20, max 100). |
| `order_by` |  | Sort order. `asc` for oldest first, `desc` for newest first. |

```sh
upbit pockets list-transfers \
  --direction "out" \
  --currency "XRP" \
  --limit 2 \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---

## List Pocket API Keys
Auth required

| Name | Required | Description |
|------|:--------:|-------------|
| `uuids` |  | Array of pocket UUIDs to query. |
| `include_expired` |  | Whether to include expired API keys in the results. |

```sh
upbit pockets list-api-keys \
  --uuid "9ca023a5-851b-4fec-9f0a-48cd83c2eaae" \
  --header 'X-Upbit-Initiator: upbit-cli-skill/{metadata.version}'
```

---
