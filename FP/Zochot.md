# DIXAK_ER 
## A 
A из кф
## B
B из кф
## C 
C из кф
## D 
D из кф
## E 
E из кф
## F 
F из кф
## S
биномиальная куча

# DEYTD
## A
на вход подаётся некоторый алфавит. Построить все сочетания для этого алфавита. 
## B
```data Builder = One Char | Many [Builder] ```
написать инстансы функтора, аппликатива и монады для этого так, чтобы toList . (>>=) f  работало также как и (>>=) (toList . f)
## C
```data Arrow a b = Arrow { vec :: a -> b }```
написать инстанс монойда, если известно што b -- монойд
## D
написать a. k. a. file system с командами типа cd, ls но без работы с реальной фс
## E
написать 2048
## F
написать сокобан   
## S
S-s-s-nake + пара фич

# GrandArchTemplar
## A
## B
## C
## D
## E
## F
## S


# Dubrov_eva
## A
программа которая ищет все подпоследовательности из данной строки
## B
data BiAlgebra a b = Bi { lEndo :: a -> a, rendo :: b -> b }
написать инстанс монойда для етого
## C
```
class Functor w => CComonad w where
    (>=>=) :: (w a -> b) -> (w b -> c) -> (w a -> c)
    cextract :: w a -> a
```
data Ident a = Ident { val :: a } 
реализовать инстансы полугруппы, монойда, функтора, аппликативы, монады и комонады для этого 
## D
написать тетрис
## E
написать тиндер с текстовыми описаниями вместо фоток и без мессаджинга и сетевых протоколов: только лайк или дислайк 
текстовых описаний с запоминанием пользователей и функцией getNextCard с n гендерами и с возможностью предпочитать некоторые 
k из n гендеров
## F
написать инстанс комонады для нонемпти листа
## S
Fish monad:
```
class Applicative m => JMonad m where
    jjoin :: m (m a) -> m a
    jreturn :: a -> m a

class Applicative m => FMonad m where
  (>>=>) :: (a -> m b) -> (b -> m c) -> (a -> m c)
  freturn :: a -> m a

class Applicative m => NMonad m where
    (>>>=) :: m a -> (a -> m b) -> m b
    nreturn :: a -> m a
    
instance FMonad m => NMonad m where
   (>>>=) = ?
   nreturn = ?
   
instance NMonad m => FMonad m where
   (>>=>) = ?
   freturn = ?

instance JMonad m => NMonad m where
   (>>>=) = ?
   nreturn = ?

instance NMonad m => JMonad m where
   join = ?
   jreturn = ?

instance FMonad m => JMonad m where
   join = ?
   jreturn = ?

instance JMonad m => FMonad m where
   (>>=>) = ?
   freturn = ?
```
