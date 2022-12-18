# Leaflet

The up-to-date source code for Leaflet can be found [here](https://github.com/fireacademy/leaflet). On a high level, Leaflet is just a proxy that takes incoming HTTP endpoints, 'wraps' them with the right certificates, sends them to the Chia full node, and returns the response. It also has a readiness check endpoint on `/ready`.

Any POST request to Leaflet's port (18444) will be treated as one that needs to be proxied to the Chia full node RPC.

## Allowed endpoints

```typescript
export const ALLOWED_METHODS: string[] = [
  'get_blockchain_state',
  'get_block',
  'get_blocks',
  'get_block_count_metrics',
  'get_block_record_by_height',
  'get_block_record',
  'get_block_records',
  'get_unfinished_block_headers',
  'get_network_space',
  'get_additions_and_removals',
  'get_network_info',
  'get_recent_signage_point_or_eos',
  'get_coin_records_by_puzzle_hash',
  'get_coin_records_by_puzzle_hashes',
  'get_coin_record_by_name',
  'get_coin_records_by_names',
  // 'get_coin_records_by_parent_ids',
  'get_coin_records_by_hint',
  'push_tx',
  'get_puzzle_and_solution',
  'get_all_mempool_tx_ids',
  'get_all_mempool_items',
  'get_mempool_item_by_tx_id',
  'get_routes',
  'healthz',
];
```

## Note on \`get\_coin\_records\_by\_parent\_ids\`

`get_coin_records_by_parent_ids` was disabled because it takes a lot of time (and resources) to execute. We recommend getting the puzzle and solution for each parent coin, running them, and deriving the children from there.
