# Data Structures and Algorithms — C implementations

A collection of data-structure implementations and file-processing exercises written in C, developed for university coursework.

## Contents

### `B+Tree/` — B+ Tree

A B+ Tree with `MIN_DEGREE = 3`, implemented in a single C file. Supports:

- insertion with node splitting,
- search,
- deletion with borrowing from siblings and node merging,
- level-order display of the tree.

```bash
gcc -O2 -o B+Tree/bptree B+Tree/B+.c
./B+Tree/bptree
```

`main` inserts a small set of keys, prints the tree, and exercises search and deletion.

### `Tde_2/` — hash index over binary records

A 256-bucket hash table with separate chaining, used to index product records stored in a binary file. Includes:

- `reader.c` — sequential binary-file reading,
- `hash.c` — hash index creation, insertion, and lookup,
- `main.c` — entry point with elapsed-time measurement.

```bash
gcc -O2 -o Tde_2/src/main Tde_2/src/main.c Tde_2/src/hash.c Tde_2/src/reader.c
cd Tde_2 && ./src/main
```

The program reads `../input/produtos_final_novo.bin`, which is **not included** in the repository.

### `exec1/` — text-file join

Reads `arqMovies.txt` and `directors.txt`, stores movies and directors in structs, and matches each movie to its director by ID.

```bash
gcc -O2 -o exec1/files exec1/files.c
cd exec1 && ./files
```

### `exec2/` — binary file with a linked-list index

Reads a binary movie file (`arqMovies.bin`), builds a singly linked list indexing records by the first letter of the title, prints the index, and searches for a title.

```bash
gcc -O2 -o exec2/function exec2/function.c
cd exec2 && ./function
```

## Notes

Several compiled binaries were committed in the past (`B+Tree/B+`, `exec1/files`, `exec2/function`, `Tde_2/src/a.exe`). Remove them from version control with:

```bash
git rm --cached B+Tree/B+ exec1/files exec2/function Tde_2/src/a.exe
```
