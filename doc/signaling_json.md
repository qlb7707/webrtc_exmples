##The json message used by signaling server and client

[toc]

###1. sign in message
```
{
"eventName": "__join",
"data":
   {
	 "room":XXXX		
   }
}
```

###2. the message sent to other peers when a new peer connected

```
{
	"eventName": "_new_peer",
	"data":
	{
		"socketId":XXXX
	}
}
```

###3. the message to sent to tell the new connected pair about the info of other connected peers 
```
{
	"eventName":"_peers",
	"data":
	{
		"connections":[XXXX,XXXX,...],
		"you":XXXX
	}
}
```

###4. the message of ice candidate
```
{
	"eventName":"_ice_candidate",
	"data":
	{
		"label":XXXX,
		"sdpMid":XXXX,
		"candidate":XXXX,
		"socketId":XXXX
	}
}
```

###5. the message of offer
```
{
	"eventName":"_offer",
	"data":
	{
		"sdp":XXXX,
		"socketId":XXXX
	}
}
```

###6. the message of answer

```
{
	"eventName":"_answer",
	"data":
	{
		"sdp":XXXX,
		"socketId":XXXX
	}
}
```

###7. the message sent when a peer disconnected

```
{
	"eventName":"_remove_peer",
	"data":
	{
		"socketId":XXXX	
	}
}
```
