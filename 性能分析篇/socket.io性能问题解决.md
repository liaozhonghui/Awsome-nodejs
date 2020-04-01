

# socket.io性能问题解决

```js
const sp=require('schemapack');
const playerSchema=sp.build([{
    uuid:'string',
    mode:'string',
    nodeType:'string',
    lastUpdateTime:'uint32',
    sampleNum:'uint16',
    queueValues:[{
        k:'uint32',
        v:'float64'
    }],
}])
// encode
var buffer = playerSchema.encode(player);
socket.emit('player-message', buffer); // Use some JavaScript WebSocket library to get this socket variable.

// decode 
socket.on('player-message', function(buffer) {
    var player = playerSchema.decode(buffer);
}
```
