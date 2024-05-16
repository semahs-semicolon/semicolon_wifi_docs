# RESTFUL API

## Endpoint: /api/rest

[Datatype (typescript)](https://www.notion.so/Datatype-typescript-97b2e0724be242339a3e628ce8ed3d10?pvs=21) 

## Without Authentication

### GET: /api/rest/status

- Response: JSON
- HTTP Code: 200

```json
{
	server: "up" | "down"
	api: {
		rest: "up" | "down"
		websocket: "up" | "down"
	}
}
```

## With Authentication

- Using sha-256 based Authentication Header
- Return 401 Unauthorized if Authentication Header is not provided or vaild

### GET: /api/rest/floor

모든 Floor를 반환

- Response: JSON
- Data: Floor[]

### GET: /api/rest/floor/{floor}

Floor가 {floor}인 Floor 반환

- Response: JSON
- Data: Floor

### GET: /api/rest/ap

모든 AP를 반환

- Response: JSON
- Data: AP[]

### POST: /api/rest/ap

Request Form 조건에 맞는 모든 AP를 반환

- Response: JSON
- Request Form

```json
{
	//AP 인터페이스의 아무 항목 (1개 이상)
	[k in AP]: AP[k]
}
```

- Data: AP[]

### GET: /api/rest/ap/{id}

아이디가 {id}인 AP를 반환

- Response: JSON
- Data: AP

### GET: /api/rest/sta

모든 STA를 반환

- Response: JSON
- Data: STA[]

### POST: /api/rest/sta

Request Form에 맞는 모든 STA를 반환

- Response: JSON
- Request Form

```json
{
	//STA 인터페이스의 아무 항목 (1개 이상)
	[k in STA]: STA[k]
}
```

- Data: STA[]

### GET: /api/rest/sta/{id}

id가 {id}인 STA를 반호

- Response: JSON
- Data: STA

###
