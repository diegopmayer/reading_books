# Data Science para Negócios

Author: Foster Provost & Tom Fawcett
Publisher: Alta Books
Publishing/Release Date: Jan 1, 2016
Score /5: ⭐️⭐️⭐️⭐️⭐️
Status: Reading
Summary: O que Você precisa saber sobre Mineração de dados e pensamento analítico de dados
Type: Books

> Registros dos pontos relevantes durante a leitura.

[Processo de leitura](Data%20Science%20para%20Nego%CC%81cios%204389c27aa0cb47339c509d0aae71494f/Processo%20de%20leitura%20e6ef94042f9740c2b0de1bd7712c6aed.md)

---

[Seleção de atributos por GI ([Ganho de Informação](http://www.esalq.usp.br/lepse/imgs/conteudo_thumb/Entropia--Ganho-de-informa--o-e-Decision-trees.pdf))](Data%20Science%20para%20Nego%CC%81cios%204389c27aa0cb47339c509d0aae71494f/Selec%CC%A7a%CC%83o%20de%20atributos%20por%20GI%20(Ganho%20de%20Informac%CC%A7a%20890dc07421b34274ae4f45ceb059f289.md)

- Copy of Seleção de atributos por GI ([Ganho de Informação](http://www.esalq.usp.br/lepse/imgs/conteudo_thumb/Entropia--Ganho-de-informa--o-e-Decision-trees.pdf))
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