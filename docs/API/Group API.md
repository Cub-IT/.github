# That document describes API that is used by clients to interact with CubIT

### GET /api/v1/user/:userId/groups
<details>
	<summary>All groups that usar take part in</summary>
	
	#### Example:
	
	```
	curl --location --request GET 'https://cub.it/api/v1/user/cabef633-3b34-45db-801f-d5b21b9e7bee/groups' \
	--header 'Content-Type: application/json'
	```
	
	#### Response:
	HTTP status code: 200
	
	```
	[
		{
			“groupId” : “cabef633-3b34-45db-801f-d5b21b9e7bee”
			“name” : “Group name1”,
			“description” : “This is a cool group1”,
			“ownerFirstName” : “Alex1”,
			“ownerLastName” : “Slabos1”,
			“ownerEmail” : “owner.email@gmail.com3”,
			“coverColor” : “#0000003c”
		},
		{
			“groupId” : “cabef633-3b34-45db-801f-d5b21b9e7bwe”,
			“name” : “Group name2”,
			“description” : “This is a cool group2”,
			“ownerFirstName” : “Alex2”,
			“ownerLastName” : “Slabos2”,
			“ownerEmail” : “owner.email@gmail.com2”,
			“coverColor” : “#0000004f”
		},
		{	
			“groupId” : “cabef633-3b34-45db-801f-d5b21b9e7bef”,
			“name” : “Group name3”,
			“description” : “This is a cool group3”,
			“ownerFirstName” : “Alex3”,
			“ownerLastName” : “Slabos3”,
			“ownerEmail” : “owner.email@gmail.com3”,
			“coverColor” : “#0000003c”
		}
	]
	```
</details>
