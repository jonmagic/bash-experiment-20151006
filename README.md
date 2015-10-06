# bash experiment 20151005

Loop through results from find command and extract a part of each result and then test if that path exists.

```bash
$ git clone https://github.com/jonmagic/bash-experiment-20151006
...
$ cd bash-experiment-20151006
```

```bash
bash-experiment-20151006 $ tree
.
├── README.md
├── cache
│   └── data
│       ├── a
│       │   ├── 1
│       │   │   └── cache
│       │   ├── 2
│       │   │   └── cache
│       │   ├── 3
│       │   │   └── cache
│       │   └── cache
│       ├── b
│       │   └── 4
│       │       └── cache
│       └── c
│           ├── 7
│           └── 8
│               └── cache
├── data
│   ├── a
│   │   ├── 1
│   │   └── 2
│   ├── b
│   │   ├── 4
│   │   ├── 5
│   │   └── 6
│   └── c
│       ├── 7
│       └── 9
└── run

28 directories, 2 files
```

```bash
bash-experiment-20151006 $ ./run
cache dir: ./cache/data/a/1/cache
possible associated path: ./data/a/1
found: ./data/a/1

cache dir: ./cache/data/a/2/cache
possible associated path: ./data/a/2
found: ./data/a/2

cache dir: ./cache/data/a/3/cache
possible associated path: ./data/a/3
not found: ./data/a/3

cache dir: ./cache/data/b/4/cache
possible associated path: ./data/b/4
found: ./data/b/4

cache dir: ./cache/data/c/8/cache
possible associated path: ./data/c/8
not found: ./data/c/8
```
