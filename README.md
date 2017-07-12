# rect_packer
Simple algorithm for packing rects into a bigger rect.

# Usage
```nim
import rect_packer

let p = newPacker(1024, 1024)
let sizesToPack = [ (100, 100), (50, 50), (100, 50) ]
for i, s in sizesToPack:
    let res = p.pack(s[0].int32, s[1].int32)
    echo "Rect ", i, " coords: ", res
```
Output:
```
Rect 0 coords: (x: 0, y: 0)
Rect 1 coords: (x: 100, y: 0)
Rect 2 coords: (x: 150, y: 0)
```
