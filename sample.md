'5JbJrZY1M1jRuDBtnuJb9kyrTnxYM2tN7PRQ2vNJ9cxgVegM4Ak', '5KS9N7WMK4omrnw9ew96TYSXwph3defKFPXiGKZqmcTmwKF468i'

'5KERTkmTwMRa6RWAHJnatkn8zzdofDb3qVGTQoCPncMzFuFvWZL', '5JcvEzdbfh8skospbe8cSkqF4k9AeXmcNtWNwk8HE2JmUiEseCS'

# new-account-creation topic

{"creator_account" : "unknown", "account_name" : "oriontester1", "block_time" : "1538384744", "block_num" : "4", "tx_id" : "faef23e5d9c82edad26d89e4820d5f608775d46aa79ac4c72cfaabd52c152351"}
{"creator_account" : "eosio", "account_name" : "skygamesim25", "block_time" : "1538384744", "block_num" : "4", "tx_id" : "faef23e5d9c82edad26d89e4820d5f608775d46aa79ac4c72cfaabd52c152351"}


## transaction:

```
{"block_number" : 5728, "block_time" : 1537960381500, "trace" : { "id" : "1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165", "block_num" : 3056, "block_time" : "2018-09-26T11:13:00.500", "receipt" : { "status" : "executed", "cpu_usage_us" : 100, "net_usage_words" : 10 }, "elapsed" : 102, "net_usage" : 0, "scheduled" : false, "action_traces" : [ { "receipt" : { "receiver" : "eosio", "act_digest" : "7c3c2b94f91994365a4713db12de77b9c04857227797daea555d041707075bb0", "global_sequence" : 3055, "recv_sequence" : 3055, "auth_sequence" : [ [ "eosio", 3055 ] ], "code_sequence" : 0, "abi_sequence" : 0 }, "act" : { "account" : "eosio.token", "name" : "setcode", "authorization" : [ { "actor" : "oriontester1", "permission" : "active" } ], "data" : "784c7c460000000000ea3055000000000bee82c6f6724cf880e2ec723cfe06f5d137f5371920caa5f214a856ab5d0000000000000000000000000000000000000000000000000000000000000000983b223855decdf7c9c93b793d0409384292a8166fefd56be583a6206e8f6ecb000000000000" }, "context_free" : false, "elapsed" : 34, "cpu_usage" : 0, "console" : "", "total_cpu_usage" : 0, "trx_id" : "1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165", "block_num" : 3056, "block_time" : "2018-09-26T11:13:02.500", "account_ram_deltas" : [ ], "inline_traces" : [ ] } ], "failed_dtrx_trace" : null } }
```

```
{"block_number":12229136,"block_time":1549276472500,"trace":{"id":"1c4b01dd309fa7722f7186b2c780ce8ccb227af86dfac41fdc982c6e61b0e2d1","block_num":12229136,"block_time":"2019-02-04T10:34:32.500","producer_block_id":"00ba9a109d932fa214962a18182e0026485a4ff17e6effcf7e7d6464b993bb26","receipt":{"status":"executed","cpu_usage_us":80,"net_usage_words":0},"elapsed":546,"net_usage":0,"scheduled":false,"action_traces":[{"receipt":{"receiver":"eosio","act_digest":"8b081375d942b34ab0fcd78f5b629bc0062a2739b1f8bb8759fe19bbcd66f6e0","global_sequence":68703413,"recv_sequence":13656975,"auth_sequence":[["eosio",15163779]],"code_sequence":4,"abi_sequence":5},"act":{"account":"eosio","name":"onblock","authorization":[{"actor":"eosio","permission":"active"}],"data":"70a3d54760a6cb53b16bf464000000ba9a0ec193d7f9847cf4652241f1f7cc5a97beb73c7ce262b8de23da949ae781a1f0465514c54c500ecccb7f9eebdf2ef2342eab2bce733a0735847aafcd2228e1e7012047e0a760e8e95fa4bc5acd66e8c87e85c44378a0ac76ac99d939d4670000000000"},"context_free":false,"elapsed":452,"console":"","trx_id":"1c4b01dd309fa7722f7186b2c780ce8ccb227af86dfac41fdc982c6e61b0e2d1","block_num":12229136,"block_time":"2019-02-04T10:34:32.500","producer_block_id":"00ba9a109d932fa214962a18182e0026485a4ff17e6effcf7e7d6464b993bb26","account_ram_deltas":[],"inline_traces":[]}],"failed_dtrx_trace":null},"type": "applied"}
```

# transaction multi action:

