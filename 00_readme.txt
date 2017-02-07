This directory contains the data reverted from the smesma dictionary of apertium.
Goal: Lene's unification plans with the existing smanobswe for her own purposes.

Kommando for å se bare entryer med flere enn en oversetting, som ei liste med sma-ord pluss sme-oversettinger, inkludert <re>:
sed  's/<e/¢<e/' smasme/src/x_smasme.xml | tr '\n' '€' | tr '¢' '\n' | grep '<mg>.*<mg>' | tr '€' '\n' |sed 's/<l /¢<l /' | sed 's/<t /¢<t /g' |egrep '(¢|<re>)' |tr '<' '>' | cut -d '>' -f1,3 |less

Kommando for å se alle entryer som ei liste med sma-ord pluss sme-oversettinger, inkludert <re>:
sed 's/<l /¢<l /' smasme/src/x_smasme.xml | sed 's/<t /¢<t /g' | egrep '(¢|<re>)' |tr '<' '>' | cut -d '>' -f1,3 |less
