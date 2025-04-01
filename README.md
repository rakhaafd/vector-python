## Basic Vector

### Apa itu **Vector** ⁉️
Vektor adalah struktur data yang merepresentasikan suatu objek dalam ruang dengan besar (magnitude) dan arah (direction). Dalam matematika dan komputasi, vektor sering digunakan untuk grafik, kecerdasan buatan, fisika, dan analisis data.

### Karakteristik Vektor
- Dimensi: Vektor bisa satu dimensi (1D), dua dimensi (2D), atau lebih tinggi (nD).
- Operasi: Bisa dilakukan operasi matematika seperti penjumlahan, pengurangan, perkalian skalar, dan produk dot.

### Contoh Vector
- Vektor 2D: v = (x, y) -> Contohnya (3, 4)
- Vektor 3D: v = (x, y, z) -> Contohnya (1, 2, 3)

### Implementasi Dasar Vector di Python
```python
import numpy as np

v1 = np.array([3, 4])
v2 = np.array([1, 2])

# Operasi pada vektor lebih mudah
print("Penjumlahan vektor:", v1 + v2)
print("Pengurangan vektor:", v1 - v2)
print("Perkalian skalar:", 2 * v1)
print("Dot product:", np.dot(v1, v2))  # (3*1) + (4*2)

# Output
Penjumlahan vektor: [4 6]
Pengurangan vektor: [2 2]
Perkalian skalar: [6 8]
Dot product: 11
```
___

#### 1. Panjang (Magnitudo) Vector
> Panjang vektor (norma) dihitung dengan rumus:  
``|v| = √x2 + y2``

Implementasi di Python:  
```python
v = np.array([1,2,3])
magnitude = np.linalg.norm(v)
print(f"panjang vector: {magnitude}")
```

#### 2. Vector Satuan
> Panjang satuan dihitung dengan rumus:  
``v/|v|``

Implementasi di Python:  
```python
a = np.array([3,4])
def unit_vector(b):
    m = np.linalg.norm(b)
    return b/m

#vector satuan
a_unit = unit_vector(a)
print(f"vector satuan: {a_unit}")

#panjang vector satuan
print(f"panjang vector satuan: {np.linalg.norm(a_unit)}")
```