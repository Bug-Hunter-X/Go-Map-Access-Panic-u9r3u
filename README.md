# Go Map Access Panic

This repository demonstrates a common error in Go: panicking due to accessing an uninitialized map.  Uninitialized maps in Go will result in a runtime panic if you try to access or modify them.

## The Bug

The `bug.go` file shows a simple program that attempts to assign a value to a map without first initializing the map using `make()`. This results in a runtime panic.

## The Solution

The `bugSolution.go` file shows the corrected code. By using `make(map[string]int)` before accessing the map, we allocate the map in memory, preventing the panic. This should always be done when declaring a map if you intend to populate it with data later.