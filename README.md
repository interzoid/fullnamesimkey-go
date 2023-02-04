## fullnamesimkey-go

Go package for generating a similarity key from the input data used to match with other similar full name data. Use the generated similarity key, rather than the actual data itself, to match and/or sort individual name data by similarity. This avoids the problems of data inconsistency, misspellings, and name variations when matching within a single dataset, and can also help matching across datasets or for more advanced searching.

The key generation is based on a series of tests, algorithms, AI, and an ever-growing body of Machine Learning-based generated knowledge.

### Usage

To generate the similarity key, you will need the following information:

- an API License key, available at https://www.interzoid.com
- an individual full name to generate the similarity key for

Begin by importing the package:

    import "github.com/interzoid/fullnamesimkey-go"

Then, feed the information into the GetSimKey() method:

    simkey, code, credits, err := FullNameSimKey.GetSimKey("YOUR-API-KEY","Jim Smith")


The return values will be the similarity key, a code (success or failure), how many remaining credits on your API key, and any error messages. The similarity key can be used to search for other similar names, to sort large datasets by similarity, and perhaps use additional attributes to identify duplicates/redundancy.

Examples:

    jim smith  ->  7Kbdndkyln_1iZckUFnSOpwEve7t_USswPjJDAy2Qek
    James E. Smyth  ->  7Kbdndkyln_1iZckUFnSOpwEve7t_USswPjJDAy2Qek

    SALLY ANDERSON  ->   fOjMwYe9hOgKTa5LCDruK-NgkyDzasOV9Fqf-luTWXw
    Ms Sallie P. Andersen  ->  fOjMwYe9hOgKTa5LCDruK-NgkyDzasOV9Fqf-luTWXw

See Also:

**Individual Name Match Scoring**: https://github.com/interzoid/fullnamematchscore-go

**Company Name Similarity Keys**: https://github.com/interzoid/companynamesimkey-go

**Street Address Similarity Keys**: https://github.com/interzoid/streetaddresssimkey-go