```
{"block_number" : 7158, "block_time" : 1537960380500, "trace" : { "id" : "1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165", "block_num" : 3056, "block_time" : "2018-09-26T11:13:00.500", "receipt" : { "status" : "executed", "cpu_usage_us" : 100, "net_usage_words" : 0 }, "elapsed" : 102, "net_usage" : 0, "scheduled" : false, "action_traces" : [ { "receipt" : { "receiver" : "eosio", "act_digest" : "7c3c2b94f91994365a4713db12de77b9c04857227797daea555d041707075bb0", "global_sequence" : 3055, "recv_sequence" : 3055, "auth_sequence" : [ [ "eosio", 3055 ] ], "code_sequence" : 0, "abi_sequence" : 0 }, "act" : [ {"account":"tryrepeateoz","name":"onblock","authorization":[{"actor":"eosio","permission":"active"}],"data":"f438a3460000000000ea305500000000001a81cc655eddc59c7705dda6fded71bc0d08779724ea4745004b3d478f0000000000000000000000000000000000000000000000000000000000000000b9aa61b0d111ff815937ff90f88bb78b1f00d1dfb328f8b90526674e724c550c000000000000"},{ "account" : "tryrepeateoz", "name" : "create", "authorization" : [ { "actor" : "partner11111", "permission" : "active" } ], "data" : "104208e1aa99afa9208410e2aa99afa9204e00000000000004454f53530000001c50617920706172746e65723120746f203220736f6d65206d6f6e6579" }, { "account" : "tryrepeateoz", "name" : "transfer", "authorization" : [ { "actor" : "partner11111", "permission" : "active" } ], "data" : "104208e1aa99afa9208410e2aa99afa9204e00000000000004454f53530000001c50617920706172746e65723120746f203220736f6d65206d6f6e6579" }, { "account" : "tryrepeateoz", "name" : "create", "authorization" : [ { "actor" : "partner11111", "permission" : "active" } ], "data" : "104208e1aa99afa9208410e2aa99afa9204e00000000000004454f53530000001c50617920706172746e65723120746f203220736f6d65206d6f6e6579" } ], "context_free" : false, "elapsed" : 34, "cpu_usage" : 0, "console" : "", "total_cpu_usage" : 0, "trx_id" : "1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165", "block_num" : 3056, "block_time" : "2018-09-26T11:13:00.500", "account_ram_deltas" : [ ], "inline_traces" : [ ] } ], "failed_dtrx_trace" : null } }
```

# actions:

{"account":"eosio.token","data":"f438a3460000000000e","action":"setcode","count":1,"timestamp":1548313369961,"account_name":"oriontester1","block_time":1537960382500, "block_number" : 5728, "cpu_usage":100,"net_usage":10,"tx_id":"1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165"}

{"account":"eosio.token","data":"00ea305500000000","action":"transfer","count":1,"timestamp":1548313369961,"account_name":"mvpmvpmvpmv1","block_time":1537960382500, "block_number" : 11748796, "cpu_usage":100,"net_usage":10,"tx_id":"1125ede029b3585ab5dad7d87354f5a46625b9ef72f6811f468e294398e7e165"}

{ "tx_id" : "3d63bd649da4d5734b5c6af25adbd3711ad15f1bd9a40f654fa3491ba2a8ea0a", "timestamp" : 1549030424549, "action" : "transfer", "account_name" : "mvpmvpmvpmv1", "account" : "eosio.token", "data" : "10b6ac5bd62deb9650b7ac5bd62deb96010000000000000004454f530000000000", "cpu_usage" : 599, "net_usage" : 91, "block_number" : 11748525, "block_time" : 1549030424500, "last_updated_time" : 1549030424553}

{ "tx_id" : "3d63bd649da4d5734b5c6af25adbd3711ad15f1bd9a40f654fa3491ba2a8ea0a", "timestamp" : 1549030424549, "action" : "transfer", "account_name" : "mvpmvpmvpmv1", "account" : "eosio.token", "data" : "10b6ac5bd62deb9650b7ac5bd62deb96010000000000000004454f530000000000", "cpu_usage" : 599, "net_usage" : 91, "block_number" : 11748796, "block_time" : 1549030424500, "last_updated_time" : 1549030424553}

{"blockNumber":12322908,"blockTime":1549323994500,"txId":"d9940d5ffe785244f124d41ea48049d7805ef561f1e29cc142c3a72d2a39d870","actions":[{"account":"eosio.token","authorization":[{"actor":"bingotester5","permission":"active"}],"data":"{\"from\":\"bingotester5\",\"to\":\"betdice\",\"quantity\":\"1.0000 EOS\",\"memo\":\"\"}","name":"transfer"},{"account":"bingobetgame","authorization":[{"actor":"bingotester5","permission":"active"}],"data":"{\"from\":\"bingotester5\",\"to\":\"bingobetgame\",\"quantity\":\"1.0000 EOS\",\"memo\":\"\"}","name":"playslot"}],"cpuUsage":1324,"netUsage":232}



