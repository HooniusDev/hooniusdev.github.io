## My first post


This be crazy 

```gdscript {.line-numbers}
extends PanelContainer

#Cache reference to Minefield TileMap
@onready var minefield: TileMap = $Minefield

func _gui_input(event: InputEvent) -> void:
    Convert mouse position to a Minefield cell coordinate
    var mouse_cell: Vector2i = minefield.local_to_map(minefield.get_local_mouse_position())
    #Only act if mouse button is released
    if event is InputEventMouseButton and event.is_released():
        if event.button_index == MOUSE_BUTTON_LEFT:
            # print to console what cell was LEFT clicked
            print("cell left clicked: " , mouse_cell)
        elif event.button_index == MOUSE_BUTTON_RIGHT:
            #print to console what cell was RIGHT clicked
            print("cell right clicked: " , mouse_cell)`
```
