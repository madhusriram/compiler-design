# Backus-Naur Form

Introduction:
-------------
One of the two main notation techniques for context-free grammars

A BNF specification is a set of derivation rules, written as

\<symbol\> ::= \_\_expression\_\_

where, \<symbol\> is a nonterminal, and the \_\_expression\_\_ consists of one or more sequences of symbols; more sequences are seperated by the vertical bar, '|', indicating a choice, the whole being a possible substitution for the symbol on the left. Symbols that never appear on a left side are terminals. On the other hand, symbols that appear on a left side are non-terminals and are always enclosed between the pair <>.

The '::=' means that the symbol on the left must be replaced with the expression on the right

Example:
--------
As an example, consider this possible BNF for a U.S. postal address:

> \<postal-address\> ::= \<name-part\> \<street-address\> \<zip-part\>
> \<name-part\> 	 ::= \<personal-part\> \<last-name\> \<opt-suffix-part\> \<EOL\> | \<personal-part\> \<name-part\>
