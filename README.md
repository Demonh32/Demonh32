{
  "$name": "Server Info",
  "$description": "Displays server information",
  "$trigger": {
    "$type": "message",
    "$event": "messageReceived",
    "$filter": {
      "$type": "messageContent",
      "$value": "تعريف"
    }
  },
  "$response": {
    "$type": "embed",
    "$title": "Server Information 📊",
    "$description": "Here is the information about this server:",
    "$color": "#3498db",
    "$fields": [
      {
        "$name": "Server Name",
        "$value": "${server.name}",
        "$inline": true
      },
      {
        "$name": "Server ID",
        "$value": "${server.id}",
        "$inline": true
      },
      {
        "$name": "Member Count",
        "$value": "${server.memberCount}",
        "$inline": true
      },
      {
        "$name": "Owner",
        "$value": "${server.owner.username}#${server.owner.discriminator}",
        "$inline": true
      }
    ]
  }
}
