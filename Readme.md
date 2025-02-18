# Go Core Utils Library

A collection of fundamental utility functions built from scratch without external dependencies. This serves as my personal toolkit for common operations used across different projects.

## 🎯 Overview

Building core utilities from scratch to understand the underlying mechanics and avoid external dependencies. This includes cryptographic functions, sorting algorithms, and other essential tools.

## 📦 Core Packages

### `crypto`

```go
package crypto

// Cryptographic implementations from scratch
func SHA256(data []byte) []byte
func HashPassword(password []byte) ([]byte, error)
func VerifyPassword(hashedPassword, password []byte) bool
func GenerateRandomBytes(length int) []byte
```

### `jwt`

```go
package jwt

// Custom JWT implementation
func CreateToken(payload map[string]interface{}, secret []byte) string
func VerifyToken(token string, secret []byte) (map[string]interface{}, error)
```

### `sort`

```go
package sort

// Sorting algorithm implementations
func QuickSort(arr []int) []int
func MergeSort(arr []int) []int
func HeapSort(arr []int) []int
func BinarySearch(arr []int, target int) int
```

### `datastructures`

```go
package datastructures

// Custom data structure implementations
type LinkedList[T any]
type Stack[T any]
type Queue[T any]

```

### `encoding`

```go
package encoding

// Custom encoders/decoders
func Base64Encode(data []byte) string
func Base64Decode(str string) []byte
func HexEncode(data []byte) string
```

### `validation`

```go
package validation

// Input validation
func IsEmail(email string) bool
func IsNumeric(str string) bool
func IsAlphanumeric(str string) bool
```

## 🚀 Usage Example

```go
package main

import (
    "fmt"
    "github.com/thnamuS/goutils/crypto"
    "github.com/thnamuS/goutils/sort"
)

func main() {
    // Using crypto
    hash := crypto.SHA256([]byte("hello"))

    // Using sorting
    arr := []int{64, 34, 25, 12, 22, 11, 90}
    sorted := sort.QuickSort(arr)
}
```

the above code is just a example usage

## 📝 Project Structure

```
.
├── crypto/
├── jwt/
├── sort/
├── datastructures/
├── encoding/
├── validation/
└── tests/
```

## 🔨 Development Principles

1. Pure Go implementation
2. Zero external dependencies
3. Clear documentation
4. Comprehensive testing
5. Performance optimization

## 📈 Future Additions

- [ ] RSA encryption
- [ ] More sorting algorithms(thinking to add 2)
- [ ] Network utilities
- [ ] Compression algorithms (Wild Toughts in mind)

## 📞 Contact

sumanthmahantu@gmail.com
