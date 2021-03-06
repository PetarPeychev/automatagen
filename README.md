# automatagen
Generate random terrain using cellular automata.

Compatibilities
------------

* *Python 3.x*
* *Any Operating System*

Installation
------------

automatagen is published on **PyPi**, so you only need to run the following command:

    $ pip install automatagen
    
Usage
------------

Note: TerrainGenerator.generate(width, height) returns a 2d array of boolean values. All visualisations are made using numpy and matplotlib.

Instantiating a new TerrainGenerator:

```python
from automatagen import TerrainGenerator
    
terrgen = TerrainGenerator()
```

Generating a random 196x64 size map:

```python
map = terrgen.generate(196, 64)
```
![196x64 default settings](196x64_default.png?raw=true "196x64 default settings")

Instantiating a TerrainGenerator with different options:

```python
terrgen = TerrainGenerator(initial_density = 0.25, steps = 10, loneliness_limit = 5)
```

Generating a random 196x64 map with the new options:

```python
map = terrgen.generate(196, 64)
```
![196x64 different options](196x64_10steps_0.25density_5loneliness.png?raw=true "196x64 different options")

Generating a 196x64 map with a specific seed:

```python
map = terrgen.generate(seed = 9001)
```
![196x64 seeded map](seeded_map.png?raw=true "196x64 seeded map")

And generating another one with the same seed:

```python
map = terrgen.generate(seed = 9001)
```
![196x64 seeded map](seeded_map.png?raw=true "196x64 seeded map")
