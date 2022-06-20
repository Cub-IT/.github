# That document describes API that is used by clients to interact with CubIT

### GET /api/v1/user/:userId/groups
<details>
<summary>All groups that user take part in</summary>
	
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

### GET /api/v1/user/:userId/groups/:groupId
<details>
<summary>A group that user take part in</summary>
	
#### Example:
	
```
curl --location --request GET 'https://cub.it/api/v1/group/cabef633-3b34-45db-801f-d5b21b9e7bee' \
--header 'Content-Type: application/json'
```
	
#### Response:
HTTP status code: 200
```
{
	{
		“groupId” : “groupId1”,
		“name” : “Group name1”,
		“description” : “This is a cool group1”,
		“ownerFirstName” : “Axel”,
		“ownerLastName” : “Slabos”
		“ownerEmail” : “owner.email@gmail.com”,
		“coverColor” : “#0000003c”

	},
	“taskList” : [
		{
			“id” : “postId1”,
			“creationDate” : “12.17.1973”,
			“userFirstName” : “Axel”,
			“userLastName” : “Slabos”,
			“content” : “content first line\ncontent second line\nhttps://some-link.com”
			“userColor” : “#0000003c”
		},
		{
			“id” : “postId2”,
			“creationDate” : “12.17.1973”,
			“userFirstName” : “Axel”,
			“userLastName” : “Slabos”,
			“content” : “content first line\ncontent second line\nhttps://some-link.com”
			“userColor” : “#0000003c”
		}
	]
}
```
</details>

### POST /api/v1/user/:userId/groups/
<details>
<summary>Create a new group</summary>
	
</details>

### POST /api/v1/user/:userId/groups/
<details>
<summary>Join the group</summary>
	
### Request
```
	{
		"groupCode" : "H3F4691J"
	}
```
### Response
HTTP status code: 200
	
</details>

### PATCH /api/v1/user/:userId/groups/:groupId
<details>
<summary>Change an information about a group</summary>
	
</details>

### DELETE /api/v1/user/:userId/groups/:groupId
<details>
<summary>Leave a group</summary>
	
</details>
