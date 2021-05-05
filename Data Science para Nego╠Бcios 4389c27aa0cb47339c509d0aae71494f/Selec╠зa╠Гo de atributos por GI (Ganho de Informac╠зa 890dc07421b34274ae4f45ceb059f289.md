# Seleção de atributos por GI (Ganho de Informação)

- Fórmula de entropia "entropy"

    $Entropia = p1 log(p1)-p2log(p2) - ...$

    ```python
    a, b = 7, 3 
    p1, p2 = a/(a+b), b/(a+b)
    # entropia de todo conjunto denominado S
    entropia_S = -(p1*np.log2(p1) + p2*np.log2(p2))
    ```

    $Entropia(pai) = -[p(c1).log2p(c1) + p(c2).log2p(c2)]$

    ```python
    prob = lambda x, y: x/(x+y)
    entropia_pai = -(prob(c1, c2)*np.log2(prob(c1, c2)) + prob(c2, c1)*np.log2(prob(c2, c1)))
    ```

- Fórmula de ganho de informação

    $GI(pai, filho) = entropia(pai) - [p(c1).entropia(c1) + p(c2).entropia(c2)+...]$

    pai = todo o conjunto de dados

    filho = atributo ou coluna de uma detaframe

    p(cn) = p →é a proporção de uma coluna "c" e "n" é cada coluna 1, 2, 3...