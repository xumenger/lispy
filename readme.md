```
xumenger-mac:lispy xumenger$ python2 lis.py 
lispy> (quote (testing 1 (2.0) -3.14e159))
(testing 1 (2.0) -3.14e+159)
lispy> (+ 2 2)
4
lispy> (+ (* 2 100) (* 1 10))
210
lispy> (if (> 6 5) (+ 1 1) (+ 2 2))
2
lispy> (define x 3)
lispy> (begin (define x 1) (set! x (+ x 1)) (+ x 1))
3
lispy> ((lambda (x) (+ x x)) 5)
10
lispy> (define twice (lambda (x) (* 2 x)))
lispy> (twice 5)
10
lispy> (define compose (lambda (f g) (lambda (x) (f (g x)))))
lispy> ((compose list twice) 5)
(10)
lispy> (define repeat (lambda (f) (compose f f)))
lispy> ((repeat twice) 5)
20
lispy> ((repeat (repeat twice)) 5)
80
lispy> (define fact (lambda (n) (if (<= n 1) 1 (* n (fact (- n 1))))))
lispy> (fact 3)
6
lispy> (fact 50)
30414093201713378043612608166064768844377641568960512000000000000
lispy> (define abs (lambda (n) ((if (> n 0) + -) 0 n)))
lispy> (list (abs -3) (abs 0) (abs 3))
(3 0 3)
```
