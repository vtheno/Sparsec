# Sparsec
Parser Combinator in Python. Some demos can be found here.

### [Simple Calculator](Demos/SimpleCalc.py)
Parse arithmetic expression and calculate them.

    calculate("3*2*4/(2+2)+2*2/4+2")
    calculate("2+(3+4)*5")

### [Json Parser](Demos/JsonParser.py)
Parse Json format input string into python dict, list, etc.

    load("""{
            "programmers": [{
                "firstName": "Brett",
                "lastName": "McLaughlin",
                "email": "aaaa"
            }, {
                "firstName": "Jason",
                "lastName": "Hunter",
                "email": "bbbb"
            }],
            "authors": [{
                "firstName": "Isaac",
                "lastName": "Asimov",
                "genre": "sciencefiction"
            }]
        }""")

### [Schemer](Demos/Schemer.py)
Parse Scheme code into AST and evaluate them using visitor pattern.
    
    v = EvalVisitor(env)
    v.visit(ReadExpr("(- (+ 4 6 3) 3 5 2)"))
    v.visit(ReadExpr("(define f (lambda (x y) (+ x y)))"))
    v.visit(ReadExpr(("(f 1 2)"))
