## mongodb shell commands

	show dbs;
	show collections;
	use db_name;

## get docs from a collection

	db.collection_name.find().pretty()	//pretty for json formattting

## sort
	db.account_actions.find().sort( { block_time: -1 } )

	db.account_actions.aggregate([{$sort: {timestamp : -1}}, {$limit: 1}]);

## insrert doc
	db.collection_name.insertOne(doc_json);

## get indexes

	db.getCollectionNames().forEach(function(collection) {
   		indexes = db[collection].getIndexes();
   		print("Indexes for " + collection + ":");
   		printjson(indexes);
	});

	db.collection_name.getIndexes();

## rename databse
	db.copyDatabase('stake_channel','old_stake_channel_2');

## drop
	db.dropDatabase()

## distinct field values
	db.collection.distinct( "field" )

## updateMany
	db.accounts.updateMany({}, {$set: {tracked: 0}})

## aggregation with match and group

	db.account_actions.aggregate( [
  	{ $match: { account_name : "wintownworld" }, timestamp : { $gte: 1547673402500 }}},
  	{ $group: {_id: "$account_name", avgCpuUsgae: { $avg: "$cpu_usage" }, totalCount: { $sum: "$count" } } } 
	] );

## aggregation with 
	db.account_actions.aggregate( [
  	{ $match: { account_name : "pokereoshund", timestamp : { $gte: 1548419912698} }},
	{ $count: "actions"}
	]);


## difference
	{ "tx_id" : "3d63bd649da4d5734b5c6af25adbd3711ad15f1bd9a40f654fa3491ba2a8ea0a", "timestamp" : 1549030424549, "action" : "transfer", "account_name" : "mvpmvpmvpmv1", "account" : "eosio.token", "data" : "10b6ac5bd62deb9650b7ac5bd62deb96010000000000000004454f530000000000", "cpu_usage" : 599, "net_usage" : 91, "block_number" : 11748525, "block_time" : 1549030424500, "last_updated_time" : 1549030424553}
	
	db.account_actions.aggregate([ { "$match": { account_name : "junglefaucet", block_number : { $gte: 11748525 }}}, {"$group": {_id: "$account_name", max: { $max: "$block_time" }, min: { $min: "$block_time" }, count: { $sum: 1} }}]);
	

##	number of actions for account and dapp

	db.account_actions.aggregate([ 
		{ "$match": { account_name : "bingotester5", "dapp_account" : "eosio.token"}}, 
		{ "$group": { _id: "$account_name", count: { $sum: 1} }}
	]);

##	total number of actions dapp

	db.account_actions.aggregate([ 
		{ "$match": { "dapp_account" : "owdinnetwork"}}, 
		{ "$group": { _id: "$dapp_account", count: { $sum: 1} }}
	]);

##	

	db.account_actions.aggregate([ 
		{ "$match": { "dapp_account" : "owdinnetwork"}}, 
		{ "$group": { _id: "$account_name", count: { $sum: 1} }},
		{ "$group": { _id: "$account_name", max: { $max: "$count"} }}
	]);

		db.account_actions.aggregate([ 
			{ "$match": { "account" : "eosio.token", "data.to": "bingobetgame"}},
			{ "$group": { _id: "$data.to", max: { $max: "$data.quantity" }}},
		]);

##	max amount for bet

		db.account_actions.aggregate([
			{ "$match": { "account" : "eosio.token", "dapp_account": "bingobetgame"}},
			{ $project : { quantity : { $split: ["$data.quantity", " "]}, dapp_account: 1  } },
			{ $unwind : "$quantity" },
			{ $match : { quantity : { "$regex" : "/[0-9]/", "$options" : "" } } },
			{ $group : { _id: "$dapp_account", max : { "$max" : "$quantity" } } }
		]);

##	

		db.account_actions.aggregate([
			{ "$match": { "account" : "eosio.token", "dapp_account": "bingobetgame" }},
			{ $project : { quantity : { $split: ["$data.quantity", " "]}, data: 1 } },
			{ $unwind : "$quantity" },
			{ $match : { quantity : /[0-9]/ } },
			{ $group : { _id: "$dapp_account", max : { "$max" : "$quantity" } } },
			{ $sort : { max : -1 } }
		]);

	db.account_actions.aggregate([ 
		{ "$match": { "account" : "eosio.token"}}, 
		{ "$group": { _id: "$account_name", count: { $sum: 1} }},
		{ "$sort": { count: -1} }
	]);


	db.account_actions.aggregate( [
  	{ $match: { account_name : "sicborobot24"}},
	{ $group: {_id: "$account_name", max: { $max: "$block_number" } } } 
	]);

		{ "$unwind": "$data" },
		{ "$project": {"diff": {"$divide": [
                { "$subtract": [ "$firstX", "$lastX" ] },
                { "$subtract": [ "$firstY", "$lastY" ] }
            ]
        }
    }},
	]);

	db.scoring_rules.updateOne({"name":"bot"}, {$set: {rule_param.count: 5}})