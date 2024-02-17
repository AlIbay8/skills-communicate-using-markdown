# H1 Header
###### H6 header

![Waking up in Outer Wilds](https://github.com/AlIbay8/skills-communicate-using-markdown/assets/43456952/fbf6c6fb-12fc-46a3-b8ce-1b5b06f56059)

``` gdscript
extends LdStreamPlayer
class_name LdStreamPlayer3D

func init_stream_players_node() -> void:
	var stream_players_node: Node = Node3D.new()
	stream_players_node.name = "StreamPlayers"
	self.add_child(stream_players_node)
	self.stream_players = stream_players_node

func get_player_template() -> Node:
	var player_node: AudioStreamPlayer3D = AudioStreamPlayer3D.new()
	for child in self.get_children():
		if child is AudioStreamPlayer3D:
			player_node = child.duplicate()
			child.queue_free()
			break
	return player_node
```

## Legadot to-do list
- [x] Debug imperfect loops caused by AudioServer latency
- [ ] Finish text documentation
- [ ] Make video tutorials
