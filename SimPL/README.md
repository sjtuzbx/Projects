#Simple programming language

This is simplified **interpreter** in JAVA. It's **functional** and **imperative**.

##Usage

There're examples in in doc/ folder. You can use `java -jar SimPL.jar factorial.spl` to run the program. Here're some example usages.

###Calculate the factorial

    let fact = rec f =fn x =if x=1 then 1 else x * (f (x-1))
    in  fact 4
    end
    (* ==24 *)

###Sum of a list of integers

	let
	  sum = rec sum =>
	  		fn a => if a=nil
	                then 0
	                else hd a + sum (tl a)
	in
	  sum (1::2::3::nil)
	end
	(* ==> 6 *)

###Greatest common divisor

	let gcd = rec g => fn a => fn b =>
	            if b=0 then a else g b (a % b)
	in  gcd 34986 3087
	end
	(* ==> 1029 *)