# add scoring rule
curl -X POST -d '{"name":"contract", "score":0, "enabled":1, "rule_params": {}}' -H "Content-Type: application/json" http://localhost:8800/scoring-service/v1/rules

curl -X POST -d '{"name":"bot", "score":0, "enabled":1, "rule_params": {"threshold":"1000", "count":"5"}}' -H "Content-Type: application/json" http://localhost:8805/scoring-service/v1/rules

curl -X POST -d '{"name":"dapp", "score":1, "enabled":1, "rule_params": {"betdice":"2.0", "eosknight":"1.12", "twitter": "0.5"}}' -H "Content-Type: application/json" http://localhost:8805/scoring-service/v1/rules


curl -X POST -d '{"name":"dapp_affinity", "score":50, "enabled":1, "rule_params": {}}' -H "Content-Type: application/json" http://localhost:8805/scoring-service/v1/rules

```
{
	"_id" : ObjectId("5c7624db0542231b6e0c6926"),
	"name" : "dapp_affinity",
	"score" : 50,
	"enabled" : true,
	"rule_params" : {
		
	},
	"timestamp" : NumberLong("1550063140987"),
	"_class" : "com.dunya.orion.scoring.model.ScoringRule"
}
```

## add dapps

curl -X POST -d '{"name":"bingobet", "accounts":["bingobetgame"], "type":"bet"}' -H "Content-Type: application/json" http://localhost:8805/scoring-service/v1/dapps?score=1


# get account score
curl -X GET -H "Content-Type: application/json" http://localhost:8805/v1/scores/score?account=oriontester1

# sample `accounts` document

{
	"tx_id" : "faef23e5d9c82edad26d89e4820d5f608775d46aa79ac4c72cfaabd52c152452",
	"creator_account" : "unknown",
	"account_name" : "eosio",
	"block_time" : NumberLong(1538384744),
	"block_num" : NumberLong(4),
	"score" : 100,
	"blacklist" : 0,
	"last_updated_time" : NumberLong("1540199702033"),
	"_class" : "com.dunya.stakechannel.accounts.model.Account"
}

# get scoring_rules
curl -X GET -H "Content-Type: application/json" http://localhost:8805/v1/scores/rules


# pool manager
curl -X POST 'http://localhost:8804/v1/pool_manager/pools/?valid=1' -H 'cache-control: no-cache' -H 'cont
ent-type: application/json' -d '{
    "name"    :    "tryrepeateoz",
    "valid"    :    true,
    "timestamp"    :    0,
    "total_eos"    :    23
}'

## blacklist an account
curl -X PUT 'http://localhost:8800/v1/accounts/eosio/blacklist' -H 'cache-control: no-cache' -H 'content-type: application/json' -d '{
    "blacklist" : 1,
    "blacklist_comment"    :    "API check"
}'

# force unstake
curl -X POST 'http://localhost:8802/v1/delegate' -H 'cache-control: no-cache' -H 'content-type: application/json' -d '{
    "account" : "eosio",
    "forceUnstake"    :    false
}'

# stake call to delegation service
curl -X POST 'http://localhost:8801/v1/stake' -H 'cache-control: no-cache' -H 'content-type: application/json' -d '{"from_account":"oriontester1","to_account":"skygamesim25","stake_cpu":1,"stake_net":0}'

## createOrUpdate pools
curl -X POST http://localhost:8804/v1/pool_manager/createOrUpdate -H 'cache-control: no-cache' -H 'content-type: application/json' -d '{"name":"stakech11111","valid":true}'

# add delegation to rule to mongo collection

db.cpu_delegation_rules.insertOne({
...         "rule_name" : "cpu1",
...         "valid" : true,
...         "created_at" : 1541577570,
...         "pool_object" : {
...                 "minscore" : 70,
...                 "maxeosdelegation" : 1000,
...                 "availabletarget" : 4000
...         }
... });

{"msg": "succeeded", "keys": {"active_key": {"public": "EOS57S6nWwv9JcUgdBNLbbaQryPGRCZgia9iRmvyeffzXrpdp5bex", "private": "5KERTkmTwMRa6RWAHJnatkn8zzdofDb3qVGTQoCPncMzFuFvWZL"}, "owner_key": {"public": "EOS4yVniVJ2HPZC99Ff3LvDvcpDQmVwwrqKgQikVmWdL72MezB2pz", "private": "5JEDUu8LZ8tvPkSGEVF2NkyKyyVYJ1cuJtpgGwmByG14N94diEG"}}, "account": "tryeosuseeo4"}

{"creator_account" : "NULL", "account_name" : "eosio", "block_time" : "1539235826", "block_num" : "11", "tx_id" : "213e361e32f897fc8d5a67600edd1046c2b78c55146d5cdebaf19ba8e683d406"}


