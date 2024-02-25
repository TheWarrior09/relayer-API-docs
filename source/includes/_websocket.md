# Websocket API

## Subscribe Live Price Data

```javascript
const socket = new WebSocket("wss://twilight.rest/ws");

const subscriptionPayload = {
  jsonrpc: "2.0",
  method: "subscribe_live_price_data",
  id: 123,
  params: null,
};

socket.onopen = () => {
  socket.send(JSON.stringify(subscriptionPayload));
};

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log("Received live price update:", data);
};
```

> The result from the above endpoint looks like this:

```json
{
  "jsonrpc": "2.0",
  "result": 1634715868348666,
  "id": 123
}
```

### Endpoint URL

`wss://twilight.rest/ws`

### Description

Subscribe Live Price Data

### Parameters

- **`jsonrpc`** (String, required): The JSON-RPC protocol version. Must be set to `"2.0"`.
- **`method`** (String, required): The name of the method to be invoked.
- **`id`** (Number, required): A unique identifier for the request.
- **`params`** (Object, optional): Additional parameters for the method, if any.

### Method

`subscribe_live_price_data`

## Subscribe Order Book

```javascript
const socket = new WebSocket("wss://twilight.rest/ws");

const subscriptionPayload = {
  jsonrpc: "2.0",
  method: "subscribe_order_book",
  id: 123,
  params: null,
};

socket.onopen = () => {
  socket.send(JSON.stringify(subscriptionPayload));
};

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log("Received live order book update:", data);
};
```

> The result from the above endpoint looks like this:

```json
{
  "jsonrpc": "2.0",
  "result": 7768140282752642,
  "id": 123
}
```

### Endpoint URL

`wss://twilight.rest/ws`

### Description

Subscribe Order Book

### Parameters

- **`jsonrpc`** (String, required): The JSON-RPC protocol version. Must be set to `"2.0"`.
- **`method`** (String, required): The name of the method to be invoked.
- **`id`** (Number, required): A unique identifier for the request.
- **`params`** (Object, optional): Additional parameters for the method, if any.

### Method

`subscribe_order_book`

## Subscribe Candle Data

```javascript
const socket = new WebSocket("wss://twilight.rest/ws");

const subscriptionPayload = {
  jsonrpc: "2.0",
  method: "subscribe_candle_data",
  id: 123,
  params: { interval: "ONE_HOUR" },
};

socket.onopen = () => {
  socket.send(JSON.stringify(subscriptionPayload));
};

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log("Received live candle data update:", data);
};
```

> The result from the above endpoint looks like this:

```json
{
  "jsonrpc": "2.0",
  "method": "s_candle_data",
  "params": {
    "subscription": 1177191929099717,
    "result": []
  }
}
```

### Endpoint URL

`wss://twilight.rest/ws`

### Description

Subscribe Candle Data

### Parameters

- **`jsonrpc`** (String, required): The JSON-RPC protocol version. Must be set to `"2.0"`.
- **`method`** (String, required): The name of the method to be invoked.
- **`id`** (Number, required): A unique identifier for the request.
- **`params`** (Object, optional): Additional parameters for the method, if any.

### Method

`subscribe_candle_data`

## Subscribe Recent Trades

```javascript
const socket = new WebSocket("wss://twilight.rest/ws");

const subscriptionPayload = {
  jsonrpc: "2.0",
  method: "subscribe_recent_trades",
  id: 123,
  params: null,
};

socket.onopen = () => {
  socket.send(JSON.stringify(subscriptionPayload));
};

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log("Received live recent trades update:", data);
};
```

> The result from the above endpoint looks like this:

```json
{
  "jsonrpc": "2.0",
  "result": 2931691776204415,
  "id": 123
}
```

### Endpoint URL

`wss://twilight.rest/ws`

### Description

Subscribe Recent Trades

### Parameters

- **`jsonrpc`** (String, required): The JSON-RPC protocol version. Must be set to `"2.0"`.
- **`method`** (String, required): The name of the method to be invoked.
- **`id`** (Number, required): A unique identifier for the request.
- **`params`** (Object, optional): Additional parameters for the method, if any.

### Method

`subscribe_recent_trades`

## Subscribe Heartbeat

```javascript
const socket = new WebSocket("wss://twilight.rest/ws");

const subscriptionPayload = {
  jsonrpc: "2.0",
  method: "subscribe_heartbeat",
  id: 123,
  params: null,
};

socket.onopen = () => {
  socket.send(JSON.stringify(subscriptionPayload));
};

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  console.log("Received live recent trades update:", data);
};
```

> The result from the above endpoint looks like this:

```json
{
  "jsonrpc": "2.0",
  "method": "s_heartbeat",
  "params": {
    "subscription": 8669657463617608,
    "result": "BEAT"
  }
}
```

### Endpoint URL

`wss://twilight.rest/ws`

### Description

Subscribe Heartbeat

### Parameters

- **`jsonrpc`** (String, required): The JSON-RPC protocol version. Must be set to `"2.0"`.
- **`method`** (String, required): The name of the method to be invoked.
- **`id`** (Number, required): A unique identifier for the request.
- **`params`** (Object, optional): Additional parameters for the method, if any.

### Method

`subscribe_heartbeat`
