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

	<postal-address> ::= <name-part> <street-address> <zip-part>
	<name-part> 	 ::= <personal-part> <last-name> <opt-suffix-part> <EOL> | <personal-part> <name-part>
	<personal-part>  ::= <initial> "." | <first-name>
	<street-address> ::= <house-num> <street-name> <opt-apt-num> <EOL>
	<zip-part>		 ::= <town-name> "," <state-code> <ZIP-code> <EOL>
	<opt-suffix-part>::= "Sr." | "Jr." | <roman-numeral> | ""
	<opt-apt-num>	 ::= <apt-num> | ""

This translates into English as:
- A postal address consists of a name-part, followed by a street-address part, followed by a zip-code part.
- A name-part consists of either: a personal-part followed by a last name followed by an optional suffix (Jr., Sr., or dynastic number) and end-of-line, or a personal part followed by a name part (this rule illustrates the use of recursion in BNFs, covering the case of people who use multiple first and middle names and/or initials).
- A personal-part consists of either a first name or an initial followed by a dot.
- A street address consists of a house number, followed by a street name, followed by an optional apartment specifier, followed by an end-of-line.
- A zip-part consists of a town-name, followed by a comma, followed by a state code, followed by a ZIP-code followed by an end-of-line.
- A opt-suffix-part consists of a suffix, such as "Sr.", "Jr." or a roman-numeral, or an empty string (i.e. nothing).
- A opt-apt-num consists of an apartment number or an empty string (i.e. nothing).

Another example:
----------------