{"block_number":28,"block_time":1539235834500,"trace":{"id":"82f69e5d35c223c253c7e1907b4d927aca6f408b72281d8655c7800f6364aa4c","block_num":28,"block_time":"2018-10-11T05:30:34.500","receipt":{"status":"executed","cpu_usage_us":100,"net_usage_words":0},"elapsed":101,"net_usage":0,"scheduled":false,"action_traces":[{"receipt":{"receiver":"eosio","act_digest":"43a9f2621154e7ad6f401f225f23244ea10c13914d08f91f6a59da48b22517f8","global_sequence":28,"recv_sequence":28,"auth_sequence":[["eosio",28]],"code_sequence":0,"abi_sequence":0},"act":{"account":"eosio","name":"onblock","authorization":[{"actor":"eosio","permission":"active"}],"data":"f438a3460000000000ea305500000000001a81cc655eddc59c7705dda6fded71bc0d08779724ea4745004b3d478f0000000000000000000000000000000000000000000000000000000000000000b9aa61b0d111ff815937ff90f88bb78b1f00d1dfb328f8b90526674e724c550c000000000000"},"context_free":false,"elapsed":30,"cpu_usage":0,"console":"","total_cpu_usage":0,"trx_id":"82f69e5d35c223c253c7e1907b4d927aca6f408b72281d8655c7800f6364aa4c","block_num":28,"block_time":"2018-10-11T05:30:34.500","account_ram_deltas":[],"inline_traces":[]}],"failed_dtrx_trace":null},"type": "applied"}




curl -X POST -d '{"account":"tryrepeateoz"}' -H "Content-Type: application/json" http://localhost:8802/v1/delegate






db.account_delegation_transactions.aggregate([{  
...   "$group":{  
...     "_id":"$pool_name",
...     "totalEosDelegatedForCpu":{  
...       "$sum":"$eos_delegated_for_cpu"
...     },
...     "totalEosUnDelegatedForCpu":{  
...       "$sum":"$eos_undelegated_for_cpu"
...     },
...     "totalEosDelegatedForNet":{  
...       "$sum":"$eos_delegated_for_net"
...     },
...     "totalEosUnDelegatedForNet":{  
...       "$sum":"$eos_undelegated_for_net"
...     },
...     "poolName":{  
...       "$addToSet":"$pool_name"
...     }
...   }
... }], "cursor" : { "batchSize" : 2147483647 } })


db.account_actions.aggregate([{  
...   "$group":{  
...     "_id":"$account_name",
...     "totalCount":{  
...       "$sum":"$count"
...     },
		"totalCpuUsage":{  
...       "$sum":"$cpu_usage"
...     },
		"totalNetUsage":{  
...       "$sum":"$net_usage"
...     },
...     "accountName":{  
...       "$addToSet":"$account_name"
...     }
...   }
... }])









"data" : {
		"_children" : {
			"from" : {
				"_value" : "bingotester5",
				"_class" : "com.fasterxml.jackson.databind.node.TextNode"
			},
			"to" : {
				"_value" : "bingobetgame",
				"_class" : "com.fasterxml.jackson.databind.node.TextNode"
			},
			"quantity" : {
				"_value" : "1.0000 EOS",
				"_class" : "com.fasterxml.jackson.databind.node.TextNode"
			},
			"memo" : {
				"_value" : "",
				"_class" : "com.fasterxml.jackson.databind.node.TextNode"
			}
		},
		"_nodeFactory" : {
			"_cfgBigDecimalExact" : false
		},
		"_class" : "com.fasterxml.jackson.databind.node.ObjectNode"
	},














Aggregation aggregation = Aggregation.newAggregation(Aggregation.match(Criteria.where("account_name")
//				.is(action.getAccountName()).and("block_time").gte(1537960380500l - 50000)),
//				Aggregation.count().as("actions"));
//
//		AggregationResults<LinkedHashMap> results = this.mongoOperations.aggregate(aggregation, "account_actions",
//				LinkedHashMap.class);
//		System.out.println("Agg Results: " + results.getMappedResults().get(0).get("actions"));
//
//		int count = (int) results.getMappedResults().get(0).get("actions");
		//if (count > (int) rule.getRuleParams().get("threshold")) {
			Aggregation aggregation2 = Aggregation.newAggregation(
					Aggregation.match(Criteria.where("account_name").is(action.getAccountName()).and("timestamp")
							.gte(1537960380500l - 50000)),
					Aggregation.sort(Direction.DESC, "timestamp"), Aggregation.project("timestamp").andExclude("_id"));

			AggregationResults<LinkedHashMap> results = this.mongoOperations.aggregate(aggregation2, "account_actions", LinkedHashMap.class);
			for (Object time : results.getMappedResults().toArray())
				System.out.println(time);
