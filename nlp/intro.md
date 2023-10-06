

### TF-IDF
Term Frequency - Inverse Document Frequency (TF-IDF) is a widely used statistical method to measure how important a term is within a document _relative to a collection of documents_ (i.e. a corpus). "Term" is used as opposed to "word" since documents may contain words, acronyms, abbreviations etc. 

#### Term Frequency (TF)
The TF value tells us how often a term $t$ appears in one specific document $d$.

$$
TF(t, d) = \frac{ \text{ \# of times $t$ appears in $d$} }{ \text{\# number of terms in $d$} }
$$

#### Inverse Document Frequency (IDF)
The IDF value reflects what proportion of documents in the corpus contain the term. Terms that appear in only a small number of documents will have a _higher_ value.

$$
IDF(t) = \log\frac{ \text{\# of documents} }{ \text{\# of documents that contain $t$} }
$$

The logarithm is used as when the number of words and documents increases the IDF value can explode (consider for example a web search engine using IDF in ranking search results); using the logarithm smoothes out the scale of values. No base is specified in the above equation as this can vary depending on context; base 2 and base 10 are common choices. Of course, logarithm base choices only differ by a constant factor:

$$
    \log_ax = \frac{\log_bx}{\log_ba}
$$

#### TF-IDF
The Term Frequency - Inverse Document Frequency (TF-IDF) value is the product of TD and IDF. Terms with larger values are deemed to be more important than terms with smaller values.

$$
TF\text{-}IDF(t, d) = TF(t, d) * IDF(t)
$$