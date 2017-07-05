Haskell 勉強会
=========

もくもく会
「すごいHaskell」を読む

## 2017/7/5 (Wed) @ Yahoo コワーキングスペース
 - Haskell 開発環境構築
```
brew install ghc
```
終わり

 - "Hello world!"
```
⋊> ~/D/G/haskell_study on master ⨯ ghc -e main 0705.hs                                                                                                                       20:55:11
Hello World!
```

```
> head [1, 3]
1
> fst (1, 3)
1
> zip [1,2,3,4] [4,5,5]
[(1,4),(2,5),(3,5)]
> let rightTriangles = [ (a,b,c) | c <- [1..10], b <- [1..c], a <- [1..b], a^2 + b^2 == c^2]
> rightTriangles
[(3,4,5),(6,8,10)]
> let rightTriangles2 = [ (a,b,c) | c <- [1..10], b <- [1..10], a <- [1..10], a^2 + b^2 == c^2]
> rightTriangles2
[(4,3,5),(3,4,5),(8,6,10),(6,8,10)]
> :t "a"
'a' :: Char
> :t (True, "True")
(True, "True") :: (Bool, [Char])
```

Functions also have types. When writing our own functions, we can choose to give them an explicit type declaration.

```
> :t head
head :: [a] -> a
> :t fst
fst :: (a, b) -> a
> :t (==)
(==) :: Eq a=> a -> a -> Bool
> :t (>)
(>) :: Ord a => a -> a -> Bool
> read "3.4" + 8.4
11.8
> :t read
read :: Read a => String -> a
> [LT .. GT]
[LT,EQ,GT]
```