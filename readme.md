Howdy, welcome to the extra credit. Looks a lot like the final...Let's get started.

Lexeme Table
    token_code. token -> symbol
    1. real_literal -> {0-9}\*.{0-9}\*
    2. int_literal -> {0-9}\*
    3. bool_literal -> True | False
    4. char_literal -> '{a-zA-Z,.\'\";:\\!@#%^&*()_-=+`~<>?/\t\n\f\b}'
    5. string_literal -> "{a-zA-Z,.\'\";:\\!@#%^&*()_-=+`~<>?/\t\n\f\b}\*"
    6. selection_keyword_if -> if
    7. selection_keyword_else -> else
    8. iteration_keyword_while -> while
    9. iteration_keyword_for -> for
    10. iteration_keyword_do -> do
    11. variable_keyword_var -> var
    12. type_keyword_nat -> nat
    13. type_keyword_bool -> bool
    14. type_keyword_char -> char
    15. type_keyword_string -> string
    16. type_keyword_real -> real
    17. addition_operator -> +
    18. subtraction_operator -> -
    19. multiplication_operator -> *
    20. division_operator -> /
    21. modulo_operator -> %
    22. assignment_operator -> =
    23. equality_operator -> ==
    24. inequality_operator -> !==  
    25. less_than_operator -> <
    26. greater_than_operator -> >
    27. less_than_or_equal_operator -> <==
    28. greater_than_or_equal_operator -> >==
    29. logical_and_operator -> &&
    30. logical_or_operator -> ||
    31. logical_not_operator -> !
    32. exponentiation_operator -> **
    33. left_parenthesis -> (
    34. right_parenthesis -> )
    35. left_brace -> {
    36. right_brace -> }
    37. negation_operator -> -
    38. function_keyword -> function
    39. identifier -> id

Syntax Table:
    <stmt> --> <block> | <if_stmt> | <assignment> | <empty>
    <block> --> `{`{<stmt>}`}`
    <loop> --> <while_loop> | <do_while> | <for_loop>
    <if_stmt>   -->  `if``(`<bool_stmt> `)`<stmt>[`else ` <stmt>]
    <do_while> --> `do` <block> <while_loop>
    <while_loop> -->  `while``(`<bool_stmt>`)`<stmt>
    <for_loop> --> `for``(`<bool_stmt>`)`<block>
    <assignment> --> `var` <id> `=` <expr>
    <functions> -- > `function` <id> `(` <id> `)` <block>
    <expr> --> <term> {(`+`|`-`)<term>}
    <term> --> <val>{(`*`|`/`|`%`|`\*\*`)<val>}
    <val> --> <id> | <real_literal> | <integer_literal> | <bool_literal> | <char_literal> | <string_literal> | `(` <expr> `)`
    <bool_stmt> --> `True` | `False` | <expr> (`==`|`!==`|`<`|`>`|`<==`|`>==`) <expr> | `(` <bool_stmt> `)` | `!` <bool_stmt> | <bool_stmt> (`&&`|`||`) <bool_stmt> --> `True` | `False` | <expr> (`==`|`!==`|`<`|`>`|`<==`|`>==`|`&&`|`||`) <expr>
    <empty> --> ``
