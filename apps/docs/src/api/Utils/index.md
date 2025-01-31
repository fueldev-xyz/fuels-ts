# Module: @fuel-ts/utils

## Classes

- [DateTime](/api/Utils/DateTime.md)

## Variables

### defaultConsensusKey

• `Const` **defaultConsensusKey**: ``"0xa449b1ffee0e2205fa924c6740cc48b3b473aa28587df6dab12abc245d1f5298"``

#### Defined in

[packages/utils/src/utils/defaultSnapshotConfigs.ts:11](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/defaultSnapshotConfigs.ts#L11)

___

### defaultSnapshotConfigs

• `Const` **defaultSnapshotConfigs**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `chainConfigJson` | { `chain_name`: `string` = "local\_testnet"; `consensus`: { `PoA`: { `signing_key`: `string` = "0x94ffcc53b892684acefaebc8a3d4a595e528a8cf664eeb3ef36f1020b0809d0d" }  } ; `consensus_parameters`: { `V1`: { `base_asset_id`: `string` = "0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07"; `block_gas_limit`: `number` = 100000000; `chain_id`: `number` = 0; `contract_params`: { `V1`: { `contract_max_size`: `number` = 262144; `max_storage_slots`: `number` = 1760 }  } ; `fee_params`: { `V1`: { `gas_per_byte`: `number` = 63; `gas_price_factor`: `number` = 92 }  } ; `gas_costs`: { `V1`: { `add`: `number` = 2; `addi`: `number` = 2; `aloc`: `number` = 2; `and`: `number` = 2; `andi`: `number` = 2; `bal`: `number` = 86; `bhei`: `number` = 2; `bhsh`: `number` = 2; `burn`: `number` = 25770; `call`: { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } ; `cb`: `number` = 2; `ccp`: { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } ; `cfei`: `number` = 2; `cfsi`: `number` = 2; `contract_root`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } ; `croo`: { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } ; `csiz`: { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } ; `div`: `number` = 2; `divi`: `number` = 2; `eck1`: `number` = 3114; `ecr1`: `number` = 42270; `ed19`: `number` = 2878; `eq`: `number` = 2; `exp`: `number` = 2; `expi`: `number` = 2; `flag`: `number` = 1; `gm`: `number` = 2; `gt`: `number` = 2; `gtf`: `number` = 12; `ji`: `number` = 2; `jmp`: `number` = 2; `jmpb`: `number` = 1; `jmpf`: `number` = 1; `jne`: `number` = 2; `jneb`: `number` = 1; `jnef`: `number` = 1; `jnei`: `number` = 2; `jnzb`: `number` = 1; `jnzf`: `number` = 1; `jnzi`: `number` = 2; `k256`: { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } ; `lb`: `number` = 2; `ldc`: { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } ; `log`: `number` = 165; `logd`: { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } ; `lt`: `number` = 2; `lw`: `number` = 2; `mcl`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } ; `mcli`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } ; `mcp`: { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } ; `mcpi`: { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } ; `meq`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } ; `mint`: `number` = 29024; `mldv`: `number` = 3; `mlog`: `number` = 2; `mod_op`: `number` = 2; `modi`: `number` = 2; `move_op`: `number` = 2; `movi`: `number` = 2; `mroo`: `number` = 4; `mul`: `number` = 2; `muli`: `number` = 2; `new_storage_per_byte`: `number` = 63; `noop`: `number` = 1; `not`: `number` = 2; `or`: `number` = 2; `ori`: `number` = 2; `poph`: `number` = 3; `popl`: `number` = 3; `pshh`: `number` = 4; `pshl`: `number` = 4; `ret`: `number` = 134; `retd`: { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } ; `rvrt`: `number` = 153; `s256`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } ; `sb`: `number` = 2; `scwq`: { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } ; `sll`: `number` = 2; `slli`: `number` = 2; `smo`: { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } ; `srl`: `number` = 2; `srli`: `number` = 2; `srw`: `number` = 209; `srwq`: { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } ; `state_root`: { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } ; `sub`: `number` = 2; `subi`: `number` = 2; `sw`: `number` = 2; `sww`: `number` = 22501; `swwq`: { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } ; `time`: `number` = 50; `tr`: `number` = 33912; `tro`: `number` = 24294; `vm_initialization`: { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } ; `wdam`: `number` = 9; `wdcm`: `number` = 2; `wddv`: `number` = 5; `wdmd`: `number` = 10; `wdml`: `number` = 3; `wdmm`: `number` = 10; `wdop`: `number` = 3; `wqam`: `number` = 11; `wqcm`: `number` = 3; `wqdv`: `number` = 6; `wqmd`: `number` = 17; `wqml`: `number` = 4; `wqmm`: `number` = 10; `wqop`: `number` = 3; `xor`: `number` = 2; `xori`: `number` = 2 }  } ; `predicate_params`: { `V1`: { `max_gas_per_predicate`: `number` = 100000000; `max_message_data_length`: `number` = 102400; `max_predicate_data_length`: `number` = 102400; `max_predicate_length`: `number` = 102400 }  } ; `privileged_address`: `string` = "0000000000000000000000000000000000000000000000000000000000000000"; `script_params`: { `V1`: { `max_script_data_length`: `number` = 102400; `max_script_length`: `number` = 102400 }  } ; `tx_params`: { `V1`: { `max_bytecode_subsections`: `number` = 256; `max_gas_per_tx`: `number` = 100000000; `max_inputs`: `number` = 255; `max_outputs`: `number` = 255; `max_size`: `number` = 262144; `max_witnesses`: `number` = 255 }  }  }  }  } |
| `chainConfigJson.chain_name` | `string` |
| `chainConfigJson.consensus` | { `PoA`: { `signing_key`: `string` = "0x94ffcc53b892684acefaebc8a3d4a595e528a8cf664eeb3ef36f1020b0809d0d" }  } |
| `chainConfigJson.consensus.PoA` | { `signing_key`: `string` = "0x94ffcc53b892684acefaebc8a3d4a595e528a8cf664eeb3ef36f1020b0809d0d" } |
| `chainConfigJson.consensus.PoA.signing_key` | `string` |
| `chainConfigJson.consensus_parameters` | { `V1`: { `base_asset_id`: `string` = "0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07"; `block_gas_limit`: `number` = 100000000; `chain_id`: `number` = 0; `contract_params`: { `V1`: { `contract_max_size`: `number` = 262144; `max_storage_slots`: `number` = 1760 }  } ; `fee_params`: { `V1`: { `gas_per_byte`: `number` = 63; `gas_price_factor`: `number` = 92 }  } ; `gas_costs`: { `V1`: { `add`: `number` = 2; `addi`: `number` = 2; `aloc`: `number` = 2; `and`: `number` = 2; `andi`: `number` = 2; `bal`: `number` = 86; `bhei`: `number` = 2; `bhsh`: `number` = 2; `burn`: `number` = 25770; `call`: { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } ; `cb`: `number` = 2; `ccp`: { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } ; `cfei`: `number` = 2; `cfsi`: `number` = 2; `contract_root`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } ; `croo`: { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } ; `csiz`: { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } ; `div`: `number` = 2; `divi`: `number` = 2; `eck1`: `number` = 3114; `ecr1`: `number` = 42270; `ed19`: `number` = 2878; `eq`: `number` = 2; `exp`: `number` = 2; `expi`: `number` = 2; `flag`: `number` = 1; `gm`: `number` = 2; `gt`: `number` = 2; `gtf`: `number` = 12; `ji`: `number` = 2; `jmp`: `number` = 2; `jmpb`: `number` = 1; `jmpf`: `number` = 1; `jne`: `number` = 2; `jneb`: `number` = 1; `jnef`: `number` = 1; `jnei`: `number` = 2; `jnzb`: `number` = 1; `jnzf`: `number` = 1; `jnzi`: `number` = 2; `k256`: { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } ; `lb`: `number` = 2; `ldc`: { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } ; `log`: `number` = 165; `logd`: { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } ; `lt`: `number` = 2; `lw`: `number` = 2; `mcl`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } ; `mcli`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } ; `mcp`: { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } ; `mcpi`: { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } ; `meq`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } ; `mint`: `number` = 29024; `mldv`: `number` = 3; `mlog`: `number` = 2; `mod_op`: `number` = 2; `modi`: `number` = 2; `move_op`: `number` = 2; `movi`: `number` = 2; `mroo`: `number` = 4; `mul`: `number` = 2; `muli`: `number` = 2; `new_storage_per_byte`: `number` = 63; `noop`: `number` = 1; `not`: `number` = 2; `or`: `number` = 2; `ori`: `number` = 2; `poph`: `number` = 3; `popl`: `number` = 3; `pshh`: `number` = 4; `pshl`: `number` = 4; `ret`: `number` = 134; `retd`: { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } ; `rvrt`: `number` = 153; `s256`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } ; `sb`: `number` = 2; `scwq`: { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } ; `sll`: `number` = 2; `slli`: `number` = 2; `smo`: { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } ; `srl`: `number` = 2; `srli`: `number` = 2; `srw`: `number` = 209; `srwq`: { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } ; `state_root`: { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } ; `sub`: `number` = 2; `subi`: `number` = 2; `sw`: `number` = 2; `sww`: `number` = 22501; `swwq`: { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } ; `time`: `number` = 50; `tr`: `number` = 33912; `tro`: `number` = 24294; `vm_initialization`: { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } ; `wdam`: `number` = 9; `wdcm`: `number` = 2; `wddv`: `number` = 5; `wdmd`: `number` = 10; `wdml`: `number` = 3; `wdmm`: `number` = 10; `wdop`: `number` = 3; `wqam`: `number` = 11; `wqcm`: `number` = 3; `wqdv`: `number` = 6; `wqmd`: `number` = 17; `wqml`: `number` = 4; `wqmm`: `number` = 10; `wqop`: `number` = 3; `xor`: `number` = 2; `xori`: `number` = 2 }  } ; `predicate_params`: { `V1`: { `max_gas_per_predicate`: `number` = 100000000; `max_message_data_length`: `number` = 102400; `max_predicate_data_length`: `number` = 102400; `max_predicate_length`: `number` = 102400 }  } ; `privileged_address`: `string` = "0000000000000000000000000000000000000000000000000000000000000000"; `script_params`: { `V1`: { `max_script_data_length`: `number` = 102400; `max_script_length`: `number` = 102400 }  } ; `tx_params`: { `V1`: { `max_bytecode_subsections`: `number` = 256; `max_gas_per_tx`: `number` = 100000000; `max_inputs`: `number` = 255; `max_outputs`: `number` = 255; `max_size`: `number` = 262144; `max_witnesses`: `number` = 255 }  }  }  } |
| `chainConfigJson.consensus_parameters.V1` | { `base_asset_id`: `string` = "0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07"; `block_gas_limit`: `number` = 100000000; `chain_id`: `number` = 0; `contract_params`: { `V1`: { `contract_max_size`: `number` = 262144; `max_storage_slots`: `number` = 1760 }  } ; `fee_params`: { `V1`: { `gas_per_byte`: `number` = 63; `gas_price_factor`: `number` = 92 }  } ; `gas_costs`: { `V1`: { `add`: `number` = 2; `addi`: `number` = 2; `aloc`: `number` = 2; `and`: `number` = 2; `andi`: `number` = 2; `bal`: `number` = 86; `bhei`: `number` = 2; `bhsh`: `number` = 2; `burn`: `number` = 25770; `call`: { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } ; `cb`: `number` = 2; `ccp`: { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } ; `cfei`: `number` = 2; `cfsi`: `number` = 2; `contract_root`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } ; `croo`: { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } ; `csiz`: { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } ; `div`: `number` = 2; `divi`: `number` = 2; `eck1`: `number` = 3114; `ecr1`: `number` = 42270; `ed19`: `number` = 2878; `eq`: `number` = 2; `exp`: `number` = 2; `expi`: `number` = 2; `flag`: `number` = 1; `gm`: `number` = 2; `gt`: `number` = 2; `gtf`: `number` = 12; `ji`: `number` = 2; `jmp`: `number` = 2; `jmpb`: `number` = 1; `jmpf`: `number` = 1; `jne`: `number` = 2; `jneb`: `number` = 1; `jnef`: `number` = 1; `jnei`: `number` = 2; `jnzb`: `number` = 1; `jnzf`: `number` = 1; `jnzi`: `number` = 2; `k256`: { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } ; `lb`: `number` = 2; `ldc`: { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } ; `log`: `number` = 165; `logd`: { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } ; `lt`: `number` = 2; `lw`: `number` = 2; `mcl`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } ; `mcli`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } ; `mcp`: { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } ; `mcpi`: { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } ; `meq`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } ; `mint`: `number` = 29024; `mldv`: `number` = 3; `mlog`: `number` = 2; `mod_op`: `number` = 2; `modi`: `number` = 2; `move_op`: `number` = 2; `movi`: `number` = 2; `mroo`: `number` = 4; `mul`: `number` = 2; `muli`: `number` = 2; `new_storage_per_byte`: `number` = 63; `noop`: `number` = 1; `not`: `number` = 2; `or`: `number` = 2; `ori`: `number` = 2; `poph`: `number` = 3; `popl`: `number` = 3; `pshh`: `number` = 4; `pshl`: `number` = 4; `ret`: `number` = 134; `retd`: { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } ; `rvrt`: `number` = 153; `s256`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } ; `sb`: `number` = 2; `scwq`: { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } ; `sll`: `number` = 2; `slli`: `number` = 2; `smo`: { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } ; `srl`: `number` = 2; `srli`: `number` = 2; `srw`: `number` = 209; `srwq`: { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } ; `state_root`: { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } ; `sub`: `number` = 2; `subi`: `number` = 2; `sw`: `number` = 2; `sww`: `number` = 22501; `swwq`: { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } ; `time`: `number` = 50; `tr`: `number` = 33912; `tro`: `number` = 24294; `vm_initialization`: { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } ; `wdam`: `number` = 9; `wdcm`: `number` = 2; `wddv`: `number` = 5; `wdmd`: `number` = 10; `wdml`: `number` = 3; `wdmm`: `number` = 10; `wdop`: `number` = 3; `wqam`: `number` = 11; `wqcm`: `number` = 3; `wqdv`: `number` = 6; `wqmd`: `number` = 17; `wqml`: `number` = 4; `wqmm`: `number` = 10; `wqop`: `number` = 3; `xor`: `number` = 2; `xori`: `number` = 2 }  } ; `predicate_params`: { `V1`: { `max_gas_per_predicate`: `number` = 100000000; `max_message_data_length`: `number` = 102400; `max_predicate_data_length`: `number` = 102400; `max_predicate_length`: `number` = 102400 }  } ; `privileged_address`: `string` = "0000000000000000000000000000000000000000000000000000000000000000"; `script_params`: { `V1`: { `max_script_data_length`: `number` = 102400; `max_script_length`: `number` = 102400 }  } ; `tx_params`: { `V1`: { `max_bytecode_subsections`: `number` = 256; `max_gas_per_tx`: `number` = 100000000; `max_inputs`: `number` = 255; `max_outputs`: `number` = 255; `max_size`: `number` = 262144; `max_witnesses`: `number` = 255 }  }  } |
| `chainConfigJson.consensus_parameters.V1.base_asset_id` | `string` |
| `chainConfigJson.consensus_parameters.V1.block_gas_limit` | `number` |
| `chainConfigJson.consensus_parameters.V1.chain_id` | `number` |
| `chainConfigJson.consensus_parameters.V1.contract_params` | { `V1`: { `contract_max_size`: `number` = 262144; `max_storage_slots`: `number` = 1760 }  } |
| `chainConfigJson.consensus_parameters.V1.contract_params.V1` | { `contract_max_size`: `number` = 262144; `max_storage_slots`: `number` = 1760 } |
| `chainConfigJson.consensus_parameters.V1.contract_params.V1.contract_max_size` | `number` |
| `chainConfigJson.consensus_parameters.V1.contract_params.V1.max_storage_slots` | `number` |
| `chainConfigJson.consensus_parameters.V1.fee_params` | { `V1`: { `gas_per_byte`: `number` = 63; `gas_price_factor`: `number` = 92 }  } |
| `chainConfigJson.consensus_parameters.V1.fee_params.V1` | { `gas_per_byte`: `number` = 63; `gas_price_factor`: `number` = 92 } |
| `chainConfigJson.consensus_parameters.V1.fee_params.V1.gas_per_byte` | `number` |
| `chainConfigJson.consensus_parameters.V1.fee_params.V1.gas_price_factor` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs` | { `V1`: { `add`: `number` = 2; `addi`: `number` = 2; `aloc`: `number` = 2; `and`: `number` = 2; `andi`: `number` = 2; `bal`: `number` = 86; `bhei`: `number` = 2; `bhsh`: `number` = 2; `burn`: `number` = 25770; `call`: { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } ; `cb`: `number` = 2; `ccp`: { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } ; `cfei`: `number` = 2; `cfsi`: `number` = 2; `contract_root`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } ; `croo`: { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } ; `csiz`: { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } ; `div`: `number` = 2; `divi`: `number` = 2; `eck1`: `number` = 3114; `ecr1`: `number` = 42270; `ed19`: `number` = 2878; `eq`: `number` = 2; `exp`: `number` = 2; `expi`: `number` = 2; `flag`: `number` = 1; `gm`: `number` = 2; `gt`: `number` = 2; `gtf`: `number` = 12; `ji`: `number` = 2; `jmp`: `number` = 2; `jmpb`: `number` = 1; `jmpf`: `number` = 1; `jne`: `number` = 2; `jneb`: `number` = 1; `jnef`: `number` = 1; `jnei`: `number` = 2; `jnzb`: `number` = 1; `jnzf`: `number` = 1; `jnzi`: `number` = 2; `k256`: { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } ; `lb`: `number` = 2; `ldc`: { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } ; `log`: `number` = 165; `logd`: { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } ; `lt`: `number` = 2; `lw`: `number` = 2; `mcl`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } ; `mcli`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } ; `mcp`: { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } ; `mcpi`: { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } ; `meq`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } ; `mint`: `number` = 29024; `mldv`: `number` = 3; `mlog`: `number` = 2; `mod_op`: `number` = 2; `modi`: `number` = 2; `move_op`: `number` = 2; `movi`: `number` = 2; `mroo`: `number` = 4; `mul`: `number` = 2; `muli`: `number` = 2; `new_storage_per_byte`: `number` = 63; `noop`: `number` = 1; `not`: `number` = 2; `or`: `number` = 2; `ori`: `number` = 2; `poph`: `number` = 3; `popl`: `number` = 3; `pshh`: `number` = 4; `pshl`: `number` = 4; `ret`: `number` = 134; `retd`: { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } ; `rvrt`: `number` = 153; `s256`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } ; `sb`: `number` = 2; `scwq`: { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } ; `sll`: `number` = 2; `slli`: `number` = 2; `smo`: { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } ; `srl`: `number` = 2; `srli`: `number` = 2; `srw`: `number` = 209; `srwq`: { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } ; `state_root`: { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } ; `sub`: `number` = 2; `subi`: `number` = 2; `sw`: `number` = 2; `sww`: `number` = 22501; `swwq`: { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } ; `time`: `number` = 50; `tr`: `number` = 33912; `tro`: `number` = 24294; `vm_initialization`: { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } ; `wdam`: `number` = 9; `wdcm`: `number` = 2; `wddv`: `number` = 5; `wdmd`: `number` = 10; `wdml`: `number` = 3; `wdmm`: `number` = 10; `wdop`: `number` = 3; `wqam`: `number` = 11; `wqcm`: `number` = 3; `wqdv`: `number` = 6; `wqmd`: `number` = 17; `wqml`: `number` = 4; `wqmm`: `number` = 10; `wqop`: `number` = 3; `xor`: `number` = 2; `xori`: `number` = 2 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1` | { `add`: `number` = 2; `addi`: `number` = 2; `aloc`: `number` = 2; `and`: `number` = 2; `andi`: `number` = 2; `bal`: `number` = 86; `bhei`: `number` = 2; `bhsh`: `number` = 2; `burn`: `number` = 25770; `call`: { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } ; `cb`: `number` = 2; `ccp`: { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } ; `cfei`: `number` = 2; `cfsi`: `number` = 2; `contract_root`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } ; `croo`: { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } ; `csiz`: { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } ; `div`: `number` = 2; `divi`: `number` = 2; `eck1`: `number` = 3114; `ecr1`: `number` = 42270; `ed19`: `number` = 2878; `eq`: `number` = 2; `exp`: `number` = 2; `expi`: `number` = 2; `flag`: `number` = 1; `gm`: `number` = 2; `gt`: `number` = 2; `gtf`: `number` = 12; `ji`: `number` = 2; `jmp`: `number` = 2; `jmpb`: `number` = 1; `jmpf`: `number` = 1; `jne`: `number` = 2; `jneb`: `number` = 1; `jnef`: `number` = 1; `jnei`: `number` = 2; `jnzb`: `number` = 1; `jnzf`: `number` = 1; `jnzi`: `number` = 2; `k256`: { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } ; `lb`: `number` = 2; `ldc`: { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } ; `log`: `number` = 165; `logd`: { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } ; `lt`: `number` = 2; `lw`: `number` = 2; `mcl`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } ; `mcli`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } ; `mcp`: { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } ; `mcpi`: { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } ; `meq`: { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } ; `mint`: `number` = 29024; `mldv`: `number` = 3; `mlog`: `number` = 2; `mod_op`: `number` = 2; `modi`: `number` = 2; `move_op`: `number` = 2; `movi`: `number` = 2; `mroo`: `number` = 4; `mul`: `number` = 2; `muli`: `number` = 2; `new_storage_per_byte`: `number` = 63; `noop`: `number` = 1; `not`: `number` = 2; `or`: `number` = 2; `ori`: `number` = 2; `poph`: `number` = 3; `popl`: `number` = 3; `pshh`: `number` = 4; `pshl`: `number` = 4; `ret`: `number` = 134; `retd`: { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } ; `rvrt`: `number` = 153; `s256`: { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } ; `sb`: `number` = 2; `scwq`: { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } ; `sll`: `number` = 2; `slli`: `number` = 2; `smo`: { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } ; `srl`: `number` = 2; `srli`: `number` = 2; `srw`: `number` = 209; `srwq`: { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } ; `state_root`: { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } ; `sub`: `number` = 2; `subi`: `number` = 2; `sw`: `number` = 2; `sww`: `number` = 22501; `swwq`: { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } ; `time`: `number` = 50; `tr`: `number` = 33912; `tro`: `number` = 24294; `vm_initialization`: { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } ; `wdam`: `number` = 9; `wdcm`: `number` = 2; `wddv`: `number` = 5; `wdmd`: `number` = 10; `wdml`: `number` = 3; `wdmm`: `number` = 10; `wdop`: `number` = 3; `wqam`: `number` = 11; `wqcm`: `number` = 3; `wqdv`: `number` = 6; `wqmd`: `number` = 17; `wqml`: `number` = 4; `wqmm`: `number` = 10; `wqop`: `number` = 3; `xor`: `number` = 2; `xori`: `number` = 2 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.add` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.addi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.aloc` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.and` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.andi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.bal` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.bhei` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.bhsh` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.burn` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.call` | { `LightOperation`: { `base`: `number` = 18190; `units_per_gas`: `number` = 5 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.call.LightOperation` | { `base`: `number` = 18190; `units_per_gas`: `number` = 5 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.call.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.call.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.cb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ccp` | { `LightOperation`: { `base`: `number` = 48; `units_per_gas`: `number` = 22 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ccp.LightOperation` | { `base`: `number` = 48; `units_per_gas`: `number` = 22 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ccp.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ccp.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.cfei` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.cfsi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.contract_root` | { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 2 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.contract_root.LightOperation` | { `base`: `number` = 42; `units_per_gas`: `number` = 2 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.contract_root.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.contract_root.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.croo` | { `LightOperation`: { `base`: `number` = 131; `units_per_gas`: `number` = 2 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.croo.LightOperation` | { `base`: `number` = 131; `units_per_gas`: `number` = 2 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.croo.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.croo.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.csiz` | { `LightOperation`: { `base`: `number` = 45; `units_per_gas`: `number` = 237 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.csiz.LightOperation` | { `base`: `number` = 45; `units_per_gas`: `number` = 237 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.csiz.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.csiz.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.div` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.divi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.eck1` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ecr1` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ed19` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.eq` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.exp` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.expi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.flag` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.gm` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.gt` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.gtf` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ji` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jmp` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jmpb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jmpf` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jne` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jneb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jnef` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jnei` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jnzb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jnzf` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.jnzi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.k256` | { `LightOperation`: { `base`: `number` = 37; `units_per_gas`: `number` = 3 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.k256.LightOperation` | { `base`: `number` = 37; `units_per_gas`: `number` = 3 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.k256.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.k256.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.lb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ldc` | { `LightOperation`: { `base`: `number` = 39; `units_per_gas`: `number` = 68 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ldc.LightOperation` | { `base`: `number` = 39; `units_per_gas`: `number` = 68 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ldc.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ldc.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.log` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.logd` | { `LightOperation`: { `base`: `number` = 565; `units_per_gas`: `number` = 2 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.logd.LightOperation` | { `base`: `number` = 565; `units_per_gas`: `number` = 2 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.logd.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.logd.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.lt` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.lw` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcl` | { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 564 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcl.LightOperation` | { `base`: `number` = 3; `units_per_gas`: `number` = 564 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcl.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcl.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcli` | { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 560 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcli.LightOperation` | { `base`: `number` = 3; `units_per_gas`: `number` = 560 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcli.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcli.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcp` | { `LightOperation`: { `base`: `number` = 4; `units_per_gas`: `number` = 185 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcp.LightOperation` | { `base`: `number` = 4; `units_per_gas`: `number` = 185 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcp.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcp.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcpi` | { `LightOperation`: { `base`: `number` = 9; `units_per_gas`: `number` = 455 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcpi.LightOperation` | { `base`: `number` = 9; `units_per_gas`: `number` = 455 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcpi.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mcpi.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.meq` | { `LightOperation`: { `base`: `number` = 3; `units_per_gas`: `number` = 766 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.meq.LightOperation` | { `base`: `number` = 3; `units_per_gas`: `number` = 766 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.meq.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.meq.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mint` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mldv` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mlog` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mod_op` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.modi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.move_op` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.movi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mroo` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.mul` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.muli` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.new_storage_per_byte` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.noop` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.not` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.or` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ori` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.poph` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.popl` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.pshh` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.pshl` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.ret` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.retd` | { `LightOperation`: { `base`: `number` = 485; `units_per_gas`: `number` = 3 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.retd.LightOperation` | { `base`: `number` = 485; `units_per_gas`: `number` = 3 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.retd.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.retd.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.rvrt` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.s256` | { `LightOperation`: { `base`: `number` = 42; `units_per_gas`: `number` = 3 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.s256.LightOperation` | { `base`: `number` = 42; `units_per_gas`: `number` = 3 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.s256.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.s256.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.sb` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.scwq` | { `HeavyOperation`: { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.scwq.HeavyOperation` | { `base`: `number` = 21672; `gas_per_unit`: `number` = 22146 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.scwq.HeavyOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.scwq.HeavyOperation.gas_per_unit` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.sll` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.slli` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.smo` | { `LightOperation`: { `base`: `number` = 44437; `units_per_gas`: `number` = 1 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.smo.LightOperation` | { `base`: `number` = 44437; `units_per_gas`: `number` = 1 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.smo.LightOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.smo.LightOperation.units_per_gas` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srl` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srli` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srw` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srwq` | { `HeavyOperation`: { `base`: `number` = 239; `gas_per_unit`: `number` = 234 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srwq.HeavyOperation` | { `base`: `number` = 239; `gas_per_unit`: `number` = 234 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srwq.HeavyOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.srwq.HeavyOperation.gas_per_unit` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.state_root` | { `HeavyOperation`: { `base`: `number` = 323; `gas_per_unit`: `number` = 169 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.state_root.HeavyOperation` | { `base`: `number` = 323; `gas_per_unit`: `number` = 169 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.state_root.HeavyOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.state_root.HeavyOperation.gas_per_unit` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.sub` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.subi` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.sw` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.sww` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.swwq` | { `HeavyOperation`: { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.swwq.HeavyOperation` | { `base`: `number` = 22724; `gas_per_unit`: `number` = 21231 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.swwq.HeavyOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.swwq.HeavyOperation.gas_per_unit` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.time` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.tr` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.tro` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.vm_initialization` | { `HeavyOperation`: { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 }  } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.vm_initialization.HeavyOperation` | { `base`: `number` = 5254820; `gas_per_unit`: `number` = 0 } |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.vm_initialization.HeavyOperation.base` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.vm_initialization.HeavyOperation.gas_per_unit` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdam` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdcm` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wddv` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdmd` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdml` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdmm` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wdop` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqam` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqcm` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqdv` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqmd` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqml` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqmm` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.wqop` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.xor` | `number` |
| `chainConfigJson.consensus_parameters.V1.gas_costs.V1.xori` | `number` |
| `chainConfigJson.consensus_parameters.V1.predicate_params` | { `V1`: { `max_gas_per_predicate`: `number` = 100000000; `max_message_data_length`: `number` = 102400; `max_predicate_data_length`: `number` = 102400; `max_predicate_length`: `number` = 102400 }  } |
| `chainConfigJson.consensus_parameters.V1.predicate_params.V1` | { `max_gas_per_predicate`: `number` = 100000000; `max_message_data_length`: `number` = 102400; `max_predicate_data_length`: `number` = 102400; `max_predicate_length`: `number` = 102400 } |
| `chainConfigJson.consensus_parameters.V1.predicate_params.V1.max_gas_per_predicate` | `number` |
| `chainConfigJson.consensus_parameters.V1.predicate_params.V1.max_message_data_length` | `number` |
| `chainConfigJson.consensus_parameters.V1.predicate_params.V1.max_predicate_data_length` | `number` |
| `chainConfigJson.consensus_parameters.V1.predicate_params.V1.max_predicate_length` | `number` |
| `chainConfigJson.consensus_parameters.V1.privileged_address` | `string` |
| `chainConfigJson.consensus_parameters.V1.script_params` | { `V1`: { `max_script_data_length`: `number` = 102400; `max_script_length`: `number` = 102400 }  } |
| `chainConfigJson.consensus_parameters.V1.script_params.V1` | { `max_script_data_length`: `number` = 102400; `max_script_length`: `number` = 102400 } |
| `chainConfigJson.consensus_parameters.V1.script_params.V1.max_script_data_length` | `number` |
| `chainConfigJson.consensus_parameters.V1.script_params.V1.max_script_length` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params` | { `V1`: { `max_bytecode_subsections`: `number` = 256; `max_gas_per_tx`: `number` = 100000000; `max_inputs`: `number` = 255; `max_outputs`: `number` = 255; `max_size`: `number` = 262144; `max_witnesses`: `number` = 255 }  } |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1` | { `max_bytecode_subsections`: `number` = 256; `max_gas_per_tx`: `number` = 100000000; `max_inputs`: `number` = 255; `max_outputs`: `number` = 255; `max_size`: `number` = 262144; `max_witnesses`: `number` = 255 } |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_bytecode_subsections` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_gas_per_tx` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_inputs` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_outputs` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_size` | `number` |
| `chainConfigJson.consensus_parameters.V1.tx_params.V1.max_witnesses` | `number` |
| `metadataJson` | { `chain_config`: `string` = "chainConfig.json"; `table_encoding`: { `Json`: { `filepath`: `string` = "stateConfig.json" }  }  } |
| `metadataJson.chain_config` | `string` |
| `metadataJson.table_encoding` | { `Json`: { `filepath`: `string` = "stateConfig.json" }  } |
| `metadataJson.table_encoding.Json` | { `filepath`: `string` = "stateConfig.json" } |
| `metadataJson.table_encoding.Json.filepath` | `string` |
| `stateConfigJson` | { `block_height`: `number` = 0; `coins`: { `amount`: `number` = 18446744073709551615; `asset_id`: `string` = "0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07"; `output_index`: `number` = 0; `owner`: `string` = "0x94ffcc53b892684acefaebc8a3d4a595e528a8cf664eeb3ef36f1020b0809d0d"; `tx_id`: `string` = "0x0000000000000000000000000000000000000000000000000000000000000001"; `tx_pointer_block_height`: `number` = 0; `tx_pointer_tx_idx`: `number` = 0 }[] ; `contracts`: `never`[] = []; `da_block_height`: `number` = 0; `messages`: { `amount`: `number` = 18446744073709551615; `da_height`: `number` = 0; `data`: `string` = ""; `nonce`: `string` = "0101010101010101010101010101010101010101010101010101010101010101"; `recipient`: `string` = "0x69a2b736b60159b43bb8a4f98c0589f6da5fa3a3d101e8e269c499eb942753ba"; `sender`: `string` = "0xc43454aa38dd91f88109a4b7aef5efb96ce34e3f24992fe0f81d233ca686f80f" }[]  } |
| `stateConfigJson.block_height` | `number` |
| `stateConfigJson.coins` | { `amount`: `number` = 18446744073709551615; `asset_id`: `string` = "0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07"; `output_index`: `number` = 0; `owner`: `string` = "0x94ffcc53b892684acefaebc8a3d4a595e528a8cf664eeb3ef36f1020b0809d0d"; `tx_id`: `string` = "0x0000000000000000000000000000000000000000000000000000000000000001"; `tx_pointer_block_height`: `number` = 0; `tx_pointer_tx_idx`: `number` = 0 }[] |
| `stateConfigJson.contracts` | `never`[] |
| `stateConfigJson.da_block_height` | `number` |
| `stateConfigJson.messages` | { `amount`: `number` = 18446744073709551615; `da_height`: `number` = 0; `data`: `string` = ""; `nonce`: `string` = "0101010101010101010101010101010101010101010101010101010101010101"; `recipient`: `string` = "0x69a2b736b60159b43bb8a4f98c0589f6da5fa3a3d101e8e269c499eb942753ba"; `sender`: `string` = "0xc43454aa38dd91f88109a4b7aef5efb96ce34e3f24992fe0f81d233ca686f80f" }[] |

#### Defined in

[packages/utils/src/utils/defaultSnapshotConfigs.ts:5](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/defaultSnapshotConfigs.ts#L5)

## Functions

### arrayify

▸ **arrayify**(`value`, `name?`, `copy?`): `Uint8Array`

Get a typed Uint8Array from a BytesLike object.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `value` | [`BytesLike`](/api/Interfaces/index.md#byteslike) | `undefined` | the BytesLike data. |
| `name?` | `string` | `undefined` | a display name for the error result. |
| `copy` | `boolean` | `true` | create a copy of the original data (if applicable). |

#### Returns

`Uint8Array`

- a typed Uint8Array.

#### Defined in

[packages/utils/src/utils/arrayify.ts:12](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/arrayify.ts#L12)

___

### capitalizeString

▸ **capitalizeString**(`str`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

#### Returns

`string`

#### Defined in

[packages/utils/src/utils/capitalizeString.ts:1](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/capitalizeString.ts#L1)

___

### chunkAndPadBytes

▸ **chunkAndPadBytes**(`bytes`, `chunkSize`): `Uint8Array`[]

Function to take a byte array and split into chunks of a given size

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bytes` | `Uint8Array` | The byte array to chunk |
| `chunkSize` | `number` | The size of each chunk |

#### Returns

`Uint8Array`[]

An array of byte arrays of a specified size

#### Defined in

[packages/utils/src/utils/chunkAndPadBytes.ts:8](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/chunkAndPadBytes.ts#L8)

___

### concat

▸ **concat**(`arrays`): `Uint8Array`

Concatenates multiple BytesLike into a single Uint8Array.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `arrays` | readonly [`BytesLike`](/api/Interfaces/index.md#byteslike)[] | The arrays to concatenate. |

#### Returns

`Uint8Array`

- The concatenated array.

#### Defined in

[packages/utils/src/utils/concat.ts:38](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/concat.ts#L38)

___

### concatBytes

▸ **concatBytes**(`arrays`): `Uint8Array`

Concatenates multiple Uint8Arrays into a single Uint8Array.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `arrays` | readonly `Uint8Array`[] \| readonly `number`[][] | The arrays to concatenate. |

#### Returns

`Uint8Array`

- The concatenated array.

#### Defined in

[packages/utils/src/utils/concat.ts:11](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/concat.ts#L11)

___

### dataSlice

▸ **dataSlice**(`data`, `start?`, `end?`): `string`

Returns a hex string by slicing data from the start offset to the end offset.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `data` | [`BytesLike`](/api/Interfaces/index.md#byteslike) | the data to be sliced. |
| `start?` | `number` | the start offset (default: 0). |
| `end?` | `number` | the end offset (default: length of data). |

#### Returns

`string`

- a sliced hex string from start to end.

#### Defined in

[packages/utils/src/utils/dataSlice.ts:15](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/dataSlice.ts#L15)

___

### decodeBase58

▸ **decodeBase58**(`value`): `BN`

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `string` |

#### Returns

`BN`

#### Defined in

[packages/utils/src/utils/base58.ts:51](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/base58.ts#L51)

___

### encodeBase58

▸ **encodeBase58**(`_value`): `string`

Encode value as a Base58-encoded string.

#### Parameters

| Name | Type |
| :------ | :------ |
| `_value` | [`BytesLike`](/api/Interfaces/index.md#byteslike) |

#### Returns

`string`

#### Defined in

[packages/utils/src/utils/base58.ts:30](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/base58.ts#L30)

___

### hexlify

▸ **hexlify**(`data`): `string`

Returns a hex representation of the inputted bytes.

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | [`BytesLike`](/api/Interfaces/index.md#byteslike) |

#### Returns

`string`

#### Defined in

[packages/utils/src/utils/hexlify.ts:10](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/hexlify.ts#L10)

___

### isDefined

▸ **isDefined**&lt;`T`\>(`value`): value is T

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `undefined` \| `T` |

#### Returns

value is T

#### Defined in

[packages/utils/src/utils/isDefined.ts:1](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/isDefined.ts#L1)

___

### normalizeString

▸ **normalizeString**(`str`): `string`

Converts `some.string-value` into `SomeStringValue`.

Examples:
 my-simple.test —— MySimpleTest
 myFile.ts —— MyFileTs
 my-abi.json —— MyAbiJson

#### Parameters

| Name | Type |
| :------ | :------ |
| `str` | `string` |

#### Returns

`string`

#### Defined in

[packages/utils/src/utils/normalizeString.ts:11](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/normalizeString.ts#L11)

___

### toUtf8Bytes

▸ **toUtf8Bytes**(`stri`, `form?`): `Uint8Array`

Returns the UTF-8 byte representation of str.

 If form is disabled, the string is not normalized.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `stri` | `string` | `undefined` | the string to convert to UTF-8 bytes. |
| `form` | `boolean` | `true` | whether to normalize the string. |

#### Returns

`Uint8Array`

- the UTF-8 byte representation of str.

#### Defined in

[packages/utils/src/utils/toUtf8Bytes.ts:11](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/toUtf8Bytes.ts#L11)

___

### toUtf8String

▸ **toUtf8String**(`bytes`): `string`

Returns the string represented by the UTF-8 data bytes.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bytes` | [`BytesLike`](/api/Interfaces/index.md#byteslike) | the UTF-8 data bytes |

#### Returns

`string`

the string represented by the UTF-8 data bytes

#### Defined in

[packages/utils/src/utils/toUtf8String.ts:179](https://github.com/FuelLabs/fuels-ts/blob/12602001/packages/utils/src/utils/toUtf8String.ts#L179)
