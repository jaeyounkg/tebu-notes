-   関数内包 (function closure)
-   let f(x_1, x_2, …, x_n) = e;;
	-   関数のパラメーター名の列
	-   本体式
	-   eに現れるx_i以外の変数の値で作った環境
-   型スキーム
	-   型変数が含まれた型
	-   val size : 'a tree -> int = <fun>
-   主要型(principal type) 
	-   OCaml の型推論機能は，引数がどんな使われ方をしているかを調べて，できるだけ多相的な，つまり一般的な，型(スキーム)を推論する
-   匿名関数
	-   (fun n -> n*n)

```ocaml
(* Replace Lf with e and Br with f *)  
let rec treefold e f t =  
  match t with  
    Lf -> e  
  | Br {left=l; value=v; right=r} ->  
    f (treefold e f l)  
      v  
      (treefold e f r)  
  
(* Interpret Lf as 0 and Br as addition *)  
let s6 = treefold 0 (fun l v r -> l + v + r) t6  
let s7 = treefold 0 (fun l v r -> l + v + r) t7  
  
(* Conversion to a string can be written in terms of fold *)  
let str6 = treefold "leaf" (fun l v r -> "branch(" ^ l ^ ", " ^ (string_of_int v) ^ ", " ^ r ^ ")") t6  
let str7 = treefold "leaf" (fun l v r -> "branch(" ^ l ^ ", " ^ (string_of_int v) ^ ", " ^ r ^ ")") t7
```