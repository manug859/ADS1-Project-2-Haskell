# Haskell

## Proyecto 1

### Summary
This project introduces different types of data.

### Some interesting functions of this project 

``` haskell 
la_concat :: ListaAsoc a b -> ListaAsoc a b -> ListaAsoc a b 
la_concat xs Vacia = xs
la_concat Vacia xs = xs
la_concat (Nodo a b xs) ys = (Nodo a b(la_concat xs ys))

la_agregar :: Eq a => ListaAsoc a b -> a -> b -> ListaAsoc a b
la_agregar Vacia clave valor = Nodo clave valor Vacia
la_agregar (Nodo a b xs) clave valor | (a==clave) = (Nodo a valor xs)
                                     | otherwise = Nodo a b (la_agregar xs clave valor)
```
Based on the associated list concept.
