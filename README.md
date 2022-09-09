# GridManager V1.1

## About the grid manager
The grid manager is a simple script that gives you acces to building a custom grid on the unity world.<br>
when you want to check something in the grid or load the grid or even make a perlin noise random world generation it is all possible with my grid manager.


## Instalment
```bash
window > package manager > add from github > this.URL
```

## Note
- This manager is a stand alone form the grid component<br>
- This manager is still in development<br>
- Some features have minor bugs<br>



# Development
### Features to be added
- Better random world generation<br>
- Custom UI<br>

### Custom UI features
- Automaticly updating Width and Height for 2d array<br>
- Scrollbar for 2d array<br>

# Functions

### Save / Load
```cs
SaveGrid(string);
- the given string is gonna be the world/grid name.
- places the saved file into the default unity directory

LoadGrid(string);
- loads the grid from a name.

ReloadMap(); (has to be changed to ReloadGrid (it is NOT a map it is  A GRID))
- Reloads the grid if something went wrong when loading it in
- Gets called during {"LoadGrid();"}
```

### Convert Tile data
```cs
TileToGrid(TileData);
- returns 2d array of int
- used for bug hunting {"when ReloadMap();"} doesnt fix the bug
```

### Reusable Functions / Basic Logic
```cs
GetWorldPosition(int, int);
- Declaration [X, Y]
- returns Vector3 of unity world position

GetXY(Vector3, out int, out int);
-  Declaration [WorldPosition, X, Y]
- returns local grid cordinates

SetValue(int, int, int, bool);
- Declaration [X, Y, Value, Indexes-Text]
- sets the corect value onto the 2d array

SetValue(vector3, int, bool);
- Using [WorldPosition, Value, Indexes-Text]
- sets the correct value onto the 2d array

GetValue(int, int);
- Declaration [X, Y]
- returns int from the GridMap(int,int)

GetValue(Vector3);
- Declaration [WorldPosition]
- returns int form the GridMap(int,int)
```
